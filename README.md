# STM32WB55 Bluetooth Hardware Design (Phil's Lab Tutorial)

This repository contains my first STM32-based PCB design, created by following [Phil's Lab's YouTube series](https://youtu.be/nkHFoxe0mrU).  
The goal was to learn the fundamentals of microcontroller hardware design, RF front-ends, power supplies, best practices in schematic and PCB layout design.
It was an amazing learning experience.

---

## Overview
- **MCU**: STM32WB55
- **Power Supply**: MIC5365-3.3 LDO (USB-C 5V → 3.3V)
- **Oscillators**:  
  - 32.768 kHz LSE  
  - 32 MHz HSE  
- **RF Front-End**: U.FL connector with DLF162500LT-5028A1
- **Debug Interface**: SWD via TC2030 connector (4-pin breakout)
- **Boot/Programming**: BOOT0 switch with debouncing capacitors
- **Indicators**: Status LED
- **USB Connector**: USB-C Receptacle (USB2.0, 16-pin)

---

## Key Learnings
- Using ST application notes to correctly configure LSE/HSE oscillators, decoupling capacitors, and the VLXSMPS supply.  
- Power distribution best practices with decoupling capacitors for every supply pin.  
- Breaking out SWD pins and designing for test/debug early in the schematic.  
- Organizing schematic sheets and net classes for readability.  
- RF design basics (front-end + U.FL connector integration).  

---

## Credits
- Tutorial by [Phil’s Lab](https://www.youtube.com/@PhilsLab).  
- All mistakes, modifications, and learning notes are proudly my own.

---

## License
This project is licensed under the MIT License. See [LICENSE](LICENSE) for details.
