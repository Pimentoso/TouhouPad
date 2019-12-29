Ergonomic gamepad to play Touhou Project games. Left-hand controls shoot/slow/bomb, and right hand controls movement. The bomb button is supposed to be pressed with the left thumb.

## Materials needed

- 9 mechanical switches
- 9 keycaps
- 12mm M3 screws (2)
- M3 nuts (2)
- a 3d printer
- an Arduino Pro Micro
- optionally, 9 Amoeba single switch PCBs for a cleaner wiring job
- soldering iron and wires

Use any mechanical switch you want. I'm using scraps and use a gateron yellow for slow movement, a gateron brown for shooting, and blues for the rest.

The pad has only 9 keys so we can just make a single row with 9 columns, so there's no need for diodes.

If you use the amoebas for the wiring, make sure to bridge the diode pads/holes since they're not used. This is easily done by placing some solder on the SMD diode pads until they are connected (you can also use a small strand of wire or a piece of diode leg)

Default pins used:

- Row pin: F4
- Column pin 0 (left shift): F5
- Column pin 1 (Z): F6
- Column pin 2 (X): F7
- Column pin 3 (left arrow): D7
- Column pin 4 (down arrow): C6
- Column pin 5 (right arrow): D4
- Column pin 6 (up arrow): D0
- Column pin 7 (esc): B1
- Column pin 8 (enter): D1

## Firmware

You can load the touhoupad.json file into https://kbfirmware.com/ and edit the keys. Use the compile function on that site to get the hex file.

I use QMK toolbox [https://github.com/qmk/qmk_toolbox] for easy flashing. There's a precompiled hex file in the firmware folder.

If you need to flash it after assembling, there's a hole on the bottom you can use for shorting the RESET and GROUND pins, to enter flashing mode. Stick a bent paperclip in it or something.

## Keyboard Layout Editor link

http://www.keyboard-layout-editor.com/##@_name=Touhou%20pad%3B&@_y:1.75&x:4.5&a:7%3B&=up%3B&@_x:1.5%3B&=x&_x:1%3B&=left&=down&=right%3B&@_r:15&rx:3.5&ry:1.25&y:-1&x:-1.25%3B&=esc&=enter%3B&@_r:45&rx:2.75&y:0.5&x:-2.25%3B&=shift&=z


## 3d printing directions

- use 0.2mm layer height.
- print the plate face down and VERY slow on the first layer for the letters to come out decent.
- no support needed, just punch open the screw holes after printing.