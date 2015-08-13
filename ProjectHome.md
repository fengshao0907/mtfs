# Overview #
MTFS(`MulTi File System`) is a stackable file system, which takes multiple directories as its lower branches in order to add new features to existing file systems, including  replication, unification, tracing and more.
Mtfs is originally designed and mainly used as a reliability improvement mechanism for [Lustre file system](http://www.lustre.org). It aims to become a general platform for stackable file system development.

# Features #
  * Can be mounted on top of any combination of network, distributed, disk-based, and memory-based file systems. [A series of file systems](SupportedFileSystems.md) can be used as its lower file system including Lustre, ext2(3, 4), nfs, ntfs-3g and tmpfs.
  * Can be easily added support for new kinds of file systems.
  * Can take full advantage of characteristic features of a specific lower file system.
  * Have a test framework with plenty of test suites for the POSIX I/O interface, which is very helpful for its correctness.

When used as a reliability improvement mechanism for storage systems, mtfs is able to:
  * Replicate files and directories across multiple branches.
  * Selfheal if any branch is broken.
  * Replicate files synchronously or asynchronously.
  * Apply various replication policies according to file-name pattern.

# What's New #
2013.8.18 Mtfs-0.0.12 is be released.
  * Log framework for journal based recovery.
  * Fixed some bugs

2013.3.16 Mtfs-0.0.11 is released.
  * Online check of async replication.
  * Removing dirty extents of async replication when truncate.

2013.2.19 Mtfs-0.0.10 is released.
  * Optimization of extent lock which improve the performance of applications.
  * Fixed some bugs.

2013.1.25 Mtfs-0.0.9 is released.
  * Online checksum for file replications for consistency assurance。
  * Fixed some bugs.

2012.12.15 Mtfs-0.0.8 is released.
  * Rewrited asynchronous replication subject support for better performance.
  * Updated supports for different lower file systems.
  * Fixed some bugs.

2012.11.20 Mtfs-0.0.7 is released.
  * Asynchronous replication subject.
  * Totally new software stack for all io operations.
  * Fixed some bus.

2012.10.24 Mtfs-0.0.6-rc1 is released.
  * Fixed some bugs.

2012.10.22 Mtfs-0.0.6 is released.
  * Support for different subjects.
  * Added trace subject.
  * Fixed some bugs.

2012.09.22 Mtfs-0.0.5 is released.
  * New software stack for writev/readv in order to reduce code redundancy.
  * Fixed some bugs of extent lock.

2012.09.02 Mtfs-0.0.4 is released.
  * Added extent lock to speed up concurrent read/write to the same file.
  * Fixed some bugs when built on RHEL6.

2012.07.18 Mtfs-0.0.3 is released.
  * Selfheal framework is completed.
  * Fixed some bugs.

2012.06.18 Mtfs-0.0.2 is released.
  * Removed dependency on libcfs.
  * Improved Supports for RHEL5 kernels.
  * Fixed some bugs.

Click [here](ChangeLog.md) for more informantion.
# Quick start #
To use mtfs, you simply need to do the following:
  * Check whether the file system types of lower directories are [supported](SupportedFileSystems.md) by mtfs. If not, contact us to add support for it if you like to.
  * Check whether your [kernel](SupportedKernels.md) is supported by mtfs. If not, try to compile the source code. If the compiling fails, contact us if you like to.
  * [Install](Install.md) the kernel modules and userspace utils of mtfs
  * Mount mtfs file system to an existing mount point. For example:
```
mount -t mtfs /path/to/dir1:/path/to/dir2 /mnt/mtfs
```
  * Acces /mnt/mtfs as if it is a normal file system.

# How to get help #
If you have any question, please send an email to [the mtfs mailing list](http://groups.google.com/group/mtfs). If you can read Chinese, please check [my blog](http://blog.csdn.net/fsdev) for more information.

There is a group of filesystem developers [here](http://qun.qq.com/#jointhegroup/gid/249858913). Please join us!

# How to contribute #
It needs so much work to make mtfs stable and powerful enough for enterprise use. We are always looking for new contributors.
If you are interested in joining us, send an email to pkuelelixi@gmail.com with your contact information. We are looking forward to working with you!