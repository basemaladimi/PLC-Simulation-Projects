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
  - All buttons turn on the lights.
  - Pressing the Start button starts the Entry conveyor, feeding Blue Lid, Base, or Raw materials from the feeder.
    - Configure the Emitter to only feed blue products.
  - The Vision sensor detects the product and writes values to INT_IN_0:
    - Lid = 1, Base = 2, Raw = 3.
  - Based on the product type:
    - Lid → Sorter 1 turns on.
    - Base → Sorter 2 turns on.
    - Raw → Sorter 3 turns on.
    - The product waits 5 seconds before moving.
  - After 5 seconds, both the Entry conveyor and the Exit conveyor start.
  - When the product reaches the exit area, the sorter stops, and the corresponding counter updates:
    - Lid → Counter 1
    - Base → Counter 2
    - Raw → Counter 3
  - The system waits for Start to restart.
  - Pressing Reset resets all outputs and counters.
# Ladder Diagram:
![image](https://github.com/user-attachments/assets/decc08c5-279a-49e1-acb7-883c094358d8)
# Video:
https://github.com/user-attachments/assets/0d2f0e1c-6d91-430d-b361-7356c83febea
________________________________________________________________________________________________


# Lap3 - Pick And Place
# Scenario:
  - Start State: When the system is in the start position, pressing the Start button activates the Entry Conveyor.
  - When the Item at Entry sensor detects the item, the Entry Conveyor stops, and the robot moves along the Z-axis (Move Z).
  - Once the Item Detected sensor sees the item, the robot grabs it and moves back to the neutral Z position.
  - When the robot's Z-axis stops moving, it begins moving along the X-axis.
  - After the X-axis stops, the robot moves along the Z-axis.
  - When the Item at Exit sensor detects the item, the robot releases the grab and returns to the neutral Z position.
  - The Exit Conveyor starts once the robot reaches the neutral position, and the robot returns to its neutral X position.
# Ladder Diagram:
![image](https://github.com/user-attachments/assets/1c646e4d-21a4-4a51-bda6-5b2bd67fb805)
# Video:
https://github.com/user-attachments/assets/6602f677-45f2-46f8-9a84-763147fbc0d5
________________________________________________________________________________________________
# Lap4 - Assembler
# Scenario:

  - Start Button: Pressing the Start button activates the Bases Conveyor, and a base part is moved.
  - Base at Place Sensor: When the base part passes the sensor, the Bases Conveyor stops, and the Clamp Base starts to hold the part.
  - Lids Conveyor: When the base is clamped, the Lids Conveyor starts, and the lid part is moved.
  - Lid at Place Sensor: When the lid part passes the sensor, the Lids Conveyor stops, and the Clamp Lid starts.
  - Move Z: When the lid is clamped, the Move Z function is triggered.
  - Item Detected Sensor: Once detected, the Grab function holds the part, and the Clamp Lid releases the part.
  - Move Z Stops: When the part is released, the Move Z stops, and the robot returns to the neutral Z position.
  - Move X: Once in neutral, the robot moves along the X-axis.
  - Assembly Completion: The Clamp Base releases the base part, and after 1 second, the Grab function stops.
  - Pos Raise Bases: The bases are raised, and the Bases Conveyor works until the Part Leaving Sensor is triggered.
  - Auto Mode: If Auto is on, the operation continues automatically; otherwise, it waits for the Start button.
  - Reset/Stop: Pressing the Reset button resets the system, while Stop halts the system until the Start button is pressed again.
  - Display: The display shows the number of completed assemblies.
# Video:
https://github.com/user-attachments/assets/b8801593-4310-4dbf-bb80-501da23dc2fd




