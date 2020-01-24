# Linux file system structure

## /
root

## /bin
Stores binaries, usually core CLI commands and utilities like `rm`, `cd`, etc.

## /boot
Stores files neded for OS to boot. Can be moved to a different physical location, but will always be in this logical location.

## /dev
Provides a file interface for physical devices.

## /etc
Stores global configuration files.

## /home
Stores user files. Typically, `home/username`.

## /lib
Stores shared libraries. Generally installed by the package manager as a dependency.

## /media
Provides interface to usb drives, cd drives, etc.

## /mnt
This is a generic mount point. Typically used for network drives.

## /opt
Stores optional software not handled by package manager. Not frequently used.

## /proc
Provides a file interface to system and process information. Everything is a file in Linux.

## /root
Home folder for root user (superuser).

## /sbin
This is `/bin` for commands that can only be run by root.

## /tmp
Holds temp files. Genereally deleted on shut down.

## /usr
Files that are shared between all users.

## /var
Stores 'variable data'. Things like system logs.
