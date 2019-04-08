# Firmware

## Setup QMK Firmware
- https://github.com/qmk/qmk_firmware
- https://docs.qmk.fm/#/newbs_getting_started

## Build and burn default keymap
In your qmk directory,

#### Just building firmware
```
make plaid:default
```

#### Build and burn to plaid
After entering bootloader mode,
```
make plaid:default:program
```

## Test with wire
When you burn default keymap, test without soldering switches.   
You can use any wire and connect switch pads on pcb.

## Customize keymaps
- https://docs.qmk.fm/#/newbs_building_firmware

## If you improve firmware
Send PR!

## NEXT
[Solder switches and complete](./case.md)