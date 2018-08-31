# linux-kernel

## What is Kernel?

Kernel is the core component of Operating system which is a bridge between application and hardware.

## Basic functionalities of Kernel

* Kernel’s primary function is to manage the computer’s resource and allow other programs to run and use these resources.

* The Kernel is responsible for deciding which memory each process can use and also determine what to do when not enough memory is available.

* Kernel allocates request from application to perform I/O operation to appropriate device. 

* Process management, Memory management and System Calls.

## User Space and Kernel Space

* Kernel runs in Kernel space and normal programs run in user space. Kernel space is accessed by user processes only through the System calls. System calls are request by kernel like I/O or Process creation.

* Whatever normally we do in Linux system like writing text in editor, making graphical program...etc is in User space.

* Calling interrupts I/O device communication...etc comes in Kernel space.

* Main reason for separating these two spaces is improving performance and making stable system. Otherwise user data and Kernel data will be disturb with each other causing fault or errors.

## Hello world of Kernel module Programming

* Check version of your Kernel by uname –r command in terminal.

* Two files:

1. Hello.c (Our program code written)

2. Makefile (Program compilation command written)

* Function explaination:

**Init_module()**
Is init of kernel module. It registers a handler for something with kernel or it replaces any of kernel function code.

**Cleanup_module()**
Safely unload of module. It does reverse of Init_module.

**Printk()**
Use for kernel log information or warning.

* Make commands:

make -C /lib/modules/$(shell uname -r)/build M=$(PWD) modules

make -C /lib/modules/$(shell uname -r)/build M=$(PWD) clean

## Linux User Space and Kernel Space

![alt text](http://derekmolloy.ie/wp-content/uploads/2015/04/userspace-kernelspace.png)

## Fundamental Architecture of the GNU/Linux Operating System

![alt text](https://www.engineersgarage.com/sites/default/files/wysiwyg_imageupload/4214/Architecture-of-LINUX-Operating-System_0.jpg)

## Utilities to Manipulate Kernel Modules

* lsmod – List Modules that Loaded Already

* insmod – Insert Module into Kernel

* modinfo – Display Module Info

* rmmod – Remove Module from Kernel

## Reference

http://kernelx.weebly.com/linux-kernel-programming--part1.html

http://linuxkernellearning.blogspot.com/

https://www.thegeekstuff.com/2013/07/write-linux-kernel-module/?utm_source=tuicool
