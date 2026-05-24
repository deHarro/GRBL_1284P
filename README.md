# My Custom GRBL v1.1 for ATmega1284p (Creality Ender-2 Board)

## ⚠️ Important Disclaimer: No Support!
This repository is a **private backup** of my personal, working firmware configuration. 
- I am **not** a professional programmer.
- I cannot provide any technical support or troubleshooting help.
- Use this code entirely at your own risk.
- Unlikely, but possible: If it bricks your board or damages your machine, you are on your own.

---

## What is this?
This is a specific copy of GRBL v1.1 adapted to run on the **ATmega1284p** chip, which is used on older green 3D printer mainboards like the **Creality v1.1.2 / v1.1.3** (from the original Ender-2). 

I am using this firmware to control a small custom DIY Mini-CNC machine using the built-in stepper drivers of the old printer board.

### Key Changes in this Version:
- Configured specifically to match the pinout of the Creality/Melzi printer board.
- Modified pin mappings to allow the connection of a custom **optical limit switch** (endstop) through the board's standard headers.

---

## 📚 Origin of the Source Code
Since standard GRBL only supports the ATmega328p (Arduino Uno), this version builds upon community ports to make it compatible with the ATmega1284p chip and standard Melzi pin layouts. 

The lineage of this specific code base is:
1. **Official GRBL v1.1** by Sonny Jeon (`gnea/grbl`) – The core CNC logic.
2. **grbl-Mega-5X (Version 1.1q)** by Gauthier Brière (`fra589`) – Which serves as the direct foundation for the 1284p register and timer configurations.
3. **My Custom Configuration** (This Repository) – 3 modified files to map the pins for the Creality Ender-2 stock board and custom optical limit sensors.

---

## How it was compiled
This exact code folder is archived here because it successfully compiles on my local Windows machine using **Visual Studio 2019** (with the *Visual Micro* extension in **Release** mode) and contains remnants of a *PlatformIO* setup (`platformio.ini`). 

I uploaded the entire project folder structure as-is to ensure it can be opened and compiled again in Visual Studio without breaking the internal file paths.

---

## Contributing / License
Feel free to fork this repository if you are building something similar and need a starting point for an ATmega1284p board. However, please do not open Issues or Pull Requests asking for help.

Based on the official open-source GRBL releases (GPLv3 License).
