---
sidebar_position: 3
---

# Linux

To enable logging on linux, fire up a terminal, and using your favorite text editor, create the flirc.ini file

```bash # sudo vi /usr/bin/flirc.ini```    
Copy and paste the text in the file:
```
; COPYRIGHT 2016 Flirc, Inc. All rights reserved.
;
; This copyright notice is Copyright Management Information under 17 USC 1202
; and is included to protect this work and deter copyright infringement.
; Removal or alteration of this Copyright Management Information without
; the express written permission of Flirc, Inc. is prohibited, and any
; such unauthorized removal or alteration will be a violation of federal law.
;
; @brief Flirc configuration file, currently used to setup logging

[logging]             ; Protocol configuration
loglevel = 5          ; 0 = None
; 1 = Error
; 2 = Warning
; 3 = Info
; 4 = Debug
; 5 = Verbose

libusb = true         ; Log libusb events
logtofile = true      ; True or true
append = true         ; Append or create new log file
file = flirc_log.txt  ; File to Log
desktop = true        ; Save file to Desktop, this should be set for windows
```

Save the file, that's it. Running the GUI will now place a log file on the desktop. To disable logging, change the loglevel to zero in the flirc.ini file.
