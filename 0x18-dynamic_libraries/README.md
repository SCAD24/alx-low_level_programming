# 0x18. C - Dynamic Libraries

## Overview

This project dives into the world of dynamic libraries in the C programming language. It is an ongoing second chance project started on Jan 29, 2024, and must be completed by Feb 3, 2024, with an auto review scheduled at the deadline.

## Learning Objectives

At the end of this project, you should be able to:

- Explain what a dynamic library is, how it works, how to create one, and how to use it.
- Understand the environment variable `$LD_LIBRARY_PATH` and its usage.
- Recognize the differences between static and shared libraries.
- Utilize basic tools such as `nm`, `ldd`, and `ldconfig` for library management.

## Resources

Read or watch:

- [Difference between Dynamic and Static library (Static and Dynamic linking)](https://www.geeksforgeeks.org/static-vs-dynamic-libraries/)
- [Create dynamic libraries on Linux](https://www.cprogramming.com/tutorial/shared-libraries-linux-gcc.html)

## Copyright - Plagiarism

It's crucial to remember that coming up with solutions for the tasks independently is essential to meet the learning objectives. Avoid copying and pasting someone else's work. Plagiarism is strictly forbidden and may result in removal from the program.

## Requirements

### C

- Allowed editors: vi, vim, emacs
- Compilation on Ubuntu 20.04 LTS using `gcc` with the options `-Wall -Werror -Wextra -pedantic -std=gnu89`
- All files should end with a new line
- A `README.md` file, at the root of the project folder, is mandatory
- Code should adhere to the Betty style
- No global variables allowed
- No more than 5 functions per file
- The standard library is not allowed, except for `_putchar`
- Push your `main.h` file containing prototypes for all functions
- Don't forget to push your header file

### Bash

- Allowed editors: vi, vim, emacs
- Scripts will be tested on Ubuntu 20.04 LTS
- All files should end with a new line
- The first line of all files should be exactly `#!/bin/bash`
- A `README.md` file, at the root of the project folder, should describe the purpose of each script
- All files must be executable

## Tasks

### 0. A library is not a luxury but one of the necessities of life

Create the dynamic library `libdynamic.so` containing various functions specified in the task. Make sure to push your `main.h` file with prototypes.

Example usage:

```bash
$ ls -la lib*
-rwxrwxr-x 1 user user 13632 Jan 7 06:25 libdynamic.so
$ nm -D libdynamic.so
# (output showing symbols and addresses)
$ gcc -Wall -pedantic -Werror -Wextra -L. 0-main.c -ldynamic -o len
$ ldd len
# (output showing linked libraries)
$ export LD_LIBRARY_PATH=.:$LD_LIBRARY_PATH
$ ldd len
# (output showing linked libraries with dynamic library in current directory)
$ ./len
# (output based on the executed program)
```

### 1. Without libraries what have we? We have no past and no future

Create a script `1-create_dynamic_lib.sh` that compiles all `.c` files in the current directory into a dynamic library called `liball.so`.

Example usage:

```bash
$ ls *.c
abs.c   isalpha.c  islower.c  memcpy.c  putchar.c  strcat.c  strcmp.c  strlen.c   strncpy.c  strspn.c
atoi.c  isdigit.c  isupper.c  memset.c  puts.c     strchr.c  strcpy.c  strncat.c  strpbrk.c  strstr.c
$ ./1-create_dynamic_lib.sh
$ nm -D --defined-only liball.so
# (output showing symbols and addresses)
```

### 2. Let's call C functions from Python

Create a dynamic library `100-operations.so` with C functions that can be called from Python. An example Python script `100-tests.py` is provided to demonstrate calling these functions from Python.

Example usage:

```bash
$ python3 100-tests.py
# (output based on executed Python script)
```

### 3. Code injection: Win the Giga Millions!

Write a shell script `101-make_me_win.sh` that, when executed on the server, will increase the chances of winning the Giga Millions jackpot. The script should run two commands, not exceeding three lines, and not containing certain characters. Detailed instructions are provided in the task.

Example usage:

```bash
$ . ./101-make_me_win.sh
$ rm 101-make_me_win.sh
$ ls -la
# (output showing the contents of the directory)
$ history -c
$ clear
$ ls -la
# (output showing the contents of the directory after clearing history and terminal)
$ md5sum gm
# (output showing the MD5 checksum of the program gm)
$ ./gm 9 8 10 24 75 9
# (output based on the executed program)
$ exit
```
