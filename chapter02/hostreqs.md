# 2.2 宿主机需求

以下是您的主机系统应安装有的软件和它们的最小版本，对于大多数现代Linux发行版来说，这不应该是一个问题。还要注意，许多发行版将软件头放入单独的包中，通常以“&lt;package-name&gt;-devel”或“&lt;package-name&gt;-dev”的形式。如果你的发行提供了它们，一定要安装它们。

下面软件的旧版本可能可以工作，但是没有经过测试。

**Bash-3.2** (/bin/sh应该被链接到bash)

**Binutils-2.25** (不推荐版本大于2.31.1，因为它们没有被测试过。)

**Bison-2.7** (/usr/bin/yacc应该是bison或执行bison的小脚本的链接)

**Bzip2-1.0.4**

**Coreutils-6.9**

**Diffutils-2.8.1**

**Findutils-4.2.31**

**Gawk-4.0.1** (/usr/bin/awk应该链接到gawk)

**GCC-4.9** 包括C++编译器,g++(不推荐大于8.2.0的版本，因为它们没有被测试过)

**Glibc-2.11** (不推荐大于2.28的版本，因为它们没有被测试过）

**Grep-2.5.1a**

**Gzip-1.3.12**

**Linux Kernel-3.2**

我们在第6章中根据开发人员的建议构建glibc时指定了该内核版本，这就是内核版本不能过低的原因，此外，udev也需要它。

如果主机内核低于3.2，则需要用更新的版本来替换它。有两种方法可以解决这个问题：首先，看看Linux供应商是否提供了一个3.2或更高版本的内核包。如果是，安装它。如果您的供应商没有提供可接受的内核包，或者您不希望安装它，那么您可以自己编译内核。编译内核和配置引导加载器的指令（假设主机使用GRUB）位于第8章。

**M4-1.4.10

**Make-4.0**

**Patch-2.5.4**

**Perl-5.8.8**

**Sed-4.1.5**

**Tar-1.22**

**Texinfo-4.7**

**Xz-5.0.0**

>请注意，使用本书中包含的指令来构建LFS系统需要上面提到的符号链接，若它们指向其他软件（如dash、mawk等），也许可以工作，但是LFS开发团队没有测试或支持，并且可能需要偏离指令或对某些包进行额外的补丁。

要查看主机系统所有的包都是适当的版本，以及拥有编译程序的能力，请运行以下内容：

```bash
cat > version-check.sh << "EOF"
#!/bin/bash
# Simple script to list version numbers of critical development tools
export LC_ALL=C
bash --version | head -n1 | cut -d" " -f2-4
MYSH=$(readlink -f /bin/sh)
echo "/bin/sh -> $MYSH"
echo $MYSH | grep -q bash || echo "ERROR: /bin/sh does not point to bash"
unset MYSH

echo -n "Binutils: "; ld --version | head -n1 | cut -d" " -f3-
bison --version | head -n1

if [ -h /usr/bin/yacc ]; then
  echo "/usr/bin/yacc -> `readlink -f /usr/bin/yacc`";
elif [ -x /usr/bin/yacc ]; then
  echo yacc is `/usr/bin/yacc --version | head -n1`
else
  echo "yacc not found" 
fi

bzip2 --version 2>&1 < /dev/null | head -n1 | cut -d" " -f1,6-
echo -n "Coreutils: "; chown --version | head -n1 | cut -d")" -f2
diff --version | head -n1
find --version | head -n1
gawk --version | head -n1

if [ -h /usr/bin/awk ]; then
  echo "/usr/bin/awk -> `readlink -f /usr/bin/awk`";
elif [ -x /usr/bin/awk ]; then
  echo awk is `/usr/bin/awk --version | head -n1`
else 
  echo "awk not found" 
fi

gcc --version | head -n1
g++ --version | head -n1
ldd --version | head -n1 | cut -d" " -f2-  # glibc version
grep --version | head -n1
gzip --version | head -n1
cat /proc/version
m4 --version | head -n1
make --version | head -n1
patch --version | head -n1
echo Perl `perl -V:version`
sed --version | head -n1
tar --version | head -n1
makeinfo --version | head -n1
xz --version | head -n1

echo 'int main(){}' > dummy.c && g++ -o dummy dummy.c
if [ -x dummy ]
  then echo "g++ compilation OK";
  else echo "g++ compilation failed"; fi
rm -f dummy.c dummy
EOF

bash version-check.sh
```
