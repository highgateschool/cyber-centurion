# Linux

Linux is the name given to the project started by Linus Torvalds in 1990 to build a POSIX compliant UNIX environment, built entirely from code which is unconstrained by commercial licenses. He started with the *kernel*, which is the core code that enables the operating system to communicate with the computer's components - the CPU, disk drive, mouse etc. You can see the effect of this by looking in the ```/dev```, ```/proc``` and ```/sys``` folders: Like all UNIX systems, the peripherals are made accessible to the operating systems using filenames, so ```/dev/sda1``` is the first attached SCSI Disk and ```/sys/cpu``` gains access to the CPU. It goes without saying that *you need to be really careful* when accessing these folders, as messing around could literally wipe a disk or crash the computer. The kernel is updated regularly by the development teams, and is then used by the various distro-projects as the basis of their releases. Often an update of Ubuntu or Fedora will include a kernel update. You can see which one is running by looking in the file ```/proc/version```, so just type ```cat /proc/version```.

## Debian



## Ubuntu

## Fedora

# BASH

If the **kernel** is at the heart of the Operating System, then the **shell** is on the outside, and is the way that you interact with it. Windows is the shell that you will be most used to, and ```cmd.exe``` or PowerShell are both examples of Command Line shells. There are lots of shells, most of which have silly names ```sh``` (pronounced "ssshhhh"), ```csh``` (pronounced sea shell), ```fish``` (think about it) are all good examples. Most Linux distros use ```BASH``` (which means Bourne Again SHell) and Macs now use ```zsh```. There are some important differences, but mostly they all have the same key commands and then their own funky quirks.

Here are some basic shell commands that you should know about:

```ls``` - lists all the files in the present working directory

- ``ls -l`` will give you the info in a nice list
- ```ls -lh``` will give you the info in a nice list in human readable form
- ```ls -a``` will include all files (filenames starting with a "." are normally hidden)
- ```ls /home``` will tell you the files in a specific folder rather than the pwd
- ```ls --help``` will give you a quick summary of options
- ```man ls``` will give you the full manual for ```ls```

```pwd``` - tells you the present working directory

```cd``` - changes the pwd to your default (home) directory

- ```cd /home``` will change the pwd to the ```/home``` folder
- ```cd ..``` will move one folder down the file hierarchy
- ```cd ../..``` will move down two folders
- ```cd ~/Pictures``` will move to the ```Pictures``` folder in your home directory (which can always be referred to using the ```~``` symbol)
- ```cd ~/..``` will move you where?

