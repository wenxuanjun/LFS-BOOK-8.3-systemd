# LFS 和标准

LFS 的结构尽可能的遵循 Linux 的标准。主要的标准有：
* [POSIX.1-2008.](http://pubs.opengroup.org/onlinepubs/9699919799/)
* [文件系统层次标准 版本 3.0 草案 1 (FHS)](www.linuxfoundation.org/collaborate/workgroups/lsb/fhs-30-draft-1)
* [Linux 标准基础（LSB）规格](http://refspecs.linuxfoundation.org/lsb.shtml)

LSB 有五个独立的标准：内核、C++、桌面、运行时语言和输出。除了普通的要求，还有架构特定要求。LFS 试图遵从前一节中所讨论的架构要求。 

> 很多人不认同 LSB 的要求。定义它的主要目的是确保私有软件能够在兼容的系统上安装并正常运行。由于 LFS 是基于源代码的，用户对于需要什么软件包有完全的控制权，很多人选择不安装 LSB 规范所要求的软件包。

创建一个能够通过 LSB 认证测试的完整 LFS 系统是可行的，但需要很多 LFS 范围之外的额外软件包。在 BLFS 中有这些额外软件包的安装说明。

### 由 LFS 提供，用于满足 LSB 要求的软件包

| 类别 | 软件包 |
| ------ | ------ | ------ |
| LSB 内核: | Bash, Bc, Binutils, Coreutils, Diffutils, File, Findutils, Gawk, Grep, Gzip, M4, Man-DB, Ncurses, Procps, Psmisc, Sed, Shadow, Tar, Util-linux, Zlib |
| LSB 桌面: | 无 |
| LSB 运行时语言: | Perl |
| LSB 显示:| 无 |
| LSB GTK3和LSB图形（试用）:| 无 |

### 由BLFS提供，用于满足 LSB 要求的软件包

| 类别 | 软件包 |
| ------ | ------ | ------ |
| LSB 内核: | At, Batch (a part of At), Cpio, Ed, Fcrontab, Initd-tools, Lsb_release, NSPR, NSS, PAM, Pax, Sendmail (or Postfix or Exim), time |
| LSB 桌面: | Alsa, ATK, Cairo, Desktop-file-utils, Freetype, Fontconfig, Gdk-pixbuf, Glib2, GTK+2, Icon-naming-utils, Libjpeg-turbo, Libpng, Libtiff, Libxml2, MesaLib, Pango, Xdg-utils, Xorg |
| LSB 运行时语言: | Python, Libxml2, Libxslt |
| LSB 显示:| CUPS, Cups-filters, Ghostscript, SANE |
| LSB GTK3和LSB图形（试用）:| GTK+3 |

### LFS 和 BLFS 没有提供，用于满足 LSB 要求的软件包

| 类别 | 软件包 |
| ------ | ------ | ------ |
| LSB 内核: | 无 |
| LSB 桌面: | Qt4（但Qt5是提供的） |
| LSB 运行时语言: | 无 |
| LSB 显示:| 无 |
| LSB GTK3和LSB图形（试用）:| 无 |