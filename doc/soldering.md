# Assembly

## Before starting assembly
- Check the components are complete. See [BOM](assembly.md). 
- If you are not used to soldering, learn how to solder components.
  - https://learn.adafruit.com/adafruit-guide-excellent-soldering/tools

## Soldering
### Zener diodes (D49,50)
Solder D49 and D50.   
Diode is a `polarized` component and therefore take care of direction.   
A Black line on diode is cathode. (square pad on pcb)
![zener diode](./img/assembly/1.JPG)

### Resistors (R1,2,3,4,7,8)
Solder resistors.
Don't place on R5 and R6. (They are for i2c)

| Ref    | Value | Color code              |
|--------|-------|-------------------------|
| R1,7,8 | 1.5k  | Brown/Green/Red/Gold    |
| R2,3   | 75    | Purple/Green/Black/Gold |
| R4     | 10k   | Brown/Black/Orange/Gold |
| R5,6   | I2C   | Do not place            |
![resistor](./img/assembly/2.JPG)

### Diodes 1N4148 (D1-48)
Diode is a `polarized` component and therefore take care of direction.
A Black line on diode is cathode. (square pad on pcb)
![1N4148](./img/assembly/3.JPG)

### Crystal
![crystal](./img/assembly/4.JPG)

### Capacitors (C1,2,4,5)
There are 2 kinds of lead pitch.

| Ref  | Value | Lead pitch |
|------|-------|------------|
| C1,2 | 22pF  | 2.5mm      |
| C4,5 | 0.1uF | 5mm        |
![MLCC](./img/assembly/5.JPG)

### USB connector
Narrow pitch! Be careful of solder bridge between pins. 
![USB](./img/assembly/6.JPG)

### LEDs
LED is a `polarized` component and therefore take care of direction.
A short leg is cathode. (square pad on pcb)
![LED](./img/assembly/7.JPG)

If you use leds, make bridge J4 and J5 on bottom side.
![LED jumper](./img/assembly/8.JPG)

### IC socket
Solder IC socket.
IC socket is a `polarized` component and therefore take care of direction.
Check the notch on silk and IC Socket.  
![ic socket](./img/assembly/9.JPG)

### Electrolytic capacitor(C3) and Resettable fuse(F1)
Electrolytic capacitor is a `polarized` component and therefore take care of direction.
A short leg is cathode. (square pad on pcb)

And after soldering resettable fuse, bend like the image. 
![Electrolytic capacitor and resettable fuse](./img/assembly/10.JPG)

### Tactile Switch(SW50,51) and pin header
![SW and pin header](./img/assembly/11.JPG)

### ATMEGA328p
Insert ATMEGA328P into IC Socket.

ATMEGA328 is a `polarized` component and therefore take care of direction.
See the image.
![ATMEGA328p](./img/assembly/12.JPG)

## Check list before connect USB
- No short between VCC and GND, USB connector pins.
- Direction of polarized components.(ATMEGA328p, diode, resettable fuse, electrolytic capacitor)
- Resistor value

## NEXT
[Connect USB cable and test bootloader](./bootloader.md)