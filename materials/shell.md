---
title: Shell Basics
description: 
published: true
date: 2023-09-07T15:40:03.978Z
tags: 
editor: markdown
dateCreated: 2022-08-12T11:18:14.783Z
---

# Quick guide to the Linux/macOS shell

This is a quick crash course on using the shell, for a more in depth guide see [Unix shell](/en/stack/unixsh)

> *Note that the name "Linux shell" isn't entirely accurate, since almost all the commands here can work on BSD systems and macOS (and any unix-like system), however for simplicity's sake we will refer it as such in this article*
{.is-info}


## For Windows users

*Make sure you've finished the guide in [Setting up](/en/materials/setup)*

*Upon the first launch of Ubuntu, the system may prompt you to enable the Windows optional feature. In this case, you need to do the following:*

- *Open Windows PowerShell as Administrator and run*
    
  `Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux`
    
- *Restart your computer.*


> It will also ask for a username and password (which will be different from your Windows account). Please remember the password at least, since you will need it for administrative tasks.
{.is-info}

After it has started up, type and enter both ``sudo apt update`` and ``sudo apt upgrade`` (if it asks for a yes/no question, type y and enter).


# Basics
## Starting up the shell

Varies between system.
For Windows users search for Ubuntu in the start menu (if you can't find it, see above for help)
macOS users should search for a terminal with whatever they use to find stuff.
Ubuntu users (and linux people with GNOME Desktop), press the start button on the keyboard and search for the terminal

![terminal.png](/assets/materials/terminal.png =x450)

You should find something similar to this

![screen.png](/assets/shell/screen.png =x450)

## Where are you?
Think of the shell as both a file manager and a program launcher. Try typing `pwd` (**P**rint **W**orking **D**irectory), enter and see what happens.

![pwd.png](/assets/shell/pwd.png =x450)

Computers (and users) use a system of directories (or folders) for organising files (which can be things like videos, documents, music etc.) in a logical order. The command prints the current folder you're in.
> You might be familiar with what files are in Windows, however in Linux (and all unix) systems **EVERYTHING** is a file, including things like disk drives.
{.is-info}

## Moving around

Let's try listing files and directories in the folder we are in. To do this write `ls` (**L**i**S**t) and enter.
It should look something like this:

![ls.png](/assets/shell/ls.png =x450)

If the folder is colored blue, it means it's a folder. If it's any other color it's a file
> Note that sometimes it might not show colors if the shell is not configured correctly. To definitely check if something is a directory use `ls -l` and check if the line with the folder listed there starts with a 'd' (meaning it's a directory) or - (meaning it's a file).
{.is-info}

> Unlike Windows, files in linux are **case-sensitive**. This means `desktop` and `Desktop` are different folders/files, so if you type `cd desktop`, you will probably get a error saying no such file or directory exists.
{.is-warning}


Let's try changing our directory to the Desktop in the output of ls. Type `cd Desktop` (**C**hange **D**irectory) and press enter.

![desktop.png](/assets/shell/desktop.png =x450)

> You will notice the ~ changed to Desktop. The ~ is sort hand for 'current user home folder'. You can use it to return the home directory quickly regardless where you are by typing `cd ~`. You can also access files and sub-directories from (example: `cd ~/Desktop` will take you to the desktop folder in your home folder)
{.is-success}

To go to the parent directory (i.e, the folder you that houses 'Desktop'), type `cd ..` and enter.

![home_folder_again.png](/assets/shell/home_folder_again.png =x450)

Let's try moving to a directory that isn't in the current folder nor a parent. Type `cd /` and enter to move the "root" directory, and then enter `ls` to see the files and folders there.

![root.png](/assets/shell/root.png =x450)

> The root folder (/) is akin to a C Drive in windows ([although not quite the same](https://averagelinuxuser.com/linux-root-folders-explained/))
{.is-info}

> You might have noticed as a Windows user that directory paths (like /home/username are with the forward-slash (/), not the backwards slash (\\). This is a significant difference, so don't confuse them
{.is-info}

Finally, you can type `cd -` to go the previous directory, i.e back to '/home/username'.

![home_folder_prev.png](/assets/shell/home_folder_prev.png =x450)

# Files and folders
Like most operating systems, You can have files in Linux that contain information, and folders
(also called directories) that contain files and other folders.

## Creating files
You can create a file in various ways:

1. `touch <filename>` Will create an empty file. e.g `touch hello.txt`
2. `<command> > <filename>` will create a file that contains the output of command, e.g `echo "Hello" > hello.txt` will create a file called hello.txt with the contents of "Hello". Note that this will overwrite hello.txt if it already exists (You can append the output of a command to a file with `>>`, i.e `echo "Hello" >> hello.txt`)

## Creating folders
You can create folders with `mkdir <folder name>`. You can also create folders in other filders, by adding a path before the folder name (You can also do this for any operation regarding files as well) `mkdir <path> <folder name>`.

For example, if I am in the folder `/home/student/`, and I wanted to create a folder called `code` in `/home/student/Documents`, I can do `mkdir Documents/code`. If I wanted in the /home/ folder, I can do `mkdir /home/code` (`../code` is also valid!)

## Opening files

1. You can output the file contents with `cat <filename>`
2. If you want to scroll through the file contents, you can use `less <filename>`

## Editing files

1. For Linux beginners, it is recommended you use 'nano' to edit files. You can use the arrow keys to traverse the file. `nano <filename>`
2. Advanced users should probably (but not necessarily) learn about [Vi family of editors](/en/materials/vi) or [GNU Emacs](/en/materials/emacs)

# Copying/Moving
You can copy files with `cp`, and cut/rename them with 'mv'

## Copying
`cp <filename> <destination>`. Optionally, you can rename the copy (on copy) with `cp <filename> <destination>/[new filename]`

## Moving
`mv <filename> <destination>`. Again, add filename to the end if you want to rename it. The destination should be a folder.

## Renaming
You can use the `mv` command to rename files as well: `mv <filename> <new name>`

# Running programs
Most shells use the variable $PATH to determine where to look for programs to run, seperated by a `:`. For example if $PATH is `/usr/local/bin:/usr/bin:/usr/local/sbin`, it will look into these folders for a program to run. If I type the command `cat` into the terminal, and `cat` is located in `/usr/bin`, it will first look into `/usr/local/bin`. Since it isn't there, it will look into `/usr/bin`, find it and then run it. If it weren't in any directory, then the command would simply fail.

## Running programs in the current directory
If you want to run a program in the current directory, say `my_program`, then you add a `./` to the name to indicate that you want to run the program that's in the current directory.

`./my_program` Will execute the program.

## Piping
You can send the output of a program as the input to another with piping. You can use the `|` symbol for this.

Say you have a file called `words.txt` that you want to search for the amount of lines that contain "Hello". You could do it manually, or you could simply list the lines with `cat words.txt | grep -c "Hello"`. `grep` is a command that searches for lines with the specified text, with the `-c` telling it to count the occurences.

# Scripting
WIP

# Tips and tricks
WIP

# More info
WIP

# References