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

## Setup Bash Git Prompt

This adds the Git prompt information to the terminal.

First, clone the repo:

```
git clone https://github.com/magicmonty/bash-git-prompt.git ~/.bash-git-prompt --depth=1
```

Then, add the following to the end of the `.bash_profile` file:

```
# Bash Git Prompt
if [ -f "$HOME/.bash-git-prompt/gitprompt.sh" ]; then
    GIT_PROMPT_ONLY_IN_REPO=1
    GIT_PROMPT_THEME=Default_Ubuntu
    source $HOME/.bash-git-prompt/gitprompt.sh
fi
```

## Setup Aliases

Copy the `.bash_alias` file to the home directory. Then add this to the `.bash_profile`.

```
# Setup Aliases
source ~/.bash_alias
```