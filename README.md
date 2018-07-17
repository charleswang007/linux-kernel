# linux-kernel

## What is Kernel?

Kernel is the core component of Operating system which is a bridge between application and hardware.

## Basic functionalities of Kernel

* Kernel’s Primary function is to manage the computer’s resource and allow other programs to run and use these resources.

* The Kernel is responsible for deciding which memory each process can use and also determine that what to do when not enough memory is available.

* Kernel allocate request from application to perform I/O operation to appropriate device. 

* Process management, Memory management and System Calls.

## User Space and Kernel Space

* Kernel runs in Kernel space and normal programs run in user space. Kernel space is accessed by user processes only through the System calls. System calls are request by kernel like I/O or Process creation.

* Whatever normally we do in Linux system like writing text in editor, making graphical program,..Etc is in User space.

* Calling interrupts I/O device communication..Etc comes in Kernel space.

* Main reason for separating these two spaces is improve performance and making stable system. Otherwise user data and Kernel data will be disturb with each other causing fault or errors.

## Hello world of Kernel module Programming

* Check version of your Kernel by uname –r command in terminal.

* Two files:

1. Hello.c (Our Program code written)

2. Makefile (Program compilation command written)

## Reference

http://kernelx.weebly.com/linux-kernel-programming--part1.html [http://kernelx.weebly.com/linux-kernel-programming--part1.html]
