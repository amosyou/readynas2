# Troubleshoot Errors

## Missing package dependencies
```
ubuntu@ubuntu:~/Downloads/fuse-ext2-master$ ./autogen.sh
Running autoreconf --verbose --install --force
autoreconf: Entering directory `.'
autoreconf: configure.ac: not using Gettext
autoreconf: running: aclocal --force 
autoreconf: configure.ac: tracing
autoreconf: running: libtoolize --copy --force
libtoolize: putting auxiliary files in '.'.
libtoolize: copying file './ltmain.sh'
libtoolize: Consider adding 'AC_CONFIG_MACRO_DIRS([m4])' to configure.ac,
libtoolize: and rerunning libtoolize and aclocal.
libtoolize: Consider adding '-I m4' to ACLOCAL_AMFLAGS in Makefile.am.
autoreconf: running: /usr/bin/autoconf --force
autoreconf: running: /usr/bin/autoheader --force
autoreconf: running: automake --add-missing --copy --force-missing
configure.ac:10: installing './compile'
configure.ac:4: installing './missing'
fuse-ext2/Makefile.am: installing './depcomp'
autoreconf: Leaving directory `.'
Removing autom4te.cache

ubuntu@ubuntu:~/Downloads/fuse-ext2-master$ ./configure
checking build system type... x86_64-pc-linux-gnu
checking host system type... x86_64-pc-linux-gnu
checking target system type... x86_64-pc-linux-gnu
checking for a BSD-compatible install... /usr/bin/install -c
checking whether build environment is sane... yes
checking for a thread-safe mkdir -p... /usr/bin/mkdir -p
checking for gawk... no
checking for mawk... mawk
checking whether make sets $(MAKE)... yes
checking whether make supports nested variables... yes
checking for g++... no
checking for c++... no
checking for gpp... no
checking for aCC... no
checking for CC... no
checking for cxx... no
checking for cc++... no
checking for cl.exe... no
checking for FCC... no
checking for KCC... no
checking for RCC... no
checking for xlC_r... no
checking for xlC... no
checking whether the C++ compiler works... no
configure: error: in `/home/ubuntu/Downloads/fuse-ext2-master':
configure: error: C++ compiler cannot create executables
See `config.log' for more details
ize: Consider adding '-I m4' to ACLOCAL_AMFLAGS in Makefile.am.
autoreconf: running: /usr/bin/autoconf --force
autoreconf: running: /usr/bin/autoheader --force
autoreconf: running: automake --add-missing --copy --force-missing
configure.ac:10: installing './compile'
configure.ac:4: installing './missing'
fuse-ext2/Makefile.am: installing './depcomp'
autoreconf: Leaving directory `.'
Removing autom4te.cache
ubuntu@ubuntu:~/Downloads/fuse-ext2-master$ ./configure
checking build system type... x86_64-pc-linux-gnu
checking host system type... x86_64-pc-linux-gnu
checking targe

ubuntu@ubuntu:~/Downloads/fuse-ext2-master$ make
make: *** No targets specified and no makefile found.  Stop.

ubuntu@ubuntu:~/Downloads/fuse-ext2-master$ sudo make install
make: *** No rule to make target 'install'.  Stop.
```

## Compiling application properly
```
ubuntu@ubuntu:~/Downloads/fuse-ext2-master$ ./configure
checking build system type... x86_64-pc-linux-gnu
checking host system type... x86_64-pc-linux-gnu
checking target system type... x86_64-pc-linubuntu@ubuntu:~/Downloads/fuse-ext2-master$ ./configure
checking build system type... x86_64-pc-linux-gnu
checking host system type... x86_64-pc-linux-gnu
checking target system type... x86_64-pc-linux-gnu
checking for a BSD-compatible install... /usr/bin/install -c
checking whether build environment is sane... yes
checking for a thread-safe mkdir -p... /usr/bin/mkdir -p
checking for gawk... gawk
checking whether make sets $(MAKE)... yes
checking whether make supports nested variables... yes
checking for g++... g++
checking whether the C++ compiler works... yes
checking for C++ compiler default output file name... a.out
checking for suffix of executables... 
checking whether we are cross compiling... no
checking for suffix of object files... o
checking whether we are using the GNU C++ compiler... yes
checking whether g++ accepts -g... yes
checking whether make supports the include directive... yes (GNU style)
checking dependency style of g++... gcc3
checking for gawk... (cached) gawk
checking for gcc... gcc
checking whether we are using the GNU C compiler... yes
checking whether gcc accepts -g... yes
checking for gcc option to accept ISO C89... none needed
checking whether gcc understands -c and -o together... yes
checking dependency style of gcc... gcc3
checking for ar... ar
checking the archiver (ar) interface... ar
checking for gcc... gcc
checking whether we are using the GNU Objective C compiler... no
checking whether gcc accepts -g... no
checking dependency style of gcc... gcc3
checking how to print strings... printf
checking for a sed that does not truncate output... /usr/bin/sed
checking for grep that handles long lines and -e... /usr/bin/grep
checking for egrep... /usr/bin/grep -E
checking for fgrep... /usr/bin/grep -F
checking for ld used by gcc... /usr/bin/ld
checking if the linker (/usr/bin/ld) is GNU ld... yes
checking for BSD- or MS-compatible name lister (nm)... /usr/bin/nm -B
checking the name lister (/usr/bin/nm -B) interface... BSD nm
checking whether ln -s works... yes
checking the maximum length of command line arguments... 1572864
checking how to convert x86_64-pc-linux-gnu file names to x86_64-pc-linux-gnu format... func_convert_file_noop
checking how to convert x86_64-pc-linux-gnu file names to toolchain format... func_convert_file_noop
checking for /usr/bin/ld option to reload object files... -r
checking for objdump... objdump
checking how to recognize dependent libraries... pass_all
checking for dlltool... no
checking how to associate runtime and link libraries... printf %s\n
checking for archiver @FILE support... @
checking for strip... strip
checking for ranlib... ranlib
checking command to parse /usr/bin/nm -B output from gcc object... ok
checking for sysroot... no
checking for a working dd... /usr/bin/dd
checking how to truncate binary pipes... /usr/bin/dd bs=4096 count=1
checking for mt... mt
checking if mt is a manifest tool... no
checking how to run the C preprocessor... gcc -E
checking for ANSI C header files... yes
checking for sys/types.h... yes
checking for sys/stat.h... yes
checking for stdlib.h... yes
checking for string.h... yes
checking for memory.h... yes
checking for strings.h... yes
checking for inttypes.h... yes
checking for stdint.h... yes
checking for unistd.h... yes
checking for dlfcn.h... yes
checking for objdir... .libs
checking if gcc supports -fno-rtti -fno-exceptions... no
checking for gcc option to produce PIC... -fPIC -DPIC
checking if gcc PIC flag -fPIC -DPIC works... yes
checking if gcc static flag -static works... yes
checking if gcc supports -c -o file.o... yes
checking if gcc supports -c -o file.o... (cached) yes
checking whether the gcc linker (/usr/bin/ld -m elf_x86_64) supports shared libraries... yes
checking whether -lc should be explicitly linked in... no
checking dynamic linker characteristics... GNU/Linux ld.so
checking how to hardcode library paths into programs... immediate
checking whether stripping libraries is possible... yes
checking if libtool supports shared libraries... yes
checking whether to build shared libraries... yes
checking whether to build static libraries... yes
checking how to run the C++ preprocessor... g++ -E
checking for ld used by g++... /usr/bin/ld -m elf_x86_64
checking if the linker (/usr/bin/ld -m elf_x86_64) is GNU ld... yes
checking whether the g++ linker (/usr/bin/ld -m elf_x86_64) supports shared libraries... yes
checking for g++ option to produce PIC... -fPIC -DPIC
checking if g++ PIC flag -fPIC -DPIC works... yes
checking if g++ static flag -static works... yes
checking if g++ supports -c -o file.o... yes
checking if g++ supports -c -o file.o... (cached) yes
checking whether the g++ linker (/usr/bin/ld -m elf_x86_64) supports shared libraries... yes
checking dynamic linker characteristics... (cached) GNU/Linux ld.so
checking how to hardcode library paths into programs... immediate
checking for chmod... /usr/bin/chmod
checking for size_t... yes
checking for off_t... yes
checking for dirent.h that defines DIR... yes
checking for library containing opendir... none required
checking for ANSI C header files... (cached) yes
checking whether sys/types.h defines makedev... no
checking sys/mkdev.h usability... no
checking sys/mkdev.h presence... no
checking for sys/mkdev.h... no
checking sys/sysmacros.h usability... yes
checking sys/sysmacros.h presence... yes
checking for sys/sysmacros.h... yes
checking fcntl.h usability... yes
checking fcntl.h presence... yes
checking for fcntl.h... yes
checking malloc.h usability... yes
checking malloc.h presence... yes
checking for malloc.h... yes
checking mntent.h usability... yes
checking mntent.h presence... yes
checking for mntent.h... yes
checking netinet/in.h usability... yes
checking netinet/in.h presence... yes
checking for netinet/in.h... yes
checking paths.h usability... yes
checking paths.h presence... yes
checking for paths.h... yes
checking stddef.h usability... yes
checking stddef.h presence... yes
checking for stddef.h... yes
checking for stdlib.h... (cached) yes
checking for string.h... (cached) yes
checking linux/fd.h usability... yes
checking linux/fd.h presence... yes
checking for linux/fd.h... yes
checking sys/file.h usability... yes
checking sys/file.h presence... yes
checking for sys/file.h... yes
checking sys/ioctl.h usability... yes
checking sys/ioctl.h presence... yes
checking for sys/ioctl.h... yesize: Consider adding '-I m4' to ACLOCAL_AMFLAGS in Makefile.am.
autoreconf: running: /usr/bin/autoconf --force
autoreconf: running: /usr/bin/autoheader --force
autoreconf: running: automake --add-missing --copy --force-missing
configure.ac:10: installing './compile'
configure.ac:4: installing './missing'
fuse-ext2/Makefile.am: installing './depcomp'
autoreconf: Leaving directory `.'
Removing autom4te.cache
ubuntu@ubuntu:~/Downloads/fuse-ext2-master$ ./configure
checking build system type... x86_64-pc-linux-gnu
checking host system type... x86_64-pc-linux-gnu
checking targe
checking sys/mount.h usability... yes
checking sys/mount.h presence... yes
checking for sys/mount.h... yes
checking sys/param.h usability... yes
checking sys/param.h presence... yes
checking for sys/param.h... yes
checking sys/statvfs.h usability... yes
checking sys/statvfs.h presence... yes
checking for sys/statvfs.h... yes
checking sys/time.h usability... yes
checking sys/time.h presence... yes
checking for sys/time.h... yes
checking for sys/types.h... (cached) yes
checking for sys/stat.h... (cached) yes
checking for sys/mkdev.h... (cached) no
checking for sys/ioctl.h... (cached) yes
checking sys/syscall.h usability... yes
checking sys/syscall.h presence... yes
checking for sys/syscall.h... yes
checking sys/resource.h usability... yes
checking sys/resource.h presence... yes
checking for sys/resource.h... yes
checking sys/mman.h usability... yes
checking sys/mman.h presence... yes
checking for sys/mman.h... yes
checking sys/prctl.h usability... yes
checking sys/prctl.h presence... yes
checking for sys/prctl.h... yes
checking sys/disklabel.h usability... no
checking sys/disklabel.h presence... no
checking for sys/disklabel.h... no
checking sys/queue.h usability... yes
checking sys/queue.h presence... yes
checking for sys/queue.h... yes
checking sys/socket.h usability... yes
checking sys/socket.h presence... yes
checking for sys/socket.h... yes
checking sys/un.h usability... yes
checking sys/un.h presence... yes
checking for sys/un.h... yes
checking sys/sockio.h usability... no
checking sys/sockio.h presence... no
checking for sys/sockio.h... no
checking net/if.h usability... yes
checking net/if.h presence... yes
checking for net/if.h... yes
checking for netinet/in.h... (cached) yes
checking net/if_dl.h usability... no
checking net/if_dl.h presence... no
checking for net/if_dl.h... no
checking errno.h usability... yes
checking errno.h presence... yes
checking for errno.h... yes
checking for unistd.h... (cached) yes
checking utime.h usability... yes
checking utime.h presence... yes
checking for utime.h... yes
checking getopt.h usability... yes
checking getopt.h presence... yes
checking for getopt.h... yes
checking for inttypes.h... (cached) yes
checking for sys/disk.h... no
checking for sys/mount.h... (cached) yes
checking for an ANSI C-conforming const... yes
checking for inline... inline
checking for mode_t... yes
checking for off_t... (cached) yes
checking for size_t... (cached) yes
checking for ssize_t... yes
checking for struct stat.st_blksize... yes
checking for struct stat.st_blocks... yes
checking for struct stat.st_rdev... yes
checking whether time.h and sys/time.h may both be included... yes
checking whether llseek is declared... no
checking whether lseek64 is declared... yes
checking for ssize_t... (cached) yes
checking for vprintf... yes
checking for _doprnt... no
checking for uid_t in sys/types.h... yes
checking for unistd.h... (cached) yes
checking for working chown... yes
checking whether closedir returns void... no
checking for library containing getmntent... none required
checking whether gcc needs -traditional... no
checking for stdlib.h... (cached) yes
checking for GNU libc compatible malloc... yes
checking for working memcmp... yes
checking for stdlib.h... (cached) yes
checking for unistd.h... (cached) yes
checking for sys/param.h... (cached) yes
checking for utime.h... (cached) yes
checking for getpagesize... yes
checking for working mmap... yes
checking for stdlib.h... (cached) yes
checking for GNU libc compatible realloc... yes
checking sys/select.h usability... yes
checking sys/select.h presence... yes
checking for sys/select.h... yes
checking for sys/socket.h... (cached) yes
checking types of arguments for select... int,fd_set *,struct timeval *
checking whether lstat correctly handles trailing slash... yes
checking whether stat accepts an empty string... no
checking whether utime accepts a null argument... yes
checking for ftruncate... yes
checking for getmntent... (cached) yes
checking for getmntinfo... no
checking for getpagesize... (cached) yes
checking for hasmntopt... yes
checking for memmove... yes
checking for memset... yes
checking for munmap... yes
checking for random... yes
checking for select... yes
checking for srand... yes
checking for srandom... yes
checking for strcasecmp... yes
checking for strchr... yes
checking for strdup... yes
checking for strerror... yes
checking for strrchr... yes
checking for strtol... yes
checking for strtoul... yes
checking for strtoull... yes
checking for uname... yes
checking for utime... yes
checking for llseek... no
checking for lseek64... yes
checking for library containing sem_post... -lpthread
checking for library containing fuse_main... -lfuse
checking for library containing com_err... -lcom_err
checking for library containing ext2fs_open... -lext2fs
checking if FUSE on this system is too new for us... yes
Disabling debug support by default
checking that generated files are newer than configure... done
configure: creating ./config.status
config.status: creating fuse-ext2.pc
config.status: creating Makefile
config.status: creating fuse-ext2/Makefile
config.status: creating tools/Makefile
config.status: creating tools/macosx/Makefile
config.status: creating config.h
config.status: executing depfiles commands
config.status: executing libtool commands
ubuntu@ubuntu:~/Downloads/fuse-ext2-master$ make
make  all-recursive
make[1]: Entering directory '/home/ubuntu/Downloads/fuse-ext2-master'
Making all in fuse-ext2
make[2]: Entering directory '/home/ubuntu/Downloads/fuse-ext2-master/fuse-ext2'
gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -I/usr/local/include  -g -O2 -MT fuse_ext2-fuse-ext2.o -MD -MP -MF .deps/fuse_ext2-fuse-ext2.Tpo -c -o fuse_ext2-fuse-ext2.o `test -f 'fuse-ext2.c' || echo './'`fuse-ext2.c
mv -f .deps/fuse_ext2-fuse-ext2.Tpo .deps/fuse_ext2-fuse-ext2.Po
gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -I/usr/local/include  -g -O2 -MT fuse_ext2-do_probe.o -MD -MP -MF .deps/fuse_ext2-do_probe.Tpo -c -o fuse_ext2-do_probe.o `test -f 'do_probe.c' || echo './'`do_probe.c
mv -f .deps/fuse_ext2-do_probe.Tpo .deps/fuse_ext2-do_probe.Po
gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -I/usr/local/include  -g -O2 -MT fuse_ext2-do_check.o -MD -MP -MF .deps/fuse_ext2-do_check.Tpo -c -o fuse_ext2-do_check.o `test -f 'do_check.c' || echo './'`do_check.c
mv -f .deps/fuse_ext2-do_check.Tpo .deps/fuse_ext2-do_check.Po
gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -I/usr/local/include  -g -O2 -MT fuse_ext2-do_fillstatbuf.o -MD -MP -MF .deps/fuse_ext2-do_fillstatbuf.Tpo -c -o fuse_ext2-do_fillstatbuf.o `test -f 'do_fillstatbuf.c' || echo './'`do_fillstatbuf.c
mv -f .deps/fuse_ext2-do_fillstatbuf.Tpo .deps/fuse_ext2-do_fillstatbuf.Po
gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -I/usr/local/include  -g -O2 -MT fuse_ext2-do_readinode.o -MD -MP -MF .deps/fuse_ext2-do_readinode.Tpo -c -o fuse_ext2-do_readinode.o `test -f 'do_readinode.c' || echo './'`do_readinode.c
mv -f .deps/fuse_ext2-do_readinode.Tpo .deps/fuse_ext2-do_readinode.Po
gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -I/usr/local/include  -g -O2 -MT fuse_ext2-do_writeinode.o -MD -MP -MF .deps/fuse_ext2-do_writeinode.Tpo -c -o fuse_ext2-do_writeinode.o `test -f 'do_writeinode.c' || echo './'`do_writeinode.c
mv -f .deps/fuse_ext2-do_writeinode.Tpo .deps/fuse_ext2-do_writeinode.Po
gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -I/usr/local/include  -g -O2 -MT fuse_ext2-do_killfilebyinode.o -MD -MP -MF .deps/fuse_ext2-do_killfilebyinode.Tpo -c -o fuse_ext2-do_killfilebyinode.o `test -f 'do_killfilebyinode.c' || echo './'`do_killfilebyinode.c
mv -f .deps/fuse_ext2-do_killfilebyinode.Tpo .deps/fuse_ext2-do_killfilebyinode.Po
gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -I/usr/local/include  -g -O2 -MT fuse_ext2-op_init.o -MD -MP -MF .deps/fuse_ext2-op_init.Tpo -c -o fuse_ext2-op_init.o `test -f 'op_init.c' || echo './'`op_init.c
mv -f .deps/fuse_ext2-op_init.Tpo .deps/fuse_ext2-op_init.Po
gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -I/usr/local/include  -g -O2 -MT fuse_ext2-op_destroy.o -MD -MP -MF .deps/fuse_ext2-op_destroy.Tpo -c -o fuse_ext2-op_destroy.o `test -f 'op_destroy.c' || echo './'`op_destroy.c
mv -f .deps/fuse_ext2-op_destroy.Tpo .deps/fuse_ext2-op_destroy.Po
gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -I/usr/local/include  -g -O2 -MT fuse_ext2-op_access.o -MD -MP -MF .deps/fuse_ext2-op_access.Tpo -c -o fuse_ext2-op_access.o `test -f 'op_access.c' || echo './'`op_access.c
mv -f .deps/fuse_ext2-op_access.Tpo .deps/fuse_ext2-op_access.Po
gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -I/usr/local/include  -g -O2 -MT fuse_ext2-op_fgetattr.o -MD -MP -MF .deps/fuse_ext2-op_fgetattr.Tpo -c -o fuse_ext2-op_fgetattr.o `test -f 'op_fgetattr.c' || echo './'`op_fgetattr.c
mv -f .deps/fuse_ext2-op_fgetattr.Tpo .deps/fuse_ext2-op_fgetattr.Po
gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -I/usr/local/include  -g -O2 -MT fuse_ext2-op_getattr.o -MD -MP -MF .deps/fuse_ext2-op_getattr.Tpo -c -o fuse_ext2-op_getattr.o `test -f 'op_getattr.c' || echo './'`op_getattr.c
mv -f .deps/fuse_ext2-op_getattr.Tpo .deps/fuse_ext2-op_getattr.Po
gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -I/usr/local/include  -g -O2 -MT fuse_ext2-op_getxattr.o -MD -MP -MF .deps/fuse_ext2-op_getxattr.Tpo -c -o fuse_ext2-op_getxattr.o `test -f 'op_getxattr.c' || echo './'`op_getxattr.c
mv -f .deps/fuse_ext2-op_getxattr.Tpo .deps/fuse_ext2-op_getxattr.Po
gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -I/usr/local/include  -g -O2 -MT fuse_ext2-op_open.o -MD -MP -MF .deps/fuse_ext2-op_open.Tpo -c -o fuse_ext2-op_open.o `test -f 'op_open.c' || echo './'`op_open.c
mv -f .deps/fuse_ext2-op_open.Tpo .deps/fuse_ext2-op_open.Po
gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -I/usr/local/include  -g -O2 -MT fuse_ext2-op_read.o -MD -MP -MF .deps/fuse_ext2-op_read.Tpo -c -o fuse_ext2-op_read.o `test -f 'op_read.c' || echo './'`op_read.c
mv -f .deps/fuse_ext2-op_read.Tpo .deps/fuse_ext2-op_read.Po
gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -I/usr/local/include  -g -O2 -MT fuse_ext2-op_readdir.o -MD -MP -MF .deps/fuse_ext2-op_readdir.Tpo -c -o fuse_ext2-op_readdir.o `test -f 'op_readdir.c' || echo './'`op_readdir.c
mv -f .deps/fuse_ext2-op_readdir.Tpo .deps/fuse_ext2-op_readdir.Po
gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -I/usr/local/include  -g -O2 -MT fuse_ext2-op_readlink.o -MD -MP -MF .deps/fuse_ext2-op_readlink.Tpo -c -o fuse_ext2-op_readlink.o `test -f 'op_readlink.c' || echo './'`op_readlink.c
mv -f .deps/fuse_ext2-op_readlink.Tpo .deps/fuse_ext2-op_readlink.Po
gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -I/usr/local/include  -g -O2 -MT fuse_ext2-op_release.o -MD -MP -MF .deps/fuse_ext2-op_release.Tpo -c -o fuse_ext2-op_release.o `test -f 'op_release.c' || echo './'`op_release.c
mv -f .deps/fuse_ext2-op_release.Tpo .deps/fuse_ext2-op_release.Po
gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -I/usr/local/include  -g -O2 -MT fuse_ext2-op_statfs.o -MD -MP -MF .deps/fuse_ext2-op_statfs.Tpo -c -o fuse_ext2-op_statfs.o `test -f 'op_statfs.c' || echo './'`op_statfs.c
mv -f .deps/fuse_ext2-op_statfs.Tpo .deps/fuse_ext2-op_statfs.Po
gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -I/usr/local/include  -g -O2 -MT fuse_ext2-op_chown.o -MD -MP -MF .deps/fuse_ext2-op_chown.Tpo -c -o fuse_ext2-op_chown.o `test -f 'op_chown.c' || echo './'`op_chown.c
mv -f .deps/fuse_ext2-op_chown.Tpo .deps/fuse_ext2-op_chown.Po
gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -I/usr/local/include  -g -O2 -MT fuse_ext2-op_chmod.o -MD -MP -MF .deps/fuse_ext2-op_chmod.Tpo -c -o fuse_ext2-op_chmod.o `test -f 'op_chmod.c' || echo './'`op_chmod.c
mv -f .deps/fuse_ext2-op_chmod.Tpo .deps/fuse_ext2-op_chmod.Po
gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -I/usr/local/include  -g -O2 -MT fuse_ext2-op_create.o -MD -MP -MF .deps/fuse_ext2-op_create.Tpo -c -o fuse_ext2-op_create.o `test -f 'op_create.c' || echo './'`op_create.c
mv -f .deps/fuse_ext2-op_create.Tpo .deps/fuse_ext2-op_create.Po
gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -I/usr/local/include  -g -O2 -MT fuse_ext2-op_flush.o -MD -MP -MF .deps/fuse_ext2-op_flush.Tpo -c -o fuse_ext2-op_flush.o `test -f 'op_flush.c' || echo './'`op_flush.c
mv -f .deps/fuse_ext2-op_flush.Tpo .deps/fuse_ext2-op_flush.Po
gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -I/usr/local/include  -g -O2 -MT fuse_ext2-op_fsync.o -MD -MP -MF .deps/fuse_ext2-op_fsync.Tpo -c -o fuse_ext2-op_fsync.o `test -f 'op_fsync.c' || echo './'`op_fsync.c
mv -f .deps/fuse_ext2-op_fsync.Tpo .deps/fuse_ext2-op_fsync.Po
gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -I/usr/local/include  -g -O2 -MT fuse_ext2-op_mkdir.o -MD -MP -MF .deps/fuse_ext2-op_mkdir.Tpo -c -o fuse_ext2-op_mkdir.o `test -f 'op_mkdir.c' || echo './'`op_mkdir.c
mv -f .deps/fuse_ext2-op_mkdir.Tpo .deps/fuse_ext2-op_mkdir.Po
gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -I/usr/local/include  -g -O2 -MT fuse_ext2-op_rmdir.o -MD -MP -MF .deps/fuse_ext2-op_rmdir.Tpo -c -o fuse_ext2-op_rmdir.o `test -f 'op_rmdir.c' || echo './'`op_rmdir.c
mv -f .deps/fuse_ext2-op_rmdir.Tpo .deps/fuse_ext2-op_rmdir.Po
gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -I/usr/local/include  -g -O2 -MT fuse_ext2-op_unlink.o -MD -MP -MF .deps/fuse_ext2-op_unlink.Tpo -c -o fuse_ext2-op_unlink.o `test -f 'op_unlink.c' || echo './'`op_unlink.c
mv -f .deps/fuse_ext2-op_unlink.Tpo .deps/fuse_ext2-op_unlink.Po
gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -I/usr/local/include  -g -O2 -MT fuse_ext2-op_utimens.o -MD -MP -MF .deps/fuse_ext2-op_utimens.Tpo -c -o fuse_ext2-op_utimens.o `test -f 'op_utimens.c' || echo './'`op_utimens.c
mv -f .deps/fuse_ext2-op_utimens.Tpo .deps/fuse_ext2-op_utimens.Po
gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -I/usr/local/include  -g -O2 -MT fuse_ext2-op_write.o -MD -MP -MF .deps/fuse_ext2-op_write.Tpo -c -o fuse_ext2-op_write.o `test -f 'op_write.c' || echo './'`op_write.c
mv -f .deps/fuse_ext2-op_write.Tpo .deps/fuse_ext2-op_write.Po
gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -I/usr/local/include  -g -O2 -MT fuse_ext2-op_mknod.o -MD -MP -MF .deps/fuse_ext2-op_mknod.Tpo -c -o fuse_ext2-op_mknod.o `test -f 'op_mknod.c' || echo './'`op_mknod.c
mv -f .deps/fuse_ext2-op_mknod.Tpo .deps/fuse_ext2-op_mknod.Po
gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -I/usr/local/include  -g -O2 -MT fuse_ext2-op_symlink.o -MD -MP -MF .deps/fuse_ext2-op_symlink.Tpo -c -o fuse_ext2-op_symlink.o `test -f 'op_symlink.c' || echo './'`op_symlink.c
mv -f .deps/fuse_ext2-op_symlink.Tpo .deps/fuse_ext2-op_symlink.Po
gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -I/usr/local/include  -g -O2 -MT fuse_ext2-op_truncate.o -MD -MP -MF .deps/fuse_ext2-op_truncate.Tpo -c -o fuse_ext2-op_truncate.o `test -f 'op_truncate.c' || echo './'`op_truncate.c
mv -f .deps/fuse_ext2-op_truncate.Tpo .deps/fuse_ext2-op_truncate.Po
gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -I/usr/local/include  -g -O2 -MT fuse_ext2-op_link.o -MD -MP -MF .deps/fuse_ext2-op_link.Tpo -c -o fuse_ext2-op_link.o `test -f 'op_link.c' || echo './'`op_link.c
mv -f .deps/fuse_ext2-op_link.Tpo .deps/fuse_ext2-op_link.Po
gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -I/usr/local/include  -g -O2 -MT fuse_ext2-op_rename.o -MD -MP -MF .deps/fuse_ext2-op_rename.Tpo -c -o fuse_ext2-op_rename.o `test -f 'op_rename.c' || echo './'`op_rename.c
mv -f .deps/fuse_ext2-op_rename.Tpo .deps/fuse_ext2-op_rename.Po
/bin/bash ../libtool  --tag=CC   --mode=link gcc -Wall -DHAVE_CONFIG_H -I/usr/local/include  -g -O2   -o fuse-ext2 fuse_ext2-fuse-ext2.o fuse_ext2-do_probe.o fuse_ext2-do_check.o fuse_ext2-do_fillstatbuf.o fuse_ext2-do_readinode.o fuse_ext2-do_writeinode.o fuse_ext2-do_killfilebyinode.o fuse_ext2-op_init.o fuse_ext2-op_destroy.o fuse_ext2-op_access.o fuse_ext2-op_fgetattr.o fuse_ext2-op_getattr.o fuse_ext2-op_getxattr.o fuse_ext2-op_open.o fuse_ext2-op_read.o fuse_ext2-op_readdir.o fuse_ext2-op_readlink.o fuse_ext2-op_release.o fuse_ext2-op_statfs.o fuse_ext2-op_chown.o fuse_ext2-op_chmod.o fuse_ext2-op_create.o fuse_ext2-op_flush.o fuse_ext2-op_fsync.o fuse_ext2-op_mkdir.o fuse_ext2-op_rmdir.o fuse_ext2-op_unlink.o fuse_ext2-op_utimens.o fuse_ext2-op_write.o fuse_ext2-op_mknod.o fuse_ext2-op_symlink.o fuse_ext2-op_truncate.o fuse_ext2-op_link.o fuse_ext2-op_rename.o  -lext2fs -lcom_err -lfuse -lpthread 
libtool: link: gcc -Wall -DHAVE_CONFIG_H -I/usr/local/include -g -O2 -o fuse-ext2 fuse_ext2-fuse-ext2.o fuse_ext2-do_probe.o fuse_ext2-do_check.o fuse_ext2-do_fillstatbuf.o fuse_ext2-do_readinode.o fuse_ext2-do_writeinode.o fuse_ext2-do_killfilebyinode.o fuse_ext2-op_init.o fuse_ext2-op_destroy.o fuse_ext2-op_access.o fuse_ext2-op_fgetattr.o fuse_ext2-op_getattr.o fuse_ext2-op_getxattr.o fuse_ext2-op_open.o fuse_ext2-op_read.o fuse_ext2-op_readdir.o fuse_ext2-op_readlink.o fuse_ext2-op_release.o fuse_ext2-op_statfs.o fuse_ext2-op_chown.o fuse_ext2-op_chmod.o fuse_ext2-op_create.o fuse_ext2-op_flush.o fuse_ext2-op_fsync.o fuse_ext2-op_mkdir.o fuse_ext2-op_rmdir.o fuse_ext2-op_unlink.o fuse_ext2-op_utimens.o fuse_ext2-op_write.o fuse_ext2-op_mknod.o fuse_ext2-op_symlink.o fuse_ext2-op_truncate.o fuse_ext2-op_link.o fuse_ext2-op_rename.o  -lext2fs -lcom_err -lfuse -lpthread
gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -I/usr/local/include  -g -O2 -MT fuse_ext2_probe-fuse-ext2.probe.o -MD -MP -MF .deps/fuse_ext2_probe-fuse-ext2.probe.Tpo -c -o fuse_ext2_probe-fuse-ext2.probe.o `test -f 'fuse-ext2.probe.c' || echo './'`fuse-ext2.probe.c
mv -f .deps/fuse_ext2_probe-fuse-ext2.probe.Tpo .deps/fuse_ext2_probe-fuse-ext2.probe.Po
gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -I/usr/local/include  -g -O2 -MT fuse_ext2_probe-do_probe.o -MD -MP -MF .deps/fuse_ext2_probe-do_probe.Tpo -c -o fuse_ext2_probe-do_probe.o `test -f 'do_probe.c' || echo './'`do_probe.c
mv -f .deps/fuse_ext2_probe-do_probe.Tpo .deps/fuse_ext2_probe-do_probe.Po
/bin/bash ../libtool  --tag=CC   --mode=link gcc -Wall -DHAVE_CONFIG_H -I/usr/local/include  -g -O2   -o fuse-ext2.probe fuse_ext2_probe-fuse-ext2.probe.o fuse_ext2_probe-do_probe.o  -lext2fs -lcom_err -lfuse -lpthread 
libtool: link: gcc -Wall -DHAVE_CONFIG_H -I/usr/local/include -g -O2 -o fuse-ext2.probe fuse_ext2_probe-fuse-ext2.probe.o fuse_ext2_probe-do_probe.o  -lext2fs -lcom_err -lfuse -lpthread
/bin/bash ../libtool  --tag=CC   --mode=compile gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE  -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-fuse-ext2.lo -MD -MP -MF .deps/umfuseext2_la-fuse-ext2.Tpo -c -o umfuseext2_la-fuse-ext2.lo `test -f 'fuse-ext2.c' || echo './'`fuse-ext2.c
libtool: compile:  gcc -DHAVE_CONFIG_H -I. -I.. -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-fuse-ext2.lo -MD -MP -MF .deps/umfuseext2_la-fuse-ext2.Tpo -c fuse-ext2.c  -fPIC -DPIC -o .libs/umfuseext2_la-fuse-ext2.o
libtool: compile:  gcc -DHAVE_CONFIG_H -I. -I.. -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-fuse-ext2.lo -MD -MP -MF .deps/umfuseext2_la-fuse-ext2.Tpo -c fuse-ext2.c -o umfuseext2_la-fuse-ext2.o >/dev/null 2>&1
mv -f .deps/umfuseext2_la-fuse-ext2.Tpo .deps/umfuseext2_la-fuse-ext2.Plo
/bin/bash ../libtool  --tag=CC   --mode=compile gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE  -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-do_probe.lo -MD -MP -MF .deps/umfuseext2_la-do_probe.Tpo -c -o umfuseext2_la-do_probe.lo `test -f 'do_probe.c' || echo './'`do_probe.c
libtool: compile:  gcc -DHAVE_CONFIG_H -I. -I.. -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-do_probe.lo -MD -MP -MF .deps/umfuseext2_la-do_probe.Tpo -c do_probe.c  -fPIC -DPIC -o .libs/umfuseext2_la-do_probe.o
libtool: compile:  gcc -DHAVE_CONFIG_H -I. -I.. -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-do_probe.lo -MD -MP -MF .deps/umfuseext2_la-do_probe.Tpo -c do_probe.c -o umfuseext2_la-do_probe.o >/dev/null 2>&1
mv -f .deps/umfuseext2_la-do_probe.Tpo .deps/umfuseext2_la-do_probe.Plo
/bin/bash ../libtool  --tag=CC   --mode=compile gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE  -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-do_check.lo -MD -MP -MF .deps/umfuseext2_la-do_check.Tpo -c -o umfuseext2_la-do_check.lo `test -f 'do_check.c' || echo './'`do_check.c
libtool: compile:  gcc -DHAVE_CONFIG_H -I. -I.. -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-do_check.lo -MD -MP -MF .deps/umfuseext2_la-do_check.Tpo -c do_check.c  -fPIC -DPIC -o .libs/umfuseext2_la-do_check.o
libtool: compile:  gcc -DHAVE_CONFIG_H -I. -I.. -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-do_check.lo -MD -MP -MF .deps/umfuseext2_la-do_check.Tpo -c do_check.c -o umfuseext2_la-do_check.o >/dev/null 2>&1
mv -f .deps/umfuseext2_la-do_check.Tpo .deps/umfuseext2_la-do_check.Plo
/bin/bash ../libtool  --tag=CC   --mode=compile gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE  -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-do_fillstatbuf.lo -MD -MP -MF .deps/umfuseext2_la-do_fillstatbuf.Tpo -c -o umfuseext2_la-do_fillstatbuf.lo `test -f 'do_fillstatbuf.c' || echo './'`do_fillstatbuf.c
libtool: compile:  gcc -DHAVE_CONFIG_H -I. -I.. -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-do_fillstatbuf.lo -MD -MP -MF .deps/umfuseext2_la-do_fillstatbuf.Tpo -c do_fillstatbuf.c  -fPIC -DPIC -o .libs/umfuseext2_la-do_fillstatbuf.o
libtool: compile:  gcc -DHAVE_CONFIG_H -I. -I.. -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-do_fillstatbuf.lo -MD -MP -MF .deps/umfuseext2_la-do_fillstatbuf.Tpo -c do_fillstatbuf.c -o umfuseext2_la-do_fillstatbuf.o >/dev/null 2>&1
mv -f .deps/umfuseext2_la-do_fillstatbuf.Tpo .deps/umfuseext2_la-do_fillstatbuf.Plo
/bin/bash ../libtool  --tag=CC   --mode=compile gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE  -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-do_readinode.lo -MD -MP -MF .deps/umfuseext2_la-do_readinode.Tpo -c -o umfuseext2_la-do_readinode.lo `test -f 'do_readinode.c' || echo './'`do_readinode.c
libtool: compile:  gcc -DHAVE_CONFIG_H -I. -I.. -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-do_readinode.lo -MD -MP -MF .deps/umfuseext2_la-do_readinode.Tpo -c do_readinode.c  -fPIC -DPIC -o .libs/umfuseext2_la-do_readinode.o
libtool: compile:  gcc -DHAVE_CONFIG_H -I. -I.. -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-do_readinode.lo -MD -MP -MF .deps/umfuseext2_la-do_readinode.Tpo -c do_readinode.c -o umfuseext2_la-do_readinode.o >/dev/null 2>&1
mv -f .deps/umfuseext2_la-do_readinode.Tpo .deps/umfuseext2_la-do_readinode.Plo
/bin/bash ../libtool  --tag=CC   --mode=compile gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE  -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-do_writeinode.lo -MD -MP -MF .deps/umfuseext2_la-do_writeinode.Tpo -c -o umfuseext2_la-do_writeinode.lo `test -f 'do_writeinode.c' || echo './'`do_writeinode.c
libtool: compile:  gcc -DHAVE_CONFIG_H -I. -I.. -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-do_writeinode.lo -MD -MP -MF .deps/umfuseext2_la-do_writeinode.Tpo -c do_writeinode.c  -fPIC -DPIC -o .libs/umfuseext2_la-do_writeinode.o
libtool: compile:  gcc -DHAVE_CONFIG_H -I. -I.. -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-do_writeinode.lo -MD -MP -MF .deps/umfuseext2_la-do_writeinode.Tpo -c do_writeinode.c -o umfuseext2_la-do_writeinode.o >/dev/null 2>&1
mv -f .deps/umfuseext2_la-do_writeinode.Tpo .deps/umfuseext2_la-do_writeinode.Plo
/bin/bash ../libtool  --tag=CC   --mode=compile gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE  -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-do_killfilebyinode.lo -MD -MP -MF .deps/umfuseext2_la-do_killfilebyinode.Tpo -c -o umfuseext2_la-do_killfilebyinode.lo `test -f 'do_killfilebyinode.c' || echo './'`do_killfilebyinode.c
libtool: compile:  gcc -DHAVE_CONFIG_H -I. -I.. -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-do_killfilebyinode.lo -MD -MP -MF .deps/umfuseext2_la-do_killfilebyinode.Tpo -c do_killfilebyinode.c  -fPIC -DPIC -o .libs/umfuseext2_la-do_killfilebyinode.o
libtool: compile:  gcc -DHAVE_CONFIG_H -I. -I.. -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-do_killfilebyinode.lo -MD -MP -MF .deps/umfuseext2_la-do_killfilebyinode.Tpo -c do_killfilebyinode.c -o umfuseext2_la-do_killfilebyinode.o >/dev/null 2>&1
mv -f .deps/umfuseext2_la-do_killfilebyinode.Tpo .deps/umfuseext2_la-do_killfilebyinode.Plo
/bin/bash ../libtool  --tag=CC   --mode=compile gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE  -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_init.lo -MD -MP -MF .deps/umfuseext2_la-op_init.Tpo -c -o umfuseext2_la-op_init.lo `test -f 'op_init.c' || echo './'`op_init.c
libtool: compile:  gcc -DHAVE_CONFIG_H -I. -I.. -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_init.lo -MD -MP -MF .deps/umfuseext2_la-op_init.Tpo -c op_init.c  -fPIC -DPIC -o .libs/umfuseext2_la-op_init.o
libtool: compile:  gcc -DHAVE_CONFIG_H -I. -I.. -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_init.lo -MD -MP -MF .deps/umfuseext2_la-op_init.Tpo -c op_init.c -o umfuseext2_la-op_init.o >/dev/null 2>&1
mv -f .deps/umfuseext2_la-op_init.Tpo .deps/umfuseext2_la-op_init.Plo
/bin/bash ../libtool  --tag=CC   --mode=compile gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE  -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_destroy.lo -MD -MP -MF .deps/umfuseext2_la-op_destroy.Tpo -c -o umfuseext2_la-op_destroy.lo `test -f 'op_destroy.c' || echo './'`op_destroy.c
libtool: compile:  gcc -DHAVE_CONFIG_H -I. -I.. -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_destroy.lo -MD -MP -MF .deps/umfuseext2_la-op_destroy.Tpo -c op_destroy.c  -fPIC -DPIC -o .libs/umfuseext2_la-op_destroy.o
libtool: compile:  gcc -DHAVE_CONFIG_H -I. -I.. -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_destroy.lo -MD -MP -MF .deps/umfuseext2_la-op_destroy.Tpo -c op_destroy.c -o umfuseext2_la-op_destroy.o >/dev/null 2>&1
mv -f .deps/umfuseext2_la-op_destroy.Tpo .deps/umfuseext2_la-op_destroy.Plo
/bin/bash ../libtool  --tag=CC   --mode=compile gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE  -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_access.lo -MD -MP -MF .deps/umfuseext2_la-op_access.Tpo -c -o umfuseext2_la-op_access.lo `test -f 'op_access.c' || echo './'`op_access.c
libtool: compile:  gcc -DHAVE_CONFIG_H -I. -I.. -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_access.lo -MD -MP -MF .deps/umfuseext2_la-op_access.Tpo -c op_access.c  -fPIC -DPIC -o .libs/umfuseext2_la-op_access.o
libtool: compile:  gcc -DHAVE_CONFIG_H -I. -I.. -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_access.lo -MD -MP -MF .deps/umfuseext2_la-op_access.Tpo -c op_access.c -o umfuseext2_la-op_access.o >/dev/null 2>&1
mv -f .deps/umfuseext2_la-op_access.Tpo .deps/umfuseext2_la-op_access.Plo
/bin/bash ../libtool  --tag=CC   --mode=compile gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE  -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_fgetattr.lo -MD -MP -MF .deps/umfuseext2_la-op_fgetattr.Tpo -c -o umfuseext2_la-op_fgetattr.lo `test -f 'op_fgetattr.c' || echo './'`op_fgetattr.c
libtool: compile:  gcc -DHAVE_CONFIG_H -I. -I.. -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_fgetattr.lo -MD -MP -MF .deps/umfuseext2_la-op_fgetattr.Tpo -c op_fgetattr.c  -fPIC -DPIC -o .libs/umfuseext2_la-op_fgetattr.o
libtool: compile:  gcc -DHAVE_CONFIG_H -I. -I.. -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_fgetattr.lo -MD -MP -MF .deps/umfuseext2_la-op_fgetattr.Tpo -c op_fgetattr.c -o umfuseext2_la-op_fgetattr.o >/dev/null 2>&1
mv -f .deps/umfuseext2_la-op_fgetattr.Tpo .deps/umfuseext2_la-op_fgetattr.Plo
/bin/bash ../libtool  --tag=CC   --mode=compile gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE  -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_getattr.lo -MD -MP -MF .deps/umfuseext2_la-op_getattr.Tpo -c -o umfuseext2_la-op_getattr.lo `test -f 'op_getattr.c' || echo './'`op_getattr.c
libtool: compile:  gcc -DHAVE_CONFIG_H -I. -I.. -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_getattr.lo -MD -MP -MF .deps/umfuseext2_la-op_getattr.Tpo -c op_getattr.c  -fPIC -DPIC -o .libs/umfuseext2_la-op_getattr.o
libtool: compile:  gcc -DHAVE_CONFIG_H -I. -I.. -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_getattr.lo -MD -MP -MF .deps/umfuseext2_la-op_getattr.Tpo -c op_getattr.c -o umfuseext2_la-op_getattr.o >/dev/null 2>&1
mv -f .deps/umfuseext2_la-op_getattr.Tpo .deps/umfuseext2_la-op_getattr.Plo
/bin/bash ../libtool  --tag=CC   --mode=compile gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE  -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_getxattr.lo -MD -MP -MF .deps/umfuseext2_la-op_getxattr.Tpo -c -o umfuseext2_la-op_getxattr.lo `test -f 'op_getxattr.c' || echo './'`op_getxattr.c
libtool: compile:  gcc -DHAVE_CONFIG_H -I. -I.. -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_getxattr.lo -MD -MP -MF .deps/umfuseext2_la-op_getxattr.Tpo -c op_getxattr.c  -fPIC -DPIC -o .libs/umfuseext2_la-op_getxattr.o
libtool: compile:  gcc -DHAVE_CONFIG_H -I. -I.. -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_getxattr.lo -MD -MP -MF .deps/umfuseext2_la-op_getxattr.Tpo -c op_getxattr.c -o umfuseext2_la-op_getxattr.o >/dev/null 2>&1
mv -f .deps/umfuseext2_la-op_getxattr.Tpo .deps/umfuseext2_la-op_getxattr.Plo
/bin/bash ../libtool  --tag=CC   --mode=compile gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE  -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_open.lo -MD -MP -MF .deps/umfuseext2_la-op_open.Tpo -c -o umfuseext2_la-op_open.lo `test -f 'op_open.c' || echo './'`op_open.c
libtool: compile:  gcc -DHAVE_CONFIG_H -I. -I.. -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_open.lo -MD -MP -MF .deps/umfuseext2_la-op_open.Tpo -c op_open.c  -fPIC -DPIC -o .libs/umfuseext2_la-op_open.o
libtool: compile:  gcc -DHAVE_CONFIG_H -I. -I.. -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_open.lo -MD -MP -MF .deps/umfuseext2_la-op_open.Tpo -c op_open.c -o umfuseext2_la-op_open.o >/dev/null 2>&1
mv -f .deps/umfuseext2_la-op_open.Tpo .deps/umfuseext2_la-op_open.Plo
/bin/bash ../libtool  --tag=CC   --mode=compile gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE  -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_read.lo -MD -MP -MF .deps/umfuseext2_la-op_read.Tpo -c -o umfuseext2_la-op_read.lo `test -f 'op_read.c' || echo './'`op_read.c
libtool: compile:  gcc -DHAVE_CONFIG_H -I. -I.. -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_read.lo -MD -MP -MF .deps/umfuseext2_la-op_read.Tpo -c op_read.c  -fPIC -DPIC -o .libs/umfuseext2_la-op_read.o
libtool: compile:  gcc -DHAVE_CONFIG_H -I. -I.. -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_read.lo -MD -MP -MF .deps/umfuseext2_la-op_read.Tpo -c op_read.c -o umfuseext2_la-op_read.o >/dev/null 2>&1
mv -f .deps/umfuseext2_la-op_read.Tpo .deps/umfuseext2_la-op_read.Plo
/bin/bash ../libtool  --tag=CC   --mode=compile gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE  -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_readdir.lo -MD -MP -MF .deps/umfuseext2_la-op_readdir.Tpo -c -o umfuseext2_la-op_readdir.lo `test -f 'op_readdir.c' || echo './'`op_readdir.c
libtool: compile:  gcc -DHAVE_CONFIG_H -I. -I.. -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_readdir.lo -MD -MP -MF .deps/umfuseext2_la-op_readdir.Tpo -c op_readdir.c  -fPIC -DPIC -o .libs/umfuseext2_la-op_readdir.o
libtool: compile:  gcc -DHAVE_CONFIG_H -I. -I.. -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_readdir.lo -MD -MP -MF .deps/umfuseext2_la-op_readdir.Tpo -c op_readdir.c -o umfuseext2_la-op_readdir.o >/dev/null 2>&1
mv -f .deps/umfuseext2_la-op_readdir.Tpo .deps/umfuseext2_la-op_readdir.Plo
/bin/bash ../libtool  --tag=CC   --mode=compile gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE  -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_readlink.lo -MD -MP -MF .deps/umfuseext2_la-op_readlink.Tpo -c -o umfuseext2_la-op_readlink.lo `test -f 'op_readlink.c' || echo './'`op_readlink.c
libtool: compile:  gcc -DHAVE_CONFIG_H -I. -I.. -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_readlink.lo -MD -MP -MF .deps/umfuseext2_la-op_readlink.Tpo -c op_readlink.c  -fPIC -DPIC -o .libs/umfuseext2_la-op_readlink.o
libtool: compile:  gcc -DHAVE_CONFIG_H -I. -I.. -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_readlink.lo -MD -MP -MF .deps/umfuseext2_la-op_readlink.Tpo -c op_readlink.c -o umfuseext2_la-op_readlink.o >/dev/null 2>&1
mv -f .deps/umfuseext2_la-op_readlink.Tpo .deps/umfuseext2_la-op_readlink.Plo
/bin/bash ../libtool  --tag=CC   --mode=compile gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE  -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_release.lo -MD -MP -MF .deps/umfuseext2_la-op_release.Tpo -c -o umfuseext2_la-op_release.lo `test -f 'op_release.c' || echo './'`op_release.c
libtool: compile:  gcc -DHAVE_CONFIG_H -I. -I.. -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_release.lo -MD -MP -MF .deps/umfuseext2_la-op_release.Tpo -c op_release.c  -fPIC -DPIC -o .libs/umfuseext2_la-op_release.o
libtool: compile:  gcc -DHAVE_CONFIG_H -I. -I.. -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_release.lo -MD -MP -MF .deps/umfuseext2_la-op_release.Tpo -c op_release.c -o umfuseext2_la-op_release.o >/dev/null 2>&1
mv -f .deps/umfuseext2_la-op_release.Tpo .deps/umfuseext2_la-op_release.Plo
/bin/bash ../libtool  --tag=CC   --mode=compile gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE  -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_statfs.lo -MD -MP -MF .deps/umfuseext2_la-op_statfs.Tpo -c -o umfuseext2_la-op_statfs.lo `test -f 'op_statfs.c' || echo './'`op_statfs.c
libtool: compile:  gcc -DHAVE_CONFIG_H -I. -I.. -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_statfs.lo -MD -MP -MF .deps/umfuseext2_la-op_statfs.Tpo -c op_statfs.c  -fPIC -DPIC -o .libs/umfuseext2_la-op_statfs.o
libtool: compile:  gcc -DHAVE_CONFIG_H -I. -I.. -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_statfs.lo -MD -MP -MF .deps/umfuseext2_la-op_statfs.Tpo -c op_statfs.c -o umfuseext2_la-op_statfs.o >/dev/null 2>&1
mv -f .deps/umfuseext2_la-op_statfs.Tpo .deps/umfuseext2_la-op_statfs.Plo
/bin/bash ../libtool  --tag=CC   --mode=compile gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE  -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_chown.lo -MD -MP -MF .deps/umfuseext2_la-op_chown.Tpo -c -o umfuseext2_la-op_chown.lo `test -f 'op_chown.c' || echo './'`op_chown.c
libtool: compile:  gcc -DHAVE_CONFIG_H -I. -I.. -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_chown.lo -MD -MP -MF .deps/umfuseext2_la-op_chown.Tpo -c op_chown.c  -fPIC -DPIC -o .libs/umfuseext2_la-op_chown.o
libtool: compile:  gcc -DHAVE_CONFIG_H -I. -I.. -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_chown.lo -MD -MP -MF .deps/umfuseext2_la-op_chown.Tpo -c op_chown.c -o umfuseext2_la-op_chown.o >/dev/null 2>&1
mv -f .deps/umfuseext2_la-op_chown.Tpo .deps/umfuseext2_la-op_chown.Plo
/bin/bash ../libtool  --tag=CC   --mode=compile gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE  -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_chmod.lo -MD -MP -MF .deps/umfuseext2_la-op_chmod.Tpo -c -o umfuseext2_la-op_chmod.lo `test -f 'op_chmod.c' || echo './'`op_chmod.c
libtool: compile:  gcc -DHAVE_CONFIG_H -I. -I.. -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_chmod.lo -MD -MP -MF .deps/umfuseext2_la-op_chmod.Tpo -c op_chmod.c  -fPIC -DPIC -o .libs/umfuseext2_la-op_chmod.o
libtool: compile:  gcc -DHAVE_CONFIG_H -I. -I.. -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_chmod.lo -MD -MP -MF .deps/umfuseext2_la-op_chmod.Tpo -c op_chmod.c -o umfuseext2_la-op_chmod.o >/dev/null 2>&1
mv -f .deps/umfuseext2_la-op_chmod.Tpo .deps/umfuseext2_la-op_chmod.Plo
/bin/bash ../libtool  --tag=CC   --mode=compile gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE  -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_create.lo -MD -MP -MF .deps/umfuseext2_la-op_create.Tpo -c -o umfuseext2_la-op_create.lo `test -f 'op_create.c' || echo './'`op_create.c
libtool: compile:  gcc -DHAVE_CONFIG_H -I. -I.. -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_create.lo -MD -MP -MF .deps/umfuseext2_la-op_create.Tpo -c op_create.c  -fPIC -DPIC -o .libs/umfuseext2_la-op_create.o
libtool: compile:  gcc -DHAVE_CONFIG_H -I. -I.. -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_create.lo -MD -MP -MF .deps/umfuseext2_la-op_create.Tpo -c op_create.c -o umfuseext2_la-op_create.o >/dev/null 2>&1
mv -f .deps/umfuseext2_la-op_create.Tpo .deps/umfuseext2_la-op_create.Plo
/bin/bash ../libtool  --tag=CC   --mode=compile gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE  -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_flush.lo -MD -MP -MF .deps/umfuseext2_la-op_flush.Tpo -c -o umfuseext2_la-op_flush.lo `test -f 'op_flush.c' || echo './'`op_flush.c
libtool: compile:  gcc -DHAVE_CONFIG_H -I. -I.. -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_flush.lo -MD -MP -MF .deps/umfuseext2_la-op_flush.Tpo -c op_flush.c  -fPIC -DPIC -o .libs/umfuseext2_la-op_flush.o
libtool: compile:  gcc -DHAVE_CONFIG_H -I. -I.. -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_flush.lo -MD -MP -MF .deps/umfuseext2_la-op_flush.Tpo -c op_flush.c -o umfuseext2_la-op_flush.o >/dev/null 2>&1
mv -f .deps/umfuseext2_la-op_flush.Tpo .deps/umfuseext2_la-op_flush.Plo
/bin/bash ../libtool  --tag=CC   --mode=compile gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE  -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_fsync.lo -MD -MP -MF .deps/umfuseext2_la-op_fsync.Tpo -c -o umfuseext2_la-op_fsync.lo `test -f 'op_fsync.c' || echo './'`op_fsync.c
libtool: compile:  gcc -DHAVE_CONFIG_H -I. -I.. -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_fsync.lo -MD -MP -MF .deps/umfuseext2_la-op_fsync.Tpo -c op_fsync.c  -fPIC -DPIC -o .libs/umfuseext2_la-op_fsync.o
libtool: compile:  gcc -DHAVE_CONFIG_H -I. -I.. -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_fsync.lo -MD -MP -MF .deps/umfuseext2_la-op_fsync.Tpo -c op_fsync.c -o umfuseext2_la-op_fsync.o >/dev/null 2>&1
mv -f .deps/umfuseext2_la-op_fsync.Tpo .deps/umfuseext2_la-op_fsync.Plo
/bin/bash ../libtool  --tag=CC   --mode=compile gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE  -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_mkdir.lo -MD -MP -MF .deps/umfuseext2_la-op_mkdir.Tpo -c -o umfuseext2_la-op_mkdir.lo `test -f 'op_mkdir.c' || echo './'`op_mkdir.c
libtool: compile:  gcc -DHAVE_CONFIG_H -I. -I.. -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_mkdir.lo -MD -MP -MF .deps/umfuseext2_la-op_mkdir.Tpo -c op_mkdir.c  -fPIC -DPIC -o .libs/umfuseext2_la-op_mkdir.o
libtool: compile:  gcc -DHAVE_CONFIG_H -I. -I.. -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_mkdir.lo -MD -MP -MF .deps/umfuseext2_la-op_mkdir.Tpo -c op_mkdir.c -o umfuseext2_la-op_mkdir.o >/dev/null 2>&1
mv -f .deps/umfuseext2_la-op_mkdir.Tpo .deps/umfuseext2_la-op_mkdir.Plo
/bin/bash ../libtool  --tag=CC   --mode=compile gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE  -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_rmdir.lo -MD -MP -MF .deps/umfuseext2_la-op_rmdir.Tpo -c -o umfuseext2_la-op_rmdir.lo `test -f 'op_rmdir.c' || echo './'`op_rmdir.c
libtool: compile:  gcc -DHAVE_CONFIG_H -I. -I.. -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_rmdir.lo -MD -MP -MF .deps/umfuseext2_la-op_rmdir.Tpo -c op_rmdir.c  -fPIC -DPIC -o .libs/umfuseext2_la-op_rmdir.o
libtool: compile:  gcc -DHAVE_CONFIG_H -I. -I.. -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_rmdir.lo -MD -MP -MF .deps/umfuseext2_la-op_rmdir.Tpo -c op_rmdir.c -o umfuseext2_la-op_rmdir.o >/dev/null 2>&1
mv -f .deps/umfuseext2_la-op_rmdir.Tpo .deps/umfuseext2_la-op_rmdir.Plo
/bin/bash ../libtool  --tag=CC   --mode=compile gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE  -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_unlink.lo -MD -MP -MF .deps/umfuseext2_la-op_unlink.Tpo -c -o umfuseext2_la-op_unlink.lo `test -f 'op_unlink.c' || echo './'`op_unlink.c
libtool: compile:  gcc ubuntu@ubuntu:~/Downloads/fuse-ext2-master$ ./configure
checking build system type... x86_64-pc-linux-gnu
checking host system type... x86_64-pc-linux-gnu
checking target system type... x86_64-pc-linux-gnu
checking for a BSD-compatible install... /usr/bin/install -c
checking whether build environment is sane... yes
checking for a thread-safe mkdir -p... /usr/bin/mkdir -p
checking for gawk... gawk
checking whether make sets $(MAKE)... yes
checking whether make supports nested variables... yes
checking for g++... g++
checking whether the C++ compiler works... yes
checking for C++ compiler default output file name... a.out
checking for suffix of executables... 
checking whether we are cross compiling... no
checking for suffix of object files... o
checking whether we are using the GNU C++ compiler... yes
checking whether g++ accepts -g... yes
checking whether make supports the include directive... yes (GNU style)
checking dependency style of g++... gcc3
checking for gawk... (cached) gawk
checking for gcc... gcc
checking whether we are using the GNU C compiler... yes
checking whether gcc accepts -g... yes
checking for gcc option to accept ISO C89... none needed
checking whether gcc understands -c and -o together... yes
checking dependency style of gcc... gcc3
checking for ar... ar
checking the archiver (ar) interface... ar
checking for gcc... gcc
checking whether we are using the GNU Objective C compiler... no
checking whether gcc accepts -g... no
checking dependency style of gcc... gcc3
checking how to print strings... printf
checking for a sed that does not truncate output... /usr/bin/sed
checking for grep that handles long lines and -e... /usr/bin/grep
checking for egrep... /usr/bin/grep -E
checking for fgrep... /usr/bin/grep -F
checking for ld used by gcc... /usr/bin/ld
checking if the linker (/usr/bin/ld) is GNU ld... yes
checking for BSD- or MS-compatible name lister (nm)... /usr/bin/nm -B
checking the name lister (/usr/bin/nm -B) interface... BSD nm
checking whether ln -s works... yes
checking the maximum length of command line arguments... 1572864
checking how to convert x86_64-pc-linux-gnu file names to x86_64-pc-linux-gnu format... func_convert_file_noop
checking how to convert x86_64-pc-linux-gnu file names to toolchain format... func_convert_file_noop
checking for /usr/bin/ld option to reload object files... -r
checking for objdump... objdump
checking how to recognize dependent libraries... pass_all
checking for dlltool... no
checking how to associate runtime and link libraries... printf %s\n
checking for archiver @FILE support... @
checking for strip... strip
checking for ranlib... ranlib
checking command to parse /usr/bin/nm -B output from gcc object... ok
checking for sysroot... no
checking for a working dd... /usr/bin/dd
checking how to truncate binary pipes... /usr/bin/dd bs=4096 count=1
checking for mt... mt
checking if mt is a manifest tool... no
checking how to run the C preprocessor... gcc -E
checking for ANSI C header files... yes
checking for sys/types.h... yes
checking for sys/stat.h... yes
checking for stdlib.h... yes
checking for string.h... yes
checking for memory.h... yes
checking for strings.h... yes
checking for inttypes.h... yes
checking for stdint.h... yes
checking for unistd.h... yes
checking for dlfcn.h... yes
checking for objdir... .libs
checking if gcc supports -fno-rtti -fno-exceptions... no
checking for gcc option to produce PIC... -fPIC -DPIC
checking if gcc PIC flag -fPIC -DPIC works... yes
checking if gcc static flag -static works... yes
checking if gcc supports -c -o file.o... yes
checking if gcc supports -c -o file.o... (cached) yes
checking whether the gcc linker (/usr/bin/ld -m elf_x86_64) supports shared libraries... yes
checking whether -lc should be explicitly linked in... no
checking dynamic linker characteristics... GNU/Linux ld.so
checking how to hardcode library paths into programs... immediate
checking whether stripping libraries is possible... yes
checking if libtool supports shared libraries... yes
checking whether to build shared libraries... yes
checking whether to build static libraries... yes
checking how to run the C++ preprocessor... g++ -E
checking for ld used by g++... /usr/bin/ld -m elf_x86_64
checking if the linker (/usr/bin/ld -m elf_x86_64) is GNU ld... yes
checking whether the g++ linker (/usr/bin/ld -m elf_x86_64) supports shared libraries... yes
checking for g++ option to produce PIC... -fPIC -DPIC
checking if g++ PIC flag -fPIC -DPIC works... yes
checking if g++ static flag -static works... yes
checking if g++ supports -c -o file.o... yes
checking if g++ supports -c -o file.o... (cached) yes
checking whether the g++ linker (/usr/bin/ld -m elf_x86_64) supports shared libraries... yes
checking dynamic linker characteristics... (cached) GNU/Linux ld.so
checking how to hardcode library paths into programs... immediate
checking for chmod... /usr/bin/chmod
checking for size_t... yes
checking for off_t... yes
checking for dirent.h that defines DIR... yes
checking for library containing opendir... none required
checking for ANSI C header files... (cached) yes
checking whether sys/types.h defines makedev... no
checking sys/mkdev.h usability... no
checking sys/mkdev.h presence... no
checking for sys/mkdev.h... no
checking sys/sysmacros.h usability... yes
checking sys/sysmacros.h presence... yes
checking for sys/sysmacros.h... yes
checking fcntl.h usability... yes
checking fcntl.h presence... yes
checking for fcntl.h... yes
checking malloc.h usability... yes
checking malloc.h presence... yes
checking for malloc.h... yes
checking mntent.h usability... yes
checking mntent.h presence... yes
checking for mntent.h... yes
checking netinet/in.h usability... yes
checking netinet/in.h presence... yes
checking for netinet/in.h... yes
checking paths.h usability... yes
checking paths.h presence... yes
checking for paths.h... yes
checking stddef.h usability... yes
checking stddef.h presence... yes
checking for stddef.h... yes
checking for stdlib.h... (cached) yes
checking for string.h... (cached) yes
checking linux/fd.h usability... yes
checking linux/fd.h presence... yes
checking for linux/fd.h... yes
checking sys/file.h usability... yes
checking sys/file.h presence... yes
checking for sys/file.h... yes
checking sys/ioctl.h usability... yes
checking sys/ioctl.h presence... yes
checking for sys/ioctl.h... yes
checking sys/mount.h usability... yes
checking sys/mount.h presence... yes
checking for sys/mount.h... yes
checking sys/param.h usability... yes
checking sys/param.h presence... yes
checking for sys/param.h... yes
checking sys/statvfs.h usability... yes
checking sys/statvfs.h presence... yes
checking for sys/statvfs.h... yes
checking sys/time.h usability... yes
checking sys/time.h presence... yes
checking for sys/time.h... yes
checking for sys/types.h... (cached) yes
checking for sys/stat.h... (cached) yes
checking for sys/mkdev.h... (cached) no
checking for sys/ioctl.h... (cached) yes
checking sys/syscall.h usability... yes
checking sys/syscall.h presence... yes
checking for sys/syscall.h... yes
checking sys/resource.h usability... yes
checking sys/resource.h presence... yes
checking for sys/resource.h... yes
checking sys/mman.h usability... yes
checking sys/mman.h presence... yes
checking for sys/mman.h... yes
checking sys/prctl.h usability... yes
checking sys/prctl.h presence... yes
checking for sys/prctl.h... yes
checking sys/disklabel.h usability... no
checking sys/disklabel.h presence... no
checking for sys/disklabel.h... no
checking sys/queue.h usability... yes
checking sys/queue.h presence... yes
checking for sys/queue.h... yes
checking sys/socket.h usability... yes
checking sys/socket.h presence... yes
checking for sys/socket.h... yes
checking sys/un.h usability... yes
checking sys/un.h presence... yes
checking for sys/un.h... yes
checking sys/sockio.h usability... no
checking sys/sockio.h presence... no
checking for sys/sockio.h... no
checking net/if.h usability... yes
checking net/if.h presence... yes
checking for net/if.h... yes
checking for netinet/in.h... (cached) yes
checking net/if_dl.h usability... no
checking net/if_dl.h presence... no
checking for net/if_dl.h... no
checking errno.h usability... yes
checking errno.h presence... yes
checking for errno.h... yes
checking for unistd.h... (cached) yes
checking utime.h usability... yes
checking utime.h presence... yes
checking for utime.h... yes
checking getopt.h usability... yes
checking getopt.h presence... yes
checking for getopt.h... yes
checking for inttypes.h... (cached) yes
checking for sys/disk.h... no
checking for sys/mount.h... (cached) yes
checking for an ANSI C-conforming const... yes
checking for inline... inline
checking for mode_t... yes
checking for off_t... (cached) yes
checking for size_t... (cached) yes
checking for ssize_t... yes
checking for struct stat.st_blksize... yes
checking for struct stat.st_blocks... yes
checking for struct stat.st_rdev... yes
checking whether time.h and sys/time.h may both be included... yes
checking whether llseek is declared... no
checking whether lseek64 is declared... yes
checking for ssize_t... (cached) yes
checking for vprintf... yes
checking for _doprnt... no
checking for uid_t in sys/types.h... yes
checking for unistd.h... (cached) yes
checking for working chown... yes
checking whether closedir returns void... no
checking for library containing getmntent... none required
checking whether gcc needs -traditional... no
checking for stdlib.h... (cached) yes
checking for GNU libc compatible malloc... yes
checking for working memcmp... yes
checking for stdlib.h... (cached) yes
checking for unistd.h... (cached) yes
checking for sys/param.h... (cached) yes
checking for utime.h... (cached) yes
checking for getpagesize... yes
checking for working mmap... yes
checking for stdlib.h... (cached) yes
checking for GNU libc compatible realloc... yes
checking sys/select.h usability... yes
checking sys/select.h presence... yes
checking for sys/select.h... yes
checking for sys/socket.h... (cached) yes
checking types of arguments for select... int,fd_set *,struct timevize: Consider adding '-I m4' to ACLOCAL_AMFLAGS in Makefile.am.
autoreconf: running: /usr/bin/autoconf --force
autoreconf: running: /usr/bin/autoheader --force
autoreconf: running: automake --add-missing --copy --force-missing
configure.ac:10: installing './compile'
configure.ac:4: installing './missing'
fuse-ext2/Makefile.am: installing './depcomp'
autoreconf: Leaving directory `.'
Removing autom4te.cache
ubuntu@ubuntu:~/Downloads/fuse-ext2-master$ ./configure
checking build system type... x86_64-pc-linux-gnu
checking host system type... x86_64-pc-linux-gnu
checking targeal *
checking whether lstat correctly handles trailing slash... yes
checking whether stat accepts an empty string... no
checking whether utime accepts a null argument... yes
checking for ftruncate... yes
checking for getmntent... (cached) yes
checking for getmntinfo... noize: Consider adding '-I m4' to ACLOCAL_AMFLAGS in Makefile.am.
autoreconf: running: /usr/bin/autoconf --force
autoreconf: running: /usr/bin/autoheader --force
autoreconf: running: automake --add-missing --copy --force-missing
configure.ac:10: installing './compile'
configure.ac:4: installing './missing'
fuse-ext2/Makefile.am: installing './depcomp'
autoreconf: Leaving directory `.'
Removing autom4te.cache
ubuntu@ubuntu:~/Downloads/fuse-ext2-master$ ./configure
checking build system type... x86_64-pc-linux-gnu
checking host system type... x86_64-pc-linux-gnu
checking targe
checking for getpagesize... (cached) yes
checking for hasmntopt... yes
checking for memmove... yes
checking for memset... yes
checking for munmap... yes
checking for random... yes
checking for select... yes
checking for srand... yes
checking for srandom... yes
checking for strcasecmp... yes
checking for strchr... yes
checking for strdup... yes
checking for strerror... yes
checking for strrchr... yes
checking for strtol... yes
checking for strtoul... yes
checking for strtoull... yes
checking for uname... yes
checking for utime... yes
checking for llseek... no
checking for lseek64... yes
checking for library containing sem_post... -lpthread
checking for library containing fuse_main... -lfuse
checking for library containing com_err... -lcom_err
checking for library containing ext2fs_open... -lext2fs
checking if FUSE on this system is too new for us... yes
Disabling debug support by default
checking that generated files are newer than configure... done
configure: creating ./config.status
config.status: creating fuse-ext2.pc
config.status: creating Makefile
config.status: creating fuse-ext2/Makefile
config.status: creating tools/Makefile
config.status: creating tools/macosx/Makefile
config.status: creating config.h
config.status: executing depfiles commands
config.status: executing libtool commands


ubuntu@ubuntu:~/Downloads/fuse-ext2-master$ make
make  all-recursive
make[1]: Entering directory '/home/ubuntu/Downloads/fuse-ext2-master'
Making all in fuse-ext2
make[2]: Entering directory '/home/ubuntu/Downloads/fuse-ext2-master/fuse-ext2'
gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -I/usr/local/include  -g -O2 -MT fuse_ext2-fuse-ext2.o -MD -MP -MF .deps/fuse_ext2-fuse-ext2.Tpo -c -o fuse_ext2-fuse-ext2.o `test -f 'fuse-ext2.c' || echo './'`fuse-ext2.c
mv -f .deps/fuse_ext2-fuse-ext2.Tpo .deps/fuse_ext2-fuse-ext2.Po
gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -I/usr/local/include  -g -O2 -MT fuse_ext2-do_probe.o -MD -MP -MF .deps/fuse_ext2-do_probe.Tpo -c -o fuse_ext2-do_probe.o `test -f 'do_probe.c' || echo './'`do_probe.c
mv -f .deps/fuse_ext2-do_probe.Tpo .deps/fuse_ext2-do_probe.Po
gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -I/usr/local/include  -g -O2 -MT fuse_ext2-do_check.o -MD -MP -MF .deps/fuse_ext2-do_check.Tpo -c -o fuse_ext2-do_check.o `test -f 'do_check.c' || echo './'`do_check.c
mv -f .deps/fuse_ext2-do_check.Tpo .deps/fuse_ext2-do_check.Po
gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -I/usr/local/include  -g -O2 -MT fuse_ext2-do_fillstatbuf.o -MD -MP -MF .deps/fuse_ext2-do_fillstatbuf.Tpo -c -o fuse_ext2-do_fillstatbuf.o `test -f 'do_fillstatbuf.c' || echo './'`do_fillstatbuf.c
mv -f .deps/fuse_ext2-do_fillstatbuf.Tpo .deps/fuse_ext2-do_fillstatbuf.Po
gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -I/usr/local/include  -g -O2 -MT fuse_ext2-do_readinode.o -MD -MP -MF .deps/fuse_ext2-do_readinode.Tpo -c -o fuse_ext2-do_readinode.o `test -f 'do_readinode.c' || echo './'`do_readinode.c
mv -f .deps/fuse_ext2-do_readinode.Tpo .deps/fuse_ext2-do_readinode.Po
gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -I/usr/local/include  -g -O2 -MT fuse_ext2-do_writeinode.o -MD -MP -MF .deps/fuse_ext2-do_writeinode.Tpo -c -o fuse_ext2-do_writeinode.o `test -f 'do_writeinode.c' || echo './'`do_writeinode.c
mv -f .deps/fuse_ext2-do_writeinode.Tpo .deps/fuse_ext2-do_writeinode.Po
gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -I/usr/local/include  -g -O2 -MT fuse_ext2-do_killfilebyinode.o -MD -MP -MF .deps/fuse_ext2-do_killfilebyinode.Tpo -c -o fuse_ext2-do_killfilebyinode.o `test -f 'do_killfilebyinode.c' || echo './'`do_killfilebyinode.c
mv -f .deps/fuse_ext2-do_killfilebyinode.Tpo .deps/fuse_ext2-do_killfilebyinode.Po
gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -I/usr/local/include  -g -O2 -MT fuse_ext2-op_init.o -MD -MP -MF .deps/fuse_ext2-op_init.Tpo -c -o fuse_ext2-op_init.o `test -f 'op_init.c' || echo './'`op_init.c
mv -f .deps/fuse_ext2-op_init.Tpo .deps/fuse_ext2-op_init.Po
gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -I/usr/local/include  -g -O2 -MT fuse_ext2-op_destroy.o -MD -MP -MF .deps/fuse_ext2-op_destroy.Tpo -c -o fuse_ext2-op_destroy.o `test -f 'op_destroy.c' || echo './'`op_destroy.c
mv -f .deps/fuse_ext2-op_destroy.Tpo .deps/fuse_ext2-op_destroy.Po
gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -I/usr/local/include  -g -O2 -MT fuse_ext2-op_access.o -MD -MP -MF .deps/fuse_ext2-op_access.Tpo -c -o fuse_ext2-op_access.o `test -f 'op_access.c' || echo './'`op_access.c
mv -f .deps/fuse_ext2-op_access.Tpo .deps/fuse_ext2-op_access.Po
gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -I/usr/local/include  -g -O2 -MT fuse_ext2-op_fgetattr.o -MD -MP -MF .deps/fuse_ext2-op_fgetattr.Tpo -c -o fuse_ext2-op_fgetattr.o `test -f 'op_fgetattr.c' || echo './'`op_fgetattr.c
mv -f .deps/fuse_ext2-op_fgetattr.Tpo .deps/fuse_ext2-op_fgetattr.Po
gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -I/usr/local/include  -g -O2 -MT fuse_ext2-op_getattr.o -MD -MP -MF .deps/fuse_ext2-op_getattr.Tpo -c -o fuse_ext2-op_getattr.o `test -f 'op_getattr.c' || echo './'`op_getattr.c
mv -f .deps/fuse_ext2-op_getattr.Tpo .deps/fuse_ext2-op_getattr.Po
gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -I/usr/local/include  -g -O2 -MT fuse_ext2-op_getxattr.o -MD -MP -MF .deps/fuse_ext2-op_getxattr.Tpo -c -o fuse_ext2-op_getxattr.o `test -f 'op_getxattr.c' || echo './'`op_getxattr.c
mv -f .deps/fuse_ext2-op_getxattr.Tpo .deps/fuse_ext2-op_getxattr.Po
gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -I/usr/local/include  -g -O2 -MT fuse_ext2-op_open.o -MD -MP -MF .deps/fuse_ext2-op_open.Tpo -c -o fuse_ext2-op_open.o `test -f 'op_open.c' || echo './'`op_open.c
mv -f .deps/fuse_ext2-op_open.Tpo .deps/fuse_ext2-op_open.Po
gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -I/usr/local/include  -g -O2 -MT fuse_ext2-op_read.o -MD -MP -MF .deps/fuse_ext2-op_read.Tpo -c -o fuse_ext2-op_read.o `test -f 'op_read.c' || echo './'`op_read.c
mv -f .deps/fuse_ext2-op_read.Tpo .deps/fuse_ext2-op_read.Po
gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -I/usr/local/include  -g -O2 -MT fuse_ext2-op_readdir.o -MD -MP -MF .deps/fuse_ext2-op_readdir.Tpo -c -o fuse_ext2-op_readdir.o `test -f 'op_readdir.c' || echo './'`op_readdir.c
mv -f .deps/fuse_ext2-op_readdir.Tpo .deps/fuse_ext2-op_readdir.Po
gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -I/usr/local/include  -g -O2 -MT fuse_ext2-op_readlink.o -MD -MP -MF .deps/fuse_ext2-op_readlink.Tpo -c -o fuse_ext2-op_readlink.o `test -f 'op_readlink.c' || echo './'`op_readlink.c
mv -f .deps/fuse_ext2-op_readlink.Tpo .deps/fuse_ext2-op_readlink.Po
gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -I/usr/local/include  -g -O2 -MT fuse_ext2-op_release.o -MD -MP -MF .deps/fuse_ext2-op_release.Tpo -c -o fuse_ext2-op_release.o `test -f 'op_release.c' || echo './'`op_release.c
mv -f .deps/fuse_ext2-op_release.Tpo .deps/fuse_ext2-op_release.Po
gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -I/usr/local/include  -g -O2 -MT fuse_ext2-op_statfs.o -MD -MP -MF .deps/fuse_ext2-op_statfs.Tpo -c -o fuse_ext2-op_statfs.o `test -f 'op_statfs.c' || echo './'`op_statfs.c
mv -f .deps/fuse_ext2-op_statfs.Tpo .deps/fuse_ext2-op_statfs.Po
gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -I/usr/local/include  -g -O2 -MT fuse_ext2-op_chown.o -MD -MP -MF .deps/fuse_ext2-op_chown.Tpo -c -o fuse_ext2-op_chown.o `test -f 'op_chown.c' || echo './'`op_chown.c
mv -f .deps/fuse_ext2-op_chown.Tpo .deps/fuse_ext2-op_chown.Po
gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -I/usr/local/include  -g -O2 -MT fuse_ext2-op_chmod.o -MD -MP -MF .deps/fuse_ext2-op_chmod.Tpo -c -o fuse_ext2-op_chmod.o `test -f 'op_chmod.c' || echo './'`op_chmod.c
mv -f .deps/fuse_ext2-op_chmod.Tpo .deps/fuse_ext2-op_chmod.Po
gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -I/usr/local/include  -g -O2 -MT fuse_ext2-op_create.o -MD -MP -MF .deps/fuse_ext2-op_create.Tpo -c -o fuse_ext2-op_create.o `test -f 'op_create.c' || echo './'`op_create.c
mv -f .deps/fuse_ext2-op_create.Tpo .deps/fuse_ext2-op_create.Po
gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -I/usr/local/include  -g -O2 -MT fuse_ext2-op_flush.o -MD -MP -MF .deps/fuse_ext2-op_flush.Tpo -c -o fuse_ext2-op_flush.o `test -f 'op_flush.c' || echo './'`op_flush.c
mv -f .deps/fuse_ext2-op_flush.Tpo .deps/fuse_ext2-op_flush.Po
gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -I/usr/local/include  -g -O2 -MT fuse_ext2-op_fsync.o -MD -MP -MF .deps/fuse_ext2-op_fsync.Tpo -c -o fuse_ext2-op_fsync.o `test -f 'op_fsync.c' || echo './'`op_fsync.c
mv -f .deps/fuse_ext2-op_fsync.Tpo .deps/fuse_ext2-op_fsync.Po
gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -I/usr/local/include  -g -O2 -MT fuse_ext2-op_mkdir.o -MD -MP -MF .deps/fuse_ext2-op_mkdir.Tpo -c -o fuse_ext2-op_mkdir.o `test -f 'op_mkdir.c' || echo './'`op_mkdir.c
mv -f .deps/fuse_ext2-op_mkdir.Tpo .deps/fuse_ext2-op_mkdir.Po
gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -I/usr/local/include  -g -O2 -MT fuse_ext2-op_rmdir.o -MD -MP -MF .deps/fuse_ext2-op_rmdir.Tpo -c -o fuse_ext2-op_rmdir.o `test -f 'op_rmdir.c' || echo './'`op_rmdir.c
mv -f .deps/fuse_ext2-op_rmdir.Tpo .deps/fuse_ext2-op_rmdir.Po
gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -I/usr/local/include  -g -O2 -MT fuse_ext2-op_unlink.o -MD -MP -MF .deps/fuse_ext2-op_unlink.Tpo -c -o fuse_ext2-op_unlink.o `test -f 'op_unlink.c' || echo './'`op_unlink.c
mv -f .deps/fuse_ext2-op_unlink.Tpo .deps/fuse_ext2-op_unlink.Po
gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -I/usr/local/include  -g -O2 -MT fuse_ext2-op_utimens.o -MD -MP -MF .deps/fuse_ext2-op_utimens.Tpo -c -o fuse_ext2-op_utimens.o `test -f 'op_utimens.c' || echo './'`op_utimens.c
mv -f .deps/fuse_ext2-op_utimens.Tpo .deps/fuse_ext2-op_utimens.Po
gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -I/usr/local/include  -g -O2 -MT fuse_ext2-op_write.o -MD -MP -MF .deps/fuse_ext2-op_write.Tpo -c -o fuse_ext2-op_write.o `test -f 'op_write.c' || echo './'`op_write.c
mv -f .deps/fuse_ext2-op_write.Tpo .deps/fuse_ext2-op_write.Po
gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -I/usr/local/include  -g -O2 -MT fuse_ext2-op_mknod.o -MD -MP -MF .deps/fuse_ext2-op_mknod.Tpo -c -o fuse_ext2-op_mknod.o `test -f 'op_mknod.c' || echo './'`op_mknod.c
mv -f .deps/fuse_ext2-op_mknod.Tpo .deps/fuse_ext2-op_mknod.Po
gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -I/usr/local/include  -g -O2 -MT fuse_ext2-op_symlink.o -MD -MP -MF .deps/fuse_ext2-op_symlink.Tpo -c -o fuse_ext2-op_symlink.o `test -f 'op_symlink.c' || echo './'`op_symlink.c
mv -f .deps/fuse_ext2-op_symlink.Tpo .deps/fuse_ext2-op_symlink.Po
gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -I/usr/local/include  -g -O2 -MT fuse_ext2-op_truncate.o -MD -MP -MF .deps/fuse_ext2-op_truncate.Tpo -c -o fuse_ext2-op_truncate.o `test -f 'op_truncate.c' || echo './'`op_truncate.c
mv -f .deps/fuse_ext2-op_truncate.Tpo .deps/fuse_ext2-op_truncate.Po
gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -I/usr/local/include  -g -O2 -MT fuse_ext2-op_link.o -MD -MP -MF .deps/fuse_ext2-op_link.Tpo -c -o fuse_ext2-op_link.o `test -f 'op_link.c' || echo './'`op_link.c
mv -f .deps/fuse_ext2-op_link.Tpo .deps/fuse_ext2-op_link.Po
gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -I/usr/local/include  -g -O2 -MT fuse_ext2-op_rename.o -MD -MP -MF .deps/fuse_ext2-op_rename.Tpo -c -o fuse_ext2-op_rename.o `test -f 'op_rename.c' || echo './'`op_rename.c
mv -f .deps/fuse_ext2-op_rename.Tpo .deps/fuse_ext2-op_rename.Po
/bin/bash ../libtool  --tag=CC   --mode=link gcc -Wall -DHAVE_CONFIG_H -I/usr/local/include  -g -O2   -o fuse-ext2 fuse_ext2-fuse-ext2.o fuse_ext2-do_probe.o fuse_ext2-do_check.o fuse_ext2-do_fillstatbuf.o fuse_ext2-do_readinode.o fuse_ext2-do_writeinode.o fuse_ext2-do_killfilebyinode.o fuse_ext2-op_init.o fuse_ext2-op_destroy.o fuse_ext2-op_access.o fuse_ext2-op_fgetattr.o fuse_ext2-op_getattr.o fuse_ext2-op_getxattr.o fuse_ext2-op_open.o fuse_ext2-op_read.o fuse_ext2-op_readdir.o fuse_ext2-op_readlink.o fuse_ext2-op_release.o fuse_ext2-op_statfs.o fuse_ext2-op_chown.o fuse_ext2-op_chmod.o fuse_ext2-op_create.o fuse_ext2-op_flush.o fuse_ext2-op_fsync.o fuse_ext2-op_mkdir.o fuse_ext2-op_rmdir.o fuse_ext2-op_unlink.o fuse_ext2-op_utimens.o fuse_ext2-op_write.o fuse_ext2-op_mknod.o fuse_ext2-op_symlink.o fuse_ext2-op_truncate.o fuse_ext2-op_link.o fuse_ext2-op_rename.o  -lext2fs -lcom_err -lfuse -lpthread 
libtool: link: gcc -Wall -DHAVE_CONFIG_H -I/usr/local/include -g -O2 -o fuse-ext2 fuse_ext2-fuse-ext2.o fuse_ext2-do_probe.o fuse_ext2-do_check.o fuse_ext2-do_fillstatbuf.o fuse_ext2-do_readinode.o fuse_ext2-do_writeinode.o fuse_ext2-do_killfilebyinode.o fuse_ext2-op_init.o fuse_ext2-op_destroy.o fuse_ext2-op_access.o fuse_ext2-op_fgetattr.o fuse_ext2-op_getattr.o fuse_ext2-op_getxattr.o fuse_ext2-op_open.o fuse_ext2-op_read.o fuse_ext2-op_readdir.o fuse_ext2-op_readlink.o fuse_ext2-op_release.o fuse_ext2-op_statfs.o fuse_ext2-op_chown.o fuse_ext2-op_chmod.o fuse_ext2-op_create.o fuse_ext2-op_flush.o fuse_ext2-op_fsync.o fuse_ext2-op_mkdir.o fuse_ext2-op_rmdir.o fuse_ext2-op_unlink.o fuse_ext2-op_utimens.o fuse_ext2-op_write.o fuse_ext2-op_mknod.o fuse_ext2-op_symlink.o fuse_ext2-op_truncate.o fuse_ext2-op_link.o fuse_ext2-op_rename.o  -lext2fs -lcom_err -lfuse -lpthread
gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -I/usr/local/include  -g -O2 -MT fuse_ext2_probe-fuse-ext2.probe.o -MD -MP -MF .deps/fuse_ext2_probe-fuse-ext2.probe.Tpo -c -o fuse_ext2_probe-fuse-ext2.probe.o `test -f 'fuse-ext2.probe.c' || echo './'`fuse-ext2.probe.c
mv -f .deps/fuse_ext2_probe-fuse-ext2.probe.Tpo .deps/fuse_ext2_probe-fuse-ext2.probe.Po
gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -I/usr/local/include  -g -O2 -MT fuse_ext2_probe-do_probe.o -MD -MP -MF .deps/fuse_ext2_probe-do_probe.Tpo -c -o fuse_ext2_probe-do_probe.o `test -f 'do_probe.c' || echo './'`do_probe.c
mv -f .deps/fuse_ext2_probe-do_probe.Tpo .deps/fuse_ext2_probe-do_probe.Po
/bin/bash ../libtool  --tag=CC   --mode=link gcc -Wall -DHAVE_CONFIG_H -I/usr/local/include  -g -O2   -o fuse-ext2.probe fuse_ext2_probe-fuse-ext2.probe.o fuse_ext2_probe-do_probe.o  -lext2fs -lcom_err -lfuse -lpthread 
libtool: link: gcc -Wall -DHAVE_CONFIG_H -I/usr/local/include -g -O2 -o fuse-ext2.probe fuse_ext2_probe-fuse-ext2.probe.o fuse_ext2_probe-do_probe.o  -lext2fs -lcom_err -lfuse -lpthread
/bin/bash ../libtool  --tag=CC   --mode=compile gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE  -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-fuse-ext2.lo -MD -MP -MF .deps/umfuseext2_la-fuse-ext2.Tpo -c -o umfuseext2_la-fuse-ext2.lo `test -f 'fuse-ext2.c' || echo './'`fuse-ext2.c
libtool: compile:  gcc -DHAVE_CONFIG_H -I. -I.. -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-fuse-ext2.lo -MD -MP -MF .deps/umfuseext2_la-fuse-ext2.Tpo -c fuse-ext2.c  -fPIC -DPIC -o .libs/umfuseext2_la-fuse-ext2.o
libtool: compile:  gcc -DHAVE_CONFIG_H -I. -I.. -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-fuse-ext2.lo -MD -MP -MF .deps/umfuseext2_la-fuse-ext2.Tpo -c fuse-ext2.c -o umfuseext2_la-fuse-ext2.o >/dev/null 2>&1
mv -f .deps/umfuseext2_la-fuse-ext2.Tpo .deps/umfuseext2_la-fuse-ext2.Plo
/bin/bash ../libtool  --tag=CC   --mode=compile gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE  -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-do_probe.lo -MD -MP -MF .deps/umfuseext2_la-do_probe.Tpo -c -o umfuseext2_la-do_probe.lo `test -f 'do_probe.c' || echo './'`do_probe.c
libtool: compile:  gcc -DHAVE_CONFIG_H -I. -I.. -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-do_probe.lo -MD -MP -MF .deps/umfuseext2_la-do_probe.Tpo -c do_probe.c  -fPIC -DPIC -o .libs/umfuseext2_la-do_probe.o
libtool: compile:  gcc -DHAVE_CONFIG_H -I. -I.. -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-do_probe.lo -MD -MP -MF .deps/umfuseext2_la-do_probe.Tpo -c do_probe.c -o umfuseext2_la-do_probe.o >/dev/null 2>&1
mv -f .deps/umfuseext2_la-do_probe.Tpo .deps/umfuseext2_la-do_probe.Plo
/bin/bash ../libtool  --tag=CC   --mode=compile gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE  -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-do_check.lo -MD -MP -MF .deps/umfuseext2_la-do_check.Tpo -c -o umfuseext2_la-do_check.lo `test -f 'do_check.c' || echo './'`do_check.c
libtool: compile:  gcc -DHAVE_CONFIG_H -I. -I.. -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-do_check.lo -MD -MP -MF .deps/umfuseext2_la-do_check.Tpo -c do_check.c  -fPIC -DPIC -o .libs/umfuseext2_la-do_check.o
libtool: compile:  gcc -DHAVE_CONFIG_H -I. -I.. -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-do_check.lo -MD -MP -MF .deps/umfuseext2_la-do_check.Tpo -c do_check.c -o umfuseext2_la-do_check.o >/dev/null 2>&1
mv -f .deps/umfuseext2_la-do_check.Tpo .deps/umfuseext2_la-do_check.Plo
/bin/bash ../libtool  --tag=CC   --mode=compile gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE  -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-do_fillstatbuf.lo -MD -MP -MF .deps/umfuseext2_la-do_fillstatbuf.Tpo -c -o umfuseext2_la-do_fillstatbuf.lo `test -f 'do_fillstatbuf.c' || echo './'`do_fillstatbuf.c
libtool: compile:  gcc -DHAVE_CONFIG_H -I. -I.. -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-do_fillstatbuf.lo -MD -MP -MF .deps/umfuseext2_la-do_fillstatbuf.Tpo -c do_fillstatbuf.c  -fPIC -DPIC -o .libs/umfuseext2_la-do_fillstatbuf.o
libtool: compile:  gcc -DHAVE_CONFIG_H -I. -I.. -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-do_fillstatbuf.lo -MD -MP -MF .deps/umfuseext2_la-do_fillstatbuf.Tpo -c do_fillstatbuf.c -o umfuseext2_la-do_fillstatbuf.o >/dev/null 2>&1
mv -f .deps/umfuseext2_la-do_fillstatbuf.Tpo .deps/umfuseext2_la-do_fillstatbuf.Plo
/bin/bash ../libtool  --tag=CC   --mode=compile gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE  -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-do_readinode.lo -MD -MP -MF .deps/umfuseext2_la-do_readinode.Tpo -c -o umfuseext2_la-do_readinode.lo `test -f 'do_readinode.c' || echo './'`do_readinode.c
libtool: compile:  gcc -DHAVE_CONFIG_H -I. -I.. -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-do_readinode.lo -MD -MP -MF .deps/umfuseext2_la-do_readinode.Tpo -c do_readinode.c  -fPIC -DPIC -o .libs/umfuseext2_la-do_readinode.o
libtool: compile:  gcc -DHAVE_CONFIG_H -I. -I.. -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-do_readinode.lo -MD -MP -MF .deps/umfuseext2_la-do_readinode.Tpo -c do_readinode.c -o umfuseext2_la-do_readinode.o >/dev/null 2>&1
mv -f .deps/umfuseext2_la-do_readinode.Tpo .deps/umfuseext2_la-do_readinode.Plo
/bin/bash ../libtool  --tag=CC   --mode=compile gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE  -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-do_writeinode.lo -MD -MP -MF .deps/umfuseext2_la-do_writeinode.Tpo -c -o umfuseext2_la-do_writeinode.lo `test -f 'do_writeinode.c' || echo './'`do_writeinode.c
libtool: compile:  gcc -DHAVE_CONFIG_H -I. -I.. -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-do_writeinode.lo -MD -MP -MF .deps/umfuseext2_la-do_writeinode.Tpo -c do_writeinode.c  -fPIC -DPIC -o .libs/umfuseext2_la-do_writeinode.o
libtool: compile:  gcc -DHAVE_CONFIG_H -I. -I.. -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-do_writeinode.lo -MD -MP -MF .deps/umfuseext2_la-do_writeinode.Tpo -c do_writeinode.c -o umfuseext2_la-do_writeinode.o >/dev/null 2>&1
mv -f .deps/umfuseext2_la-do_writeinode.Tpo .deps/umfuseext2_la-do_writeinode.Plo
/bin/bash ../libtool  --tag=CC   --mode=compile gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE  -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-do_killfilebyinode.lo -MD -MP -MF .deps/umfuseext2_la-do_killfilebyinode.Tpo -c -o umfuseext2_la-do_killfilebyinode.lo `test -f 'do_killfilebyinode.c' || echo './'`do_killfilebyinode.c
libtool: compile:  gcc -DHAVE_CONFIG_H -I. -I.. -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-do_killfilebyinode.lo -MD -MP -MF .deps/umfuseext2_la-do_killfilebyinode.Tpo -c do_killfilebyinode.c  -fPIC -DPIC -o .libs/umfuseext2_la-do_killfilebyinode.o
libtool: compile:  gcc -DHAVE_CONFIG_H -I. -I.. -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-do_killfilebyinode.lo -MD -MP -MF .deps/umfuseext2_la-do_killfilebyinode.Tpo -c do_killfilebyinode.c -o umfuseext2_la-do_killfilebyinode.o >/dev/null 2>&1
mv -f .deps/umfuseext2_la-do_killfilebyinode.Tpo .deps/umfuseext2_la-do_killfilebyinode.Plo
/bin/bash ../libtool  --tag=CC   --mode=compile gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE  -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_init.lo -MD -MP -MF .deps/umfuseext2_la-op_init.Tpo -c -o umfuseext2_la-op_init.lo `test -f 'op_init.c' || echo './'`op_init.c
libtool: compile:  gcc -DHAVE_CONFIG_H -I. -I.. -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_init.lo -MD -MP -MF .deps/umfuseext2_la-op_init.Tpo -c op_init.c  -fPIC -DPIC -o .libs/umfuseext2_la-op_init.o
libtool: compile:  gcc -DHAVE_CONFIG_H -I. -I.. -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_init.lo -MD -MP -MF .deps/umfuseext2_la-op_init.Tpo -c op_init.c -o umfuseext2_la-op_init.o >/dev/null 2>&1
mv -f .deps/umfuseext2_la-op_init.Tpo .deps/umfuseext2_la-op_init.Plo
/bin/bash ../libtool  --tag=CC   --mode=compile gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE  -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_destroy.lo -MD -MP -MF .deps/umfuseext2_la-op_destroy.Tpo -c -o umfuseext2_la-op_destroy.lo `test -f 'op_destroy.c' || echo './'`op_destroy.c
libtool: compile:  gcc -DHAVE_CONFIG_H -I. -I.. -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_destroy.lo -MD -MP -MF .deps/umfuseext2_la-op_destroy.Tpo -c op_destroy.c  -fPIC -DPIC -o .libs/umfuseext2_la-op_destroy.o
libtool: compile:  gcc -DHAVE_CONFIG_H -I. -I.. -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_destroy.lo -MD -MP -MF .deps/umfuseext2_la-op_destroy.Tpo -c op_destroy.c -o umfuseext2_la-op_destroy.o >/dev/null 2>&1
mv -f .deps/umfuseext2_la-op_destroy.Tpo .deps/umfuseext2_la-op_destroy.Plo
/bin/bash ../libtool  --tag=CC   --mode=compile gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE  -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_access.lo -MD -MP -MF .deps/umfuseext2_la-op_access.Tpo -c -o umfuseext2_la-op_access.lo `test -f 'op_access.c' || echo './'`op_access.c
libtool: compile:  gcc -DHAVE_CONFIG_H -I. -I.. -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_access.lo -MD -MP -MF .deps/umfuseext2_la-op_access.Tpo -c op_access.c  -fPIC -DPIC -o .libs/umfuseext2_la-op_access.o
libtool: compile:  gcc -DHAVE_CONFIG_H -I. -I.. -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_access.lo -MD -MP -MF .deps/umfuseext2_la-op_access.Tpo -c op_access.c -o umfuseext2_la-op_access.o >/dev/null 2>&1
mv -f .deps/umfuseext2_la-op_access.Tpo .deps/umfuseext2_la-op_access.Plo
/bin/bash ../libtool  --tag=CC   --mode=compile gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE  -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_fgetattr.lo -MD -MP -MF .deps/umfuseext2_la-op_fgetattr.Tpo -c -o umfuseext2_la-op_fgetattr.lo `test -f 'op_fgetattr.c' || echo './'`op_fgetattr.c
libtool: compile:  gcc -DHAVE_CONFIG_H -I. -I.. -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_fgetattr.lo -MD -MP -MF .deps/umfuseext2_la-op_fgetattr.Tpo -c op_fgetattr.c  -fPIC -DPIC -o .libs/umfuseext2_la-op_fgetattr.o
libtool: compile:  gcc -DHAVE_CONFIG_H -I. -I.. -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_fgetattr.lo -MD -MP -MF .deps/umfuseext2_la-op_fgetattr.Tpo -c op_fgetattr.c -o umfuseext2_la-op_fgetattr.o >/dev/null 2>&1
mv -f .deps/umfuseext2_la-op_fgetattr.Tpo .deps/umfuseext2_la-op_fgetattr.Plo
/bin/bash ../libtool  --tag=CC   --mode=compile gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE  -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_getattr.lo -MD -MP -MF .deps/umfuseext2_la-op_getattr.Tpo -c -o umfuseext2_la-op_getattr.lo `test -f 'op_getattr.c' || echo './'`op_getattr.c
libtool: compile:  gcc -DHAVE_CONFIG_H -I. -I.. -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_getattr.lo -MD -MP -MF .deps/umfuseext2_la-op_getattr.Tpo -c op_getattr.c  -fPIC -DPIC -o .libs/umfuseext2_la-op_getattr.o
libtool: compile:  gcc -DHAVE_CONFIG_H -I. -I.. -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_getattr.lo -MD -MP -MF .deps/umfuseext2_la-op_getattr.Tpo -c op_getattr.c -o umfuseext2_la-op_getattr.o >/dev/null 2>&1
mv -f .deps/umfuseext2_la-op_getattr.Tpo .deps/umfuseext2_la-op_getattr.Plo
/bin/bash ../libtool  --tag=CC   --mode=compile gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE  -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_getxattr.lo -MD -MP -MF .deps/umfuseext2_la-op_getxattr.Tpo -c -o umfuseext2_la-op_getxattr.lo `test -f 'op_getxattr.c' || echo './'`op_getxattr.c
libtool: compile:  gcc -DHAVE_CONFIG_H -I. -I.. -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_getxattr.lo -MD -MP -MF .deps/umfuseext2_la-op_getxattr.Tpo -c op_getxattr.c  -fPIC -DPIC -o .libs/umfuseext2_la-op_getxattr.o
libtool: compile:  gcc -DHAVE_CONFIG_H -I. -I.. -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_getxattr.lo -MD -MP -MF .deps/umfuseext2_la-op_getxattr.Tpo -c op_getxattr.c -o umfuseext2_la-op_getxattr.o >/dev/null 2>&1
mv -f .deps/umfuseext2_la-op_getxattr.Tpo .deps/umfuseext2_la-op_getxattr.Plo
/bin/bash ../libtool  --tag=CC   --mode=compile gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE  -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_open.lo -MD -MP -MF .deps/umfuseext2_la-op_open.Tpo -c -o umfuseext2_la-op_open.lo `test -f 'op_open.c' || echo './'`op_open.c
libtool: compile:  gcc -DHAVE_CONFIG_H -I. -I.. -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_open.lo -MD -MP -MF .deps/umfuseext2_la-op_open.Tpo -c op_open.c  -fPIC -DPIC -o .libs/umfuseext2_la-op_open.o
libtool: compile:  gcc -DHAVE_CONFIG_H -I. -I.. -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_open.lo -MD -MP -MF .deps/umfuseext2_la-op_open.Tpo -c op_open.c -o umfuseext2_la-op_open.o >/dev/null 2>&1
mv -f .deps/umfuseext2_la-op_open.Tpo .deps/umfuseext2_la-op_open.Plo
/bin/bash ../libtool  --tag=CC   --mode=compile gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE  -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_read.lo -MD -MP -MF .deps/umfuseext2_la-op_read.Tpo -c -o umfuseext2_la-op_read.lo `test -f 'op_read.c' || echo './'`op_read.c
libtool: compile:  gcc -DHAVE_CONFIG_H -I. -I.. -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_read.lo -MD -MP -MF .deps/umfuseext2_la-op_read.Tpo -c op_read.c  -fPIC -DPIC -o .libs/umfuseext2_la-op_read.o
libtool: compile:  gcc -DHAVE_CONFIG_H -I. -I.. -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_read.lo -MD -MP -MF .deps/umfuseext2_la-op_read.Tpo -c op_read.c -o umfuseext2_la-op_read.o >/dev/null 2>&1
mv -f .deps/umfuseext2_la-op_read.Tpo .deps/umfuseext2_la-op_read.Plo
/bin/bash ../libtool  --tag=CC   --mode=compile gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE  -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_readdir.lo -MD -MP -MF .deps/umfuseext2_la-op_readdir.Tpo -c -o umfuseext2_la-op_readdir.lo `test -f 'op_readdir.c' || echo './'`op_readdir.c
libtool: compile:  gcc -DHAVE_CONFIG_H -I. -I.. -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_readdir.lo -MD -MP -MF .deps/umfuseext2_la-op_readdir.Tpo -c op_readdir.c  -fPIC -DPIC -o .libs/umfuseext2_la-op_readdir.o
libtool: compile:  gcc -DHAVE_CONFIG_H -I. -I.. -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_readdir.lo -MD -MP -MF .deps/umfuseext2_la-op_readdir.Tpo -c op_readdir.c -o umfuseext2_la-op_readdir.o >/dev/null 2>&1
mv -f .deps/umfuseext2_la-op_readdir.Tpo .deps/umfuseext2_la-op_readdir.Plo
/bin/bash ../libtool  --tag=CC   --mode=compile gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE  -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_readlink.lo -MD -MP -MF .deps/umfuseext2_la-op_readlink.Tpo -c -o umfuseext2_la-op_readlink.lo `test -f 'op_readlink.c' || echo './'`op_readlink.c
libtool: compile:  gcc -DHAVE_CONFIG_H -I. -I.. -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_readlink.lo -MD -MP -MF .deps/umfuseext2_la-op_readlink.Tpo -c op_readlink.c  -fPIC -DPIC -o .libs/umfuseext2_la-op_readlink.o
libtool: compile:  gcc -DHAVE_CONFIG_H -I. -I.. -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_readlink.lo -MD -MP -MF .deps/umfuseext2_la-op_readlink.Tpo -c op_readlink.c -o umfuseext2_la-op_readlink.o >/dev/null 2>&1
mv -f .deps/umfuseext2_la-op_readlink.Tpo .deps/umfuseext2_la-op_readlink.Plo
/bin/bash ../libtool  --tag=CC   --mode=compile gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE  -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_release.lo -MD -MP -MF .deps/umfuseext2_la-op_release.Tpo -c -o umfuseext2_la-op_release.lo `test -f 'op_release.c' || echo './'`op_release.c
libtool: compile:  gcc -DHAVE_CONFIG_H -I. -I.. -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_release.lo -MD -MP -MF .deps/umfuseext2_la-op_release.Tpo -c op_release.c  -fPIC -DPIC -o .libs/umfuseext2_la-op_release.o
libtool: compile:  gcc -DHAVE_CONFIG_H -I. -I.. -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_release.lo -MD -MP -MF .deps/umfuseext2_la-op_release.Tpo -c op_release.c -o umfuseext2_la-op_release.o >/dev/null 2>&1
mv -f .deps/umfuseext2_la-op_release.Tpo .deps/umfuseext2_la-op_release.Plo
/bin/bash ../libtool  --tag=CC   --mode=compile gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE  -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_statfs.lo -MD -MP -MF .deps/umfuseext2_la-op_statfs.Tpo -c -o umfuseext2_la-op_statfs.lo `test -f 'op_statfs.c' || echo './'`op_statfs.c
libtool: compile:  gcc -DHAVE_CONFIG_H -I. -I.. -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_statfs.lo -MD -MP -MF .deps/umfuseext2_la-op_statfs.Tpo -c op_statfs.c  -fPIC -DPIC -o .libs/umfuseext2_la-op_statfs.o
libtool: compile:  gcc -DHAVE_CONFIG_H -I. -I.. -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_statfs.lo -MD -MP -MF .deps/umfuseext2_la-op_statfs.Tpo -c op_statfs.c -o umfuseext2_la-op_statfs.o >/dev/null 2>&1
mv -f .deps/umfuseext2_la-op_statfs.Tpo .deps/umfuseext2_la-op_statfs.Plo
/bin/bash ../libtool  --tag=CC   --mode=compile gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE  -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_chown.lo -MD -MP -MF .deps/umfuseext2_la-op_chown.Tpo -c -o umfuseext2_la-op_chown.lo `test -f 'op_chown.c' || echo './'`op_chown.c
libtool: compile:  gcc -DHAVE_CONFIG_H -I. -I.. -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_chown.lo -MD -MP -MF .deps/umfuseext2_la-op_chown.Tpo -c op_chown.c  -fPIC -DPIC -o .libs/umfuseext2_la-op_chown.o
libtool: compile:  gcc -DHAVE_CONFIG_H -I. -I.. -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_chown.lo -MD -MP -MF .deps/umfuseext2_la-op_chown.Tpo -c op_chown.c -o umfuseext2_la-op_chown.o >/dev/null 2>&1
mv -f .deps/umfuseext2_la-op_chown.Tpo .deps/umfuseext2_la-op_chown.Plo
/bin/bash ../libtool  --tag=CC   --mode=compile gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE  -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_chmod.lo -MD -MP -MF .deps/umfuseext2_la-op_chmod.Tpo -c -o umfuseext2_la-op_chmod.lo `test -f 'op_chmod.c' || echo './'`op_chmod.c
libtool: compile:  gcc -DHAVE_CONFIG_H -I. -I.. -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_chmod.lo -MD -MP -MF .deps/umfuseext2_la-op_chmod.Tpo -c op_chmod.c  -fPIC -DPIC -o .libs/umfuseext2_la-op_chmod.o
libtool: compile:  gcc -DHAVE_CONFIG_H -I. -I.. -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_chmod.lo -MD -MP -MF .deps/umfuseext2_la-op_chmod.Tpo -c op_chmod.c -o umfuseext2_la-op_chmod.o >/dev/null 2>&1
mv -f .deps/umfuseext2_la-op_chmod.Tpo .deps/umfuseext2_la-op_chmod.Plo
/bin/bash ../libtool  --tag=CC   --mode=compile gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE  -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_create.lo -MD -MP -MF .deps/umfuseext2_la-op_create.Tpo -c -o umfuseext2_la-op_create.lo `test -f 'op_create.c' || echo './'`op_create.c
libtool: compile:  gcc -DHAVE_CONFIG_H -I. -I.. -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_create.lo -MD -MP -MF .deps/umfuseext2_la-op_create.Tpo -c op_create.c  -fPIC -DPIC -o .libs/umfuseext2_la-op_create.o
libtool: compile:  gcc -DHAVE_CONFIG_H -I. -I.. -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_create.lo -MD -MP -MF .deps/umfuseext2_la-op_create.Tpo -c op_create.c -o umfuseext2_la-op_create.o >/dev/null 2>&1
mv -f .deps/umfuseext2_la-op_create.Tpo .deps/umfuseext2_la-op_create.Plo
/bin/bash ../libtool  --tag=CC   --mode=compile gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE  -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_flush.lo -MD -MP -MF .deps/umfuseext2_la-op_flush.Tpo -c -o umfuseext2_la-op_flush.lo `test -f 'op_flush.c' || echo './'`op_flush.c
libtool: compile:  gcc -DHAVE_CONFIG_H -I. -I.. -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_flush.lo -MD -MP -MF .deps/umfuseext2_la-op_flush.Tpo -c op_flush.c  -fPIC -DPIC -o .libs/umfuseext2_la-op_flush.o
libtool: compile:  gcc -DHAVE_CONFIG_H -I. -I.. -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_flush.lo -MD -MP -MF .deps/umfuseext2_la-op_flush.Tpo -c op_flush.c -o umfuseext2_la-op_flush.o >/dev/null 2>&1
mv -f .deps/umfuseext2_la-op_flush.Tpo .deps/umfuseext2_la-op_flush.Plo
/bin/bash ../libtool  --tag=CC   --mode=compile gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE  -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_fsync.lo -MD -MP -MF .deps/umfuseext2_la-op_fsync.Tpo -c -o umfuseext2_la-op_fsync.lo `test -f 'op_fsync.c' || echo './'`op_fsync.c
libtool: compile:  gcc -DHAVE_CONFIG_H -I. -I.. -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_fsync.lo -MD -MP -MF .deps/umfuseext2_la-op_fsync.Tpo -c op_fsync.c  -fPIC -DPIC -o .libs/umfuseext2_la-op_fsync.o
libtool: compile:  gcc -DHAVE_CONFIG_H -I. -I.. -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_fsync.lo -MD -MP -MF .deps/umfuseext2_la-op_fsync.Tpo -c op_fsync.c -o umfuseext2_la-op_fsync.o >/dev/null 2>&1
mv -f .deps/umfuseext2_la-op_fsync.Tpo .deps/umfuseext2_la-op_fsync.Plo
/bin/bash ../libtool  --tag=CC   --mode=compile gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE  -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_mkdir.lo -MD -MP -MF .deps/umfuseext2_la-op_mkdir.Tpo -c -o umfuseext2_la-op_mkdir.lo `test -f 'op_mkdir.c' || echo './'`op_mkdir.c
libtool: compile:  gcc -DHAVE_CONFIG_H -I. -I.. -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_mkdir.lo -MD -MP -MF .deps/umfuseext2_la-op_mkdir.Tpo -c op_mkdir.c  -fPIC -DPIC -o .libs/umfuseext2_la-op_mkdir.o
libtool: compile:  gcc -DHAVE_CONFIG_H -I. -I.. -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_mkdir.lo -MD -MP -MF .deps/umfuseext2_la-op_mkdir.Tpo -c op_mkdir.c -o umfuseext2_la-op_mkdir.o >/dev/null 2>&1
mv -f .deps/umfuseext2_la-op_mkdir.Tpo .deps/umfuseext2_la-op_mkdir.Plo
/bin/bash ../libtool  --tag=CC   --mode=compile gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE  -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_rmdir.lo -MD -MP -MF .deps/umfuseext2_la-op_rmdir.Tpo -c -o umfuseext2_la-op_rmdir.lo `test -f 'op_rmdir.c' || echo './'`op_rmdir.c
libtool: compile:  gcc -DHAVE_CONFIG_H -I. -I.. -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_rmdir.lo -MD -MP -MF .deps/umfuseext2_la-op_rmdir.Tpo -c op_rmdir.c  -fPIC -DPIC -o .libs/umfuseext2_la-op_rmdir.o
libtool: compile:  gcc -DHAVE_CONFIG_H -I. -I.. -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_rmdir.lo -MD -MP -MF .deps/umfuseext2_la-op_rmdir.Tpo -c op_rmdir.c -o umfuseext2_la-op_rmdir.o >/dev/null 2>&1
mv -f .deps/umfuseext2_la-op_rmdir.Tpo .deps/umfuseext2_la-op_rmdir.Plo
/bin/bash ../libtool  --tag=CC   --mode=compile gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE  -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_unlink.lo -MD -MP -MF .deps/umfuseext2_la-op_unlink.Tpo -c -o umfuseext2_la-op_unlink.lo `test -f 'op_unlink.c' || echo './'`op_unlink.c
libtool: compile:  gcc -DHAVE_CONFIG_H -I. -I.. -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_unlink.lo -MD -MP -MF .deps/umfuseext2_la-op_unlink.Tpo -c op_unlink.c  -fPIC -DPIC -o .libs/umfuseext2_la-op_unlink.o
libtool: compile:  gcc -DHAVE_CONFIG_H -I. -I.. -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_unlink.lo -MD -MP -MF .deps/umfuseext2_la-op_unlink.Tpo -c op_unlink.c -o umfuseext2_la-op_unlink.o >/dev/null 2>&1
mv -f .deps/umfuseext2_la-op_unlink.Tpo .deps/umfuseext2_la-op_unlink.Plo
/bin/bash ../libtool  --tag=CC   --mode=compile gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE  -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_utimens.lo -MD -MP -MF .deps/umfuseext2_la-op_utimens.Tpo -c -o umfuseext2_la-op_utimens.lo `test -f 'op_utimens.c' || echo './'`op_utimens.c
libtool: compile:  gcc -DHAVE_CONFIG_H -I. -I.. -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_utimens.lo -MD -MP -MF .deps/umfuseext2_la-op_utimens.Tpo -c op_utimens.c  -fPIC -DPIC -o .libs/umfuseext2_la-op_utimens.o
libtool: compile:  gcc -DHAVE_CONFIG_H -I. -I.. -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_utimens.lo -MD -MP -MF .deps/umfuseext2_la-op_utimens.Tpo -c op_utimens.c -o umfuseext2_la-op_utimens.o >/dev/null 2>&1
mv -f .deps/umfuseext2_la-op_utimens.Tpo .deps/umfuseext2_la-op_utimens.Plo
/bin/bash ../libtool  --tag=CC   --mode=compile gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE  -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_write.lo -MD -MP -MF .deps/umfuseext2_la-op_write.Tpo -c -o umfuseext2_la-op_write.lo `test -f 'op_write.c' || echo './'`op_write.c
libtool: compile:  gcc -DHAVE_CONFIG_H -I. -I.. -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_write.lo -MD -MP -MF .deps/umfuseext2_la-op_write.Tpo -c op_write.c  -fPIC -DPIC -o .libs/umfuseext2_la-op_write.o
libtool: compile:  gcc -DHAVE_CONFIG_H -I. -I.. -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_write.lo -MD -MP -MF .deps/umfuseext2_la-op_write.Tpo -c op_write.c -o umfuseext2_la-op_write.o >/dev/null 2>&1
mv -f .deps/umfuseext2_la-op_write.Tpo .deps/umfuseext2_la-op_write.Plo
/bin/bash ../libtool  --tag=CC   --mode=compile gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE  -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_mknod.lo -MD -MP -MF .deps/umfuseext2_la-op_mknod.Tpo -c -o umfuseext2_la-op_mknod.lo `test -f 'op_mknod.c' || echo './'`op_mknod.c
libtool: compile:  gcc -DHAVE_CONFIG_H -I. -I.. -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_mknod.lo -MD -MP -MF .deps/umfuseext2_la-op_mknod.Tpo -c op_mknod.c  -fPIC -DPIC -o .libs/umfuseext2_la-op_mknod.o
libtool: compile:  gcc -DHAVE_CONFIG_H -I. -I.. -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_mknod.lo -MD -MP -MF .deps/umfuseext2_la-op_mknod.Tpo -c op_mknod.c -o umfuseext2_la-op_mknod.o >/dev/null 2>&1
mv -f .deps/umfuseext2_la-op_mknod.Tpo .deps/umfuseext2_la-op_mknod.Plo
/bin/bash ../libtool  --tag=CC   --mode=compile gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE  -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_symlink.lo -MD -MP -MF .deps/umfuseext2_la-op_symlink.Tpo -c -o umfuseext2_la-op_symlink.lo `test -f 'op_symlink.c' || echo './'`op_symlink.c
libtool: compile:  gcc -DHAVE_CONFIG_H -I. -I.. -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_symlink.lo -MD -MP -MF .deps/umfuseext2_la-op_symlink.Tpo -c op_symlink.c  -fPIC -DPIC -o .libs/umfuseext2_la-op_symlink.o
libtool: compile:  gcc -DHAVE_CONFIG_H -I. -I.. -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_symlink.lo -MD -MP -MF .deps/umfuseext2_la-op_symlink.Tpo -c op_symlink.c -o umfuseext2_la-op_symlink.o >/dev/null 2>&1
mv -f .deps/umfuseext2_la-op_symlink.Tpo .deps/umfuseext2_la-op_symlink.Plo
/bin/bash ../libtool  --tag=CC   --mode=compile gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE  -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_truncate.lo -MD -MP -MF .deps/umfuseext2_la-op_truncate.Tpo -c -o umfuseext2_la-op_truncate.lo `test -f 'op_truncate.c' || echo './'`op_truncate.c
libtool: compile:  gcc -DHAVE_CONFIG_H -I. -I.. -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_truncate.lo -MD -MP -MF .deps/umfuseext2_la-op_truncate.Tpo -c op_truncate.c  -fPIC -DPIC -o .libs/umfuseext2_la-op_truncate.o
libtool: compile:  gcc -DHAVE_CONFIG_H -I. -I.. -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_truncate.lo -MD -MP -MF .deps/umfuseext2_la-op_truncate.Tpo -c op_truncate.c -o umfuseext2_la-op_truncate.o >/dev/null 2>&1
mv -f .deps/umfuseext2_la-op_truncate.Tpo .deps/umfuseext2_la-op_truncate.Plo
/bin/bash ../libtool  --tag=CC   --mode=compile gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE  -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_link.lo -MD -MP -MF .deps/umfuseext2_la-op_link.Tpo -c -o umfuseext2_la-op_link.lo `test -f 'op_link.c' || echo './'`op_link.c
libtool: compile:  gcc -DHAVE_CONFIG_H -I. -I.. -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_link.lo -MD -MP -MF .deps/umfuseext2_la-op_link.Tpo -c op_link.c  -fPIC -DPIC -o .libs/umfuseext2_la-op_link.o
libtool: compile:  gcc -DHAVE_CONFIG_H -I. -I.. -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_link.lo -MD -MP -MF .deps/umfuseext2_la-op_link.Tpo -c op_link.c -o umfuseext2_la-op_link.o >/dev/null 2>&1
mv -f .deps/umfuseext2_la-op_link.Tpo .deps/umfuseext2_la-op_link.Plo
/bin/bash ../libtool  --tag=CC   --mode=compile gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE  -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_rename.lo -MD -MP -MF .deps/umfuseext2_la-op_rename.Tpo -c -o umfuseext2_la-op_rename.lo `test -f 'op_rename.c' || echo './'`op_rename.c
libtool: compile:  gcc -DHAVE_CONFIG_H -I. -I.. -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_rename.lo -MD -MP -MF .deps/umfuseext2_la-op_rename.Tpo -c op_rename.c  -fPIC -DPIC -o .libs/umfuseext2_la-op_rename.o
libtool: compile:  gcc -DHAVE_CONFIG_H -I. -I.. -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_rename.lo -MD -MP -MF .deps/umfuseext2_la-op_rename.Tpo -c op_rename.c -o umfuseext2_la-op_rename.o >/dev/null 2>&1
mv -f .deps/umfuseext2_la-op_rename.Tpo .deps/umfuseext2_la-op_rename.Plo
/bin/bash ../libtool  --tag=CC   --mode=link gcc -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE  -I/usr/local/include/umview -I/usr/local/include -g -O2 -module -avoid-version -export-dynamic -lext2fs  -o umfuseext2.la -rpath /usr/local/lib/umview/modules umfuseext2_la-fuse-ext2.lo umfuseext2_la-do_probe.lo umfuseext2_la-do_check.lo umfuseext2_la-do_fillstatbuf.lo umfuseext2_la-do_readinode.lo umfuseext2_la-do_writeinode.lo umfuseext2_la-do_killfilebyinode.lo umfuseext2_la-op_init.lo umfuseext2_la-op_destroy.lo umfuseext2_la-op_access.lo umfuseext2_la-op_fgetattr.lo umfuseext2_la-op_getattr.lo umfuseext2_la-op_getxattr.lo umfuseext2_la-op_open.lo umfuseext2_la-op_read.lo umfuseext2_la-op_readdir.lo umfuseext2_la-op_readlink.lo umfuseext2_la-op_release.lo umfuseext2_la-op_statfs.lo umfuseext2_la-op_chown.lo umfuseext2_la-op_chmod.lo umfuseext2_la-op_create.lo umfuseext2_la-op_flush.lo umfuseext2_la-op_fsync.lo umfuseext2_la-op_mkdir.lo umfuseext2_la-op_rmdir.lo umfuseext2_la-op_unlink.lo umfuseext2_la-op_utimens.lo umfuseext2_la-op_write.lo umfuseext2_la-op_mknod.lo umfuseext2_la-op_symlink.lo umfuseext2_la-op_truncate.lo umfuseext2_la-op_link.lo umfuseext2_la-op_rename.lo  -lext2fs -lcom_err -lfuse -lpthread 
libtool: link: gcc -shared  -fPIC -DPIC  .libs/umfuseext2_la-fuse-ext2.o .libs/umfuseext2_la-do_probe.o .libs/umfuseext2_la-do_check.o .libs/umfuseext2_la-do_fillstatbuf.o .libs/umfuseext2_la-do_readinode.o .libs/umfuseext2_la-do_writeinode.o .libs/umfuseext2_la-do_killfilebyinode.o .libs/umfuseext2_la-op_init.o .libs/umfuseext2_la-op_destroy.o .libs/umfuseext2_la-op_access.o .libs/umfuseext2_la-op_fgetattr.o .libs/umfuseext2_la-op_getattr.o .libs/umfuseext2_la-op_getxattr.o .libs/umfuseext2_la-op_open.o .libs/umfuseext2_la-op_read.o .libs/umfuseext2_la-op_readdir.o .libs/umfuseext2_la-op_readlink.o .libs/umfuseext2_la-op_release.o .libs/umfuseext2_la-op_statfs.o .libs/umfuseext2_la-op_chown.o .libs/umfuseext2_la-op_chmod.o .libs/umfuseext2_la-op_create.o .libs/umfuseext2_la-op_flush.o .libs/umfuseext2_la-op_fsync.o .libs/umfuseext2_la-op_mkdir.o .libs/umfuseext2_la-op_rmdir.o .libs/umfuseext2_la-op_unlink.o .libs/umfuseext2_la-op_utimens.o .libs/umfuseext2_la-op_write.o .libs/umfuseext2_la-op_mknod.o .libs/umfuseext2_la-op_symlink.o .libs/umfuseext2_la-op_truncate.o .libs/umfuseext2_la-op_link.o .libs/umfuseext2_la-op_rename.o   -lext2fs -lcom_err -lfuse -lpthread  -g -O2   -Wl,-soname -Wl,umfuseext2.so -o .libs/umfuseext2.so
libtool: link: ar cr .libs/umfuseext2.a  umfuseext2_la-fuse-ext2.o umfuseext2_la-do_probe.o umfuseext2_la-do_check.o umfuseext2_la-do_fillstatbuf.o umfuseext2_la-do_readinode.o umfuseext2_la-do_writeinode.o umfuseext2_la-do_killfilebyinode.o umfuseext2_la-op_init.o umfuseext2_la-op_destroy.o umfuseext2_la-op_access.o umfuseext2_la-op_fgetattr.o umfuseext2_la-op_getattr.o umfuseext2_la-op_getxattr.o umfuseext2_la-op_open.o umfuseext2_la-op_read.o umfuseext2_la-op_readdir.o umfuseext2_la-op_readlink.o umfuseext2_la-op_release.o umfuseext2_la-op_statfs.o umfuseext2_la-op_chown.o umfuseext2_la-op_chmod.o umfuseext2_la-op_create.o umfuseext2_la-op_flush.o umfuseext2_la-op_fsync.o umfuseext2_la-op_mkdir.o umfuseext2_la-op_rmdir.o umfuseext2_la-op_unlink.o umfuseext2_la-op_utimens.o umfuseext2_la-op_write.o umfuseext2_la-op_mknod.o umfuseext2_la-op_symlink.o umfuseext2_la-op_truncate.o umfuseext2_la-op_link.o umfuseext2_la-op_rename.o
libtool: link: ranlib .libs/umfuseext2.a
libtool: link: ( cd ".libs" && rm -f "umfuseext2.la" && ln -s "../umfuseext2.la" "umfuseext2.la" )
make[2]: Leaving directory '/home/ubuntu/Downloads/fuse-ext2-master/fuse-ext2'
Making all in tools
make[2]: Entering directory '/home/ubuntu/Downloads/fuse-ext2-master/tools'
Making all in macosx
make[3]: Entering directory '/home/ubuntu/Downloads/fuse-ext2-master/tools/macosx'
make[3]: Nothing to be done for 'all'.
make[3]: Leaving directory '/home/ubuntu/Downloads/fuse-ext2-master/tools/macosx'
make[3]: Entering directory '/home/ubuntu/Downloads/fuse-ext2-master/tools'
make[3]: Nothing to be done for 'all-am'.
make[3]: Leaving directory '/home/ubuntu/Downloads/fuse-ext2-master/tools'
make[2]: Leaving directory '/home/ubuntu/Downloads/fuse-ext2-master/tools'
make[2]: Entering directory '/home/ubuntu/Downloads/fuse-ext2-master'
make[2]: Leaving directory '/home/ubuntu/Downloads/fuse-ext2-master'
make[1]: Leaving directory '/home/ubuntu/Downloads/fuse-ext2-master'
ubuntu@ubuntu:~/Downloads/fuse-ext2-master$ sudo make install
Making install in fuse-ext2
make[1]: Entering directory '/home/ubuntu/Downloads/fuse-ext2-master/fuse-ext2'
make[2]: Entering directory '/home/ubuntu/Downloads/fuse-ext2-master/fuse-ext2'
 /usr/bin/mkdir -p '/usr/local/bin'
  /bin/bash ../libtool   --mode=install /usr/bin/install -c fuse-ext2 fuse-ext2.probe '/usr/local/bin'
libtool: install: /usr/bin/install -c fuse-ext2 /usr/local/bin/fuse-ext2
libtool: install: /usr/bin/install -c fuse-ext2.probe /usr/local/bin/fuse-ext2.probe
/usr/bin/install -c -d "//usr/local/sbin"
ln -s -f "/usr/local/bin/fuse-ext2" "//usr/local/sbin/mount.fuse-ext2"
 /usr/bin/mkdir -p '/usr/local/lib/umview/modules'
 /bin/bash ../libtool   --mode=install /usr/bin/install -c   umfuseext2.la '/usr/local/lib/umview/modules'
libtool: install: /usr/bin/install -c .libs/umfuseext2.so /usr/local/lib/umview/modules/umfuseext2.so
libtool: install: /usr/bin/install -c .libs/umfuseext2.lai /usr/local/lib/umview/modules/umfuseext2.la
libtool: install: /usr/bin/install -c .libs/umfuseext2.a /usr/local/lib/umview/modules/umfuseext2.a
libtool: install: chmod 644 /usr/local/lib/umview/modules/umfuseext2.a
libtool: install: ranlib /usr/local/lib/umview/modules/umfuseext2.a
libtool: finish: PATH="/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/snap/bin:/sbin" ldconfig -n /usr/local/lib/umview/modules
----------------------------------------------------------------------
Libraries have been installed in:
   /usr/local/lib/umview/modules

If you ever happen to want to link against installed libraries
in a given directory, LIBDIR, you must either use libtool, and
specify the full pathname of the library, or use the '-LLIBDIR'
flag during linking and do at least one of the following:
   - add LIBDIR to the 'LD_LIBRARY_PATH' environment variable
     during execution
   - add LIBDIR to the 'LD_RUN_PATH' environment variable
     during linking
   - use the '-Wl,-rpath -Wl,LIBDIR' linker flag
   - have your system administrator add LIBDIR to '/etc/ld.so.conf'

See any operating system documentation about shared libraries for
more information, such as the ld(1) and ld.so(8) manual pages.
----------------------------------------------------------------------
make  install-data-hook
make[3]: Entering directory '/home/ubuntu/Downloads/fuse-ext2-master/fuse-ext2'
cd "//usr/local/lib/umview/modules" && rm -f umfuseext2.la
make[3]: Leaving directory '/home/ubuntu/Downloads/fuse-ext2-master/fuse-ext2'
make[2]: Leaving directory '/home/ubuntu/Downloads/fuse-ext2-master/fuse-ext2'
make[1]: Leaving directory '/home/ubuntu/Downloads/fuse-ext2-master/fuse-ext2'
Making install in tools
make[1]: Entering directory '/home/ubuntu/Downloads/fuse-ext2-master/tools'
Making install in macosx
make[2]: Entering directory '/home/ubuntu/Downloads/fuse-ext2-master/tools/macosx'
make[3]: Entering directory '/home/ubuntu/Downloads/fuse-ext2-master/tools/macosx'
make[3]: Nothing to be done for 'install-exec-am'.
make[3]: Nothing to be done for 'install-data-am'.
make[3]: Leaving directory '/home/ubuntu/Downloads/fuse-ext2-master/tools/macosx'
make[2]: Leaving directory '/home/ubuntu/Downloads/fuse-ext2-master/tools/macosx'
make[2]: Entering directory '/home/ubuntu/Downloads/fuse-ext2-master/tools'
make[3]: Entering directory '/home/ubuntu/Downloads/fuse-ext2-master/tools'
make[3]: Nothing to be done for 'install-exec-am'.
make[3]: Nothing to be done for 'install-data-am'.
make[3]: Leaving directory '/home/ubuntu/Downloads/fuse-ext2-master/tools'
make[2]: Leaving directory '/home/ubuntu/Downloads/fuse-ext2-master/tools'
make[1]: Leaving directory '/home/ubuntu/Downloads/fuse-ext2-master/tools'
make[1]: Entering directory '/home/ubuntu/Downloads/fuse-ext2-master'
make[2]: Entering directory '/home/ubuntu/Downloads/fuse-ext2-master'
make[2]: Nothing to be done for 'install-exec-am'.
 /usr/bin/mkdir -p '/usr/local/share/man/man1'
 /usr/bin/install -c -m 644 fuse-ext2.1 '/usr/local/share/man/man1'
 /usr/bin/mkdir -p '/usr/local/lib/pkgconfig'
 /usr/bin/install -c -m 644 fuse-ext2.pc '/usr/local/lib/pkgconfig'
make[2]: Leaving directory '/home/ubuntu/Downloads/fuse-ext2-master'
make[1]: Leaving directory '/home/ubuntu/Downloads/fuse-ext2-master'
-DHAVE_CONFIG_H -I. -I.. -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_unlink.lo -MD -MP -MF .deps/umfuseext2_la-op_unlink.Tpo -c op_unlink.c  -fPIC -DPIC -o .libs/umfuseext2_la-op_unlink.o
libtool: compile:  gcc -DHAVE_CONFIG_H -I. -I.. -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_unlink.lo -MD -MP -MF .deps/umfuseext2_la-op_unlink.Tpo -c op_unlink.c -o umfuseext2_la-op_unlink.o >/dev/null 2>&1
mv -f .deps/umfuseext2_la-op_unlink.Tpo .deps/umfuseext2_la-op_unlink.Plo
/bin/bash ../libtool  --tag=CC   --mode=compile gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE  -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_utimens.lo -MD -MP -MF .deps/umfuseext2_la-op_utimens.Tpo -c -o umfuseext2_la-op_utimens.lo `test -f 'op_utimens.c' || echo './'`op_utimens.c
libtool: compile:  gcc -DHAVE_CONFIG_H -I. -I.. -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_utimens.lo -MD -MP -MF .deps/umfuseext2_la-op_utimens.Tpo -c op_utimens.c  -fPIC -DPIC -o .libs/umfuseext2_la-op_utimens.o
libtool: compile:  gcc -DHAVE_CONFIG_H -I. -I.. -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_utimens.lo -MD -MP -MF .deps/umfuseext2_la-op_utimens.Tpo -c op_utimens.c -o umfuseext2_la-op_utimens.o >/dev/null 2>&1
mv -f .deps/umfuseext2_la-op_utimens.Tpo .deps/umfuseext2_la-op_utimens.Plo
/bin/bash ../libtool  --tag=CC   --mode=compile gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE  -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_write.lo -MD -MP -MF .deps/umfuseext2_la-op_write.Tpo -c -o umfuseext2_la-op_write.lo `test -f 'op_write.c' || echo './'`op_write.c
libtool: compile:  gcc -DHAVE_CONFIG_H -I. -I.. -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_write.lo -MD -MP -MF .deps/umfuseext2_la-op_write.Tpo -c op_write.c  -fPIC -DPIC -o .libs/umfuseext2_la-op_write.o
libtool: compile:  gcc -DHAVE_CONFIG_H -I. -I.. -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_write.lo -MD -MP -MF .deps/umfuseext2_la-op_write.Tpo -c op_write.c -o umfuseext2_la-op_write.o >/dev/null 2>&1
mv -f .deps/umfuseext2_la-op_write.Tpo .deps/umfuseext2_la-op_write.Plo
/bin/bash ../libtool  --tag=CC   --mode=compile gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE  -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_mknod.lo -MD -MP -MF .deps/umfuseext2_la-op_mknod.Tpo -c -o umfuseext2_la-op_mknod.lo `test -f 'op_mknod.c' || echo './'`op_mknod.c
libtool: compile:  gcc -DHAVE_CONFIG_H -I. -I.. -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_mknod.lo -MD -MP -MF .deps/umfuseext2_la-op_mknod.Tpo -c op_mknod.c  -fPIC -DPIC -o .libs/umfuseext2_la-op_mknod.o
libtool: compile:  gcc -DHAVE_CONFIG_H -I. -I.. -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_mknod.lo -MD -MP -MF .deps/umfuseext2_la-op_mknod.Tpo -c op_mknod.c -o umfuseext2_la-op_mknod.o >/dev/null 2>&1
mv -f .deps/umfuseext2_la-op_mknod.Tpo .deps/umfuseext2_la-op_mknod.Plo
/bin/bash ../libtool  --tag=CC   --mode=compile gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE  -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_symlink.lo -MD -MP -MF .deps/umfuseext2_la-op_symlink.Tpo -c -o umfuseext2_la-op_symlink.lo `test -f 'op_symlink.c' || echo './'`op_symlink.c
libtool: compile:  gcc -DHAVE_CONFIG_H -I. -I.. -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_symlink.lo -MD -MP -MF .deps/umfuseext2_la-op_symlink.Tpo -c op_symlink.c  -fPIC -DPIC -o .libs/umfuseext2_la-op_symlink.o
libtool: compile:  gcc -DHAVE_CONFIG_H -I. -I.. -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_symlink.lo -MD -MP -MF .deps/umfuseext2_la-op_symlink.Tpo -c op_symlink.c -o umfuseext2_la-op_symlink.o >/dev/null 2>&1
mv -f .deps/umfuseext2_la-op_symlink.Tpo .deps/umfuseext2_la-op_symlink.Plo
/bin/bash ../libtool  --tag=CC   --mode=compile gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE  -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_truncate.lo -MD -MP -MF .deps/umfuseext2_la-op_truncate.Tpo -c -o umfuseext2_la-op_truncate.lo `test -f 'op_truncate.c' || echo './'`op_truncate.c
libtool: compile:  gcc -DHAVE_CONFIG_H -I. -I.. -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_truncate.lo -MD -MP -MF .deps/umfuseext2_la-op_truncate.Tpo -c op_truncate.c  -fPIC -DPIC -o .libs/umfuseext2_la-op_truncate.o
libtool: compile:  gcc -DHAVE_CONFIG_H -I. -I.. -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_truncate.lo -MD -MP -MF .deps/umfuseext2_la-op_truncate.Tpo -c op_truncate.c -o umfuseext2_la-op_truncate.o >/dev/null 2>&1
mv -f .deps/umfuseext2_la-op_truncate.Tpo .deps/umfuseext2_la-op_truncate.Plo
/bin/bash ../libtool  --tag=CC   --mode=compile gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE  -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_link.lo -MD -MP -MF .deps/umfuseext2_la-op_link.Tpo -c -o umfuseext2_la-op_link.lo `test -f 'op_link.c' || echo './'`op_link.c
libtool: compile:  gcc -DHAVE_CONFIG_H -I. -I.. -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_link.lo -MD -MP -MF .deps/umfuseext2_la-op_link.Tpo -c op_link.c  -fPIC -DPIC -o .libs/umfuseext2_la-op_link.o
libtool: compile:  gcc -DHAVE_CONFIG_H -I. -I.. -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_link.lo -MD -MP -MF .deps/umfuseext2_la-op_link.Tpo -c op_link.c -o umfuseext2_la-op_link.o >/dev/null 2>&1
mv -f .deps/umfuseext2_la-op_link.Tpo .deps/umfuseext2_la-op_link.Plo
/bin/bash ../libtool  --tag=CC   --mode=compile gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE  -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_rename.lo -MD -MP -MF .deps/umfuseext2_la-op_rename.Tpo -c -o umfuseext2_la-op_rename.lo `test -f 'op_rename.c' || echo './'`op_rename.c
libtool: compile:  gcc -DHAVE_CONFIG_H -I. -I.. -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_rename.lo -MD -MP -MF .deps/umfuseext2_la-op_rename.Tpo -c op_rename.c  -fPIC -DPIC -o .libs/umfuseext2_la-op_rename.o
libtool: compile:  gcc -DHAVE_CONFIG_H -I. -I.. -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_rename.lo -MD -MP -MF .deps/umfuseext2_la-op_rename.Tpo -c op_rename.c -o umfuseext2_la-op_rename.o >/dev/null 2>&1
mv -f .deps/umfuseext2_la-op_rename.Tpo .deps/umfuseext2_la-op_rename.Plo
/bin/bash ../libtool  --tag=CC   --mode=link gcc -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE  -I/usr/local/include/umview -I/usr/local/include -g -O2 -module -avoid-version -export-dynamic -lext2fs  -o umfuseext2.la -rpath /usr/local/lib/umview/modules umfuseext2_la-fuse-ext2.lo umfuseext2_la-do_probe.lo umfuseext2_la-do_check.lo umfuseext2_la-do_fillstatbuf.lo umfuseext2_la-do_readinode.lo umfuseext2_la-do_writeinode.lo umfuseext2_la-do_killfilebyinode.lo umfuseext2_la-op_init.lo umfuseext2_la-op_destroy.lo umfuseext2_la-op_access.lo umfuseext2_la-op_fgetattr.lo umfuseext2_la-op_getattr.lo umfuseext2_la-op_getxattr.lo umfuseext2_la-op_open.lo umfuseext2_la-op_read.lo umfuseext2_la-op_readdir.lo umfuseext2_la-op_readlink.lo umfuseext2_la-op_release.lo umfuseext2_la-op_statfs.lo umfuseext2_la-op_chown.lo umfuseext2_la-op_chmod.lo umfuseext2_la-op_create.lo umfuseext2_la-op_flush.lo umfuseext2_la-op_fsync.lo umfuseext2_la-op_mkdir.lo umfuseext2_la-op_rmdir.lo umfuseext2_la-op_unlink.lo umfuseext2_la-op_utimens.lo umfuseext2_la-op_write.lo umfuseext2_la-op_mknod.lo umfuseext2_la-op_symlink.lo umfuseext2_la-op_truncate.lo umfuseext2_la-op_link.lo umfuseext2_la-op_rename.lo  -lext2fs -lcom_err -lfuse -lpthread 
libtool: link: gcc -shared  -fPIC -DPIC  .libs/umfuseext2_la-fuse-ext2.o .libs/umfuseext2_la-do_probe.o .libs/umfuseext2_la-do_check.o .libs/umfuseext2_la-do_fillstatbuf.o .libs/umfuseext2_la-do_readinode.o .libs/umfuseext2_la-do_writeinode.o .libs/umfuseext2_la-do_killfilebyinode.o .libs/umfuseext2_la-op_init.o .libs/umfuseext2_la-op_destroy.o .libs/umfuseext2_la-op_access.o .libs/umfuseext2_la-op_fgetattr.o .libs/umfuseext2_la-op_getattr.o .libs/umfuseext2_la-op_getxattr.o .libs/umfuseext2_la-op_open.o .libs/umfuseext2_la-op_read.o .libs/umfuseext2_la-op_readdir.o .libs/umfuseext2_la-op_readlink.o .libs/umfuseext2_la-op_release.o .libs/umfuseext2_la-op_statfs.o .libs/umfuseext2_la-op_chown.o .libs/umfuseext2_la-op_chmod.o .libs/umfuseext2_la-op_create.o .libs/umfuseext2_la-op_flush.o .libs/umfuseext2_la-op_fsync.o .libs/umfuseext2_la-op_mkdir.o .libs/umfuseext2_la-op_rmdir.o .libs/umfuseext2_la-op_unlink.o .libs/umfuseext2_la-op_utimens.o .libs/umfuseext2_la-op_write.o .libs/umfuseext2_la-op_mknod.o .libs/umfuseext2_la-op_symlink.o .libs/umfuseext2_la-op_truncate.o .libs/umfuseext2_la-op_link.o .libs/umfuseext2_la-op_rename.o   -lext2fs -lcom_err -lfuse -lpthread  -g -O2   -Wl,-soname -Wl,umfuseext2.so -o .libs/umfuseext2.so
libtool: link: ar cr .libs/umfuseext2.a  umfuseext2_la-fuse-ext2.o umfuseext2_la-do_probe.o umfuseext2_la-do_check.o umfuseext2_la-do_fillstatbuf.o umfuseext2_la-do_readinode.o umfuseext2_la-do_writeinode.o umfuseext2_la-do_killfilebyinode.o umfuseext2_la-op_init.o umfuseext2_la-op_destroy.o umfuseext2_la-op_access.o umfuseext2_la-op_fgetattr.o umfuseext2_la-op_getattr.o umfuseext2_la-op_getxattr.o umfuseext2_la-op_open.o umfuseext2_la-op_read.o umfuseext2_la-op_readdir.o umfuseext2_la-op_readlink.o umfuseext2_la-op_release.o umfuseext2_la-op_statfs.o umfuseext2_la-op_chown.o umfuseext2_la-op_chmod.o umfuseext2_la-op_create.o umfuseext2_la-op_flush.o umfuseext2_la-op_fsync.o umfuseext2_la-op_mkdir.o umfuseext2_la-op_rmdir.o umfuseext2_la-op_unlink.o umfuseext2_la-op_utimens.o umfuseext2_la-op_write.o umfuseext2_la-op_mknod.o umfuseext2_la-op_symlink.o umfuseext2_la-op_truncate.o umfuseext2_la-op_link.o umfuseext2_la-op_rename.o
libtool: link: ranlib .libs/umfuseext2.a
libtool: link: ( cd ".libs" && rm -f "umfuseext2.la" && ln -s "../umfuseext2.la" "umfuseext2.la" )
make[2]: Leaving directory '/home/ubuntu/Downloads/fuse-ext2-master/fuse-ext2'
Making all in tools
make[2]: Entering directory '/home/ubuntu/Downloads/fuse-ext2-master/tools'
Making all in macosx
make[3]: Entering directory '/home/ubuntu/Downloads/fuse-ext2-master/tools/macosx'
make[3]: Nothing to be done for 'all'.
make[3]: Leaving directory '/home/ubuntu/Downloads/fuse-ext2-master/tools/macosx'
make[3]: Entering directory '/home/ubuntu/Downloads/fuse-ext2-master/tools'
make[3]: Nothing to be done for 'all-am'.
make[3]: Leaving directory '/home/ubuntu/Downloads/fuse-ext2-master/tools'
make[2]: Leaving directory '/home/ubuntu/Downloads/fuse-ext2-master/tools'
make[2]: Entering directory '/home/ubuntu/Downloads/fuse-ext2-master'
make[2]: Leaving directory '/home/ubuntu/Downloads/fuse-ext2-master'
make[1]: Leaving directory '/home/ubuntu/Downloads/fuse-ext2-master'
ubuntu@ubuntu:~/Downloads/fuse-ext2-master$ sudo make install
Making install in fuse-ext2
make[1]: Entering directory '/home/ubuntu/Downloads/fuse-ext2-master/fuse-ext2'
make[2]: Entering directory '/home/ubuntu/Downloads/fuse-ext2-master/fuse-ext2'
 /usr/bin/mkdir -p '/usr/local/bin'
  /bin/bash ../libtool   --mode=install /usr/bin/install -c fuse-ext2 fuse-ext2.probe '/usr/local/bin'
libtool: install: /usr/bin/install -c fuse-ext2 /usr/local/bin/fuse-ext2
libtool: install: /usr/bin/install -c fuse-ext2.probe /usr/local/bin/fuse-ext2.probe
/usr/bin/install -c -d "//usr/local/sbin"
ln -s -f "/usr/local/bin/fuse-ext2" "//usr/local/sbin/mount.fuse-ext2"
 /usr/bin/mkdir -p '/usr/local/lib/umview/modules'
 /bin/bash ../libtool   --mode=install /usr/bin/install -c   umfuseext2.la '/usr/local/lib/umview/modules'
libtool: install: /usr/bin/install -c .libs/umfuseext2.so /usr/local/lib/umview/modules/umfuseext2.so
libtool: install: /usr/bin/install -c .libs/umfuseext2.lai /usr/local/lib/umview/modules/umfuseext2.la
libtool: install: /usr/bin/install -c .libs/umfuseext2.a /usr/local/lib/umview/modules/umfuseext2.a
libtool: install: chmod 644 /usr/local/lib/umview/modules/umfuseext2.a
libtool: install: ranlib /usr/local/lib/umview/modules/umfuseext2.a
libtool: finish: PATH="/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/snap/bin:/sbin" ldconfig -n /usr/local/lib/umview/modules
----------------------------------------------------------------------
Libraries have been installed in:
   /usr/local/lib/umview/modules

If you ever happen to want to link against installed libraries
in a given directory, LIBDIR, you must either use libtool, and
specify the full pathname of the library, or use the '-LLIBDIR'
flag during linking and do at least one of the following:
   - add LIBDIR to the 'LD_LIBRARY_PATH' environment variable
     during execution
   - add LIBDIR to the 'LD_RUN_PATH' environment variable
     during linking
   - use the '-Wl,-rpath -Wl,LIBDIR' linker flag
   - have your system administrator add LIBDIR to '/etc/ld.so.conf'

See any operating system documentation about shared libraries for
more information, such as the ld(1) and ld.so(8) manual pages.
----------------------------------------------------------------------
make  install-data-hook
make[3]: Entering directory '/home/ubuntu/Downloads/fuse-ext2-master/fuse-ext2'
cd "//usr/local/lib/umview/modules" && rm -f umfuseext2.la
make[3]: Leaving directory '/home/ubuntu/Downloads/fuse-ext2-master/fuse-ext2'
make[2]: Leaving directory '/home/ubuntu/Downloads/fuse-ext2-master/fuse-ext2'
make[1]: Leaving directory '/home/ubuntu/Downloads/fuse-ext2-master/fuse-ext2'
Making install in tools
make[1]: Entering directory '/home/ubuntu/Downloads/fuse-ext2-master/tools'
Making install in macosx
make[2]: Entering directory '/home/ubuntu/Downloads/fuse-ext2-master/tools/macosx'
make[3]: Entering directory '/home/ubuntu/Downloads/fuse-ext2-master/tools/macosx'
make[3]: Nothing to be done for 'install-exec-am'.
make[3]: Nothing to be done for 'install-data-am'.
make[3]: Leaving directory '/home/ubuntu/Downloads/fuse-ext2-master/tools/macosx'
make[2]: Leaving directory '/home/ubuntu/Downloads/fuse-ext2-master/tools/macosx'
make[2]: Entering directory '/home/ubuntu/Downloads/fuse-ext2-master/tools'
make[3]: Entering directory '/home/ubuntu/Downloads/fuse-ext2-master/tools'
make[3]: Nothing to be done for 'install-exec-am'.
make[3]: Nothing to be done for 'install-data-am'.
make[3]: Leaving directory '/home/ubuntu/Downloads/fuse-ext2-master/tools'
make[2]: Leaving directory '/home/ubuntu/Downloads/fuse-ext2-master/tools'
make[1]: Leaving directory '/home/ubuntu/Downloads/fuse-ext2-master/tools'
make[1]: Entering directory '/home/ubuntu/Downloads/fuse-ext2-master'
make[2]: Enteriize: Consider adding '-I m4' to ACLOCAL_AMFLAGS in Makefile.am.
autoreconf: running: /usr/bin/autoconf --force
autoreconf: running: /usr/bin/autoheader --force
autoreconf: running: automake --add-missing --copy --force-missing
configure.ac:10: installing './compile'
configure.ac:4: installing './missing'
fuse-ext2/Makefile.am: installing './depcomp'
autoreconf: Leaving directory `.'
Removing autom4te.cache
ubuntu@ubuntu:~/Downloads/fuse-ext2-master$ ./configure
checking build system type... x86_64-pc-linux-gnu
checking host system type... x86_64-pc-linux-gnu
checking targeng directory '/home/ubuntu/Downloads/fuse-ext2-master'
make[2]: Nothing to be done for 'install-exec-am'.
 /usr/bin/mkdir -p '/usr/local/share/man/man1'
 /usr/bin/install -c -m 644 fuse-ext2.1 '/usr/local/share/man/man1'
 /usr/bin/mkdir -p '/usr/local/lib/pkgconfig'
 /usr/bin/install -c -m 644 fuse-ext2.pc '/usr/local/lib/pkgconfig'
make[2]: Leaving directory '/home/ubuntu/Downloads/fuse-ext2-master'
make[1]: Leaving directory '/home/ubuntu/Downloads/fuse-ext2-master'
ux-gnu
checking for a BSD-compatible install... /usr/bin/install -c
checking whether build environment is sane... yes
checking for a thread-safe mkdir -p... /usr/bin/mkdir -p
checking for gawk... gawk
checking whether make sets $(MAKE)... yes
checking whether make supports nested variables... yes
checking for g++... g++
checking whether the C++ compiler works... yes
checking for C++ compiler default output file name... a.out
checking for suffix of executables... 
checking whether we are cross compiling... no
checking for suffix of object files... o
checking whether we are using the GNU C++ compiler... yes
checking whether g++ accepts -g... yes
checking whether make supports the include directive... yes (GNU style)
checking dependency style of g++... gcc3
checking for gawk... (cached) gawk
checking for gcc... gcc
checking whether we are using the GNU C compiler... yes
checking whether gcc accepts -g... yes
checking for gcc option to accept ISO C89... none needed
checking whether gcc understands -c and -o together... yes
checking dependency style of gcc... gcc3
checking for ar... ar
checking the archiver (ar) interface... ar
checking for gcc... gcc
checking whether we are using the GNU Objective C compiler... no
checking whether gcc accepts -g... no
checking dependency style of gcc... gcc3
checking how to print strings... printf
checking for a sed that does not truncate output... /usr/bin/sed
checking for grep that handles long lines and -e... /usr/bin/grep
checking for egrep... /usr/bin/grep -E
checking for fgrep... /usr/bin/grep -F
checking for ld used by gcc... /usr/bin/ld
checking if the linker (/usr/bin/ld) is GNU ld... yes
checking foize: Consider adding '-I m4' to ACLOCAL_AMFLAGS in Makefile.am.
autoreconf: running: /usr/bin/autoconf --force
autoreconf: running: /usr/bin/autoheader --force
autoreconf: running: automake --add-missing --copy --force-missing
configure.ac:10: installing './compile'
configure.ac:4: installing './missing'
fuse-ext2/Makefile.am: installing './depcomp'
autoreconf: Leaving directory `.'
Removing autom4te.cache
ubuntu@ubuntu:~/Downloads/fuse-ext2-master$ ./configure
checking build system type... x86_64-pc-linux-gnu
checking host system type... x86_64-pc-linux-gnu
checking targer BSD- or MS-compatible name lister (nm)... /usr/bin/nm -B
checking the name lister (/usr/bin/nm -B) interface... BSD nm
checking whether ln -s works... yes
checking the maximum length of command line arguments... 1572864
checking how to convert x86_64-pc-linux-gnu file names to x86_64-pc-linux-gnu format... func_convert_file_noop
checking how to convert x86_64-pc-linux-gnu file names to toolchain format... func_convert_file_noop
checking for /usr/bin/ld option to reload object files... -r
checking for objdump... objdump
checking how to recognize dependent libraries... pass_all
checking for dlltool... no
checking how to associate runtime and link libraries... printf %s\n
checking for archiver @FILE support... @
checking for strip... strip
checking for ranlib... ranlib
checking command to parse /usr/bin/nm -B output from gcc object... ok
checking for sysroot... no
checking for a working dd... /usr/bin/dd
checking how to truncate binary pipes... /usr/bin/dd bs=4096 count=1
checking for mt... mt
checking if mt is a manifest tool... no
checking how to run the C preprocessor... gcc -E
checking for ANSI C header files... yes
checking for sys/types.h... yes
checking for sys/stat.h... yes
checking for stdlib.h... yes
checking for string.h... yes
checking for memory.h... yes
checking for strings.h... yes
checking for inttypes.h... yes
checking for stdint.h... yes
checking for unistd.h... yes
checking for dlfcn.h... yes
checking for objdir... .libs
checking if gcc supports -fno-rtti -fno-exceptions... no
checking for gcc option to produce PIC... -fPIC -DPIC
checking if gcc PIC flag -fPIC -DPIC works... yes
checking if gcc static flag -static works... yes
checking if gcc supports -c -o file.o... yes
checking if gcc supports -c -o file.o... (cached) yes
checking whether the gcc linker (/usr/bin/ld -m elf_x86_64) supports shared libraries... yes
checking whether -lc should be explicitly linked in... no
checking dynamic linker characteristics... GNU/Linux ld.so
checking how to hardcode library paths into programs... immediate
checking whether stripping libraries is possible... yes
checking if libtool supports shared libraries... yes
checking whether to build shared libraries... yes
checking whether to build static libraries... yes
checking how to run the C++ preprocessor... g++ -E
checking for ld used by g++... /usr/bin/ld -m elf_x86_64
checking if the linker (/usr/bin/ld -m elf_x86_64) is GNU ld... yes
checking whether the g++ linker (/usr/bin/ld -m elf_x86_64) supports shared libraries... yes
checking for g++ option to produce PIC... -fPIC -DPIC
checking if g++ PIC flag -fPIC -DPIC works... yes
checking if g++ static flag -static works... yes
checking if g++ supports -c -o file.o... yes
checking if g++ supports -c -o file.o... (cached) yes
checking whether the g++ linker (/usr/bin/ld -m elf_x86_64) supports shared libraries... yes
checking dynamic linker characteristics... (cached) GNU/Linux ld.so
checking how to hardcode library paths into programs... immediate
checking for chmod... /usr/bin/chmod
checking for size_t... yes
checking for off_t... yes
checking for dirent.h that defines DIR... yes
checking for library containing opendir... none required
checking for ANSI C header files... (cached) yes
checking whether sys/types.h defines makedev... no
checking sys/mkdev.h usability... no
checking sys/mkdev.h presence... no
checking for sys/mkdev.h... no
checking sys/sysmacros.h usability... yes
checking sys/sysmacros.h presence... yes
checking for sys/sysmacros.h... yes
checking fcntl.h usability... yes
checking fcntl.h presence... yes
checking for fcntl.h... yes
checking malloc.h usability... yes
checking malloc.h presence... yes
checking for malloc.h... yes
checking mntent.h usability... yes
checking mntent.h presence... yes
checking for mntent.h... yes
checking netinet/in.h usability... yes
checking netinet/in.h presence... yes
checking for netinet/in.h... yes
checking paths.h usability... yes
checking paths.h presence... yes
checking for paths.h... yes
checking stddef.h usability... yes
checking stddef.h presence... yes
checking for stddef.h... yes
checking for stdlib.h... (cached) yes
checking for string.h... (cached) yes
checking linux/fd.h usability... yes
checking linux/fd.h presence... yes
checking for linux/fd.h... yes
checking sys/file.h usability... yes
checking sys/file.h presence... yes
checking for sys/file.h... yes
checking sys/ioctl.h usability... yes
checking sys/ioctl.h presence... yes
checking for sys/ioctl.h... yes
checking sys/mount.h usability... yes
checking sys/mount.h presence... yes
checking for sys/mount.h... yes
checking sys/param.h usability... yes
checking sys/param.h presence... yes
checking for sys/param.h... yes
checking sys/statvfs.h usability... yes
checking sys/statvfs.h presence... yes
checking for sys/statvfs.h... yes
checking sys/time.h usability... yes
checking sys/time.h presence... yes
checking for sys/time.h... yes
checking for sys/types.h... (cached) yes
checking for sys/stat.h... (cached) yes
checking for sys/mkdev.h... (cached) no
checking for sys/ioctl.h... (cached) yes
checking sys/syscall.h usability... yes
checking sys/syscall.h presence... yes
checking for sys/syscall.h... yes
checking sys/resource.h usability... yes
checking sys/resource.h presence... yes
checking for sys/resource.h... yes
checking sys/mman.h usability... yes
checking sys/mman.h presence... yes
checking for sys/mman.h... yes
checking sys/prctl.h usability... yes
checking sys/prctl.h presence... yes
checking for sys/prctl.h... yes
checking sys/disklabel.h usability... no
checking sys/disklabel.h presence... no
checking for sys/disklabel.h... no
checking sys/queue.h usability... yes
checking sys/queue.h presence... yes
checking for sys/queue.h... yes
checking sys/socket.h usability... yes
checking sys/socket.h presence... yes
checking for sys/socket.h... yes
checking sys/un.h usability... yes
checking sys/un.h presence... yes
checking for sys/un.h... yes
checking sys/sockio.h usability... no
checking sys/sockio.h presence... no
checking for sys/sockio.h... no
checking net/if.h usability... yes
checking net/if.h presence... yes
checking for net/if.h... yes
checking for netinet/in.h... (cached) yes
checking net/if_dl.h usability... no
checking net/if_dl.h presence... no
checking for net/if_dl.h... no
checking errno.h usability... yes
checking errno.h presence... yes
checking for errno.h... yes
checking for unistd.h... (cached) yes
checking utime.h usability... yes
checking utime.h presence... yes
checking for utime.h... yes
checking getopt.h usability... yes
checking getopt.h presence... yes
checking for getopt.h... yes
checking for inttypes.h... (cached) yes
checking for sys/disk.h... no
checking for sys/mount.h... (cached) yes
checking for an ANSI C-conforming const... yes
checking for inline... inline
checking for mode_t... yes
checking for off_t... (cached) yes
checking for size_t... (cached) yes
checking for ssize_t... yes
checking for struct stat.st_blksize... yes
checking for struct stat.st_blocks... yes
checking for struct stat.st_rdev... yes
checking whether time.h and sys/time.h may both be included... yes
checking whether llseek is declared... no
checking whether lseek64 is declared... yes
checking for ssize_t... (cached) yes
checking for vprintf... yes
checking for _doprnt... no
checking for uid_t in sys/types.h... yes
checking for unistd.h... (cached) yes
checking for working chown... yes
checking whether closedir returns void... no
checking for library containing getmntent... none required
checking whether gcc needs -traditional... no
checking for stdlib.h... (cached) yes
checking for GNU libc compatible malloc... yes
checking for working memcmp... yes
checking for stdlib.h... (cached) yes
checking for unisize: Consider adding '-I m4' to ACLOCAL_AMFLAGS in Makefile.am.
autoreconf: running: /usr/bin/autoconf --force
autoreconf: running: /usr/bin/autoheader --force
autoreconf: running: automake --add-missing --copy --force-missing
configure.ac:10: installing './compile'
configure.ac:4: installing './missing'
fuse-ext2/Makefile.am: installing './depcomp'
autoreconf: Leaving directory `.'
Removing autom4te.cache
ubuntu@ubuntu:~/Downloads/fuse-ext2-master$ ./configure
checking build system type... x86_64-pc-linux-gnu
checking host system type... x86_64-pc-linux-gnu
checking targetd.h... (cached) yes
checking for sys/param.h... (cached) yes
checking for utime.h... (cached) yes
checking for getpagesize... yes
checking for working mmap... yes
checking for stdlib.h... (cached) yes
checking for GNU libc compatible realloc... yes
checking sys/select.h usability... yes
checking sys/select.h presence... yes
checking for sys/select.h... yes
checking for sys/socket.h... (cached) yes
checking types of arguments for select... int,fd_set *,struct timeval *
checking whether lstat correctly handles trailing slash... yes
checking whether stat accepts an empty string... no
checking whether utime accepts a null argument... yes
checking for ftruncate... yes
checking for getmntent... (cached) yes
checking for getmntinfo... no
checking for getpagesize... (cached) yes
checking for hasmntopt... yes
checking for memmove... yes
checking for memset... yes
checking for munmap... yes
checking for random... yes
checking for select... yes
checking for srand... yes
checking for srandom... yes
checking for strcasecmp... yes
checking for strchr... yes
checking for strdup... yes
checking for strerror... yes
checking for strrchr... yes
checking for strtol... yes
checking for strtoul... yes
checking for strtoull... yes
checking for uname... yes
checking for utime... yes
checking for llseek... no
checking for lseek64... yes
checking for library containing sem_post... -lpthread
checking for library containing fuse_main... -lfuse
checking for library containing com_err... -lcom_err
checking for library containing ext2fs_open... -lext2fs
checking if FUSE on this system is too new for us... yes
Disabling debug support by default
checking that generated files are newer than configure... done
configure: creating ./config.status
config.status: creating fuse-ext2.pc
config.status: creating Makefile
config.status: creating fuse-ext2/Makefile
config.status: creating tools/Makefile
config.status: creating tools/macosx/Makefile
config.status: creating config.h
config.status: executing depfiles commands
config.status: executing libtool commands
ubuntu@ubuntu:~/Downloads/fuse-ext2-master$ make
make  all-recursive
make[1]: Entering directory '/home/ubuntu/Downloads/fuse-ext2-master'
Making all in fuse-ext2
make[2]: Entering directory '/home/ubuntu/Downloads/fuse-ext2-master/fuse-ext2'
gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -I/usr/local/include  -g -O2 -MT fuse_ext2-fuse-ext2.o -MD -MP -MF .deps/fuse_ext2-fuse-ext2.Tpo -c -o fuse_ext2-fuse-ext2.o `test -f 'fuse-ext2.c' || echo './'`fuse-ext2.c
mv -f .deps/fuse_ext2-fuse-ext2.Tpo .deps/fuse_ext2-fuse-ext2.Po
gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -I/usr/local/include  -g -O2 -MT fuse_ext2-do_probe.o -MD -MP -MF .deps/fuse_ext2-do_probe.Tpo -c -o fuse_ext2-do_probe.o `test -f 'do_probe.c' || echo './'`do_probe.c
mv -f .deps/fuse_ext2-do_probe.Tpo .deps/fuse_ext2-do_probe.Po
gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -I/usr/local/include  -g -O2 -MT fuse_ext2-do_check.o -MD -MP -MF .deps/fuse_ext2-do_check.Tpo -c -o fuse_ext2-do_check.o `test -f 'do_check.c' || echo './'`do_check.c
mv -f .deps/fuse_ext2-do_check.Tpo .deps/fuse_ext2-do_check.Po
gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -I/usr/local/include  -g -O2 -MT fuse_ext2-do_fillstatbuf.o -MD -MP -MF .deps/fuse_ext2-do_fillstatbuf.Tpo -c -o fuse_ext2-do_fillstatbuf.o `test -f 'do_fillstatbuf.c' || echo './'`do_fillstatbuf.c
mv -f .deps/fuse_ext2-do_fillstatbuf.Tpo .deps/fuse_ext2-do_fillstatbuf.Po
gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -I/usr/local/include  -g -O2 -MT fuse_ext2-do_readinode.o -MD -MP -MF .deps/fuse_ext2-do_readinode.Tpo -c -o fuse_ext2-do_readinode.o `test -f 'do_readinode.c' || echo './'`do_readinode.c
mv -f .deps/fuse_ext2-do_readinode.Tpo .deps/fuse_ext2-do_readinode.Po
gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -I/usr/local/include  -g -O2 -MT fuse_ext2-do_writeinode.o -MD -MP -MF .deps/fuse_ext2-do_writeinode.Tpo -c -o fuse_ext2-do_writeinode.o `test -f 'do_writeinode.c' || echo './'`do_writeinode.c
mv -f .deps/fuse_ext2-do_writeinode.Tpo .deps/fuse_ext2-do_writeinode.Po
gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -I/usr/local/include  -g -O2 -MT fuse_ext2-do_killfilebyinode.o -MD -MP -MF .deps/fuse_ext2-do_killfilebyinode.Tpo -c -o fuse_ext2-do_killfilebyinode.o `test -f 'do_killfilebyinode.c' || echo './'`do_killfilebyinode.c
mv -f .deps/fuse_ext2-do_killfilebyinode.Tpo .deps/fuse_ext2-do_killfilebyinode.Po
gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -I/usr/local/include  -g -O2 -MT fuse_ext2-op_init.o -MD -MP -MF .deps/fuse_ext2-op_init.Tpo -c -o fuse_ext2-op_init.o `test -f 'op_init.c' || echo './'`op_init.c
mv -f .deps/fuse_ext2-op_init.Tpo .deps/fuse_ext2-op_init.Po
gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -I/usr/local/include  -g -O2 -MT fuse_ext2-op_destroy.o -MD -MP -MF .deps/fuse_ext2-op_destroy.Tpo -c -o fuse_ext2-op_destroy.o `test -f 'op_destroy.c' || echo './'`op_destroy.c
mv -f .deps/fuse_ext2-op_destroy.Tpo .deps/fuse_ext2-op_destroy.Po
gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -I/usr/local/include  -g -O2 -MT fuse_ext2-op_access.o -MD -MP -MF .deps/fuse_ext2-op_access.Tpo -c -o fuse_ext2-op_access.o `test -f 'op_access.c' || echo './'`op_access.c
mv -f .deps/fuse_ext2-op_access.Tpo .deps/fuse_ext2-op_access.Po
gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -I/usr/local/include  -g -O2 -MT fuse_ext2-op_fgetattr.o -MD -MP -MF .deps/fuse_ext2-op_fgetattr.Tpo -c -o fuse_ext2-op_fgetattr.o `test -f 'op_fgetattr.c' || echo './'`op_fgetattr.c
mv -f .deps/fuse_ext2-op_fgetattr.Tpo .deps/fuse_ext2-op_fgetattr.Po
gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -I/usr/local/include  -g -O2 -MT fuse_ext2-op_getattr.o -MD -MP -MF .deps/fuse_ext2-op_getattr.Tpo -c -o fuse_ext2-op_getattr.o `test -f 'op_getattr.c' || echo './'`op_getattr.c
mv -f .deps/fuse_ext2-op_getattr.Tpo .deps/fuse_ext2-op_getattr.Po
gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -I/usr/local/include  -g -O2 -MT fuse_ext2-op_getxattr.o -MD -MP -MF .deps/fuse_ext2-op_getxattr.Tpo -c -o fuse_ext2-op_getxattr.o `test -f 'op_getxattr.c' || echo './'`op_getxattr.c
mv -f .deps/fuse_ext2-op_getxattr.Tpo .deps/fuse_ext2-op_getxattr.Po
gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -I/usr/local/include  -g -O2 -MT fuse_ext2-op_open.o -MD -MP -MF .deps/fuse_ext2-op_open.Tpo -c -o fuse_ext2-op_open.o `test -f 'op_open.c' || echo './'`op_open.c
mv -f .deps/fuse_ext2-op_open.Tpo .deps/fuse_ext2-op_open.Po
gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -I/usr/local/include  -g -O2 -MT fuse_ext2-op_read.o -MD -MP -MF .deps/fuse_ext2-op_read.Tpo -c -o fuse_ext2-op_read.o `test -f 'op_read.c' || echo './'`op_read.c
mv -f .deps/fuse_ext2-op_read.Tpo .deps/fuse_ext2-op_read.Po
gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -I/usr/local/include  -g -O2 -MT fuse_ext2-op_readdir.o -MD -MP -MF .deps/fuse_ext2-op_readdir.Tpo -c -o fuse_ext2-op_readdir.o `test -f 'op_readdir.c' || echo './'`op_readdir.c
mv -f .deps/fuse_ext2-op_readdir.Tpo .deps/fuse_ext2-op_readdir.Po
gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -I/usr/local/include  -g -O2 -MT fuse_ext2-op_readlink.o -MD -MP -MF .deps/fuse_ext2-op_readlink.Tpo -c -o fuse_ext2-op_readlink.o `test -f 'op_readlink.c' || echo './'`op_readlink.c
mv -f .deps/fuse_ext2-op_readlink.Tpo .deps/fuse_ext2-op_readlink.Po
gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -I/usr/local/include  -g -O2 -MT fuse_ext2-op_release.o -MD -MP -MF .deps/fuse_ext2-op_release.Tpo -c -o fuse_ext2-op_release.o `test -f 'op_release.c' || echo './'`op_release.c
mv -f .deps/fuse_ext2-op_release.Tpo .deps/fuse_ext2-op_release.Po
gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -I/usr/local/include  -g -O2 -MT fuse_ext2-op_statfs.o -MD -MP -MF .deps/fuse_ext2-op_statfs.Tpo -c -o fuse_ext2-op_statfs.o `test -f 'op_statfs.c' || echo './'`op_statfs.c
mv -f .deps/fuse_ext2-op_statfs.Tpo .deps/fuse_ext2-op_statfs.Po
gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -I/usr/local/include  -g -O2 -MT fuse_ext2-op_chown.o -MD -MP -MF .deps/fuse_ext2-op_chown.Tpo -c -o fuse_ext2-op_chown.o `test -f 'op_chown.c' || echo './'`op_chown.c
mv -f .deps/fuse_ext2-op_chown.Tpo .deps/fuse_ext2-op_chown.Po
gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -I/usr/local/include  -g -O2 -MT fuse_ext2-op_chmod.o -MD -MP -MF .deps/fuse_ext2-op_chmod.Tpo -c -o fuse_ext2-op_chmod.o `test -f 'op_chmod.c' || echo './'`op_chmod.c
mv -f .deps/fuse_ext2-op_chmod.Tpo .deps/fuse_ext2-op_chmod.Po
gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -I/usr/local/include  -g -O2 -MT fuse_ext2-op_create.o -MD -MP -MF .deps/fuse_ext2-op_create.Tpo -c -o fuse_ext2-op_create.o `test -f 'op_create.c' || echo './'`op_create.c
mv -f .deps/fuse_ext2-op_create.Tpo .deps/fuse_ext2-op_create.Po
gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -I/usr/local/include  -g -O2 -MT fuse_ext2-op_flush.o -MD -MP -MF .deps/fuse_ext2-op_flush.Tpo -c -o fuse_ext2-op_flush.o `test -f 'op_flush.c' || echo './'`op_flush.c
mv -f .deps/fuse_ext2-op_flush.Tpo .deps/fuse_ext2-op_flush.Po
gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -I/usr/local/include  -g -O2 -MT fuse_ext2-op_fsync.o -MD -MP -MF .deps/fuse_ext2-op_fsync.Tpo -c -o fuse_ext2-op_fsync.o `test -f 'op_fsync.c' || echo './'`op_fsync.c
mv -f .deps/fuse_ext2-op_fsync.Tpo .deps/fuse_ext2-op_fsync.Po
gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -I/usr/local/include  -g -O2 -MT fuse_ext2-op_mkdir.o -MD -MP -MF .deps/fuse_ext2-op_mkdir.Tpo -c -o fuse_ext2-op_mkdir.o `test -f 'op_mkdir.c' || echo './'`op_mkdir.c
mv -f .deps/fuse_ext2-op_mkdir.Tpo .deps/fuse_ext2-op_mkdir.Po
gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -I/usr/local/include  -g -O2 -MT fuse_ext2-op_rmdir.o -MD -MP -MF .deps/fuse_ext2-op_rmdir.Tpo -c -o fuse_ext2-op_rmdir.o `test -f 'op_rmdir.c' || echo './'`op_rmdir.c
mv -f .deps/fuse_ext2-op_rmdir.Tpo .deps/fuse_ext2-op_rmdir.Po
gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -I/usr/local/include  -g -O2 -MT fuse_ext2-op_unlink.o -MD -MP -MF .deps/fuse_ext2-op_unlink.Tpo -c -o fuse_ext2-op_unlink.o `test -f 'op_unlink.c' || echo './'`op_unlink.c
mv -f .deps/fuse_ext2-op_unlink.Tpo .deps/fuse_ext2-op_unlink.Po
gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -I/usr/local/include  -g -O2 -MT fuse_ext2-op_utimens.o -MD -MP -MF .deps/fuse_ext2-op_utimens.Tpo -c -o fuse_ext2-op_utimens.o `test -f 'op_utimens.c' || echo './'`op_utimens.c
mv -f .deps/fuse_ext2-op_utimens.Tpo .deps/fuse_ext2-op_utimens.Po
gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -I/usr/local/include  -g -O2 -MT fuse_ext2-op_write.o -MD -MP -MF .deps/fuse_ext2-op_write.Tpo -c -o fuse_ext2-op_write.o `test -f 'op_write.c' || echo './'`op_write.c
mv -f .deps/fuse_ext2-op_write.Tpo .deps/fuse_ext2-op_write.Po
gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -I/usr/local/include  -g -O2 -MT fuse_ext2-op_mknod.o -MD -MP -MF .deps/fuse_ext2-op_mknod.Tpo -c -o fuse_ext2-op_mknod.o `test -f 'op_mknod.c' || echo './'`op_mknod.c
mv -f .deps/fuse_ext2-op_mknod.Tpo .deps/fuse_ext2-op_mknod.Po
gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -I/usr/local/include  -g -O2 -MT fuse_ext2-op_symlink.o -MD -MP -MF .deps/fuse_ext2-op_symlink.Tpo -c -o fuse_ext2-op_symlink.o `test -f 'op_symlink.c' || echo './'`op_symlink.c
mv -f .deps/fuse_ext2-op_symlink.Tpo .deps/fuse_ext2-op_symlink.Po
gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -I/usr/local/include  -g -O2 -MT fuse_ext2-op_truncate.o -MD -MP -MF .deps/fuse_ext2-op_truncate.Tpo -c -o fuse_ext2-op_truncate.o `test -f 'op_truncate.c' || echo './'`op_truncate.c
mv -f .deps/fuse_ext2-op_truncate.Tpo .deps/fuse_ext2-op_truncate.Po
gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -I/usr/local/include  -g -O2 -MT fuse_ext2-op_link.o -MD -MP -MF .deps/fuse_ext2-op_link.Tpo -c -o fuse_ext2-op_link.o `test -f 'op_link.c' || echo './'`op_link.c
mv -f .deps/fuse_ext2-op_link.Tpo .deps/fuse_ext2-op_link.Po
gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -I/usr/local/include  -g -O2 -MT fuse_ext2-op_rename.o -MD -MP -MF .deps/fuse_ext2-op_rename.Tpo -c -o fuse_ext2-op_rename.o `test -f 'op_rename.c' || echo './'`op_rename.c
mv -f .deps/fuse_ext2-op_rename.Tpo .deps/fuse_ext2-op_rename.Po
/bin/bash ../libtool  --tag=CC   --mode=link gcc -Wall -DHAVE_CONFIG_H -I/usr/local/include  -g -O2   -o fuse-ext2 fuse_ext2-fuse-ext2.o fuse_ext2-do_probe.o fuse_ext2-do_check.o fuse_ext2-do_fillstatbuf.o fuse_ext2-do_readinode.o fuse_ext2-do_writeinode.o fuse_ext2-do_killfilebyinode.o fuse_ext2-op_init.o fuse_ext2-op_destroy.o fuse_ext2-op_access.o fuse_ext2-op_fgetattr.o fuse_ext2-op_getattr.o fuse_ext2-op_getxattr.o fuse_ext2-op_open.o fuse_ext2-op_read.o fuse_ext2-op_readdir.o fuse_ext2-op_readlink.o fuse_ext2-op_release.o fuse_ext2-op_statfs.o fuse_ext2-op_chown.o fuse_ext2-op_chmod.o fuse_ext2-op_create.o fuse_ext2-op_flush.o fuse_ext2-op_fsync.o fuse_ext2-op_mkdir.o fuse_ext2-op_rmdir.o fuse_ext2-op_unlink.o fuse_ext2-op_utimens.o fuse_ext2-op_write.o fuse_ext2-op_mknod.o fuse_ext2-op_symlink.o fuse_ext2-op_truncate.o fuse_ext2-op_link.o fuse_ext2-op_rename.o  -lext2fs -lcom_err -lfuse -lpthread 
libtool: link: gcc -Wall -DHAVE_CONFIG_H -I/usr/local/include -g -O2 -o fuse-ext2 fuse_ext2-fuse-ext2.o fuse_ext2-do_probe.o fuse_ext2-do_check.o fuse_ext2-do_fillstatbuf.o fuse_ext2-do_readinode.o fuse_ext2-do_writeinode.o fuse_ext2-do_killfilebyinode.o fuse_ext2-op_init.o fuse_ext2-op_destroy.o fuse_ext2-op_access.o fuse_ext2-op_fgetattr.o fuse_ext2-op_getattr.o fuse_ext2-op_getxattr.o fuse_ext2-op_open.o fuse_ext2-op_read.o fuse_ext2-op_readdir.o fuse_ext2-op_readlink.o fuse_ext2-op_release.o fuse_ext2-op_statfs.o fuse_ext2-op_chown.o fuse_ext2-op_chmod.o fuse_ext2-op_create.o fuse_ext2-op_flush.o fuse_ext2-op_fsync.o fuse_ext2-op_mkdir.o fuse_ext2-op_rmdir.o fuse_ext2-op_unlink.o fuse_ext2-op_utimens.o fuse_ext2-op_write.o fuse_ext2-op_mknod.o fuse_ext2-op_symlink.o fuse_ext2-op_truncate.o fuse_ext2-op_link.o fuse_ext2-op_rename.o  -lext2fs -lcom_err -lfuse -lpthread
gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -I/usr/local/include  -g -O2 -MT fuse_ext2_probe-fuse-ext2.probe.o -MD -MP -MF .deps/fuse_ext2_probe-fuse-ext2.probe.Tpo -c -o fuse_ext2_probe-fuse-ext2.probe.o `test -f 'fuse-ext2.probe.c' || echo './'`fuse-ext2.probe.c
mv -f .deps/fuse_ext2_probe-fuse-ext2.probe.Tpo .deps/fuse_ext2_probe-fuse-ext2.probe.Po
gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -I/usr/local/include  -g -O2 -MT fuse_ext2_probe-do_probe.o -MD -MP -MF .deps/fuse_ext2_probe-do_probe.Tpo -c -o fuse_ext2_probe-do_probe.o `test -f 'do_probe.c' || echo './'`do_probe.c
mv -f .deps/fuse_ext2_probe-do_probe.Tpo .deps/fuse_ext2_probe-do_probe.Po
/bin/bash ../libtool  --tag=CC   --mode=link gcc -Wall -DHAVE_CONFIG_H -I/usr/local/include  -g -O2   -o fuse-ext2.probe fuse_ext2_probe-fuse-ext2.probe.o fuse_ext2_probe-do_probe.o  -lext2fs -lcom_err -lfuse -lpthread 
libtool: link: gcc -Wall -DHAVE_CONFIG_H -I/usr/local/include -g -O2 -o fuse-ext2.probe fuse_ext2_probe-fuse-ext2.probe.o fuse_ext2_probe-do_probe.o  -lext2fs -lcom_err -lfuse -lpthread
/bin/bash ../libtool  --tag=CC   --mode=compile gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE  -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-fuse-ext2.lo -MD -MP -MF .deps/umfuseext2_la-fuse-ext2.Tpo -c -o umfuseext2_la-fuse-ext2.lo `test -f 'fuse-ext2.c' || echo './'`fuse-ext2.c
libtool: compile:  gcc -DHAVE_CONFIG_H -I. -I.. -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-fuse-ext2.lo -MD -MP -MF .deps/umfuseext2_la-fuse-ext2.Tpo -c fuse-ext2.c  -fPIC -DPIC -o .libs/umfuseext2_la-fuse-ext2.o
libtool: compile:  gcc -DHAVE_CONFIG_H -I. -I.. -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-fuse-ext2.lo -MD -MP -MF .deps/umfuseext2_la-fuse-ext2.Tpo -c fuse-ext2.c -o umfuseext2_la-fuse-ext2.o >/dev/null 2>&1
mv -f .deps/umfuseext2_la-fuse-ext2.Tpo .deps/umfuseext2_la-fuse-ext2.Plo
/bin/bash ../libtool  --tag=CC   --mode=compile gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE  -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-do_probe.lo -MD -MP -MF .deps/umfuseext2_la-do_probe.Tpo -c -o umfuseext2_la-do_probe.lo `test -f 'do_probe.c' || echo './'`do_probe.c
libtool: compile:  gcc -DHAVE_CONFIG_H -I. -I.. -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-do_probe.lo -MD -MP -MF .deps/umfuseext2_la-do_probe.Tpo -c do_probe.c  -fPIC -DPIC -o .libs/umfuseext2_la-do_probe.o
libtool: compile:  gcc -DHAVE_CONFIG_H -I. -I.. -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-do_probe.lo -MD -MP -MF .deps/umfuseext2_la-do_probe.Tpo -c do_probe.c -o umfuseext2_la-do_probe.o >/dev/null 2>&1
mv -f .deps/umfuseext2_la-do_probe.Tpo .deps/umfuseext2_la-do_probe.Plo
/bin/bash ../libtool  --tag=CC   --mode=compile gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE  -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-do_check.lo -MD -MP -MF .deps/umfuseext2_la-do_check.Tpo -c -o umfuseext2_la-do_check.lo `test -f 'do_check.c' || echo './'`do_check.c
libtool: compile:  gcc -DHAVE_CONFIG_H -I. -I.. -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-do_check.lo -MD -MP -MF .deps/umfuseext2_la-do_check.Tpo -c do_check.c  -fPIC -DPIC -o .libs/umfuseext2_la-do_check.o
libtool: compile:  gcc -DHAVE_CONFIG_H -I. -I.. -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-do_check.lo -MD -MP -MF .deps/umfuseext2_la-do_check.Tpo -c do_check.c -o umfuseext2_la-do_check.o >/dev/null 2>&1
mv -f .deps/umfuseext2_la-do_check.Tpo .deps/umfuseext2_la-do_check.Plo
/bin/bash ../libtool  --tag=CC   --mode=compile gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE  -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-do_fillstatbuf.lo -MD -MP -MF .deps/umfuseext2_la-do_fillstatbuf.Tpo -c -o umfuseext2_la-do_fillstatbuf.lo `test -f 'do_fillstatbuf.c' || echo './'`do_fillstatbuf.c
libtool: compile:  gcc -DHAVE_CONFIG_H -I. -I.. -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-do_fillstatbuf.lo -MD -MP -MF .deps/umfuseext2_la-do_fillstatbuf.Tpo -c do_fillstatbuf.c  -fPIC -DPIC -o .libs/umfuseext2_la-do_fillstatbuf.o
libtool: compile:  gcc -DHAVE_CONFIG_H -I. -I.. -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-do_fillstatbuf.lo -MD -MP -MF .deps/umfuseext2_la-do_fillstatbuf.Tpo -c do_fillstatbuf.c -o umfuseext2_la-do_fillstatbuf.o >/dev/null 2>&1
mv -f .deps/umfuseext2_la-do_fillstatbuf.Tpo .deps/umfuseext2_la-do_fillstatbuf.Plo
/bin/bash ../libtool  --tag=CC   --mode=compile gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE  -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-do_readinode.lo -MD -MP -MF .deps/umfuseext2_la-do_readinode.Tpo -c -o umfuseext2_la-do_readinode.lo `test -f 'do_readinode.c' || echo './'`do_readinode.c
libtool: compile:  gcc -DHAVE_CONFIG_H -I. -I.. -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-do_readinode.lo -MD -MP -MF .deps/umfuseext2_la-do_readinode.Tpo -c do_readinode.c  -fPIC -DPIC -o .libs/umfuseext2_la-do_readinode.o
libtool: compile:  gcc -DHAVE_CONFIG_H -I. -I.. -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-do_readinode.lo -MD -MP -MF .deps/umfuseext2_la-do_readinode.Tpo -c do_readinode.c -o umfuseext2_la-do_readinode.o >/dev/null 2>&1
mv -f .deps/umfuseext2_la-do_readinode.Tpo .deps/umfuseext2_la-do_readinode.Plo
/bin/bash ../libtool  --tag=CC   --mode=compile gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE  -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-do_writeinode.lo -MD -MP -MF .deps/umfuseext2_la-do_writeinode.Tpo -c -o umfuseext2_la-do_writeinode.lo `test -f 'do_writeinode.c' || echo './'`do_writeinode.c
libtool: compile:  gcc -DHAVE_CONFIG_H -I. -I.. -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-do_writeinode.lo -MD -MP -MF .deps/umfuseext2_la-do_writeinode.Tpo -c do_writeinode.c  -fPIC -DPIC -o .libs/umfuseext2_la-do_writeinode.o
libtool: compile:  gcc -DHAVE_CONFIG_H -I. -I.. -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-do_writeinode.lo -MD -MP -MF .deps/umfuseext2_la-do_writeinode.Tpo -c do_writeinode.c -o umfuseext2_la-do_writeinode.o >/dev/null 2>&1
mv -f .deps/umfuseext2_la-do_writeinode.Tpo .deps/umfuseext2_la-do_writeinode.Plo
/bin/bash ../libtool  --tag=CC   --mode=compile gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE  -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-do_killfilebyinode.lo -MD -MP -MF .deps/umfuseext2_la-do_killfilebyinode.Tpo -c -o umfuseext2_la-do_killfilebyinode.lo `test -f 'do_killfilebyinode.c' || echo './'`do_killfilebyinode.c
libtool: compile:  gcc -DHAVE_CONFIG_H -I. -I.. -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-do_killfilebyinode.lo -MD -MP -MF .deps/umfuseext2_la-do_killfilebyinode.Tpo -c do_killfilebyinode.c  -fPIC -DPIC -o .libs/umfuseext2_la-do_killfilebyinode.o
libtool: compile:  gcc -DHAVE_CONFIG_H -I. -I.. -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-do_killfilebyinode.lo -MD -MP -MF .deps/umfuseext2_la-do_killfilebyinode.Tpo -c do_killfilebyinode.c -o umfuseext2_la-do_killfilebyinode.o >/dev/null 2>&1
mv -f .deps/umfuseext2_la-do_killfilebyinode.Tpo .deps/umfuseext2_la-do_killfilebyinode.Plo
/bin/bash ../libtool  --tag=CC   --mode=compile gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE  -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_init.lo -MD -MP -MF .deps/umfuseext2_la-op_init.Tpo -c -o umfuseext2_la-op_init.lo `test -f 'op_init.c' || echo './'`op_init.c
libtool: compile:  gcc -DHAVE_CONFIG_H -I. -I.. -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_init.lo -MD -MP -MF .deps/umfuseext2_la-op_init.Tpo -c op_init.c  -fPIC -DPIC -o .libs/umfuseext2_la-op_init.o
libtool: compile:  gcc -DHAVE_CONFIG_H -I. -I.. -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_init.lo -MD -MP -MF .deps/umfuseext2_la-op_init.Tpo -c op_init.c -o umfuseext2_la-op_init.o >/dev/null 2>&1
mv -f .deps/umfuseext2_la-op_init.Tpo .deps/umfuseext2_la-op_init.Plo
/bin/bash ../libtool  --tag=CC   --mode=compile gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE  -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_destroy.lo -MD -MP -MF .deps/umfuseext2_la-op_destroy.Tpo -c -o umfuseext2_la-op_destroy.lo `test -f 'op_destroy.c' || echo './'`op_destroy.c
libtool: compile:  gcc -DHAVE_CONFIG_H -I. -I.. -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_destroy.lo -MD -MP -MF .deps/umfuseext2_la-op_destroy.Tpo -c op_destroy.c  -fPIC -DPIC -o .libs/umfuseext2_la-op_destroy.o
libtool: compile:  gcc -DHAVE_CONFIG_H -I. -I.. -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_destroy.lo -MD -MP -MF .deps/umfuseext2_la-op_destroy.Tpo -c op_destroy.c -o umfuseext2_la-op_destroy.o >/dev/null 2>&1
mv -f .deps/umfuseext2_la-op_destroy.Tpo .deps/umfuseext2_la-op_destroy.Plo
/bin/bash ../libtool  --tag=CC   --mode=compile gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE  -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_access.lo -MD -MP -MF .deps/umfuseext2_la-op_access.Tpo -c -o umfuseext2_la-op_access.lo `test -f 'op_access.c' || echo './'`op_access.c
libtool: compile:  gcc -DHAVE_CONFIG_H -I. -I.. -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_access.lo -MD -MP -MF .deps/umfuseext2_la-op_access.Tpo -c op_access.c  -fPIC -DPIC -o .libs/umfuseext2_la-op_access.o
libtool: compile:  gcc -DHAVE_CONFIG_H -I. -I.. -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_access.lo -MD -MP -MF .deps/umfuseext2_la-op_access.Tpo -c op_access.c -o umfuseext2_la-op_access.o >/dev/null 2>&1
mv -f .deps/umfuseext2_la-op_access.Tpo .deps/umfuseext2_la-op_access.Plo
/bin/bash ../libtool  --tag=CC   --mode=compile gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE  -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_fgetattr.lo -MD -MP -MF .deps/umfuseext2_la-op_fgetattr.Tpo -c -o umfuseext2_la-op_fgetattr.lo `test -f 'op_fgetattr.c' || echo './'`op_fgetattr.c
libtool: compile:  gcc -DHAVE_CONFIG_H -I. -I.. -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_fgetattr.lo -MD -MP -MF .deps/umfuseext2_la-op_fgetattr.Tpo -c op_fgetattr.c  -fPIC -DPIC -o .libs/umfuseext2_la-op_fgetattr.o
libtool: compile:  gcc -DHAVE_CONFIG_H -I. -I.. -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_fgetattr.lo -MD -MP -MF .deps/umfuseext2_la-op_fgetattr.Tpo -c op_fgetattr.c -o umfuseext2_la-op_fgetattr.o >/dev/null 2>&1
mv -f .deps/umfuseext2_la-op_fgetattr.Tpo .deps/umfuseext2_la-op_fgetattr.Plo
/bin/bash ../libtool  --tag=CC   --mode=compile gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE  -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_getattr.lo -MD -MP -MF .deps/umfuseext2_la-op_getattr.Tpo -c -o umfuseext2_la-op_getattr.lo `test -f 'op_getattr.c' || echo './'`op_getattr.c
libtool: compile:  gcc -DHAVE_CONFIG_H -I. -I.. -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_getattr.lo -MD -MP -MF .deps/umfuseext2_la-op_getattr.Tpo -c op_getattr.c  -fPIC -DPIC -o .libs/umfuseext2_la-op_getattr.o
libtool: compile:  gcc -DHAVE_CONFIG_H -I. -I.. -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_getattr.lo -MD -MP -MF .deps/umfuseext2_la-op_getattr.Tpo -c op_getattr.c -o umfuseext2_la-op_getattr.o >/dev/null 2>&1
mv -f .deps/umfuseext2_la-op_getattr.Tpo .deps/umfuseext2_la-op_getattr.Plo
/bin/bash ../libtool  --tag=CC   --mode=compile gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE  -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_getxattr.lo -MD -MP -MF .deps/umfuseext2_la-op_getxattr.Tpo -c -o umfuseext2_la-op_getxattr.lo `test -f 'op_getxattr.c' || echo './'`op_getxattr.c
libtool: compile:  gcc -DHAVE_CONFIG_H -I. -I.. -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_getxattr.lo -MD -MP -MF .deps/umfuseext2_la-op_getxattr.Tpo -c op_getxattr.c  -fPIC -DPIC -o .libs/umfuseext2_la-op_getxattr.o
libtool: compile:  gcc -DHAVE_CONFIG_H -I. -I.. -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_getxattr.lo -MD -MP -MF .deps/umfuseext2_la-op_getxattr.Tpo -c op_getxattr.c -o umfuseext2_la-op_getxattr.o >/dev/null 2>&1
mv -f .deps/umfuseext2_la-op_getxattr.Tpo .deps/umfuseext2_la-op_getxattr.Plo
/bin/bash ../libtool  --tag=CC   --mode=compile gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE  -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_open.lo -MD -MP -MF .deps/umfuseext2_la-op_open.Tpo -c -o umfuseext2_la-op_open.lo `test -f 'op_open.c' || echo './'`op_open.c
libtool: compile:  gcc -DHAVE_CONFIG_H -I. -I.. -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_open.lo -MD -MP -MF .deps/umfuseext2_la-op_open.Tpo -c op_open.c  -fPIC -DPIC -o .libs/umfuseext2_la-op_open.o
libtool: compile:  gcc -DHAVE_CONFIG_H -I. -I.. -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_open.lo -MD -MP -MF .deps/umfuseext2_la-op_open.Tpo -c op_open.c -o umfuseext2_la-op_open.o >/dev/null 2>&1
mv -f .deps/umfuseext2_la-op_open.Tpo .deps/umfuseext2_la-op_open.Plo
/bin/bash ../libtool  --tag=CC   --mode=compile gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE  -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_read.lo -MD -MP -MF .deps/umfuseext2_la-op_read.Tpo -c -o umfuseext2_la-op_read.lo `test -f 'op_read.c' || echo './'`op_read.c
libtool: compile:  gcc -DHAVE_CONFIG_H -I. -I.. -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_read.lo -MD -MP -MF .deps/umfuseext2_la-op_read.Tpo -c op_read.c  -fPIC -DPIC -o .libs/umfuseext2_la-op_read.o
libtool: compile:  gcc -DHAVE_CONFIG_H -I. -I.. -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_read.lo -MD -MP -MF .deps/umfuseext2_la-op_read.Tpo -c op_read.c -o umfuseext2_la-op_read.o >/dev/null 2>&1
mv -f .deps/umfuseext2_la-op_read.Tpo .deps/umfuseext2_la-op_read.Plo
/bin/bash ../libtool  --tag=CC   --mode=compile gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE  -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_readdir.lo -MD -MP -MF .deps/umfuseext2_la-op_readdir.Tpo -c -o umfuseext2_la-op_readdir.lo `test -f 'op_readdir.c' || echo './'`op_readdir.c
libtool: compile:  gcc -DHAVE_CONFIG_H -I. -I.. -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_readdir.lo -MD -MP -MF .deps/umfuseext2_la-op_readdir.Tpo -c op_readdir.c  -fPIC -DPIC -o .libs/umfuseext2_la-op_readdir.o
libtool: compile:  gcc -DHAVE_CONFIG_H -I. -I.. -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_readdir.lo -MD -MP -MF .deps/umfuseext2_la-op_readdir.Tpo -c op_readdir.c -o umfuseext2_la-op_readdir.o >/dev/null 2>&1
mv -f .deps/umfuseext2_la-op_readdir.Tpo .deps/umfuseext2_la-op_readdir.Plo
/bin/bash ../libtool  --tag=CC   --mode=compile gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE  -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_readlink.lo -MD -MP -MF .deps/umfuseext2_la-op_readlink.Tpo -c -o umfuseext2_la-op_readlink.lo `test -f 'op_readlink.c' || echo './'`op_readlink.c
libtool: compile:  gcc -DHAVE_CONFIG_H -I. -I.. -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_readlink.lo -MD -MP -MF .deps/umfuseext2_la-op_readlink.Tpo -c op_readlink.c  -fPIC -DPIC -o .libs/umfuseext2_la-op_readlink.o
libtool: compile:  gcc -DHAVE_CONFIG_H -I. -I.. -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_readlink.lo -MD -MP -MF .deps/umfuseext2_la-op_readlink.Tpo -c op_readlink.c -o umfuseext2_la-op_readlink.o >/dev/null 2>&1
mv -f .deps/umfuseext2_la-op_readlink.Tpo .deps/umfuseext2_la-op_readlink.Plo
/bin/bash ../libtool  --tag=CC   --mode=compile gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE  -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_release.lo -MD -MP -MF .deps/umfuseext2_la-op_release.Tpo -c -o umfuseext2_la-op_release.lo `test -f 'op_release.c' || echo './'`op_release.c
libtool: compile:  gcc -DHAVE_CONFIG_H -I. -I.. -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_release.lo -MD -MP -MF .deps/umfuseext2_la-op_release.Tpo -c op_release.c  -fPIC -DPIC -o .libs/umfuseext2_la-op_release.o
libtool: compile:  gcc -DHAVE_CONFIG_H -I. -I.. -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_release.lo -MD -MP -MF .deps/umfuseext2_la-op_release.Tpo -c op_release.c -o umfuseext2_la-op_release.o >/dev/null 2>&1
mv -f .deps/umfuseext2_la-op_release.Tpo .deps/umfuseext2_la-op_release.Plo
/bin/bash ../libtool  --tag=CC   --mode=compile gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE  -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_statfs.lo -MD -MP -MF .deps/umfuseext2_la-op_statfs.Tpo -c -o umfuseext2_la-op_statfs.lo `test -f 'op_statfs.c' || echo './'`op_statfs.c
libtool: compile:  gcc -DHAVE_CONFIG_H -I. -I.. -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_statfs.lo -MD -MP -MF .deps/umfuseext2_la-op_statfs.Tpo -c op_statfs.c  -fPIC -DPIC -o .libs/umfuseext2_la-op_statfs.o
libtool: compile:  gcc -DHAVE_CONFIG_H -I. -I.. -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_statfs.lo -MD -MP -MF .deps/umfuseext2_la-op_statfs.Tpo -c op_statfs.c -o umfuseext2_la-op_statfs.o >/dev/null 2>&1
mv -f .deps/umfuseext2_la-op_statfs.Tpo .deps/umfuseext2_la-op_statfs.Plo
/bin/bash ../libtool  --tag=CC   --mode=compile gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE  -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_chown.lo -MD -MP -MF .deps/umfuseext2_la-op_chown.Tpo -c -o umfuseext2_la-op_chown.lo `test -f 'op_chown.c' || echo './'`op_chown.c
libtool: compile:  gcc -DHAVE_CONFIG_H -I. -I.. -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_chown.lo -MD -MP -MF .deps/umfuseext2_la-op_chown.Tpo -c op_chown.c  -fPIC -DPIC -o .libs/umfuseext2_la-op_chown.o
libtool: compile:  gcc -DHAVE_CONFIG_H -I. -I.. -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_chown.lo -MD -MP -MF .deps/umfuseext2_la-op_chown.Tpo -c op_chown.c -o umfuseext2_la-op_chown.o >/dev/null 2>&1
mv -f .deps/umfuseext2_la-op_chown.Tpo .deps/umfuseext2_la-op_chown.Plo
/bin/bash ../libtool  --tag=CC   --mode=compile gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE  -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_chmod.lo -MD -MP -MF .deps/umfuseext2_la-op_chmod.Tpo -c -o umfuseext2_la-op_chmod.lo `test -f 'op_chmod.c' || echo './'`op_chmod.c
libtool: compile:  gcc -DHAVE_CONFIG_H -I. -I.. -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_chmod.lo -MD -MP -MF .deps/umfuseext2_la-op_chmod.Tpo -c op_chmod.c  -fPIC -DPIC -o .libs/umfuseext2_la-op_chmod.o
libtool: compile:  gcc -DHAVE_CONFIG_H -I. -I.. -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_chmod.lo -MD -MP -MF .deps/umfuseext2_la-op_chmod.Tpo -c op_chmod.c -o umfuseext2_la-op_chmod.o >/dev/null 2>&1
mv -f .deps/umfuseext2_la-op_chmod.Tpo .deps/umfuseext2_la-op_chmod.Plo
/bin/bash ../libtool  --tag=CC   --mode=compile gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE  -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_create.lo -MD -MP -MF .deps/umfuseext2_la-op_create.Tpo -c -o umfuseext2_la-op_create.lo `test -f 'op_create.c' || echo './'`op_create.c
libtool: compile:  gcc -DHAVE_CONFIG_H -I. -I.. -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_create.lo -MD -MP -MF .deps/umfuseext2_la-op_create.Tpo -c op_create.c  -fPIC -DPIC -o .libs/umfuseext2_la-op_create.o
libtool: compile:  gcc -DHAVE_CONFIG_H -I. -I.. -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_create.lo -MD -MP -MF .deps/umfuseext2_la-op_create.Tpo -c op_create.c -o umfuseext2_la-op_create.o >/dev/null 2>&1
mv -f .deps/umfuseext2_la-op_create.Tpo .deps/umfuseext2_la-op_create.Plo
/bin/bash ../libtool  --tag=CC   --mode=compile gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE  -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_flush.lo -MD -MP -MF .deps/umfuseext2_la-op_flush.Tpo -c -o umfuseext2_la-op_flush.lo `test -f 'op_flush.c' || echo './'`op_flush.c
libtool: compile:  gcc -DHAVE_CONFIG_H -I. -I.. -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_flush.lo -MD -MP -MF .deps/umfuseext2_la-op_flush.Tpo -c op_flush.c  -fPIC -DPIC -o .libs/umfuseext2_la-op_flush.o
libtool: compile:  gcc -DHAVE_CONFIG_H -I. -I.. -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_flush.lo -MD -MP -MF .deps/umfuseext2_la-op_flush.Tpo -c op_flush.c -o umfuseext2_la-op_flush.o >/dev/null 2>&1
mv -f .deps/umfuseext2_la-op_flush.Tpo .deps/umfuseext2_la-op_flush.Plo
/bin/bash ../libtool  --tag=CC   --mode=compile gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE  -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_fsync.lo -MD -MP -MF .deps/umfuseext2_la-op_fsync.Tpo -c -o umfuseext2_la-op_fsync.lo `test -f 'op_fsync.c' || echo './'`op_fsync.c
libtool: compile:  gcc -DHAVE_CONFIG_H -I. -I.. -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_fsync.lo -MD -MP -MF .deps/umfuseext2_la-op_fsync.Tpo -c op_fsync.c  -fPIC -DPIC -o .libs/umfuseext2_la-op_fsync.o
libtool: compile:  gcc -DHAVE_CONFIG_H -I. -I.. -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_fsync.lo -MD -MP -MF .deps/umfuseext2_la-op_fsync.Tpo -c op_fsync.c -o umfuseext2_la-op_fsync.o >/dev/null 2>&1
mv -f .deps/umfuseext2_la-op_fsync.Tpo .deps/umfuseext2_la-op_fsync.Plo
/bin/bash ../libtool  --tag=CC   --mode=compile gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE  -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_mkdir.lo -MD -MP -MF .deps/umfuseext2_la-op_mkdir.Tpo -c -o umfuseext2_la-op_mkdir.lo `test -f 'op_mkdir.c' || echo './'`op_mkdir.c
libtool: compile:  gcc -DHAVE_CONFIG_H -I. -I.. -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_mkdir.lo -MD -MP -MF .deps/umfuseext2_la-op_mkdir.Tpo -c op_mkdir.c  -fPIC -DPIC -o .libs/umfuseext2_la-op_mkdir.o
libtool: compile:  gcc -DHAVE_CONFIG_H -I. -I.. -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_mkdir.lo -MD -MP -MF .deps/umfuseext2_la-op_mkdir.Tpo -c op_mkdir.c -o umfuseext2_la-op_mkdir.o >/dev/null 2>&1
mv -f .deps/umfuseext2_la-op_mkdir.Tpo .deps/umfuseext2_la-op_mkdir.Plo
/bin/bash ../libtool  --tag=CC   --mode=compile gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE  -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_rmdir.lo -MD -MP -MF .deps/umfuseext2_la-op_rmdir.Tpo -c -o umfuseext2_la-op_rmdir.lo `test -f 'op_rmdir.c' || echo './'`op_rmdir.c
libtool: compile:  gcc -DHAVE_CONFIG_H -I. -I.. -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_rmdir.lo -MD -MP -MF .deps/umfuseext2_la-op_rmdir.Tpo -c op_rmdir.c  -fPIC -DPIC -o .libs/umfuseext2_la-op_rmdir.o
libtool: compile:  gcc -DHAVE_CONFIG_H -I. -I.. -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_rmdir.lo -MD -MP -MF .deps/umfuseext2_la-op_rmdir.Tpo -c op_rmdir.c -o umfuseext2_la-op_rmdir.o >/dev/null 2>&1
mv -f .deps/umfuseext2_la-op_rmdir.Tpo .deps/umfuseext2_la-op_rmdir.Plo
/bin/bash ../libtool  --tag=CC   --mode=compile gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE  -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_unlink.lo -MD -MP -MF .deps/umfuseext2_la-op_unlink.Tpo -c -o umfuseext2_la-op_unlink.lo `test -f 'op_unlink.c' || echo './'`op_unlink.c
libtool: compile:  gcc -DHAVE_CONFIG_H -I. -I.. -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_unlink.lo -MD -MP -MF .deps/umfuseext2_la-op_unlink.Tpo -c op_unlink.c  -fPIC -DPIC -o .libs/umfuseext2_la-op_unlink.o
libtool: compile:  gcc -DHAVE_CONFIG_H -I. -I.. -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_unlink.lo -MD -MP -MF .deps/umfuseext2_la-op_unlink.Tpo -c op_unlink.c -o umfuseext2_la-op_unlink.o >/dev/null 2>&1
mv -f .deps/umfuseext2_la-op_unlink.Tpo .deps/umfuseext2_la-op_unlink.Plo
/bin/bash ../libtool  --tag=CC   --mode=compile gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE  -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_utimens.lo -MD -MP -MF .deps/umfuseext2_la-op_utimens.Tpo -c -o umfuseext2_la-op_utimens.lo `test -f 'op_utimens.c' || echo './'`op_utimens.c
libtool: compile:  gcc -DHAVE_CONFIG_H -I. -I.. -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_utimens.lo -MD -MP -MF .deps/umfuseext2_la-op_utimens.Tpo -c op_utimens.c  -fPIC -DPIC -o .libs/umfuseext2_la-op_utimens.o
libtool: compile:  gcc -DHAVE_CONFIG_H -I. -I.. -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_utimens.lo -MD -MP -MF .deps/umfuseext2_la-op_utimens.Tpo -c op_utimens.c -o umfuseext2_la-op_utimens.o >/dev/null 2>&1
mv -f .deps/umfuseext2_la-op_utimens.Tpo .deps/umfuseext2_la-op_utimens.Plo
/bin/bash ../libtool  --tag=CC   --mode=compile gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE  -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_write.lo -MD -MP -MF .deps/umfuseext2_la-op_write.Tpo -c -o umfuseext2_la-op_write.lo `test -f 'op_write.c' || echo './'`op_write.c
libtool: compile:  gcc -DHAVE_CONFIG_H -I. -I.. -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_write.lo -MD -MP -MF .deps/umfuseext2_la-op_write.Tpo -c op_write.c  -fPIC -DPIC -o .libs/umfuseext2_la-op_write.o
libtool: compile:  gcc -DHAVE_CONFIG_H -I. -I.. -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_write.lo -MD -MP -MF .deps/umfuseext2_la-op_write.Tpo -c op_write.c -o umfuseext2_la-op_write.o >/dev/null 2>&1
mv -f .deps/umfuseext2_la-op_write.Tpo .deps/umfuseext2_la-op_write.Plo
/bin/bash ../libtool  --tag=CC   --mode=compile gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE  -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_mknod.lo -MD -MP -MF .deps/umfuseext2_la-op_mknod.Tpo -c -o umfuseext2_la-op_mknod.lo `test -f 'op_mknod.c' || echo './'`op_mknod.c
libtool: compile:  gcc -DHAVE_CONFIG_H -I. -I.. -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_mknod.lo -MD -MP -MF .deps/umfuseext2_la-op_mknod.Tpo -c op_mknod.c  -fPIC -DPIC -o .libs/umfuseext2_la-op_mknod.o
libtool: compile:  gcc -DHAVE_CONFIG_H -I. -I.. -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_mknod.lo -MD -MP -MF .deps/umfuseext2_la-op_mknod.Tpo -c op_mknod.c -o umfuseext2_la-op_mknod.o >/dev/null 2>&1
mv -f .deps/umfuseext2_la-op_mknod.Tpo .deps/umfuseext2_la-op_mknod.Plo
/bin/bash ../libtool  --tag=CC   --mode=compile gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE  -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_symlink.lo -MD -MP -MF .deps/umfuseext2_la-op_symlink.Tpo -c -o umfuseext2_la-op_symlink.lo `test -f 'op_symlink.c' || echo './'`op_symlink.c
libtool: compile:  gcc -DHAVE_CONFIG_H -I. -I.. -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_symlink.lo -MD -MP -MF .deps/umfuseext2_la-op_symlink.Tpo -c op_symlink.c  -fPIC -DPIC -o .libs/umfuseext2_la-op_symlink.o
libtool: compile:  gcc -DHAVE_CONFIG_H -I. -I.. -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_symlink.lo -MD -MP -MF .deps/umfuseext2_la-op_symlink.Tpo -c op_symlink.c -o umfuseext2_la-op_symlink.o >/dev/null 2>&1
mv -f .deps/umfuseext2_la-op_symlink.Tpo .deps/umfuseext2_la-op_symlink.Plo
/bin/bash ../libtool  --tag=CC   --mode=compile gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE  -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_truncate.lo -MD -MP -MF .deps/umfuseext2_la-op_truncate.Tpo -c -o umfuseext2_la-op_truncate.lo `test -f 'op_truncate.c' || echo './'`op_truncate.c
libtool: compile:  gcc -DHAVE_CONFIG_H -I. -I.. -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_truncate.lo -MD -MP -MF .deps/umfuseext2_la-op_truncate.Tpo -c op_truncate.c  -fPIC -DPIC -o .libs/umfuseext2_la-op_truncate.o
libtool: compile:  gcc -DHAVE_CONFIG_H -I. -I.. -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_truncate.lo -MD -MP -MF .deps/umfuseext2_la-op_truncate.Tpo -c op_truncate.c -o umfuseext2_la-op_truncate.o >/dev/null 2>&1
mv -f .deps/umfuseext2_la-op_truncate.Tpo .deps/umfuseext2_la-op_truncate.Plo
/bin/bash ../libtool  --tag=CC   --mode=compile gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE  -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_link.lo -MD -MP -MF .deps/umfuseext2_la-op_link.Tpo -c -o umfuseext2_la-op_link.lo `test -f 'op_link.c' || echo './'`op_link.c
libtool: compile:  gcc -DHAVE_CONFIG_H -I. -I.. -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_link.lo -MD -MP -MF .deps/umfuseext2_la-op_link.Tpo -c op_link.c  -fPIC -DPIC -o .libs/umfuseext2_la-op_link.o
libtool: compile:  gcc -DHAVE_CONFIG_H -I. -I.. -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_link.lo -MD -MP -MF .deps/umfuseext2_la-op_link.Tpo -c op_link.c -o umfuseext2_la-op_link.o >/dev/null 2>&1
mv -f .deps/umfuseext2_la-op_link.Tpo .deps/umfuseext2_la-op_link.Plo
/bin/bash ../libtool  --tag=CC   --mode=compile gcc -DHAVE_CONFIG_H -I. -I..    -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE  -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_rename.lo -MD -MP -MF .deps/umfuseext2_la-op_rename.Tpo -c -o umfuseext2_la-op_rename.lo `test -f 'op_rename.c' || echo './'`op_rename.c
libtool: compile:  gcc -DHAVE_CONFIG_H -I. -I.. -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_rename.lo -MD -MP -MF .deps/umfuseext2_la-op_rename.Tpo -c op_rename.c  -fPIC -DPIC -o .libs/umfuseext2_la-op_rename.o
libtool: compile:  gcc -DHAVE_CONFIG_H -I. -I.. -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE -I/usr/local/include/umview -I/usr/local/include -g -O2 -MT umfuseext2_la-op_rename.lo -MD -MP -MF .deps/umfuseext2_la-op_rename.Tpo -c op_rename.c -o umfuseext2_la-op_rename.o >/dev/null 2>&1
mv -f .deps/umfuseext2_la-op_rename.Tpo .deps/umfuseext2_la-op_rename.Plo
/bin/bash ../libtool  --tag=CC   --mode=link gcc -Wall -DHAVE_CONFIG_H -D_GNU_SOURCE  -I/usr/local/include/umview -I/usr/local/include -g -O2 -module -avoid-version -export-dynamic -lext2fs  -o umfuseext2.la -rpath /usr/local/lib/umview/modules umfuseext2_la-fuse-ext2.lo umfuseext2_la-do_probe.lo umfuseext2_la-do_check.lo umfuseext2_la-do_fillstatbuf.lo umfuseext2_la-do_readinode.lo umfuseext2_la-do_writeinode.lo umfuseext2_la-do_killfilebyinode.lo umfuseext2_la-op_init.lo umfuseext2_la-op_destroy.lo umfuseext2_la-op_access.lo umfuseext2_la-op_fgetattr.lo umfuseext2_la-op_getattr.lo umfuseext2_la-op_getxattr.lo umfuseext2_la-op_open.lo umfuseext2_la-op_read.lo umfuseext2_la-op_readdir.lo umfuseext2_la-op_readlink.lo umfuseext2_la-op_release.lo umfuseext2_la-op_statfs.lo umfuseext2_la-op_chown.lo umfuseext2_la-op_chmod.lo umfuseext2_la-op_create.lo umfuseext2_la-op_flush.lo umfuseext2_la-op_fsync.lo umfuseext2_la-op_mkdir.lo umfuseext2_la-op_rmdir.lo umfuseext2_la-op_unlink.lo umfuseext2_la-op_utimens.lo umfuseext2_la-op_write.lo umfuseext2_la-op_mknod.lo umfuseext2_la-op_symlink.lo umfuseext2_la-op_truncate.lo umfuseext2_la-op_link.lo umfuseext2_la-op_rename.lo  -lext2fs -lcom_err -lfuse -lpthread 
libtool: link: gcc -shared  -fPIC -DPIC  .libs/umfuseext2_la-fuse-ext2.o .libs/umfuseext2_la-do_probe.o .libs/umfuseext2_la-do_check.o .libs/umfuseext2_la-do_fillstatbuf.o .libs/umfuseext2_la-do_readinode.o .libs/umfuseext2_la-do_writeinode.o .libs/umfuseext2_la-do_killfilebyinode.o .libs/umfuseext2_la-op_init.o .libs/umfuseext2_la-op_destroy.o .libs/umfuseext2_la-op_access.o .libs/umfuseext2_la-op_fgetattr.o .libs/umfuseext2_la-op_getattr.o .libs/umfuseext2_la-op_getxattr.o .libs/umfuseext2_la-op_open.o .libs/umfuseext2_la-op_read.o .libs/umfuseext2_la-op_readdir.o .libs/umfuseext2_la-op_readlink.o .libs/umfuseext2_la-op_release.o .libs/umfuseext2_la-op_statfs.o .libs/umfuseext2_la-op_chown.o .libs/umfuseext2_la-op_chmod.o .libs/umfuseext2_la-op_create.o .libs/umfuseext2_la-op_flush.o .libs/umfuseext2_la-op_fsync.o .libs/umfuseext2_la-op_mkdir.o .libs/umfuseext2_la-op_rmdir.o .libs/umfuseext2_la-op_unlink.o .libs/umfuseext2_la-op_utimens.o .libs/umfuseext2_la-op_write.o .libs/umfuseext2_la-op_mknod.o .libs/umfuseext2_la-op_symlink.o .libs/umfuseext2_la-op_truncate.o .libs/umfuseext2_la-op_link.o .libs/umfuseext2_la-op_rename.o   -lext2fs -lcom_err -lfuse -lpthread  -g -O2   -Wl,-soname -Wl,umfuseext2.so -o .libs/umfuseext2.so
libtool: link: ar cr .libs/umfuseext2.a  umfuseext2_la-fuse-ext2.o umfuseext2_la-do_probe.o umfuseext2_la-do_check.o umfuseext2_la-do_fillstatbuf.o umfuseext2_la-do_readinode.o umfuseext2_la-do_writeinode.o umfuseext2_la-do_killfilebyinode.o umfuseext2_la-op_init.o umfuseext2_la-op_destroy.o umfuseext2_la-op_access.o umfuseext2_la-op_fgetattr.o umfuseext2_la-op_getattr.o umfuseext2_la-op_getxattr.o umfuseext2_la-op_open.o umfuseext2_la-op_read.o umfuseext2_la-op_readdir.o umfuseext2_la-op_readlink.o umfuseext2_la-op_release.o umfuseext2_la-op_statfs.o umfuseext2_la-op_chown.o umfuseext2_la-op_chmod.o umfuseext2_la-op_create.o umfuseext2_la-op_flush.o umfuseext2_la-op_fsync.o umfuseext2_la-op_mkdir.o umfuseext2_la-op_rmdir.o umfuseext2_la-op_unlink.o umfuseext2_la-op_utimens.o umfuseext2_la-op_write.o umfuseext2_la-op_mknod.o umfuseext2_la-op_symlink.o umfuseext2_la-op_truncate.o umfuseext2_la-op_link.o umfuseext2_la-op_rename.o
libtool: link: ranlib .libs/umfuseext2.a
libtool: link: ( cd ".libs" && rm -f "umfuseext2.la" && ln -s "../umfuseext2.la" "umfuseext2.la" )
make[2]: Leaving directory '/home/ubuntu/Downloads/fuse-ext2-master/fuse-ext2'
Making all in tools
make[2]: Entering directory '/home/ubuntu/Downloads/fuse-ext2-master/tools'
Making all in macosx
make[3]: Entering directory '/home/ubuntu/Downloads/fuse-ext2-master/tools/macosx'
make[3]: Nothing to be done for 'all'.
make[3]: Leaving directory '/home/ubuntu/Downloads/fuse-ext2-master/tools/macosx'
make[3]: Entering directory '/home/ubuntu/Downloads/fuse-ext2-master/tools'
make[3]: Nothing to be done for 'all-am'.
make[3]: Leaving directory '/home/ubuntu/Downloads/fuse-ext2-master/tools'
make[2]: Leaving directory '/home/ubuntu/Downloads/fuse-ext2-master/tools'
make[2]: Entering directory '/home/ubuntu/Downloads/fuse-ext2-master'
make[2]: Leaving directory '/home/ubuntu/Downloads/fuse-ext2-master'
make[1]: Leaving directory '/home/ubuntu/Downloads/fuse-ext2-master'


ubuntu@ubuntu:~/Downloads/fuse-ext2-master$ sudo make install
Making install in fuse-ext2
make[1]: Entering directory '/home/ubuntu/Downloads/fuse-ext2-master/fuse-ext2'
make[2]: Entering directory '/home/ubuntu/Downloads/fuse-ext2-master/fuse-ext2'
 /usr/bin/mkdir -p '/usr/local/bin'
  /bin/bash ../libtool   --mode=install /usr/bin/install -c fuse-ext2 fuse-ext2.probe '/usr/local/bin'
libtool: install: /usr/bin/install -c fuse-ext2 /usr/local/bin/fuse-ext2
libtool: install: /usr/bin/install -c fuse-ext2.probe /usr/local/bin/fuse-ext2.probe
/usr/bin/install -c -d "//usr/local/sbin"
ln -s -f "/usr/local/bin/fuse-ext2" "//usr/local/sbin/mount.fuse-ext2"
 /usr/bin/mkdir -p '/usr/local/lib/umview/modules'
 /bin/bash ../libtool   --mode=install /usr/bin/install -c   umfuseext2.la '/usr/local/lib/umview/modules'
libtool: install: /usr/bin/install -c .libs/umfuseext2.so /usr/local/lib/umview/modules/umfuseext2.so
libtool: install: /usr/bin/install -c .libs/umfuseext2.lai /usr/local/lib/umview/modules/umfuseext2.la
libtool: install: /usr/bin/install -c .libs/umfuseext2.a /usr/local/lib/umview/modules/umfuseext2.a
libtool: install: chmod 644 /usr/local/lib/umview/modules/umfuseext2.a
libtool: install: ranlib /usr/local/lib/umview/modules/umfuseext2.a
libtool: finish: PATH="/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/snap/bin:/sbin" ldconfig -n /usr/local/lib/umview/modules
----------------------------------------------------------------------
Libraries have been installed in:
   /usr/local/lib/umview/modules

If you ever happen to want to link against installed libraries
in a given directory, LIBDIR, you must either use libtool, and
specify the full pathname of the library, or use the '-LLIBDIR'
flag during linking and do at least one of the following:
   - add LIBDIR to the 'LD_LIBRARY_PATH' environment variable
     during execution
   - add LIBDIR to the 'LD_RUN_PATH' environment variable
     during linking
   - use the '-Wl,-rpath -Wl,LIBDIR' linker flag
   - have your system administrator add LIBDIR to '/etc/ld.so.conf'

See any operating system documentation about shared libraries for
more information, such as the ld(1) and ld.so(8) manual pages.
----------------------------------------------------------------------
make  install-data-hook
make[3]: Entering directory '/home/ubuntu/Downloads/fuse-ext2-master/fuse-ext2'
cd "//usr/local/lib/umview/modules" && rm -f umfuseext2.la
make[3]: Leaving directory '/home/ubuntu/Downloads/fuse-ext2-master/fuse-ext2'
make[2]: Leaving directory '/home/ubuntu/Downloads/fuse-ext2-master/fuse-ext2'
make[1]: Leaving directory '/home/ubuntu/Downloads/fuse-ext2-master/fuse-ext2'
Making install in tools
make[1]: Entering directory '/home/ubuntu/Downloads/fuse-ext2-master/tools'
Making install in macosx
make[2]: Entering directory '/home/ubuntu/Downloads/fuse-ext2-master/tools/macosx'
make[3]: Entering directory '/home/ubuntu/Downloads/fuse-ext2-master/tools/macosx'
make[3]: Nothing to be done for 'install-exec-am'.
make[3]: Nothing to be done for 'install-data-am'.
make[3]: Leaving directory '/home/ubuntu/Downloads/fuse-ext2-master/tools/macosx'
make[2]: Leaving directory '/home/ubuntu/Downloads/fuse-ext2-master/tools/macosx'
make[2]: Entering directory '/home/ubuntu/Downloads/fuse-ext2-master/tools'
make[3]: Entering directory '/home/ubuntu/Downloads/fuse-ext2-master/tools'
make[3]: Nothing to be done for 'install-exec-am'.
make[3]: Nothing to be done for 'install-data-am'.
make[3]: Leaving directory '/home/ubuntu/Downloads/fuse-ext2-master/tools'
make[2]: Leaving directory '/home/ubuntu/Downloads/fuse-ext2-master/tools'
make[1]: Leaving directory '/home/ubuntu/Downloads/fuse-ext2-master/tools'
make[1]: Entering directory '/home/ubuntu/Downloads/fuse-ext2-master'
make[2]: Entering directory '/home/ubuntu/Downloads/fuse-ext2-master'
make[2]: Nothing to be done for 'install-exec-am'.
 /usr/bin/mkdir -p '/usr/local/share/man/man1'
 /usr/bin/install -c -m 644 fuse-ext2.1 '/usr/local/share/man/man1'
 /usr/bin/mkdir -p '/usr/local/lib/pkgconfig'
 /usr/bin/install -c -m 644 fuse-ext2.pc '/usr/local/lib/pkgconfig'
make[2]: Leaving directory '/home/ubuntu/Downloads/fuse-ext2-master'
make[1]: Leaving directory '/home/ubuntu/Downloads/fuse-ext2-master'
```
