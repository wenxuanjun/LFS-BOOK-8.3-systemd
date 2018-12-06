# 2.7 挂载新分区

至此，文件系统已经创建妥当，下一步就是访问这些分区了。为此，需要将这些建立的分区挂载到选定的挂载点。本书假定的挂载点为 <code>/mnt/lfs</code>，这里，你可以根据喜好自行更改（译者注：这里强烈建议，看这本书的读者就将挂载点设置为 <code>/mnt/lfs</code> 吧，这样在运行后面的命令时，大多数命令都无需做任何的修改）。

运行以下命令来创建挂载点并挂载 <code>LFS</code> 分区到挂载点上：

```bash
mkdir -pv $LFS
mount -v -t ext4 /dev/<xxx> $LFS
```

 (译者注：如果重启设备，可能进入后发现 <code>/mnt/lfs</code> 目录下没有内容，这时只需要再次挂载 <code>/dev/&lt;xxx&gt;</code> 到 <code>/mnt/lfs</code>。 此处 <code>&lt;xxx&gt;</code> 用实际的设备名称代替，下同）。

如果 LFS 使用了多个分区，(比如：一个 <code>/</code>，一个 <code>/usr</code>)，用下面的命令挂载它们：

```bash
mkdir -pv $LFS #建立 / 分区的挂载点
mount -v -t ext4 /dev/<xxx> $LFS # 将 /dev/<xxx> 挂载到 $LFS
mkdir -v $LFS/usr #建立 $LFS/usr 挂载点，用于挂载 /usr
mount -v -t ext4 /dev/<yyy> $LFS/usr #将 /dev/<yyy> 挂载到 $LFS/usr
```

用正确的分区的名字替换<code>&lt;xxx&gt;</code>和<code>&lt;yyy&gt;</code>。

（译者注：挂载是有顺序的！假如需要挂载以下分区：<code>/</code>、<code>/usr</code>、<code>/usr/bin</code>，在挂载的时候，只能按照这样的顺序挂载。假如先挂载 <code>/</code>，然后挂载 <code>/usr/bin</code>，再挂载 <code>/usr</code> 将会出错！）

需要注意的是挂载的时候请不要使用过于严格的权限参数(比如 <code>nosuid</code> 或 <code>nodev</code> 选项)。用不带任何参数的 <code>mount</code> 命令查看挂载的 <code>LFS</code> 分区具体使用了哪些参数。如果设置了 <code>nosuid</code> 及 <code>nodev</code> 参数，请重新挂载。

（译者注：使用不带任何参数的 <code>mount</code> 命令，可以得到类似如下的输出： <code>devtmpfs on /dev type devtmpfs (rw,relatime,size=500896k,nr_inodes=125224,mode=755)</code> 其中，括号内的内容为挂载的参数。）

>上述指令假定您不会在整个构建 <code>LFS</code> 过程中重新启动计算机。 如果关闭系统，则每次重新启动构建过程时都需要重新挂载 <code>LFS</code> 分区，或修改主机系统的<code>/etc/fstab</code>文件以在引导时自动重新挂载。 例如：
>```
/dev/<xxx>  /mnt/lfs ext4   defaults     1     1
```
>如果您使用其他可选分区，请务必同时添加它们。

如果你正在使用交换分区，用 <code>swapon</code> 命令确保它已经启用。

```bash
/sbin/swapon -v /dev/<zzz>
```

用 <code>swap</code> 分区的名字替换<code>&lt;zzz&gt;</code>。

到现在，所有的准备工作都做的差不多了，是时候下载软件包了。