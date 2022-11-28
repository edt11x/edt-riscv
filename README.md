# edt-riscv

Short scripts to get a Ubuntu RISC-V emulation up under QEMU using a Ubuntu host

## Description

Just a couple of scripts to help automate getting the RISC-V Ubuntu up and
running under QEMU on Ubuntu 22.04. 

There is a script called doit, that ideally will download Ubuntu 22.04 for the
Unmatched RISC-V embedded board, and try to setup Ubuntu QEMU and boot it.

There is a script called runit, that will just try to run the current state of
the configured Unmatched Ubuntu 22.04 QEMU.

doit is meant to be able to run again to reset the environment. With 20.04, I
found it was easy to get into a state where the image was in an unbootable
state. doit will start with the original image and boot that.

In doit, it is likely that you will have to change the release to whatever
Ubuntu has changed to. This is the current release setting:

```
UBUNTU_RELEASE=ubuntu-22.04.1-preinstalled-server-riscv64+unmatched.img
```

This is the main Wiki page to figure out what the link is currently:

[https://wiki.ubuntu.com/RISC-V](https://wiki.ubuntu.com/RISC-V)

The default login is user ubuntu, password ubuntu. On login it will prompt for
a new password and it will force you to change it.

## Getting Started

### Dependencies

doit should download the required QEMU, U-Boot, OpenSBI, toolchains, etc and
the Ubuntu 22.04 image.

### Installing

No installation, just clone into a directory from github.

### Executing program

```
$ doit
$ runit
```

