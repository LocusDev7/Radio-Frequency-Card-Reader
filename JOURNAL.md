---
Title: Radio Frequency Card Scanner
Author: locusdeveloper7
Description: A simple custom RF card scanner to check for access level.
Created On: 8/4/2026
---

# October 30th: Project Description & Start

I began the the project with the goal of creating a custom card scanner that could check if a student is present to class -- an attendance system. I needed a microcontroller that was strong enough to support WIFI, Memory, and Pin Configurations. And, the one that I landed with is the ESP32-S3. This microcontroller from Espressif is powerful. It includes:

* 2.4 GHz WIFI
* Bluetooth 5
* And 45 GPIO Pins

This was enough to satisfy the requirements for the project. As, the original concept came from my coding teacher, where he wanted to make this attendance system a school wide thing. Yet, having to manually debug and update each system in the school would take an enormous amount of time, so the best way to do this was to use a WIFI compatible microcontroller -- where the ESP32-S3 comes in. The first thing I did was immediately began designing the schematic with the basic peripherals like: 

1. USB-C
2. Voltage Regulator
3. Boot and Reset Buttons
4. LED Indicators, etc

Added the USB-C with a Polyfuse (a fuse that prevents over-current to the microcontroller)
<img width="541" height="560" alt="image" src="https://github.com/user-attachments/assets/7e8f5dde-4d4b-477f-8746-2529709b15d1" />

For the voltage regulator, I went with the AP2112K-3.3 because it is considered the standard and recommended. But the other reason why it is used is because the ESP32-S3 can require 350-500mA using WIFI and Bluetooth, but this regular provides a stable 600mA current, well above the required threshold. Also, the IC is compact and small enough to not take up too much space.

Datasheet: https://www.diodes.com/assets/Datasheets/AP2112.pdf

<img width="608" height="565" alt="image" src="https://github.com/user-attachments/assets/6f9b4ba2-eb17-4af1-ad05-b6ce562a7830" />
<img width="837" height="261" alt="image" src="https://github.com/user-attachments/assets/bb9a5528-de58-445f-a36d-64262deb7aae" />

**Total time spent: 30m**

# October 31st: Adding a crystal oscillator and data-line protection

The next step in the project is to actually connect the ESP32-S3 to the other peripherals. The KiCad library already has a premade symbol for the ESP32-S3 module so that takes away the external time that could have been used to make the symbol.

<img width="583" height="622" alt="image" src="https://github.com/user-attachments/assets/5344fdd3-d422-409b-bc70-d8de6383a21f" />
USBLC6-2 Datasheet: https://www.st.com/resource/en/datasheet/usblc6-2.pdf
<img width="804" height="607" alt="image" src="https://github.com/user-attachments/assets/32af156f-6431-4f05-98a5-66e5428551f3" />

I added an optional crystal oscillator in order to allow the ESP32-S3 to achieve precise timings. The documentation recommended a frequency of 32.768KHz.




