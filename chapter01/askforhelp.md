# 1.5 帮助

如果在使用本书的过程中有疑问或碰到问题，可以先去看下 FAQ 页面 <http://www.linuxfromscratch.org/faq/#generalfaq。> 那里已经解决了很多经常遇到的问题。如果你的问题在那里找不到答案，可以先尝试找出问题的原因。下面页面里的提示可以提供一些帮你定位问题的帮助：<http://www.linuxfromscratch.org/hints/downloads/files/errors.txt>。

如果在 FAQ 里找不到你遇到的问题，还可以在这个邮件列表里搜索一下：<http://www.linuxfromscratch.org/search.html>。

我们还有一个很棒的 LFS 社区，大家都很乐意通过邮件列表和 IRC 提供协助（参看本书章节 “1.4 资源”）。不过，我们每天收到的支持问题中有很多其实可以通过查看 FAQ 和搜索邮件列表轻松解决。所以，为了让我们能最大可能地提供更好的协助，希望你碰到问题能自己先研究一下。这样可以让我们有精力去关注更罕见的支持需求。如果你自己搜索不到解决方式，请在你的帮助请求里收集所有相关信息（下面提到的）。

### 1.5.1. 需要提供的信息

除了对你遇到的问题的一个简短描述外，任何帮助请求里都需要包含的一些关键信息：

* 所用手册的版本（本手册是 8.3-systemd）

* 用来构建 LFS 的宿主机器的 Linux 发行版以及版本

* 本书章节 vii 所需宿主系统中的脚本打印信息

* 出现问题的软件包或本书的章节

* 精确的错误信息或表现形式

* 注明你是否已经脱离了本书的内容

>脱离本书内容并不是说我们就一定不会帮你。毕竟，LFS 还是属于个人爱好。坦率地告知对已验证流程的任何改动，有助于我们评估和找到你问题的可能原因。

### 1.5.2. 配置脚本问题

如果在运行 <code>configure</code> 脚本时遇到问题，查看一下 <code>config.log</code> 文件。这个文件中会包含 <code>configure</code> 脚本运行时发生的没有输出到屏幕上的错误信息。如果你需要寻求帮助的话请包含相关行。 

### 1.5.3. 编译问题

屏幕上的显示输出和各个文件的内容都有助于定位编译发生问题的原因。<code>configure</code> 脚本和 <code>make</code> 执行时的屏幕打印输出都有用。并不需要包含整个所有输出信息，但是一定要包含足够的相关信息。下面的例子是 <code>make</code> 出错后需要包含的屏幕显示的输出信息：

```bash
gcc -DALIASPATH=\"/mnt/lfs/usr/share/locale:.\"
-DLOCALEDIR=\"/mnt/lfs/usr/share/locale\"
-DLIBDIR=\"/mnt/lfs/usr/lib\"
-DINCLUDEDIR=\"/mnt/lfs/usr/include\" -DHAVE_CONFIG_H -I. -I.
-g -O2 -c getopt1.c
gcc -g -O2 -static -o make ar.o arscan.o commands.o dir.o
expand.o file.o function.o getopt.o implicit.o job.o main.o
misc.o read.o remake.o rule.o signame.o variable.o vpath.o
default.o remote-stub.o version.o opt1.o
-lutil job.o: In function `load_too_high':
/lfs/tmp/make-3.79.1/job.c:1565: undefined reference
to `getloadavg'
collect2: ld returned 1 exit status
make[2]: *** [make] Error 1
make[2]: Leaving directory `/lfs/tmp/make-3.79.1'
make[1]: *** [all-recursive] Error 1
make[1]: Leaving directory `/lfs/tmp/make-3.79.1'
make: *** [all-recursive-am] Error 2
```

在这个例子里，很多人可能只包含了最后的部分：

```bash
make [2]: *** [make] Error 1
```
 这并没有提供足够的信息来诊断问题，因为它只能说明出问题了，而没有指出哪儿出了问题。需要保留完整的打印信息，像上面例子中的，是因为它包含了所执行的命令以及相应的错误信息。

这个链接 <http://catb.org/~esr/faqs/smart-questions.html>是一篇关于如何在互联网上寻求帮助的很好的文章。去看一下并遵循文章中给出的提示，可以增加你能得到所想要的帮助的可能性。
