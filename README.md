# PLC-Simulation-Projects
This repository showcases a series of PLC simulation projects developed using Connected Components Workbench (CCW) and Factory I/O. It includes ladder logic diagrams, project files, and recorded simulation videos from hands-on training sessions. These projects were created as part of my learning journey in industrial automation and PLC programming.
________________________________________________________________________________________________
# Lap1 – Tank Fill & Discharge Automation
# Scenario:
  - When the Fill button is pressed:

    - After 5 seconds, the Fill Valve opens and remains open for 10 seconds.

    - Even if the Fill button is released, water continues to fill the tank for the full 10 seconds.

  - The Fill Valve then closes automatically.

  - After the Filling sensor indicates that the tank is full and drops to 0, the system waits 10 seconds, then opens the Discharge Valve for 5 seconds to empty the tank.

  - If the Discharge button is pressed at any time, the Discharge Valve opens for 10 seconds, overriding the regular sequence.

## Video

https://github.com/user-attachments/assets/efbe4fcb-cfb5-489f-bcef-619759444836
________________________________________________________________________________________________

# Lap2 – Conveyor Sorting System with Vision Sensor
# Scenario:
  - All buttons turn on the lights (Lights subroutine).

  - Pressing the Start button starts the Entry conveyor, feeding Blue Lid, Base, or Raw materials from the feeder.

    - Configure the Emitter to only feed blue products.

  - The Vision sensor detects the product and writes values to INT_IN_0:

    - Lid = 1, Base = 2, Raw = 3.

  - Based on the product type:

    - Lid → Sorter 1 turns on.

    - Base → Sorter 2 turns on.

    - Raw → Sorter 3 turns on.

    - The product waits 5 seconds before moving.

  - After 5 seconds, both the Entry conveyor and Exit conveyor start.

  - When the product reaches the exit area, the sorter stops, and the corresponding counter updates:

    - Lid → Counter 1

    - Base → Counter 2

    - Raw → Counter 3

  - The system waits for Start to restart.

  - Pressing Reset resets all outputs and counters.
# Ladder Diagram
![image](https://github.com/user-attachments/assets/decc08c5-279a-49e1-acb7-883c094358d8)
# Video
https://github.com/user-attachments/assets/0d2f0e1c-6d91-430d-b361-7356c83febea



