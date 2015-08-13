# Patch the Lustre source code #
Tools such as [quilt](http://savannah.nongnu.org/projects/quilt/) can be used to apply the patches of MTFS to the Lustre source code.

# Build #
```
aclocal -I build/autoconf/ -I mtfs/autoconf
autoheader
autoconf
automake
./configure --with-linux=/lib/modules/`uname -r`/build/ --with-lustre=/usr/src/lustre-2.1.52
make
make rpms
```

Run command ./configure with --help argument for help messages about how to configure the MTFS.

Run ./configure with --disable-lustre argument to disable lustre support.



# Install #
Mtfs can be installed from the command line with the rpm installer.
```
rpm -ivh mtfs-modules-VERSION.rpm
rpm -ivh mtfs-VERSION.rpm
```
# Mount #
```
mount -t mtfs /path/to/dir1:/path/to/dir2 /mnt/mtfs
```