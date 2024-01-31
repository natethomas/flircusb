---
sidebar_position: 3
---

# Linux Installation Guide

## Installation Instructions Ubuntu i386:
```
    Add 'deb http://apt.flirc.tv/arch/i386 binary/' to /etc/apt/sources.list
    apt-get update
    apt-get install flirc
    ```
## Installation Instructions Ubuntu x64:
```
    Add 'deb http://apt.flirc.tv/arch/x64 binary/' to /etc/apt/sources.list
    apt-get update
    apt-get install flirc
    ```
> Note If you are having font issues: apt-get install ttf-mscorefonts-installer

## Software Updates

Linux software updates are automatic once the Flirc source list is added. Your Debian system will automatically prompt of software updates. If not, you can force check and force an update using the following method.

```
    bash # sudo apt-get update
    bash # sudo apt-get upgrade flirc
    ```