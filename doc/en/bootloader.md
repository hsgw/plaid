# Bootloader

This project uses USBaspLoader as USB bootloader.
- https://www.obdev.at/products/vusb/usbasploader.html
- my customized bootloader   
https://github.com/hsgw/USBaspLoader/tree/plaid
  - When you burn bootloader to raw ATMEGA328p, don't forget write fuse bits.

## If you buy kit, already burn bootloader in ATMEGA328p.

## Windows
Needs device driver.   
You can use zadig and install ```libusbK```.
- https://zadig.akeo.ie/
- https://sparks.gogo.co.nz/usbasp_drivers.html

## Enter bootloader mode
1. Plug into USB cable
2. Push and hold ```RESET``` SW
3. Push and hold ```BOOT``` SW
4. Release ```RESET``` SW
5. Release ```BOOT``` SW

If you succeed to enter bootloader mode, you can see ```usbasp``` in device manager.

## Can't recognize bootloader
- check components and soldering near ATMEGA328p.
  - Direction of ATMEGA328p
  - BOOT SW and RESET SW
  - USB connector
  - R1,R2,R3,D49,D50

- try different USB cable, PC, USB hub
  - If you connect via USB hub, try directly.

## Test with avrdude
After recognized as ```USBasp```, run this command in terminal.   
If you don't setup QMK Firmware, please read [firmware.md](./firmware.md) in this build guide.

```
avrdude -c usbasp -p m328p
```

If there is no problem, you can see like this.

```
$ avrdude -c usbasp -p m328p
avrdude.exe: AVR device initialized and ready to accept instructions
Reading | ################################################## | 100% 0.00s
avrdude.exe: Device signature = 0x1e950f (probably m328p)
avrdude.exe done.  Thank you.
```

## NEXT
[Build and burn QMK Firmware](./firmware.md)