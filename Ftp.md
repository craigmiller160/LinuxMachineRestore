# FTP

This is about setting up an FTP server for faster transfers on my LAN. Minimal security is needed because only devices on my LAN can access the machine.

## Install VSFTPD

First, install the server app:

```bash
sudo apt install vsftpd
```

Then make sure it is running:

```bash
sudo systemctl status vsftpd
```

## Configure VSFTPD

Edit the config file with:

```bash
sudo vim /etc/vsftpd.conf
```

These are the preferred settings:

```
anonymous_enable=NO
local_enable=YES
write_enable=YES
```

Then restart:

```bash
sudo systemctl restart vsftpd
```

## Connecting

Connecting to the FTP server requires using the computer's LAN IP `192.168.7.241` and the username/password of this machine. Port 21.