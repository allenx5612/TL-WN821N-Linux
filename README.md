# TL-WN821N Linux
Driver for TL-WN821N V6, TL-WN822N V5 and TL-WN823N V3 for Ubuntu 18.04.
### Work environment
| OS | Ubuntu 18.04.5 LTS |
|:-:|:-:|
| Kernel version | 5.4.0-62-generic |
| gcc version | 7.5.0 |
### Installation
1. Install gcc and make:
```sh
$ sudo apt update
$ sudo apt install build-essential
```
2. Clone the repository:
```sh
$ git clone https://github.com/SalavatD/TL-WN821N-Linux.git && cd TL-WN821N-Linux
```
3. Compile:
```sh
$ make clean && make
```
4. load the driver:
```sh
$ sudo cp 8192eu.ko /lib/modules/$(uname -r)/kernel/drivers/net/wireless/
$ sudo depmod -a
$ sudo modprobe 8192eu
```
5. Checking if the driver loaded successfully:
```sh
$ lsmod
```
