Get source from https://ftp.gnu.org/gnu/gcc/
```bash
$ ./contrib/download_prerequisites # automatically download required GMP, MPFR and MPC.
$ ./configure --prefix=/home/michaelbishop/softwares/gcc/gcc-12.2.0/install --disable-multilib # only 64bit
$ make -j 16
$ make install
```

Create module file
```bash
#%Module
set GCC /home/michaelbishop/softwares/gcc/gcc-12.2.0/install

prepend-path PATH               $GCC/bin
prepend-path LIBRARY_PATH       $GCC/lib64
prepend-path LD_LIBRARY_PATH    $GCC/lib64
prepend-path LD_RUN_PATH        $GCC/lib64
prepend-path MANPATH            $GCC/share/man
```

### 5.4.0
```bash
wget https://ftp.gnu.org/gnu/gcc/gcc-5.4.0/gcc-5.4.0.tar.gz
./contrib/download_prerequisites # automatically download required GMP, MPFR and MPC.
```
