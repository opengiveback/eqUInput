![Screenshot](./amigaps2front.png)
An experimental PCB to enable using existing Arduino Nano based sourcecode to convert PS/2 mouse to Amiga mouse signals. Also has an additional Gameport connector wired to appropriate analogue input pins on Arduino Nano, to enable connecting an analogue old PC joystick, a button (for selecting mouse resolution), and even an I2C connection for PinSockets 2.54mm, to allow for connecting other I2C devices (accelerometers or screens).

Pins were selected to suit this software opensource project : https://github.com/asig/amiga-ps2-mouse-adapter

Licensed under GPL3.
The PCB is provided "AS IS", no warranties of correctness or fitness for purpose are implied nor expressed. You use the schematic on your own responsability, if you break something usig it it is not my fault. Be warned.\par

Caution! Please note!
NEVER connect Arduino Nano to  USB power source and Amiga at the same time! The design only has a diode from power source pin from Amiga joyport, to prevent powering Amiga from the device, but other considerations were not made.

The Arduino Nano can be socketed to be able to reuse it for other Arduino Nano projects! Insert Arduino Nano with USB facing DB9 connector and do not connect USB cable to inserted Arduino Nano!

This is a small revision of v1.1 of the design. As v1.0 had wrongl wired gnd, so wire had to be added from DB9 to gnd on the mounting hole of DB9 connector. I also modified and used the PCB for an PS/2 to MSX mouse convertor project, tested working OK, and I shall be adding that version to a separate repository soon.

Arduino Nano pins connections
-----------------------------
3 = P_PS2_CLK
2 = P_PS2_DATA

1 = Button MouseDPI

0 = GamePort Button1
A0 = GamePort Axis X1
A3 = GamePort Axis Y1
5 = GamePort Button2
13 = GamePort Button3
A1 = GamePort Axis X2
A2 = GamePort Axis Y2
A6 = GamePort Button4

A4, A5 = I2C connector

// Output pins
12 = P_AMIGA_V_PULSE// Purple
11 = P_AMIGA_H_PULSE// Brown
10 = P_AMIGA_VQ_PULSE// Blue
9 = P_AMIGA_HQ_PULSE// White
8 = P_AMIGA_LMB// Yellow
7 = P_AMIGA_RMB// Green
6 = P_AMIGA_MMB// Orange





![Screenshot](./amigaps2back.png)
If you make it and sell it, please consider I declare my opengiveback.org principle requirements at 15% (FAIR) of earnings. Check out more about my opengiveback.org concept at www.opengiveback.org