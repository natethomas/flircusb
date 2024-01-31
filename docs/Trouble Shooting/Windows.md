---
sidebar_position: 1
---

# Windows Trouble Shooting

## Always Disconnected

If after installing the software, the GUI shows always disconnected, this could be one of two thing.

### 1. Device Permissions

The main reason Flirc will show as disconnected is because of permission issues. It may be necessary to run the GUI as administrator. To do that, locate the Flirc.exe in:

The location of the commandline utiltity is installed side the Graphical User interface and is installed in the C:\Program Files (x86)\Flirc directory. The application is uniquely named flirc_util.exe on windows. The application must be used and called from the windows command prompt.

`C:\Program Files (x86)\flirc`

Right click Flirc.exe, and run as administrator.

### 2. Older Version

As of writing this guide, the GUI is currently at version v3.27.10. Previous versions had an issue where windows could not open Flirc and would be left indefinitely in the 'Disconnected' state. This is now fixed, please make sure you always run the latest software.
