# ZyGrib GRIB File Viewer Weather data visualization
Is it going to be windy on the weekend?

![Image](SampleAnimation.gif?raw=true)

Many datasources from NOAA-GFS, FNMOC-WW3 covers the entire globe

![Image](SourceFeatures.gif?raw=true)

Perfect for marine related weather (excellent waves and wind section)

# zyGrib_compile_in_Ubuntu19.04
Updated instructions for compiling zyGrib, this excellent GRIB File Viewer Weather data visualization; in a 19.04 desktop Ubuntu. check https://www.zygrib.org/

## Adapted from
Check https://www.zygrib.org/#section_linux

## Environment
Strongly advice that `qt` developers check the source warnings
```
$ uname -a
Linux _ 5.0.0-20-generic #21-Ubuntu SMP Mon Jun 24 09:32:09 UTC 2019 x86_64 x86_64 x86_64 GNU/Linux
$ lsb_release -a
No LSB modules are available.
Distributor ID:	Ubuntu
Description:	Ubuntu 19.04
Release:	19.04
Codename:	disco
```
## Get and go to the source code
Download, unpack, cd to the released source: https://www.zygrib.org/getfile.php?file=zyGrib-8.0.1.tgz

## Prepare for make
Had to install some packages from apt, replace others, find some ousted from ubuntu via web... Here goes nothing:
```
$ sudo apt install build-essential g++ make libbz2-dev zlib1g-dev libproj-dev libnova-dev nettle-dev libjpeg-dev qtbase5-dev qt5-default libpng-dev 

```
Download `libjasper-dev libjasper1` via web. This search-mirror points to canonical if I'm not wrong:
- https://pkgs.org/download/libjasper-dev 
- https://pkgs.org/download/libjasper1
```
$ sudo dpkg -i libjasper-dev.{...}.deb
$ sudo dpkg -i libjasper1.{...}.deb
$ export QT_SELECT=qt5
$ make
$ make install
```
