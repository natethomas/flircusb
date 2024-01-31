---
sidebar_position: 1
---

# Versioning

There are separate versioning schemas for both the GUI and the Firmware. The firmware has two components, the run time application known as Flirc, and a special piece of firmware called the bootloader, which only has one purpose, to upgrade the application image. The bootloader and application are both independently versioned. The bootloader can never be upgraded, however, the application version can, and is upgraded very often.

All versioning schema's conform to the open semantic versioning schema. More information about semver can be found here.

## GUI Versioning

The GUI Version is found in the title bar. The GUI version will always be the same on Linux, Windows, or a Mac. Never is one system updated and not the other. An update for a bug on windows, will result in a new version for all operating systems.

## Firmware Versioning

The firmware version is always shown in the bottom left corner. There are three components to the version, Major.Minor.Patch.

For example, v4.0.16:

- Major = 4
- Minor = 0
- Patch = 16


The meanings are as follows:
```
A Major Firmware Version - denotes a new major feature release.
A Minor Firmware Version - denotes an update to a fundamental internal working of the firmware which would render the previous version of the GUI incompatble with this new firmware
A Patch Firmware Version - denose an update to a bug. No upgraded GUI is needed
```
The firmware version is revision locked to the GUI. If the firmware Minor or Major version is incremented, it will not be compatible with previous versions of the GUI.

## Bootloader Versioning

Unlike the Firmware version, the bootloader is not version locked to the GUI. The bootloader will never be updated, and users need not to be concerned about it. The bootloader version is in the same location is the firmware version, and shows up only during an upgrade. Currently, there is no other means to get the bootloader version outside of issuing a firmware upgrade.

The picture below shows the bootloader version during an upgrade.


The bootloader version will never change. There are no bootloader upgrades, oherwise we would need a bootloader loader. And that's too much inception for me.
