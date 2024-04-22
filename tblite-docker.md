```bash
sudo docker pull python-3.8:slim
sudo docker run -itd -p 40012:22 --name "tblite" python-3.8:slim
sudo docker exec -it b015d225eb69 /bin/bash

sed -i 's/deb.debian.org/mirrors.aliyun.com/g' /etc/apt/sources.list
apt update && apt install -y build-essential
apt install -y gfortran cmake libblas-dev liblapack-dev git


echo -e 'numpy~=1.23.5\nscikit-learn~=1.2.2\nrdkit~=2022.9.5\nscikit_image~=0.21.0\nopt-einsum~=3.3.0\nh5py~=3.8.0\nthrift~=0.16.0\npandas~=1.5.3\nmeson~=0.57.2\nninja~=1.10\cffi~=1.16.0' > requirements.txt

pip install -i https://mirrors.bfsu.edu.cn/pypi/web/simple/ --trusted-host mirrors.bfsu.edu.cn/pypi/web/ -r requirements.txt

git clone https://github.com/tblite/tblite.git
cd tblite/
meson setup _build -Dpython=true --prefix=$HOME/.local
meson compile -C _build
meson install -C _build

export PATH=$PATH:/root/.local/bin
export LD_LIBRARY_PATH=$LD_LIBRARY_PATH:/root/.local/lib/x86_64-linux-gnu
```

Image continuumio/miniconda3 (python3.9) not work: In python-api build, python not found...
