---
Title: Radio Frequency Card Scanner
Author: locusdeveloper7
Description: A simple custom RF card scanner to check for access level.
Created On: 8/4/2026
---

# August 4th: Project Start

The first thing I did was to come up with some potential project ideas that were not too generic. I remember my coding teacher at my high school mentioned something about creating an ID scanner for the rooms doors. So that is what inspired me to pursue this project. However, I immediately had the idea to use an ESP32-S3 because I was already familiar with it from another project and because it provides WIFI and Bluetooth, which would be useful for the project as will be mentioned later on.

<img width="1225" height="869" alt="Screenshot 2026-08-06 193710" src="https://github.com/user-attachments/assets/51da3e20-417a-46cc-87a0-f368030fc013" />

**Total Time Spent: 30m**

# August 5th: Schematic Drawing

I am going to be completely honest for these initial stages. Google Gemini was used in order to recommend possible integrated circuits that could be used and also capacitor and resistor values. I also used it to check my schematic from time to time just to make sure that I am correctly placing components on the schematic correctly. 

The entire list of things that I added to the schematic:

* Buzzer (to notify card was detected)
* RF Controller, Filter, and Power
* LED Access Level & Power Indicator
* UART Pin Section
* Battery Charger & Cell
* Power Network (using multi Schottky diode and switch)
* LCD Display
* And Micro SD Card

<img width="1226" height="868" alt="Screenshot 2026-08-06 193839" src="https://github.com/user-attachments/assets/231f263b-3032-490b-be47-4090ebed8f79" />

**Total Time Spent: 4h**

# August 6th: Schematic Adjustments

Upon reviewing my schematic from a fresh mind, I decided to remove the LCD Display from the project. This is so that I won't have to spend more time organizing space in the PCB editor for many more hours, and it is easier to just have pin headers wire it up.
<img width="1224" height="866" alt="Screenshot 2026-08-06 201009" src="https://github.com/user-attachments/assets/cd8e51d5-84af-449b-84ab-91ed8cb29d3f" />

Also, I removed the pins DB4-DB7 because the LCD display, which I had bought from an electronics kit, uses a custom integrated circuit to program the screen using just two pins -- SDA and SCL.

<img width="353" height="383" alt="Screenshot 2026-08-06 200625" src="https://github.com/user-attachments/assets/31dfa9f2-dc89-432a-b459-85a67b7fc79c" />
<img width="702" height="655" alt="Screenshot 2026-08-06 200332" src="https://github.com/user-attachments/assets/284ffbcc-8504-4b4b-ba1c-7c723eb6f73f" />
