---
sidebar_position: 3
---

# Advanced Pairing

A provided a pairing profile might not be enough for some users needs. It's also possible that some users would like to drill down certain advanced features or configurations.

## Keyboard Keys

The second best way to do any advanced pairing is through the keyboard controller. Remember, any application or device always supports keyboard keys. Hook up a keyboard, figure out how keys are mapped, and write them down. Use the keyboard controller to pair those keys manually with your remote. Then, email us or start a forum thread and share what you've found. We'll bring official support for your device or application into the GUI.



## Modifiers

Like all keyboards, there are modifiers keys which include:

1. control (left)
2. alt (left)
3. command/windows (left)
4. shift
5. caps lock.
6. control (right)
7. alt (right)
8. control (right)

Any or all modifiers can be combined with any keyboard key, however, only one keyboard key can ever be paired. For example, the following is a valid pairing: ```LEFT_CONTROL + SHIFT + 'A'```

Just like a regular keyboard, this is a valid input. An ***invalid*** input is: `LEFT_CONTROL + 'A' + 'F'` or just `'A' + 'F'`

Just like a regular keyboard, a user can not send two letters at a time.

## Modifiers Advanced

The modifiers are defined as follows. This is helpful if a user wants to use the `flirc_util record_api` command
```
#define MOD_CTRL_LEFT           (1<<0)
#define MOD_SHIFT_LEFT          (1<<1)
#define MOD_ALT_LEFT            (1<<2)
#define MOD_COMMAND_LEFT        (1<<3)
#define MOD_CTRL_RIGHT          (1<<4)
#define MOD_SHIFT_RIGHT         (1<<5)
#define MOD_ALT_RIGHT           (1<<6)
#define MOD_COMMAND_RIGHT       (1<<7)
```
More information on the record_api command can be found in the command line interface guide of this document.

## Key Definitions

Tooltips are used to help the user determine the meaning behind virtual keys. Hold the mouse over a given key for ~5 seconds and a tooltip will be shown for the specific key. This is helpful if the specific icon of the key is not obvious.

