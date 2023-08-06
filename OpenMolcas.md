GNU 11.3.0
### HDF5 1.10.4 serial
```bash
wget https://support.hdfgroup.org/ftp/HDF5/releases/hdf5-1.10/hdf5-1.10.4/src/hdf5-1.10.4.tar.gz
tar zxvf
cd
CC=gcc F77=gfortran F9X=gfortran F90=gfortran ./configure --prefix=
make -j 12
make install
```
### Openblas 0.3.10 serial
```bash
wget https://sourceforge.net/projects/openblas/files/v0.3.10/OpenBLAS%200.3.10%20version.zip/download
unzip download

make FC=gfortran CC=gcc USE_THREAD=0
make PREFIX=/home/michaelbishop/softwares/openblas/gnu-11.3.0 install
```
