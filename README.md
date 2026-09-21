# RP2040 Devboard

This is a compact, breakout-friendly devboard (2-layer PCB) built around the Raspberry Pi 2040 microcontroller. It contains an onboard QSPI flash, USB-C, and 30 GPIO pins broken out to dual 20-pin headers. 

It's designed as a base for embedded projects, with every usable GPIO routed to a header pin to be used on a breadboard or custom carrier PCB. 

## Components 

| Reference | Part | Description | Package | 
| ---------- | ----- | ---------- | --------- | 
| U1 | RP2040 | Dual-core MCU | QFN-56, 7x7 mm | 
| U2 | MCPI1700-3.3 | 3.3V LDO regulator | SOT-89-3 | 
| U3 | W25Q128JVS | 16 MB QSPI flash | USON-3, 3x2 mm | 
| Y1 | Crystal | 12 MHz (GND24 style) | 3.2x2.5 mm SMD | 
| J1 | USB-C receptacle | USB 2.0, 14-pin | SMD | 
| J2 | Pin header | GPIO breakout, 1x20 | 2.54 mm THT | 
| SW1 | Tactile switch | BOOTSEL button | SMD | 
| R1, R2 | 5.1kΩ | USB-C CC1/CC2 pull-downs | 0402 |
| R3, R4 | 27Ω | USB D+/D- series termination | 0402 | 
| R5, R7 | 1kΩ | Damping resistors | 0402 |
| R6 | 10kΩ | Standard resistor value from datasheet | 0402 | 
| C1 - C8, C10, C11, C17 | 0.1µF | Decoupling capacitors | 0402 | 
| C9, C12 | 1µF | Decoupling/bulk capacitors | 0402 | 
| C13, C14 | 10µF | Bulk/regulator capacitors | 0603 | 
| C15, C16 | 33pF | Crystal load capacitors | 0201 |


## Flashing and Debugging 

Connect a SWD debug probe to the header J4. 
| J4 Pin | Signal | 
| ------ | ------- |
| 1 | SWCLK | 
| 2 | SWD (SWDIO) | 
| 3 | GND | 


### Powering the Board

Power is supplied over a USB-C (VBUS, 5V) regulated down to 3.3V by U2. No external supply is required for typical use. 


## Design Files

<img width="1073" height="742" alt="image" src="https://github.com/user-attachments/assets/92b99a49-6b58-43f2-845f-723a911796bc" />

_Kinda messy schematic view_


<img width="927" height="801" alt="image" src="https://github.com/user-attachments/assets/3abfae14-1a6e-4ffc-a5ef-2937f37f5744" />

_Really messy view of PCB design_

<img width="905" height="627" alt="image" src="https://github.com/user-attachments/assets/7318f75a-bb65-4a9e-b1bc-d510b77e01a2" />

_uhhh view of the PCB 3D viewer_
