# 65% DIY Keyboard Build
This Page will show my process of building a 65% mechanical keyboard using an Arduino Pro Micro and QMK Firmware. This project is mostly DIY, with the exeption of the keycaps and the switches.

## Wiring
<img src="./PCB/PCB Schematics.png">

Above is the wiring Schematics of the keyboard. It utilizes a switch matrix to accommodate the large number of switches. 

The components used are
1. Diode (1N4148)
2. Arduino Pro Micro
3. Mechanical Keyboard Switches (Gateron Yellow KS-3)
4. Button

If you look closely, you'll notice that two rows/columns are not connected to any pins on the Pro Micro. This is due to the limited number of available pins on the microcontroller.
To address this issue, we can repurpose the two LED pins on the Pro Micro as additional input pins for the switch matrix. To do so, the SMD LED on the microcontroller needs to be desoldered.

### Wiring Options
1. Hand Soldering: The wiring is done by manually soldering wires to each component
2. Create PCB: Making and using a custom PCB can make the build neater and more organized.

Regardless of the method, ensure that all connections are secure and correctly placed according to the schematics.
