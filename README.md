# Cal massana energy meter

## Install
### Install Energy Meter reader MBMD
Following official docs at [https://github.com/volkszaehler/mbmd](https://github.com/volkszaehler/mbmd).
1. Download mbdb into raspberry PI
```bash
$ wget https://github.com/volkszaehler/mbmd/releases/download/0.13/mbmd_0.13_linux_armv6.tar.gz
$ tar -xvzf mbmd_0.13_linux_armv6.tar.gz
$ sudo cp mbmd /usr/local/bin
```
2. Copy this file into `/etc/systemd/system/mbmd.service`
```
[Unit]
Description=mbmd
After=syslog.target
After=network-online.target
[Service]
ExecStart=/usr/local/bin/mbmd run -a /dev/ttyUSB0 -d --comset 8E1 -d ORNO3p:1
Restart=always
[Install]
WantedBy=multi-user.target
``` 
3. Start service:
```
$ sudo systemctl start mbmd
```



