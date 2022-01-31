# SSH

This is about setting up the SSH server with key authentication from devices.

## Install OpenSSH

Install OpenSSH Server with:

```bash
sudo apt install openssh-server
```

It should now be running. Attempt to connect from another machine to verify, using the LAN IP. No key authentication is in place yet.

## Create Client Computer SSH Key

Check the machines `~/.ssh` directory for files called `id_rsa` and `id_rsa.pub`. If they are present, that means the identity keys exist. If they are not, create them with:

```bash
ssh-keygen -t rsa
```

Then transfer it to the server with:

```bash
ssh-copy-id {lan_ip}
```

## Setup Client Machine SSH Config

Add the following to the Client Machine's SSH Config:

```
Host craigpc
    Hostname craigmiller160.ddns.net
    User craig
    Port 8000
```