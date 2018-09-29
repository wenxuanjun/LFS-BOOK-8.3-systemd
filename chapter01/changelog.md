# 1.3 更新日志

这是 Linux From Scratch 手册的 8.3-systemd 版本，发布于2018年9月1日。如果距离这个时间已超过 6 个月，那么应该已经有更新和更好的版本了。要获取的话，请访问这个页面 <http://www.linuxfromscratch.org/mirrors.html> 里任意一个镜像站点。

下面是本书上一次发布之后的更新列表。

**更新日志条目：**

* 2018-09-01

    * [bdubbs] - LFS-8.3 发布.

    * [bdubbs] - 更新到 linux-4.18.5。 解决了 #4337.

* 2018-08-25

    * [bdubbs] - 禁用GCC中弃用的MPX代码。


* 2018-08-16

    * [bdubbs] - 更新到 expat-2.2.6。 解决了 #4334.

    * [bdubbs] - 更新到 openssl-1.1.0i。 解决了 #4335.

    * [bdubbs] - 更新到 iproute2-4.18.0。 解决了 #4333.

    * [bdubbs] - 更新到 linux-4.18.1。 解决了 #4336.

* 2018-08-12

    * [bdubbs] - 更新到 linux-4.18。 解决了 #4332.


* 2018-08-12

    * [bdubbs] - 更新到 dbus-1.12.10。 解决了 #4328.

    * [bdubbs] - 使用libidn2给glibc添加注释。

    * [bdubbs] - 在VIM测试指令中添加LANG。

    * [bdubbs] - 确保grep测试完成。

    * [bdubbs] - 在无特权用户下运行第6章中GCC测试。

    * [bdubbs] - 将shadow移动到GCC之前，因此GCC测试可以使用SU作为无特权用户运行.

    * [bdubbs] - 为确保没有使用宿主系统库，在第5章中添加Perl配置选项。

    * [bdubbs] - 更新glibc-2.28所需的make的最小版本到4.0版本。

    * [bdubbs] - 更新bzip2的链接到一个新地址。 解决了 #4331.

    * [bdubbs] - 更新到 linux-4.17.14。 解决了 #4330.

* 2018-08-08

    * [renodr] - 更新到 linux-4.17.13。 解决了 #4327.


* 2018-08-03

    * [renodr] - 为systemd添一个补丁来修复在glibc-2.28下编译错误的问题。


* 2018-08-02

    * [bdubbs] - 更新到 glibc-2.28。 解决了 #4326.

    * [bdubbs] - 更新到 gdbm-1.17。 解决了 #4325.

    * [bdubbs] - 更新到 linux-4.17.11。 解决了 #4322.

    * [bdubbs] - 更新到 man-db-2.8.4。 解决了 #4321.

* 2018-07-26

    * [bdubbs] - 更新镜像和翻译信息。 解决了 #4318.

    * [bdubbs] - 更新到 gcc-8.2.0。 解决了 #4320.

    * [bdubbs] - 更新到 file-5.34。 解决了 #4319.

    * [bdubbs] - 更新到 linux-4.17.10。 解决了 #4316.

* 2018-07-23

    * [renodr] - 更新到 systemd-239。 解决了 #4298.


* 2018-07-18

    * [bdubbs] - 更新到 util-linux 2.32.1。 解决了 #4315.

    * [bdubbs] - 更新到 binutils-2.31.1。 解决了 #4314.

    * [bdubbs] - 更新到 meson-0.47.1。 解决了 #4313.

    * [bdubbs] - 记录一些新的回归测试失败。

    * [bdubbs] - 更新到 linux-4.17.8。 解决了 #4312。

    * [bdubbs] - 更新到 e2fsprogs-1.44.3。 解决了 #4310.

* 2018-07-08

    * [bdubbs] - 修复Texinfo回归测试中的失败。

    * [bdubbs] - 更新到 linux-4.17.5。 解决了 #4300.

    * [bdubbs] - 更新到 meson-0.47.0。 解决了 #4306.

* 2018-07-07

    * [bdubbs] - 向libffi添加配置选项以确保正确的体系结构选择。 解决了 #4303.


* 2018-07-06

    * [bdubbs] - 使第6章开头部分的符号链接与本书的所有版本一致，允许删除e2fsprog中不再需要的环境变量。

    * [bdubbs] - 更新到 Python-3.7.0。 解决了 #4301.

    * [bdubbs] - 更新到 gdbm-1.16。 解决了 #4302.

    * [bdubbs] - 更新到 elfutils-0.173。 解决了 #4304.

    * [bdubbs] - 更新到 coreutils-8.30。 解决了 #4305.

* 2018-07-03

    * [bdubbs] - 更新到 attr-2.4.48。 解决了 #4308.

    * [bdubbs] - 更新到 acl-2.2.53。 解决了 #4307.

* 2018-06-25

    * [bdubbs] - 各种URL更新。 解决了 #4293 and #4294.

    * [bdubbs] - 更新到 perl-5.28.0。 解决了 #4299.

    * [bdubbs] - 更新到 Sysvinit 2.90。 解决了 #4297.

    * [bdubbs] - 更新到 gdbm-1.15。 解决了 #4296.

    * [bdubbs] - 更新到 elfutils-0.172。 解决了 #4292.

    * [bdubbs] - 更新到 linux-4.17.2。 解决了 #4295.

* 2018-06-12

    * [bdubbs] - XZ页面中的键入修复。 解决了 #4285.

    * [bdubbs] - 在GCC中更改一些HTTP引用到HTTPS。 解决了 #4281.

    * [bdubbs] - 更新到 iproute2-4.17.0。 解决了 #4288.

    * [bdubbs] - 更新到 bison-3.0.5。 解决了 #4284.

    * [bdubbs] - 更新到 linux-4.17.1。 解决了 #4280.

* 2018-05-22

    * [bdubbs] - 更新一些链接到HTTPS。 解决了 #4274.

    * [bdubbs] - 更新到 procps-ng-3.3.15。 解决了 #4279.

    * [bdubbs] - 更新到 vim-8,1。 解决了 #4278.

    * [bdubbs] - 更新到 meson-0.46.1。 解决了 #4277.

    * [bdubbs] - 更新到 e2fsprogs-1.44.2。 解决了 #4275.

    * [bdubbs] - 更新到 linux-4.16.10。 解决了 #4276.

* 2018-05-11

    * [bdubbs] - 更新到 linux-4.16.8。 解决了 #4267.


* 2018-05-07

    * [bdubbs] - 在第6章中更改退出操作以不需要注销。


* 2018-05-05

    * [bdubbs] - 更新到 gcc-8.1.0。 解决了 #4268.

    * [bdubbs] - 更新到 linux-4.16.7。 解决了 #4262.

    * [bdubbs] - 更新到 man-pages-4.16。 解决了 #4266.

    * [bdubbs] - 更新到 meson-0.46.0。 解决了 #4263.

    * [bdubbs] - 更新到 shadow-4.6。 解决了 #4264.

    * [bdubbs] - 更新到 tzdata-2018e。 解决了 #4269.

    * [bdubbs] - 更新到 xz-5.2.4。 解决了 #4265.

* 2018-04-20

    * [bdubbs] - 更新到 linux-4.16.2。 解决了 #4258.

    * [bdubbs] - 更新到 file-5.33。 解决了 #4261.

    * [bdubbs] - 更新到 perl-5.26.2。 解决了 #4260.

* 2018-04-16

    * [bdubbs] - 修复meson的man页面和描述。 感谢 Xi Ruoyao 提供的补丁.


* 2018-04-11

    * [bdubbs] - 修复gettext中的appdata.loc文件.

    * [bdubbs] - 更新到 linux-4.16.1。 解决了 #4256.

    * [bdubbs] - 更新到 procps-ng-3.3.14。 解决了 #4257.

* 2018-04-06

    * [bdubbs] - 把libelf添加到rationale。 解决了 #4252.

    * [bdubbs] - 更新到 man-db-2.8.3。 解决了 #4255.

    * [bdubbs] - 更新到 iproute2-4.16.0。 解决了 #4254.

    * [bdubbs] - 更新到 linux-4.16。 解决了 #4250.

    * [bdubbs] - 更新到 procps-ng-3.3.13。 解决了 #4253.

    * [bdubbs] - 更新到 sed-4.5。 解决了 #4251.

* 2018-03-23

    * [bdubbs] - 更新一些链接HTTPS。 感谢 avmaisak 提供的补丁。 解决了 #4247.

    * [bdubbs] - 更新到 Python3-3.6.5。 解决了 #4248.

    * [bdubbs] - 更新到 openssl-1.1.0h。 解决了 #4244.

    * [bdubbs] - 更新到 e2fsprogs-1.44.1。 解决了 #4244.

    * [bdubbs] - 更新到 tzdata-2018d。 解决了 #4243.

    * [bdubbs] - 更新到 meson-0.45.1。 解决了 #4242.

    * [bdubbs] - 更新到 linux-4.15.14。 解决了 #4241.

* 2018-03-23

    * [bdubbs] - 删除在第9章中引用BLFS中的OpenSSL。 解决了 #4240.

    * [bdubbs] - 更新最小主机系统要求。 解决了 #4239.

    * [bdubbs] - 增加了OpenSSL的描述。 解决了 #4234.

    * [bdubbs] - 更新到 util-linux-2.32。 解决了 #4219.

    * [bdubbs] - 更新到 meson-0.45.0。 解决了 #4232.

    * [bdubbs] - 更新到 e2fsprogs-1.44.0。 解决了 #4236.

    * [bdubbs] - 更新到 linux-4.15.11。 解决了 #4237.

    * [bdubbs] - 更新到 automake-1.16.1。 解决了 #4238.

    * [bdubbs] - 更新到 systemd-238。 解决了 #4233.

* 2018-03-03

    * [bdubbs] - 更新到 dbus-1.12.6。 解决了 #4231.

    * [bdubbs] - 更新到 man-db-2.8.2。 解决了 #4230.

    * [bdubbs] - 更新到 gawk-4.2.1。 解决了 #4227.

    * [bdubbs] - 更新到 meson-0.44.1。 解决了 #4226.

    * [bdubbs] - 更新到 meson-0.44.1。 解决了 #4222.

    * [bdubbs] - 更新到 linux-4.15.7。 解决了 #4221.

* 2018-03-02

    * [bdubbs] - LFS-8.2 发布.