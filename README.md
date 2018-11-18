# Orbit keyboard
A split ergonomic keyboard for all

![Render Image](https://raw.githubusercontent.com/ai03-2725/Orbit/master/Images/PCB-R2.0.jpg)

## Features
- Ergonomic layout based on the [crkbd](https://github.com/foostan/crkbd)
- All on-board components; no separate controller board
- USB Type-C and in-switch backlight
- Alps SKCL/M and MX compatibility
- Built-in overcurrent, reverse voltage, and ESD protection.
- Pre-panelized in a single PCB file for easy production
- Keyboard-Layout-Editor data is available [here](http://www.keyboard-layout-editor.com/#/gists/53ebf59524de12515cb7e2e6de94f0d6).

## Designed for all
- This keyboard remains close to typical QWERTY layout in key positioning.
- Most keys remain in their typical locations, which allows easy migration from standard layout keyboards.
- Whether new to ergonomic layouts or already an avid adopter, Orbit will suit your needs.

## Electrical side
- The incoming power is handled as shown:
![Diagram](https://raw.githubusercontent.com/ai03-2725/Orbit/master/Images/Power.png)
- VCC/Raw is the raw power fed through the USB connector. The ESD protection IC is bound to here.
- VBUS is "stable raw power" after being passed through a polyfuse. Used for upstream detection, for a downstream Schottky diode prevents flow from 5V into VBUS. In other words, VBUS is only at 5V when fed from upstream USB.
- 5V is the "stable power" after passing through a Schottky diode. Used for powering MCU, LEDs, and other split half. Power from the other half feeds here, for it has already been filtered on the other side.
- Measures are taken to isolate the LED, MCU, and split connection 5V as upstream as possible, to prevent interference.

