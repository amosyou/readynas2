# Mount Disk from ReadyNAS Duo v2

## Prerequisites

### fuse-ext2 Installation
```
ubuntu@ubuntu:~/Downloads/fuse-ext2-master$ ls
aclocal.m4  compile       config.sub    fuse-ext2        Makefile.am
ar-lib      config.guess  configure     fuse-ext2.1      Makefile.in
AUTHORS     config.h.in   configure.ac  fuse-ext2.pc.in  missing
autogen.sh  config.h.in~  COPYING       install-sh       README.md
ChangeLog   config.log    depcomp       ltmain.sh        tools

$ ./autogen.sh
$ ./configure
$ make
$ sudo make install
```

*Note: Ensure package dependencies for fuse-ext2 are installed.* The following packages are needed on Ubuntu 20.4.
```
sudo apt-get install gawk g++ c++
```
Otherwise, such errors would occur.


## Disk Probe
```
ubuntu@ubuntu:~$ sudo vgscan
  WARNING: PV /dev/sda5 in VG c is using an old PV header, modify the VG to update.
  Found volume group "c" using metadata type lvm2
ubuntu@ubuntu:~$ sudo vgchange -ay c
  WARNING: PV /dev/sda5 in VG c is using an old PV header, modify the VG to update.
  1 logical volume(s) in volume group "c" now active
ubuntu@ubuntu:~$ sudo lvs
  WARNING: PV /dev/sda5 in VG c is using an old PV header, modify the VG to update.
  LV   VG Attr       LSize   Pool Origin Data%  Meta%  Move Log Cpy%Sync Convert
  c    c  -wi-a----- 929.09g                                                    
ubuntu@ubuntu:~$ sudo lvdisplay /dev/c
  WARNING: PV /dev/sda5 in VG c is using an old PV header, modify the VG to update.
  --- Logical volume ---
  LV Path                /dev/c/c
  LV Name                c
  VG Name                c
  LV UUID                GdWCix-EWTF-FZiq-6lTn-MUpN-SZpo-eAQf4u
  LV Write Access        read/write
  LV Creation host, time , 
  LV Status              available
  # open                 0
  LV Size                929.09 GiB
  Current LE             29731
  Segments               1
  Allocation             inherit
  Read ahead sectors     auto
  - currently set to     256
  Block device           253:0

```


## Mounting Drive

### Create local directory
```
$ mkdir /media/readynas2
```

### Mount Volume
```
$ sudo fuse-ext2 -o sync_read,allow_other,rw+ /dev/c/c /media/readynas2
```


## Unmounting Drive
```
$ fusermount -u /media/readynas2
```


## References

[1] http://technostuff.blogspot.com/2012/06/how-to-mount-disk-used-by-readynas.html
