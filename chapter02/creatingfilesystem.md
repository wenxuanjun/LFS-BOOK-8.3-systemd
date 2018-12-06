 # 2.5 在分区上创建文件系统
 
现在已经有了一个空的分区，可以创建文件系统了。LFS 可以使用 Linux 内核能识别的任何文件系统，但最常用的类型是 ext3 和 ext4。当然，至于具体采用哪种文件系统，应该取决于所要存储的文件特点和分区的大小。例如：

##### ext2

适用于那些分区容量不是太大，更新也不频繁的情况，例如 /boot 分区。

##### ext3

是 ext2 的改进版本，其支持日志功能，能够帮助系统从非正常关机导致的异常中恢复。它通常被用作通用的文件系统。 

##### ext4

是 ext 文件系统的最新版。提供了很多新的特性，包括纳秒级时间戳、创建和使用巨型文件(16TB)、以及速度的提升。

其它文件系统，包括 FAT32、NTFS、ReiserFS、JFS 和 XFS 等都在专门领域有其独到的作用。关于这些文件系统更多的信息可以在 <http://en.wikipedia.org/wiki/Comparison_of_file_systems> 找到。

LFS 假定根文件系统(/)是 <code>ext4</code> 类型的。要在 LFS 分区上创建 <code>ext4</code> 文件系统，运行以下命令： 

```bash
mkfs -v -t ext4 /dev/<xxx>
```

如果你已经有了现成的 <code>swap</code> 分区，不需要重新格式化。如果是新建 <code>swap</code> 分区，需要用下面的命令初始化： 

```bash
mkswap /dev/<yyy>
```

其中，<code>&lt;xxx&gt;</code> 和 <code>&lt;yyy&gt;</code>都需要替换为实际的设备名称（形如 sda1，sdb2）。