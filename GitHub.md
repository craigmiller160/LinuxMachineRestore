# GitHub SSH Key

This is how to setup the GitHub SSH Key.

## Generate New SSH Key

Use the following command to begin the process of generating an SSH Key:

```
ssh-keygen -t ed25519 -C "craigmiller160@gmail.com"
```

When prompted, enter the following path for the output file:

```
/home/craig/.ssh/github
```

Lastly, for a passphrase, it can be found in 1Password under `GitHub SSH Passphrase`.

## Adding Key to GitHub

On the GitHub website, click on the account icon in the top right corner. In the dropdown menu, select Settings. Then go to the SSH and GPG Keys page. Finally, click the New SSH Key button.

On this screen, title the key "CraigPC Key". Copy the contents of `~/.ssh/github.pub` into the Key section of the screen, and save it.

## Using The Key

Make sure to only clone or add remote origins in the SSH format, and it should work perfectly.