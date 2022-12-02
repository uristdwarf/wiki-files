---
title: Setting up
description: Laptop setup
published: true
date: 2022-12-02T09:34:19.367Z
tags: 
editor: markdown
dateCreated: 2022-08-12T11:10:31.847Z
---

# Getting your Laptop ready

Here you can get short instructions and links on how to get your laptop prepared. We strongly recommend doing that **before** you arrive at Sillamäe. If you need help, our team can assist you during the very first day.

# Mac OS

First of all, install the **Homebrew ([https://brew.sh](https://brew.sh/))**

After that, using Homebrew - install these utils 

```bash
brew install coreutils
brew install jq
brew install git # (if you don’t have xCode)
brew install golang # (or install it from https://golang.org/dl/)
brew install gofumpt
```

**Visual Studio Code ([https://code.visualstudio.com](https://code.visualstudio.com/))**

- Open the **Command Palette** via **(⇧ (shift) ⌘ (command) P)** and type shell command to find the Shell Command -> install ‘code’ command in PATH

**Terminal commands**

- echo .DS_Store >> .gitignore
- git commit -am “remove .DS_Store files”
- touch ~/.gitignore_global
- git config --global core.excludesfile ~/.gitignore_global
- echo .DS_Store >> ~/.gitignore_global

Run the `brew list` command to be sure that you have all necessary packages 

# Windows Subsystem for Linux (WSL)
> A lot people have reported problems with WSL. While this remains the official way to do things on Windows as provided by the school/01, it has been recommended that if you encounter difficulties with WSL, that you try a [pure Windows setup](#Windows)
{.is-warning}


**How to Enable the Linux Bash Shell in Windows 10: [https://www.laptopmag.com/articles/use-bash-shell-windows-10](https://www.laptopmag.com/articles/use-bash-shell-windows-10) (1-9)**

**Ubuntu installation ([https://ubuntu.com/wsl](https://ubuntu.com/wsl)) - Ubuntu terminal for Windows 10**

**In case if have** **Windows 7, then here is Linux distribution for  ([http://www.cygwin.com/](http://www.cygwin.com/))**

**Install the Homebrew ([https://brew.sh](https://brew.sh/index_ru)) in Ubuntu Terminal**

```bash
**brew install coreutils
brew install jq
brew install git
brew install golang**
export PATH=$PATH:/usr/local/go/bin
**brew install gofumpt**
```

**Visual Studio Code ([https://code.visualstudio.com](https://code.visualstudio.com/)) - Windows and agree with all points in installation**

- **Remote Development Extention ([https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.vscode-remote-extensionpack)](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-wsl)**

After downloading the WSL extension, then click the green "**Open a Remote Window**" button

![wsl1.png](/wsl1.png)

And in the menu click on the "**New WSL Window**"

![wsl2.png](/wsl2.png)

When the WSL window is loaded just run the command `brew list` and it should print out all downloaded packages

# Windows
*Originally written by Olari*
If anyone's having trouble with WSL, I highly recommend just skipping it entirely.
That way it's a lot easier to set up and it makes the debugger inside VS Code work. There's really no downsides to it, you can complete all tasks without WSL.

Here's the setup in a nutshell:
1) [Download Git installer](https://git-scm.com/download/win)
2) [Download Go installer](https://go.dev/dl/)
3) Run both installers, default settings should be fine
4) You're done! You should be able to use Go commands in your console now. You can also use Git Bash if you like unix style commands.

# Linux

**Linux**

**Homebrew ([https://brew.sh](https://brew.sh/))**

- **brew install coreutils**
- **brew install jq**
- **brew install git**
- **brew install golang or install it from [https://golang.org/dl/](https://golang.org/dl/)**
- **brew install gofumpt**

**Visual Studio Code ([https://code.visualstudio.com](https://code.visualstudio.com/))**

- Open the **Command Palette** via **(Ctrl+Shift+P)** and type shell command to find the Shell Command -> install ‘code’ command in PATH

Run the `brew list` command to be sure that you have all necessary packages
