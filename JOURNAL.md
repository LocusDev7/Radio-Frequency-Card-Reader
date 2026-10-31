---
Title: Radio Frequency Card Scanner
Author: locusdeveloper7
Description: A simple custom RF card scanner to check for access level.
Created On: 8/4/2026
---

# October 30th: Project Start

I began the the project with the goal of creating a custom card scanner that could check if a student is present to class -- an attendance system. I needed a microcontroller that was strong enough to support WIFI, Memory, and Pin Configurations. And, the one that I landed with is the ESP32-S3. This microcontroller from Espressif is powerful. It includes:

* 2.4 GHz WIFI
* Bluetooth 5
* And 45 GPIO Pins

This was enough to satisfy the requirements for the project. As, the original concept came from my coding teacher, where he wanted to make this attendance system a school wide thing. Yet, having to manually debug and update each system in the school would take an enormous amount of time, so the best way to do this was to use a WIFI compatible microcontroller -- where the ESP32-S3 comes in. The first thing I did was immediatelly began designing the schematic with the basic peripherals like: 

1. USB-C
2. Voltage Regulator
3. Boot and Reset Buttons
4. LED Indicators, etc
