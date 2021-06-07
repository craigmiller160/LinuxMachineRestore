# VIM

This is for setting up VIM

## Install VIM

First, VIM needs to be installed:

```
sudo apt update
sudo apt install vim
```

## Install Vundle

Then, the VIM package manager Vundle needs to be installed:

```
git clone https://github.com/VundleVim/Vundle.vim.git ~/.vim/bundle/Vundle.vim
```

## Restore Configuration

Copy the `.vimrc` file from this project to the root of the home directory.

## Install Plugins

Open the `.vimrc` file with VIM and then run `:PluginInstall`.

## Setup Terminal Shortcuts

To modify the terminal to use VIM shortcuts, copy the `.inputrc` file from this project to the root of the home directory.