## Python3.8
psi4-v1.6 requires python3.8-numpy, psi4-v1.5 requires python 3.7-numpy

but psi4-v1.5 required special packages in libint2, which is difficult to add.

In CentOS7, one need to compile python3.8:
```bash
$ sudo yum install gcc openssl-devel libffi-devel bzip2-devel wget
$ wget https://www.python.org/ftp/python/3.8.12/Python-3.8.12.tgz
$ cd Python-3.8.12/
$  sudo ./configure --enable-optimizations 
$  sudo make altinstall

$ python3.8 -m pip install numpy # this is needed for psi4-v1.6
```

Or, set up a conda env and install python 3.8 and sompile in the env.

## Psi4-v1.6
Requirement:
```bash
Python >=3.8, gcc/g++ >= 8.1, Lapack (MKL recommended), Eigen3 (required by Libint2)
```

Install Eigen3
```bash
$ sudo yum install eigen3-devel
```
Prepare a do-configure file:
```bash
cmake -S. -B"/home/michaelbishop/softwares/psi4_mod/psi4-master/compile-psi4" \
        -DCMAKE_INSTALL_PREFIX="/home/michaelbishop/softwares/psi4_mod/psi4-master/install-psi4" \
        -DCMAKE_PREFIX_PATH="/home/michaelbishop/softwares/psi4_mod/psi4-master/install-psi4/externals/install-libint" \
        -DMAX_AM_ERI=6 \
        -DENABLE_gdma=ON \
        -DBUILD_SHARED_LIBS=ON \
        -DCMAKE_C_COMPILER=/opt/gcc/8.3.0/bin/gcc \
        -DCMAKE_CXX_COMPILER=/opt/gcc/8.3.0/bin/g++ \
        -DCMAKE_Fortran_COMPILER=/opt/gcc/8.3.0/bin/gfortran \
        -DLAPACK_LIBRARIES=/home/michaelbishop/softwares/openblas/openmpi-3.1.3-gnu-8.3.0/lib/libopenblas.a \
        -DLAPACK_INCLUDE_DIRS=/home/michaelbishop/softwares/openblas/openmpi-3.1.3-gnu-8.3.0/include \
        -DOpenMP_LIBRARY_DIRS=/home/michaelbishop/softwares/openmpi/openmpi-3.1.3/mpi_gnu830/lib/

```


