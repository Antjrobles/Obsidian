---
title: "Linux Commands"
description: "A list of Linux Commands"
tag:
- Linux
---
# LINUX COMMANDS

## LSOF

- `sudo lsof -i TCP:numero de puerto` - Ver qué proceso o programa ocupa un puerto
- `sudo lsof -i` - List all open ports.

## SHRED

when using `rm` (or DELETE) it updates the reference to the file that the OS knows about, and hence, the file will disappear from the current location, making it hidden from users. But the file will still reside somewhere on the hard disk for a period of time, and an advanced user will be able to recover and access those data very easily.

In cases where you want your deleted files to be completely removed from your system in an irrecoverable manner, especially when they contain sensitive information, you can use shred , which is a tool that can overwrite your file to hide its contents and can optionally delete it as well ( -u removes the file).

- `shred -u filetodelete` - Delete or remove file
- `shred -zvu -n 5 filetodelete`
  - -z: add a final overwrite with zeros to hide shredding
  - -v: show progress (i.e. verbose)
  - -u: truncate and remove file after overwriting
  - -n: overwrite N times instead of the default (3)

## DIFF

- A command to comapra two files or directories, and detect any difference or changes between them.
- `diff file1.txt file2.txt` - the output will show the differences. If no output, means the the files are exactly the same. You can check it wiht `echo $?`. if the output is `0`, then is correct.
- install `colordiff` - will put colors on the output.
- `diff -s file1.txt file2.txt` - report whether the files are identical
- `diff -ur folder1 folder2` - compare two folders
- `diff -ub file-1 file-2` - to ignore whitespace
- `diff -uB file-1 file-2` - to ignore blank lines
- `diff <(command1) <(command2)` - to `diff` the output of two commands or scripts
- `vimdiff /path/to/file scp://remotehost//path/to/file` - to compare two files over two servers.

## FIND
- `sudo find / -mount -type d -iname '*vim' ` -  Find directories matching a given name, in case-insensitive mode. The flag `-mount`  is for avoid mount points.
-  `sudo find / -mount -type f -iname '*vim' ` -  Find files matching a  given name, in case-insensitive mode. The flag `-mount`  is for avoid mount points.

## RESET
- `reset`  - Restart the terminal without leaving it.  

