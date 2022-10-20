# Create NPM Ubuntu Service

## Navigate to systemd
```
$ cd /etc/systemd/system
```

## Create systemd file
```
$ sudo nano npmapp.serivce
```

## Fill text
```
[Unit]
Description=NPM App

[Service]
ExecStart=/usr/bin/node /home/ady/npmapp/main.js
User=ady
Restart=on-failure
RestartSec=3

[Install]
WantedBy=multi-user.target
```

## Enable service
```
$ sudo systemctl enable npmapp.service
```

## Start service
```
$ sudo systemctl start npmapp.service
```
