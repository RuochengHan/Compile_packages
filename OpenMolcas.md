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
