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

make FC=gfortran CC=gcc USE_THREAD=0 INTERFACE64=1
make PREFIX=/home/michaelbishop/softwares/openblas/gnu-11.3.0 install
```

### pyparsing
```bash
conda install pyparsing
```

### OpenMolcas 20230806
```bash
module load
CMakeLists.txt: set OPENMP ON
./configure-cmake --compiler gnu --opt normal --openblas /home/michaelbishop/softwares/openblas/gnu-11.3.0/ --omp -j 12 --prefix /home/michaelbishop/softwares/openmolcas/openmolcas_20230806-openblas0.3.10-gnu11.3.0-20230806
./make-gnu_normal_omp_openblas
cd builds/gnu_normal_omp_openblas/
make intall
```
