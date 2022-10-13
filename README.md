# Linux

Linux is the name given to the project started by Linus Torvalds in 1990 to build a POSIX compliant UNIX environment, built entirely from code which is unconstrained by commercial licenses. He started with the *kernel*, which is the core code that enables the operating system to communicate with the computer's components - the CPU, disk drive, mouse etc. You can see the effect of this by looking in the ```/dev```, ```/proc``` and ```/sys``` folders: Like all UNIX systems, the peripherals are made accessible to the operating systems using filenames, so ```/dev/sda1``` is the first attached SCSI Disk and ```/sys/cpu``` gains access to the CPU. It goes without saying that *you need to be really careful* when accessing these folders, as messing around could literally wipe a disk or crash the computer. The kernel is updated regularly by the development teams, and is then used by the various distro-projects as the basis of their releases. Often an update of Ubuntu or Fedora will include a kernel update. You can see which one is running by looking in the file ```/proc/version```, so just type ```cat /proc/version```.

## Debian

## Ubuntu

## Fedora

# BASH

