---
slug: /DebuggingandLogging
id: Debugging and Logging
sidebar_position: 12
sidebar_label: Debugging and Logging
---
# Debugging and Logging

Sometimes, in order to get to the bottom of a problem, we need to enable logging. This section describes how to do so on each operating system. After following the instructions in this chapter, subsequently running the Flirc application will result in a helpful log file being placed on your users desktop. The file will be appended, and not over-written.

Email log files to your support agent.

If for any reason, the flirc.ini file is not present in the respected location, copy and paste the text below, and place it in a text file called flirc.ini in the same directory as the GUI.

File Name: `flirc.ini`
```

 ; COPYRIGHT 2016 Flirc, Inc. All rights reserved.
 ;
 ; This copyright notice is Copyright Management Information under 17 USC 1202
 ; and is included to protect this work and deter copyright infringement.
 ; Removal or alteration of this Copyright Management Information without
 ; the express written permission of Flirc, Inc. is prohibited, and any
 ; such unauthorized removal or alteration will be a violation of federal law.
 ;
 ; @brief    Flirc configuration file, currently used to setup logging

[logging]              ; Protocol configuration
loglevel = 5           ; 0 = None
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