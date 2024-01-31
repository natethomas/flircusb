---
sidebar_position: 3
---

# General Usage

The commandline utility has a number of supported commands. These commands provide a 'short help' and 'long help'. To list all the commands and their short help, run the command line without any commands, or run the help command.

```
bash $ flirc_util help
flirc_util version v2.3.0 [v2.3.0-2-g3bdde39+]
  Firmware: v4.0.16 [0x4E3178B5]
Commands:
  delete         Delete next remote button flirc sees from saved database
  delete_index   Delete button at index displayed in `flirc_util settings`
  device_log     Displays the log on the device
  dfu            Kick in or out of Device Firmware Upgrade mode
  dump           Dumps contents of eeprom to console
  format         Remove all saved buttons from flirc
  help           Show this help. Also try `help <command>`
  interkey_delay set the interkey delay
  keys           Shows the recorded remote keys and their pairings
  loadconfig     Load configuration file from disk to flirc
  noise_canceler Noise canceler to prevent phantom presses
  normal         Put flirc in normal user mode
  peek           Peek EEPROM address
  profiles       enable or disable built in profiles
  reboot         Displays all the devices current settings
  record         Record infrared buttons and link them to HID keys
  record_api     Advanced button recording
  saveconfig     Save configuration file to disk
  seq_modifiers  enable or disable sequencing the modifiers
  settings       Displays all the devices current settings
  sleep_detect   Turns on sleep/suspend detection
  space          Displays information about the space used and remaining
  status         Last Flirc Status
  upgrade        Uploads new firmware image to flirc hardware
  version        Print the application version and device version if connected
  wait           Waits for the device to be plugged in (used for scripting)
```

To show the long help for any given command, use the help command, along with the command name. For example;

```
bash $ flirc_util help saveconfig
Help for `saveconfig' command:
usage: 
  saveconfig '<filname>'
example:
  flirc saveconfig ~/Desktop/boxee
```

There is even a 'long help' for the help command:

```
bash $ flirc_util help help
Help for `help' command:
usage: help [command]
  `help' with no arguments will show a list of all commands.
  `help <command>' will show a detailed help for `command'
```

Because all the commands are documented heavily within the application, it is not necessary to document them again here.
