# Braet
![image of finished keyboard](/img/br%C3%A6t-finished.jpg)


A minimalistic 4x10 ortholinear handwired keyboard. Supports both MX or Choc spacing.

Aim of this keyboard is to be cheap and easy to make and modify it yourself. 
You do not need to order any PCB or case for this. It also only has 40 keys, so besides soldering tools, all you need to create this is:
 - 1x Elite-C microcontroller
 - 40x Low Profile Choc Switches or any MX style switches
 - 40x Low profile keycaps or MX style keycaps
 - 40x 1N4148 diodes
 - 18x M2(2mm) spacers/standoffs
 - 3D printed plate
 - Laser cut bottom plate. 3mm wood or acrylic. The 3d printed plate is quite wobbly so the bottom plate is just for stability.
 - 22-26 gauge solid core wire

## 3D printing the plate
The plate is 182mm wide, 70mm long and 1.2mm high. You can download the stl file from the file list above.

## Handwiring 
- I used this guide to learn how to handwire. 
- https://docs.qmk.fm/#/hand_wire?id=hand-wiring-guide
- Is not as hard on this keyboard since it has fewer keys and is ortholinear
- Note down which rows and columns go to which pin on the microcontroller, this should be updated in the MATRIX variables in `/qmk/config.h`.

![image of keyboard soldered rows and columns](/img/br%C3%A6t-soldered-rows-and-columns.jpg)
![image of keyboard soldering finished](/img/br%C3%A6t-soldered-to-microcontroller.jpg)

## Firmware
- For setting up the keyboard in QMK you can update the `rules.mk` and `config.h` files in `/handwired/pilcrow`.
- After that you can use the default layout from the pilcrow and compile the firmware with `qmk compile -kb handwired/pilcrow -km default
`.
- For flashing the Elite-C microcontroller you need to install QMK Toolbox, then when it is open you need to plug in the keyboard and short the `reset` and `ground` pins. This will put it into bootloader mode and QMK Toolbox should be able to find the keyboard. Then you just select the compiled firmware and start flashing.


