---
sidebar_position: 5
---

# Macro Usage

For a discription of what macro's are, please see the Special Feature Macro chapter.

The commandline utility allows you to record a macro. The following section will outline several examples.

## Example 1: "hello"

The following example shows how to use the commandline utility to send the word 'hello' on a single remote control press. To do this, we must first record the letter 'h', then record the remainder as macros on top of 'h'. Below will show the complete working example of this:

```
bash $ flirc_util record h
 Press any button on the remote to link it with 'h'

  Succesfully recorded button

bash $ flirc_util record e
 Press any button on the remote to link it with 'e'

  Succesfully recorded button

bash $ flirc_util record l
 Press any button on the remote to link it with 'l'

  Succesfully recorded button

bash $ flirc_util record l
 Press any button on the remote to link it with 'l'

  Succesfully recorded button

bash $ flirc_util record o
 Press any button on the remote to link it with 'o'

  Succesfully recorded button
```

## Example 2: Long Press to Macro

Say we wanted to use a remote control button as a standard button. But when we held down that same button, we wanted to have it act as a macro. The following example will show how to do this. In this example, on normal usage, the key will act as the 'enter' key. However, if we hold the button down for half a second, we want it to sound out 'Escape' + 'down'

### First record the normal key, enter:

```
bash $ flirc_util record enter
 Press any button on the remote to link it with 'enter'

  Succesfully recorded button
```

### Now let's convert the key into a long press to the first macro key:

```
bash $ flirc_util record_lp escape
 Press any button on the remote to link it with 'escape'

  Succesfully recorded button
```

### Now let's assign the second macro key:

```
bash $ flirc_util record_macro down
 Press any button on the remote to link it with 'down'

  Succesfully recorded button
```

> Note Pay attention, in the first step, we used record, the second record_lp, then record_macro

## Troubleshooting

Should you get an error recording a button, it's likely due to the fact that we didn't issue a record_macro on top of an existing key. You will get an error message as follows:

```
bash $ flirc_util record_macro o
Press any button on the remote to link it with 'e'

[D] lib/libflirc/firmware/fw_4.0.c fl_ver4_set_interrupt(326): Error: key not found
Error: You must first record this remote button with the regular flirc_util record command.
Example:
 flirc_util record `<first function>`
 flirc_util record_macro e
```