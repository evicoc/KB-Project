# 65% DIY Keyboard Build
This Page shows my process of building a 65% mechanical keyboard using an Arduino Pro Micro and QMK Firmware. This project is mostly DIY, with the exeption of the keycaps and the switches.

<image src="./assets/result.jpg">

## Wiring
<img src="./PCB/PCB Schematics.png">

Above are the wiring Schematics of the keyboard. It utilizes a switch matrix to accommodate the large number of switches. 

The components used are
1. Diode (1N4148)
2. Arduino Pro Micro
3. Mechanical Keyboard Switches (Gateron Yellow KS-3)
4. Button

If you look closely, you'll notice that two rows/columns are not connected to any pins on the Pro Micro. This is due to the limited number of available pins on the microcontroller.
To address this issue, we can repurpose the two LED pins on the Pro Micro as additional input pins for the switch matrix. The SMD LEDs on the microcontroller need to be desoldered to use these pins

### Wiring Options
1. Hand Soldering: The wiring is done by manually soldering wires to each component
2. Create PCB: Making and using a custom PCB can make the build neater and more organized.

Regardless of the method, ensure that all connections are secure and correctly placed according to the schematics.

Below is the custom PCB Layout that I created:

Top PCB:

<img src="./PCB/PCB Top.png">

Bottom PCB:

<img src="./PCB/PCB Bottom.png">

The PCB itself can be made at home using a copper-clad board (blank PCB) and etching solution. Currently, I am still using the hand soldering method, but I plan to switch to a custom PCB in the future

## Case & Plate
The case and plate are made using a 3D printer with a custom design. The case itself is made out of two parts and the plate is integrated with the top part of the case. The build is held together with 9 pairs of screws and threaded inserts.

<img src="./assets/Bottom case.png">

<img src="./assets/Top Case.png">

## Firmware
The firmware used in this build is generated using the KBfirmware Tool, which simplifies the process of customizing the firmware. Since my build is a basic keyboard, manually coding the firmware would be less efficient,

QMK firmware is chosen instead of the Arduino IDE because QMK is specifically designed for mechanical keyboards, offering a wide array of features and functionalities such as customizable key mapping, layers, macros, etc which is not natively supported by the Arduino IDE

## Tools Used
1. http://www.keyboard-layout-editor.com/ (To design the layout of the keyboard)
2. http://builder.swillkb.com/ (Create a template of a case based on the custom layout made)
3. https://www.tinkercad.com/ (Create a customized case based on the template)
4. https://easyeda.com/ (Design Wiring Schematics and PCB)
5. https://kbfirmware.com/ (Generate Custom Keyboard Firmware)
6. QMK Toolbox (To Flash the Firmware to the microcontroller)
