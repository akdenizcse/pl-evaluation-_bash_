# BASH

## History

Throughout UNIX history, many shells developed, but only a few of them widely used. Steve Bourne wrote a shell called "Bourne Shell", released in 1979. This was considered to be the first major one. It was made to be a scripting language that contains most of the features that are necessary to produce complex programs. It had control flow, variables, input-output control, etc. After this, another widely used shell was the C shell, written by Bill Joy. It was a lot like the C programming language and intended to be easier to use and learn for programmers. 

Bash, The Bourne-Again SHell, originally written by Brian Fox, first released in 1989. Name was a pun to the author of its direct ancestor, Steve Bourne. It was created to be used in GNU project. Bash includes the best features of C and Korn shells aside from its own advantages. The purpose of Bash was to be a standard shell for the GNU system. 
All versions of Bash since 0.99 have been freely available. Bash manages to be in every major version of UNIX and has rapidly become the most popular shell that is derived from the Bourne Shell. It is the standard shell in Linux. Chet Ramey is the current maintainer of Bash.


## Use Cases

You don't need to be a system administrator to start using Bash. Anybody who works on a UNIX-based system who wants to make life easier on themselves can greatly benefit from using it. Whether you want automation or just do some simple daily tasks. Once you know what you're doing, Bash can be the most practical tool of yours.

## Setting up an Environment

Bash is default on Linux distributions.

Mac users can use this [link](http://macappstore.org/bash/) to install Bash if it's not already installed. Some of the mac distributions don't have Bash as default.

Windows 10's new update added support for Linux environments. Windows users can follow this [link](https://www.howtogeek.com/249966/how-to-install-and-use-the-linux-bash-shell-on-windows-10/) to get started.


## Some Examples

We use Bash scripts to tell the Bash shell what it should do. Bash scripts are just a series of commands, some of them we type ourselves on the command line (ls, mv, mkdir e.g.) and for some of them, we should create a script file. Of course knowing that anything we can run normally on the command line, can be put to the script file and it'll work exactly the same and vice-versa. Also, we don't need to specify any extension, it'll work just fine, but for the convention, we should give script files .sh extension. If we want to create a script file, the only thing we should add is this "#!/bin/bash". This will tell the computer to interpret this file as a Bash script.
# 
In this example, I'm using the audacious program to play sound.
```bash
audacious ./sound.mp3
```
But let's say we want to play it at regular intervals. The following code will play the sound at 50 seconds intervals.
```bash
watch -n 50 audacious ./sound.mp3
```
# 
In this example, let's say we have some randomly named pictures in the "ss" folder and we want them to be organized. The following code will rename all the files in order.
```bash
#! /usr/bin/bash
count = 0
for i in ./ss/*; do
  mv $i ./ss/${count}.png
  ((count+=1))
done
```
# 
Now let's say for some reason you want to create a directory with the name of the nth Fibonacci number you've specified. The following code will create a directory called "37889062373143906" (80th Fibonacci number).
```bash
./script.sh 80
```
Inside the script file.
```bash
#! /usr/bin/bash
a=0
b=1
for (( i=0; i<$1; i++ ))
do
    c=$((a + b))
    a=$b
    b=$c
done
echo "creating a directory called $b"
mkdir $b
```
# Conclusion

Command-line is by far the most important tool in a computer. It provides the most efficient way to interact with the computer without any graphical interface.
What makes Bash unique is that Bash is also a scripting language, not just one-liner, we can create really complex programs to automate things or perform any tasks we want, in the most efficient way possible using our command line. In general, knowing Bash and being fluent in the command line can save an amount of time that no other language can achieve. For anyone who wants full control of their computer, this is a must-have skill.