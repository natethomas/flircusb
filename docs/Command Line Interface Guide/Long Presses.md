---
sidebar_position: 6
---

# Long Presses

For a discription of what macro's are, please see the Special Feature Long Press chapter.

The commandline utility allows you to record a long press. First we record our key as normal, and then, we use a special new record_lp command to record the second key as a long press.

## Long Press Example

The following example shows how we can use the arrow keys as normal, but when we press and hold the up arrow, we can send the volume up command out.

### Step 1: Record Up using the flirc_util record command

```
bash $ flirc_util record up
 Press any button on the remote to link it with 'up'

  Succesfully recorded button
```

### Step 2: Record volume up using the flirc_util record_lp command

```
bash $ flirc_util record_lp vol_up
 Press any button on the remote to link it with 'vol_up'

  Succesfully recorded button
```

## Troubleshooting

Should you get an error recording a button, it's likely due to the fact that we didn't issue a record_macro on top of an existing key. You will get an error message as follows:

```
bash $ flirc_util record_lp vol_up
  Press any button on the remote to link it with 'vol_up'

[D] lib/libflirc/firmware/fw_4.0.c fl_ver4_set_interrupt(326): Error: key not found
Error: You must first record this remote button with the regular flirc_util record command.
Example:
 flirc_util record `<first function>`
 flirc_util record_lp vol_up
```