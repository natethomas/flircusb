---
sidebar_position: 5
---

# Saving a Configuration

Saving a configuration is simple and is recommended in order to backup your hard work, or simply to save it and put it on another device.

You should see a progress bar under the Flirc Logo and saving a configuration should take a matter of seconds.



## Flirc Configuration File

Saving a configuration is simple and is recommended in order to backup your hard work, or simply to save it and put it on another device. The file is proprietary format, and has the suffix fcfg to denote 'flirc configuration'.

More information is provided in the flirc API documentation.
``` 
struct header_t {
    /* magic identifier */
    uint32_t magic;
    /* major version */
    uint16_t major;
    /* minor version */
    uint16_t minor;
    /* size of used space */
    uint32_t size;
    /* crc of eeprom not including header */
    uint32_t crc;
} __alias __packed;

struct settings_t {
    uint32_t alg;
    uint32_t timing;
    uint32_t general;
} __alias __packed;

struct ir_pattern_t {
    /* recorded hash */
    uint32_t hash;
    /* time elapsed to next pulse in ms */
    uint32_t te;
    /* not used yet, pointer to next key to send */
    uint32_t next;
    /* boolean if we should do a long press */
    uint8_t lp;
    /* usb report ID */
    uint8_t report_id;
    /* high byte in packet for USB */
    uint8_t modifier;
    /* low byte in packet for USB */
    uint8_t key;
} __alias __packed;
```     