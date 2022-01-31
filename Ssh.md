# SSH

This is about setting up the SSH server with key authentication from devices.

## Install OpenSSH

Install OpenSSH Server with:

```bash
sudo apt install openssh-server
```

It should now be running. Attempt to connect from another machine to verify, using the LAN IP. No key authentication is in place yet.