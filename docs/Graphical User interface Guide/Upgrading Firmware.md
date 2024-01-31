---
sidebar_position: 9
---

# Upgrading Firmware

Firmware updates are delivered through the GUI. Unless a beta image is received through flirc.tv, the forums, or the staff at flirc, never should a user upload a firmware version received online from an uncredible source. Firmware images are delivered encrypted, and can be verified for aunthenticity if needed.

It would be rare to receive a raw image by itself.

## Checking for Firmware Updates

Firmware updates are provided alongside GUI updates. When starting the GUI, the firmware embedded in the GUI is checked against the firmware on the device. If there is an update, the GUI will prompt for upgrade, while also detailing the changelog of the firmware. It is not required to update the firmware, only highly recommend.


Firmware update announcements are provided on the company blog, forum, and twitter. You can also subscribe to our newsletter found on the bottom of the flirc.tv home page.

## Upgrading the Firmware

After selecting Yes, on the prompt, the GUI will automatically upgrade the firmware which involves three steps, all completely automated that don't require user intervention.

Put the Device in the Bootloader
Upload the new Image
Check the device has succesfully upgraded and notify user
There is a progress bar visible during the upgrade. The entire process takes 30 seconds. Should the update take longer, the progress bar be stopped, or the GUI hung, something has gone wrong, force quit the GUI.

> Important - Do not worry, there are many safe gaurds in the firmware, and the device can not be bricked