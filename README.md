## Linux Kernel Configuration for UART serial device

This implementation follows the labwork of an open source training 'Linux kernel and driver development' from Bootlin.

https://bootlin.com/doc/training/linux-kernel/linux-kernel-slides.pdf

https://bootlin.com/doc/training/linux-kernel/linux-kernel-labs.pdf

The hardware used for this project is BeagleboneBlack. This branch has the kernel configuration for enabling ports for the UART serial device. The configuration file can be found in https://github.com/ranjithasubramaniam/Linux-Kernel-and-Driver-Development-UART-Kernel-Config/blob/uart/arch/arm/boot/dts/am335x-customboneblack.dts

In order to facilitate continuous development of the serial device driver, the driver is compiled as a standalone (out-of-tree) kernel module. The driver is developed in the host system and deployed to the target system using NFS (Network File System) root filesystem. Once the developement is frozen, the device driver will be moved to this repository as in-tree kernel module.

The current status of the device driver for UART device can be found in the link: https://github.com/ranjithasubramaniam/Linux-Kernel-and-Driver-Development-Custom-Drivers/blob/master/nfsroot/root/serial/serial.c
