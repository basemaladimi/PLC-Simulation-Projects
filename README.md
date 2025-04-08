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

##Video

https://github.com/user-attachments/assets/efbe4fcb-cfb5-489f-bcef-619759444836
________________________________________________________________________________________________


