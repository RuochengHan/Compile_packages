### Ubuntu 22.04

```bash
$ sudo dpkg --add-architecture i386
$ sudo apt-get update
$ sudo apt-get install libc6:i386 libncurses5:i386 libstdc++6:i386
$ sudo apt-get install csh rpm2cpio
./install
```

If error message: 
```bash
Couldn't get environment information from lp_echovars: -1 at /home/ms-test/Accelrys/MaterialsStudio8.0/share/Install/Scripts/MSConfig.pm line 296.
Materials Studio configuration failed
```

```bash
$ cd $HOME/Accelrys/LicensePack/etc
$ ./lp_config
$ ./lp_echovars
```

```bash
$ ./install
```

Run Gateway
```bash
Accelrys/MaterialsStudio8.0/etc/Gateway/msgateway_control_18888
```

mv licenses to /home/michaelbishop/Accelrys/Licenses/
install license:
```
lp_install /home/michaelbishop/Accelrys/Licenses/...
```


Reference:
1. https://www.freesion.com/article/7690395760/
2. https://blog.csdn.net/qq_40481843/article/details/123400600
