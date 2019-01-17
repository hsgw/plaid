Build Guide - PCB Rev.Alpha
===================================================================

## Caution
Rev.Alpha PCB has some issues, but it is working.
- missing 2U spacebar stabillizer mounting hole.
- value silks of R2 and R3 are wrong.(75ohm is correct.)
- silk is not so clear.

Plaid doesn't have switch mount plate.
Only for CherryMX compatible pcb mount(5pins) switch.

## parts list

Before assembly you should check number of parts.
If it has problem, please contact urkwtky[at]gmail.com.

|Ref|num||
| :- |  :- |  :- | 
|C1,C2|2|multilayer ceramic capacitor 22pF or 20pF|
|C3|1|electrolytic capacitor 10uF|
|C4,C5|2|multilayer ceramic capacitor 0.1uF|
|D1-48|48|diode|
|D49,D50|2|zener diode 3.6V|
|F1|1|polyfuse 100mA|
|J1|1|USB miniB connector|
|J2|1|2x3 pin header|
|LED1|1|3mm LED red|
|LED2|1|3mm LED green|
|R1,R7,R8|3|resistor 1.5kΩ|
|R2,R3|2|resistor 75Ω|
|R4|1|resistor 10kΩ|
|SW50,SW51|2|tactile switch|
|U1|1|ATMEGA328P with bootloader|
|Y1|1|crystal 16MHz|
|PCB|1|Main&Bottom plate|
|screw|10|M2 8mm|
|nut|30|M2|
|rubber foot|4||

### not include
- USB MiniB cable
- CherryMX compatible pcb mount(5pins) switch

## assembly tips
schematic https://github.com/hsgw/plaid/blob/master/pcb/plaid.pdf

**R2 and R3** have wrong value silk.
They are **75ohm** resistors.

Bridge LED solder jumper on soldering side if you use LEDs.


## bootloader
The bootloader is preprogrammed in MCU.    
https://github.com/hsgw/USBaspLoader/tree/plaid

### enter into flash mode
1. press and hold reset and boot sw.
2. release only reset.(hold boot sw)
3. release boot sw.

If it enters flash mode, it is revognized as "usbasp".

## windows
You should install `libusbK` driver, use [zadig](http://zadig.akeo.ie/).

## firmware
The firmware is not include official QMK repository.   

https://github.com/hsgw/qmk_firmware/tree/plaid

```make plaid:default:program```
