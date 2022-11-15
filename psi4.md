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

## Psi4-v1.6


