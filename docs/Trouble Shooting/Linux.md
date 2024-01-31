---
sidebar_position: 2
---

# Linux Trouble Shooting

## Always Disconnected

If after installing the software, the GUI shows always disconnected, this could be one of two thing.

### 1. Device Permissions

The main reason Flirc will show as disconnected is because of permission issues. It may be necessary to run the GUI as administrator. To do that, fire up a terminal, and run either the GUI or the Commandline as an administrator with the following:

`bash $ sudo Flirc`
or

`bash $ sudo flirc_util`

In order to not run the GUI or the commandline as sudo, udev rules can be used which tell the operating system to override the permissions for a particular USB device. Copy and paste the following into the file:

/etc/udev/rules.d/99-flirc.rules
```
# Flirc Devices

# Bootloader
SUBSYSTEM=="usb", ENV{DEVTYPE}=="usb_device", ATTR{idVendor}=="20a0", ATTR{idProduct}=="0000", MODE="0666"
SUBSYSTEM=="usb", ENV{DEVTYPE}=="usb_device", ATTR{idVendor}=="20a0", ATTR{idProduct}=="0002", MODE="0666"
SUBSYSTEM=="hidraw", ATTRS{idVendor}=="20a0", ATTRS{idProduct}=="0005", MODE="0666"

# Flirc Application
SUBSYSTEM=="usb", ENV{DEVTYPE}=="usb_device", ATTR{idVendor}=="20a0", ATTR{idProduct}=="0001", MODE="0666"
SUBSYSTEM=="usb", ENV{DEVTYPE}=="usb_device", ATTR{idVendor}=="20a0", ATTR{idProduct}=="0004", MODE="0666"
SUBSYSTEM=="hidraw", ATTRS{idVendor}=="20a0", ATTRS{idProduct}=="0006", MODE="0666"
```

> NOTE - If installed using the systems package manager, this file should be installed automatically

### 2. Older Version

As of writing this guide, the GUI is currently at version v3.27.10. Previous versions had an issue where windows could not open Flirc and would be left indefinitely in the 'Disconnected' state. This is now fixed, please make sure you always run the latest software.
