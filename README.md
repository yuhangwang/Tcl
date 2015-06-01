# Tcl
**Tcl (Tool Command Language)**

This is an unofficial verbatim redistribution of the binary&source form of the Tcl language under its open source license terms (see the LICENSE file).

This redistribution is under the same license as the original.

Please visit the official website for more details: https://www.tcl.tk

## Download
You can download the compiled binary files at the [release page](https://github.com/yuhangwang/Tcl/releases).

## Compilation notes
### Compilation environment
* CentOS 6.6
* x86_64 architecture
* Compiler: gcc version 4.4.7 20120313 (Red Hat 4.4.7-11)

### Compilation steps
#### Version: 8.6.4
```bash
go to https://www.tcl.tk/software/tcltk/download.html to download the source files
tar zxvf tcl8.6.4-src.tar.gz
mkdir build_tcl-8.6.4
cd build_tcl-8.6.4
../tcl8.6.4/unix/configure --prefix=/home/steven/install/tcl/8.6.4 --enable-threads=yes --enable-shared=yes --enable-symbols=yes --enable-64bit=yes
make -j10
make test -j10 | tee QualityVerification.txt
make install
```

### Quality verification
See the "QualityVerification.txt" for the output of "make check".