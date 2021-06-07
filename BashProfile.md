# Setup Bash Profile Settings

All of my custom bash settings go into the `.bash_profile` file. Here is how to set it up.

## Create the File

Create the file with this command:

```
echo "echo 'Loaded .bash_profile'" > ~/.bash_profile
```

## Add the File to Profile

To make sure it is loaded at startup, open up `~/.bashrc` and add this to the end of it:

```
# Add .bash_profile with custom settings
if [ -f ~/.bash_profile ]; then
	source ~/.bash_profile
fi
```

## Restart Terminal

To confirm this works, restart the terminal. "Loaded .bash_profile" should print out when the prompt opens.