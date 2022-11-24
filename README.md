# Cal Massana energy meter

## Install
Installation instructions for a raspberry pi.

### Install Energy Meter reader MBMD
Following official docs at [https://github.com/volkszaehler/mbmd](https://github.com/volkszaehler/mbmd).
1. Download mbdb into raspberry PI
```bash
$ wget https://github.com/volkszaehler/mbmd/releases/download/0.13/mbmd_0.13_linux_armv6.tar.gz
$ tar -xvzf mbmd_0.13_linux_armv6.tar.gz
$ sudo cp mbmd /usr/local/bin
```
2. Copy daemon definition 
```
$ sudo cp mbmd/mbmd.service /etc/systemd/system/mbmd.service
``` 
3. Start service:
```
$ sudo systemctl start mbmd
```
### Install docker
```
$ curl -sSL https://get.docker.com | sh
$ sudo usermod -aG docker ${USER}
$ sudo systemctl enable docker
```
### Start 



