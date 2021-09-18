# EmpVue2-Wiki
Emporia Vue 2 Wiki

This is a place for me to keep notes as I work to understand and reverse-engineer the Emporia Engery Vue (gen 2) energy monitor.

Unfortunately, Emporia only allow using their devices through their cloud service.  That's just not for me but I like the hardware design so I've decided to build my own firmware for the device.  Am I a developer?  No.  Do I have any experience reverse engineering hardware / software?  I wish.

The Vue2 uses an ESP32 microcontroller as the primary controller.  There is also an Atmel ARM microcontroller on the board which is probably used to control a set of multiplexors which read the voltages from the 19 (!) CT channels.

## Goal
I would like to use ESPHome as the firmware to allow integration of this device into Home Assistant.  This requires that I gain some understanding of the circuit design and IO of the microcontroller.

### Path 1:
Obtain information about the hardware design and functions to provide the necessary details to create custom firmware with ESPHome.

### Path 2:
Analyze and reverse-engineer the factory firmware for the Vue2 to gain the necessary information to create custom firmware with ESPHome.

### Path 3:
Use a scope, meter and logic analyzer to understand the functionality of the device.


Tasks:
1. Gain access to the ESP32 UART interface - DONE
2. Dump the factory firmware for analysis - Partially Complete
3. Analyse the firmware by disassembly/decompliling etc. - Not Started
