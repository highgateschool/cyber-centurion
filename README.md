

# Linux

Linux is the name given to the project started by Linus Torvalds in 1990 to build a POSIX compliant UNIX environment, built entirely from code which is unconstrained by commercial licenses. He started with the *kernel*, which is the core code that enables the operating system to communicate with the computer's components - the CPU, disk drive, mouse etc. You can see the effect of this by looking in the `/dev`, `/proc` and `/sys` folders: Like all UNIX systems, the peripherals are made accessible to the operating systems using filenames, so `/dev/sda1` is the first attached SCSI Disk and `/sys/cpu` gains access to the CPU. It goes without saying that *you need to be really careful* when accessing these folders, as messing around could literally wipe a disk or crash the computer. The kernel is updated regularly by the development teams, and is then used by the various distro-projects as the basis of their releases. Often an update of Ubuntu or Fedora will include a kernel update. You can see which one is running by looking in the file `/proc/version`, so just type `cat /proc/version`.


# BASH

If the **kernel** is at the heart of the Operating System, then the **shell** is on the outside, and is the way that you interact with it. Windows is the shell that you will be most used to, and `cmd.exe` or PowerShell are both examples of Command Line shells. There are lots of shells, most of which have silly names `sh` (pronounced "ssshhhh"), `csh` (pronounced sea shell), `fish` (think about it) are all good examples. Most Linux distros use `BASH` (which means Bourne Again SHell) and Macs now use `zsh`. There are some important differences, but mostly they all have the same key commands and then their own funky quirks.

## Press the tab key lots

Just like in Minecraft, the tab key is used to "autocomplete" commands. Try this...
- type just the letters "sys".
- Press tab twice.
- You should see all the commands that start with "sys"
- Keep adding letters and pressing tab until you have the command "systemctl" with a space after it
- Press tab again.
- You should see all the tasks that you can run with systemctl

BASH knows how to autocomplete most (but not all) commands. This means that if you are not sure what to do then pressing tab will often give you a good hint. Be careful though. Typing the letter "a" then hitting tab will then get BASH to list _all commands_ that begin with the letter "a".

Other useful tricks:
- ctrl+P runs the last command again
- ctrl+D drops (logs out) from the current logged-in user - so will often close the window
- ctrl+L clears the screen

## Getting around on the command line

Here are some basic shell commands that you should know about:


`ls` - lists all the files in the present working directory

- `ls -l` will give you the info in a nice list
- `ls -lh` will give you the info in a nice list in human readable form
- `ls -a` will include all files (filenames starting with a "." are normally hidden)
- `ls /home` will tell you the files in a specific folder rather than the pwd
- `ls --help` will give you a quick summary of options
- `man ls` will give you the full manual for `ls`

`sudo` - will allow you to do things as the super user (root)
- `sudo nano /etc/ssh/sshd_config` will let you edit the sshd config file

- `pwd` - tells you the present working directory

`cd` - changes the pwd to your default (home) directory

- `cd /home` will change the pwd to the `/home` folder
- `cd ..` will move one folder down the file hierarchy
- `cd ../..` will move down two folders
- `cd ~/Pictures` will move to the `Pictures` folder in your home directory (which can always be referred to using the `~` symbol)
- `cd ~/..` will move you where?

`history` - shows you the history of all the commands that you have typed (including any mistakes - be careful!)
- They are numbered, so you can then type `!21` to run item 21, for example
- `!-2` will run the command second from the bottom
- `!-1` and `!!` will both run the last command again (but ctrl+P is easier)



## User management

Managing users and groups (eg adm or sudo)

`passwd` - will let you set your password
- `sudo passwd agnes` will let you set the password for the user agnes
- `sudo passwd -d agnes` will let you delete agnes's password (and then they won't be able to login with a password).
- be careful!

`gpasswd` - will let you change some settings for a group
- `sudo gpasswd -a agnes sudo` will add agnes to the sudo group
- `sudo gpasswd -d agnes sudo` will remove agnes from the sudo group

`id` - tells you the user id (uid) of the current user, along with the group ids (gids) of all the groups to which they belong

- `id agnes` will tell you the uid and gids for the user called agnes

`getent` - tells you information about various lists in the system (press tab to see them all!
- `getent group sudo` - will tell you all the users in the sudo group
- `getent group` - will tell you all the groups
- `getent services` - will tell you all the services
- `getent services ssh` - will tell you about the ssh service

# Distributions

Once you have the linux kernel you have to wrap it up in something that people can use. This is called the distribution. Most well known distribution have a lot in common. Since they all are part of the Linux project they will have the same basic file structures and most of the same core programs available.

Distributions will differ in how they manage some of the "higher level" functions. The most obvious of these is the choice of User Interface, so whether you have a Graphical User Interface (eg GNOME or KDE), or just a Command Line Interface (eg BASH). But this can also be things like how they manage network connections, how user accounts are managed and, crucially, how packages are managed.  

## Debian

The Debian project was started in 1993 by a man called Ian. His girlfriend's name was Debra. Geddit? They married but eventually divorced. Oh well.

Debian used the program `apt` (Advanced Packaging Tool) to manage packages. Nowadays we use the `apt-get` command 

## Ubuntu

## Fedora
