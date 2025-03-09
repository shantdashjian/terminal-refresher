# Terminal Refresher

A repo to brush up on Unix-like terminal emulator use.

![Terminal](https://upload.wikimedia.org/wikipedia/commons/thumb/9/9f/DEC_VT100_terminal_transparent.png/1920px-DEC_VT100_terminal_transparent.png)

## In This Document:
  - [What is the Terminal?](#what-is-the-terminal)
  - [What is the Shell?](#what-is-the-shell)
  - [Why](#why)
  - [How Do You](#how-do-you)
  - [.bashrc vs .bash_profile](#.bashrc-vs-.bash_profile)
  - [PATH](#path)
  - [Unix Philosophy](unix-philosophy)

## What is the Terminal?
The terminal (emulator), a.k.a. the command line, the CLI (Command Line Interface), and the console, is a text-based program, that acts as an I/O interface to the Shell.

Using the terminal is more powerful than using a GUI. It's also more flexible, performant, easier to communicate commands, and automatable.

## What is the Shell?
The Shell is a program that executes Shell Script commands and programs. Those include commands to manage the operating system, the software, and the hardware.
- There are various types of shells: sh, bash, and zsh.

## Why
> In order to command my system, 

> As a programmer,

> I must be well-versed in terminal use.

## How Do You
```
> echo "Hello, World!"
> python main.py
> whoami
> expr 1 + 1
> a=2
> echo $a
> history
> clear

> pwd
> cd ~
> cd ..
> ls -lh /absolute-path-to/directory
> lsd --tree relative-path-to/directory
> cat file.txt
> cat file1.txt file2.txt
> head a.txt # Default is 10
> head -n 5 a.txt
> tail -n 5 a.txt
> less file.txt # less is more and more. Use less
> less -N file.txt # Show lines
> touch file.py
> mkdir new-directory
> mv old-name new-name
> mv file new-location
> rm file
> rm -r directory
> cp file location
> cp -R old-dir new-dir

> grep "secret" words.txt
> grep -r "secret" .
> find direcotry -name file.txt
> find direcotry -name "*partial*"

> sudo
> chmod u=rwx,g=r,o= file.txt
> chmod -R u=rwx,g=r,o= directory
> ./program.sh # You need to put ./ to prevent the Shell from thinking this is a command to be found on the PATH
> chmod -x file.sh
> chmod +x file.sh
> sudo chown -R root directory

> which sh

#! /bin/sh
#! interpreter args

> env
> export AGE=55
> echo "Age is $AGE"

> man ls
> wc -c bytes.tx
> wc -l lines.tx
> wc -w words.tx
> curl --help
> echo $? # The error code of the last command run. 0 means no error, otheriwise (usually 1) means error.
> echo "Hello world" > stdout.txt
> echo "Hello world" 2> stderr.txt
> read NAME
> echo $NAME
> grep -R "Bob" directory | wc -l

# ctrl + c to interrupt an execution of a command or program
> kill pid
> ps aux # Show all procsses, yours and others', plus extra details

> top
> top -o mem

> sudo apt install nmap
> brew install neovim
```

## .bashrc vs .bash_profile

### .bashrc
It's for non-login terminal.

1. aliases
2. prompt settings
3. shell options
4. functions

### .bash_profile
It's for login terminals.

```
if [ -f ~/.bashrc ];then
    source ~/.bashrc
fi
```
1. environment variables
2. PATH modifications


## PATH
PATH is an environment variable that consists of a list of directory for your Shell to use to find the command to run

## Unix Philosophy
Write programs:
1. that do one thing and do it well
2. to work together
3. to handle text streams



