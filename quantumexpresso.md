# QE 7.2
Time 202308

## CUDA
ver. 12.2

## NVIDIA hpc-sdk
https://developer.nvidia.com/hpc-sdk-downloads
CUDA ver. 12.2 11.8 11.0. Install version.
Include MPI (mpicc mpif90 rtc.) and other neccesary packages.
```bash
$ wget https://developer.download.nvidia.com/hpc-sdk/23.7/nvhpc_2023_237_Linux_x86_64_cuda_multi.tar.gz
$ tar xpzf nvhpc_2023_237_Linux_x86_64_cuda_multi.tar.gz
$ nvhpc_2023_237_Linux_x86_64_cuda_multi/install
```

## QE
```bash
$ cd qe-7.2/dev-tools
$ python3 get_device_props.py
```

Follow recommendations:

```bash
$ ./configure --with-cuda=yes --with-cuda-cc=75 --with-cuda-runtime=11.8 --prefix=/home/michaelbishop/softwares/qe/qe-7.2_install
```

```bash
$ make -j 12 all
$ make install
```

Note: if facing error in Wannier90 in bash```make -j 12 all```, just bash```make all``` again 
