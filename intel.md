# Intel ONEAPI
See https://www.intel.com/content/www/us/en/developer/tools/oneapi/base-toolkit-download.html?operatingsystem=linux&linux-install-type=offline
To install, pay attention to the --install-dir
```bash
sudo sh ./l_BaseKit_p_2024.2.0.634_offline.sh -a --silent --cli --eula accept --install-dir /home/michaelbishop/softwares/intel
```

Same for HPC Kit for intel ifort instal

Then go to the installed folder
```bash
cd /home/michaelbishop/softwares/intel
sh modulefiles-setup.sh
```

Move folder to the module location:
```bash
mv /home/michaelbishop/modulefiles /usr/share/module/modulefiles/intel/
```
