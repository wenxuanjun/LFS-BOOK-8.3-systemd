# 排版约定
为了能更轻松地阅读，这里有一些全书使用的排版约定。这个部分包括一些来自 Linux From Scratch 中的排版格式例子。

```bash
./configure --prefix=/usr
```
这种形式的文本被设计成完全按照看到的样子输入，除非在周围文本中另有说明。它也用在解释部分，用以指出引用的是哪个命令。

某些情况下，一个逻辑行会通过在行末添加反斜杠被折叠为两个或者更多的物理行。

```bash
CC="gcc -B/usr/bin/" ../binutils-2.18/configure \
  --prefix=/tools --disable-nls --disable-werror
```
注意，反斜杠后面必须紧跟一个回车符。其它空格字符，例如空格和tab键会导致错误结果。

```
install-info: unknown option '--dir-file=/mnt/lfs/usr/info/dir'
```

这种形式的文本（定宽文本）显示屏幕输出，通常是所运行命令的输出结果。 这种形式也用来显示文件名，例如:
<code>/etc/ld.so.conf</code>

*强调*

这种形式的文本在本书中有多重目的。主要目的是强调重要的内容或项目。

<http://www.linuxfromscratch.org/>

这种格式用来表示 LFS 社区内部及外部网页的超链接。包括 HOWTO，下载地址和网站等。 

```bash
cat > $LFS/etc/group << "EOF"
root:x:0:
bin:x:1:
......
EOF
```

这种格式在创建配置文件中会使用。第一个命令告诉系统新建一个文件 <code>$LFS/etc/group</code>，不论在后面的行中输入了什么，直到遇到文件终结符（EOF）。因此，这整个部分正如看到的那样输入。

<code>&lt;需要替换的文本&gt;</code>

这种格式用来封装需要替换为合适内容的文本，以及复制粘贴操作。

<code>[可选的文本]</code>

这种格式用来封装可选项文本。

<code>passwd(5)</code>

这种格式用来表示特定的手册 (man) 页面。括号内的数字表示该手册的特定部分。例如 <code>passwd</code> 有两个手册页面。在 LFS 安装说明中，这两个手册页面会表示为 <code>/usr/share/man/man1/passwd.1</code> 以及 <code>/usr/share/man/man5/passwd.5</code>。当书中使用 <code>passwd(5)</code> 时它特指 <code>/usr/share/man/man5/passwd.5</code>。<code>man passwd</code> 会输出它找到匹配 “passwd” 的第一个手册页面，也就是 <code>/usr/share/man/man1/passwd.1</code>。在这个例子中，你需要执行 <code>man 5 passwd</code> 才能阅读指定的手册页面。应该注意的是，大部分的手册页面在不同部分不会有重复的页面名字。因此，<code>man "program name"</code>通常就足够了。