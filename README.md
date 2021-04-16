Ergonomic gamepad to play Touhou Project games. Left-hand controls shoot/slow/bomb, and right hand controls movement. The bomb button is supposed to be pressed with the left thumb.

![Rendering](https://raw.githubusercontent.com/Pimentoso/TouhouPad/master/images/screen.png)

## Materials needed

- 9 cherry MX compatible switches
- 9 keycaps
- 12mm M3 screws (2x)
- M3 nuts (2x)
- an Arduino Pro Micro (5v model)
- optionally, 9 Amoeba single switch PCBs for a cleaner wiring job
- soldering iron and wires
- a 3d printer

The pad has only 9 keys so we can just make a single row with 9 columns, so there's no need for diodes.

If you use the amoebas for the wiring, make sure to bridge the diode pads/holes since they're not used. This is easily done by placing some solder on the SMD diode pads until they are connected (you can also use a small strand of wire or a piece of diode leg)

Wiring table:

| matrix pin | firmware pin | pro micro pin |
| --- | --- | --- |
| Row 0 | F4 | A3 |
| Column 0 (left shift) | F5 | A2 |
| Column 1 (Z key) | F6 | A1 |
| Column 2 (X key) | F7 | A0 |
| Column 3 (left arrow) | D7 | 6 |
| Column 4 (down arrow) | C6 | 5 |
| Column 5 (right arrow) | D4 | 4 |
| Column 6 (up arrow) | D0 | 3 |
| Column 7 (esc key) | B1 | 15 |
| Column 8 (enter key) | D1 | 2 |

Ugly schematics: (note: it's the bottom view of the plate)

![Schematics](https://raw.githubusercontent.com/Pimentoso/TouhouPad/master/images/schematics.png)

## Firmware

You can load the touhoupad.json file into https://kbfirmware.com/ and edit the keys. Use the compile function on that site to get the hex file.

![Layout](https://raw.githubusercontent.com/Pimentoso/TouhouPad/master/images/layout.png)

I use QMK toolbox [https://github.com/qmk/qmk_toolbox] for easy flashing. There's a precompiled hex file in the firmware folder.

If you need to flash it after assembling, there's a hole on the bottom you can use for shorting the RESET and GROUND pins, to enter flashing mode. Stick a bent paperclip in it or something.

## Keyboard Layout Editor link

http://www.keyboard-layout-editor.com/##@_name=Touhou%20pad%3B&@_y:1.75&x:4.5&a:7%3B&=up%3B&@_x:1.5%3B&=x&_x:1%3B&=left&=down&=right%3B&@_r:15&rx:3.5&ry:1.25&y:-1&x:-1.25%3B&=esc&=enter%3B&@_r:45&rx:2.75&y:0.5&x:-2.25%3B&=shift&=z


## 3d printing directions

- use 0.2mm layer height.
- print the plate face down and VERY slow on the first layer for the letters to come out decent.
- no support needed, just punch open the screw holes after printing.