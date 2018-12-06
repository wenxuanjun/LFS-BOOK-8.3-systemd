# 2.6 设置 \$LFS 变量 

在整本书里，会多次用到环境变量 <code>LFS</code>。你应该确保这个变量在整个 LFS 构建过程中总是定义了的。它应该被设置为你将要构建的 LFS 系统的目录名字——这里我们使用 <code>/mnt/lfs</code> 作为例子，但是选择哪一个目录是你的自由。如果你把 LFS 构建到一个单独的分区里，这个目录将成为那个分区的挂载点。选择一个目录并用以下命令设置该变量：

```bash
export LFS=/mnt/lfs
```

设置这个变量的好处在于当我们使用类似 <code>mkdir -v \$LFS/tools</code> 的命令时可以直接这样简洁的输入。shell 在处理这条命令时，会自动替换 “\$LFS” 为 “/mnt/lfs”（或任何这个变量所指向的地方）。

不论何时当你离开而又重新进入这个工作环境时都不要忘了检查 <code>LFS</code> 是否设置（比如当你使用 <code>su</code> 切换到 <code>root</code> 或是另一个用户时）。使用如下命令检查 <code>LFS</code> 变量是否正确设置:

```bash
echo $LFS
```

确保输出显示的是你构建 <code>LFS</code> 的那个目录的路径，如果你按照例子设置的，那就是 <code>/mnt/lfs</code> 。如果你输出的不是正确的路径，请使用本页前一部分提供的命令把 <code>\$LFS</code> 重新设置到正确的目录。 

>确保一直设置了 <code>LFS</code> 变量的一个方法是，同时编辑你的主目录下的 <code>.bash_profile</code> 和 <code>/root/.bash_profile</code>，把上方的导出命令输入进去。
