# Firmware

### Can't burn firmware with QMK Toolbox

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
make plaid:default:flash
```

#### avr-gcc version
With avr-gcc 8.2.0, you may encounter an error similar to `ERROR: address 0x8002a7 out of range at line 920 of .build/plaid_default.hex`. To work around this on macOS, install an older version of avr-gcc with homebrew,
```
brew uninstall avr-gcc
brew install avr-gcc@7
brew link --force avr-gcc@7
```
And then re-run `make plaid:default:flash`.

## Test with wire
When you burn default keymap, test without soldering switches.   
You can use any wire and connect switch pads on pcb.

## Customize keymaps
- https://docs.qmk.fm/#/newbs_building_firmware

## If you improve firmware
Send PR!

## NEXT
[Solder switches and complete](./complete.md)
