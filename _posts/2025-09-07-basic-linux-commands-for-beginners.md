---
title: Basic Linux commands for beginners
date: 2025-09-07 8:00 PM
categories: [Linux]
tags: [linux]
---

Learning how to navigate the Linux terminal is a valuable skill to have, and in this post, I'm going to go over some basic Linux commands for beginners. If you've never worked with a terminal before, it may seem intimidating at first, but it's not as scary as it seems. All it takes is some time and practice, and before you know it, you'll be navigating the Linux terminal like a pro. I hope you find this guide useful and that it helps you on your Linux journey.

## Basic Linux commands

### pwd

The `pwd` command displays the full path of the current working directory. This is useful for seeing where you're at within the file system.
```shell
pwd
```

![Screenshot of the pwd command](https://res.cloudinary.com/do8uy1fxa/image/upload/v1756918830/pwd-command_fnjafk.png)

### ls

You can use the `ls` command to list the contents of a directory. To view the contents of the current directory use `ls`. To view the contents of another directory use `ls` followed by the directory path. Some popular options include `ls -l`, which displays a long listing format, and `ls -a`, which shows all files, including hidden ones.
```shell
ls
```
The screenshot below shows the difference between the output with the `ls` and `ls -l` commands.

![Screenshot of the ls command](https://res.cloudinary.com/do8uy1fxa/image/upload/v1756918735/ls-command_f6w1vm.png)

### cd

You can change directories using the `cd` command followed by the directory path. Some popular options for the `cd` command include `cd ..` to move up one directory level, `cd -` to switch to the previous working directory, and `cd ~` to switch to your home directory.
```shell
cd [directory]
```
In the screenshot below, I used the `cd` command to change to the Documents directory. I then moved up one directory with `cd ..` and back to the previous Documents directory with `cd -`. Finally, I used the `cd ~` command to change to the home directory.

![Screenshot of the cd command](https://res.cloudinary.com/do8uy1fxa/image/upload/v1756918621/cd-command_lyj3r7.png)

### mkdir

To create a new directory, use the `mkdir` command followed by the directory name.
```shell
mkdir new_directory
```
In the example below, I created a directory called testdirectory using the `mkdir` command, and then ran `ls` to show that it was created.

![Screenshot of the mkdir command](https://res.cloudinary.com/do8uy1fxa/image/upload/v1756918785/mkdir-command_tdvfjs.png)

### rmdir

To remove an empty directory use the `rmdir` command.
```shell
rmdir directory
```
In the example below, I used the `rmdir` command to remove the directory named testdirectory and then ran the `ls` command to show that it was deleted.

![Screenshot of the rmdir command](https://res.cloudinary.com/do8uy1fxa/image/upload/v1756918875/rmdir-command_i1g5ql.png)

### rm

The `rm` command is used to remove a file. You can also use `rm -r` to remove a non-empty directory.
```shell
rm file
```
The example below shows the removal of the file testfile.txt using the `rm` command. It then shows the failed removal of the non-empty directory testdirectory using the `rmdir` command, and the successful removal using the `rm -r` command.

![Screenshot of the rm command](https://res.cloudinary.com/do8uy1fxa/image/upload/v1757092962/rm-command_cniebw.png)

### mv

The `mv` command is used to move or rename files and directories.
```shell
mv file destination
mv old_filename new_filename
```
In the example below, I used the `mv` command to move testfile.txt to Documents/testdirectory, and then ran `ls` to show that it moved.

![Screenshot of the mv command](https://res.cloudinary.com/do8uy1fxa/image/upload/v1756918808/mv-command_d8rk8j.png)

### cp

The `cp` command is used to copy files or directories.
```shell
cp file destination
```
The example below shows the `cp` command used to copy the file testfile.txt to Documents/testdirectory.

![Screenshot of the cp command](https://res.cloudinary.com/do8uy1fxa/image/upload/v1756918671/cp-command_uf1u5l.png)

### cat

To display the contents of a file you can use the `cat` command.
```shell
cat file
```
In the example below, I used the `cat` command to display the contents of testfile.txt.

![Screenshot of the cat command](https://res.cloudinary.com/do8uy1fxa/image/upload/v1756918534/cat-command_isknvg.png)

### touch

You can use the `touch` command to create a new empty file.
```shell
touch new_file
```
The example below shows the `touch` command used to create the new empty file testfile.txt.

![Screenshot of the touch command](https://res.cloudinary.com/do8uy1fxa/image/upload/v1756918900/touch-command_prfzxp.png)

### find

The `find` command is used to search for files or directories within a specified path. To search for a file, use the `-name` parameter or `-iname` parameter for a case-insensitive search. To search for only directories, use the `-type d` parameter.
```shell
find directory_path parameter
```
In the example below, I used the `find` command to search for the file testfile.txt in the current directory.

![Screenshot of the find command](https://res.cloudinary.com/do8uy1fxa/image/upload/v1756918697/find-command_hc6nti.png)

### grep

The `grep` command is used to search for a string of text within a file.
```shell
grep "pattern" file
```
In the example below, I used the `grep` command to search for the word "Hello" within testfile.txt.

![Screenshot of the grep command](https://res.cloudinary.com/do8uy1fxa/image/upload/v1756918714/grep-command_xe1dak.png)

### man

You can use the `man` command to view the manual page for a specific command. The man pages provide detailed documentation on the various Linux commands and utilities.
```shell
man command
```
The example below shows the man pages for the `ls` command.

![Screenshot of the man command](https://res.cloudinary.com/do8uy1fxa/image/upload/v1756918752/man-command_abhikb.png)
![Screenshot of the ls command man pages](https://res.cloudinary.com/do8uy1fxa/image/upload/v1756918767/man-command-output_urcbxw.png)