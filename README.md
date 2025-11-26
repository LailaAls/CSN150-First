# CSN150-First
1. Project Overview

This project shows how I set up the ESP32‑CAM as a Wi‑Fi Access Point and hosted a simple webpage where I could view the live camera feed. I followed the Random Nerd Tutorials guide and documented the full process here.

2. Materials Used

ESP32‑CAM module

Jumper wires

USB cable

Computer with Arduino IDE

3. Steps I Followed
Step 1 — Set Up the Arduino IDE

Installed the ESP32 board package in Arduino IDE.

Selected AI Thinker ESP32‑CAM as the board.

Chose the correct COM port for the FTDI programmer.

step 2 - Uploading the Code

Used the Access Point example code.

Set the Wi‑Fi name and password.

Hit Upload, waited for flashing to finish.

Step 3 — Running the Camera Access Point


Opened the Serial Monitor.

Saw the message:

"Access Point started!"

"IP address: 192.168.4.1"

Connected my phone/laptop to the new Wi‑Fi network.

Opened a browser and went to:

http://192.168.4.1

The ESP32‑CAM live video stream worked.


4. Problems I Encountered & How I Solved Them

Problem 1: Serial Monitor Showing Gibberish

Issue: Serial Monitor showed unreadable symbols.

Cause: Baud rate was incorrectly set to 2400.

Fix: Changed baud rate to 115200.

Problem 2: Wrong Camera Model Setting

Issue: ESP32-CAM wouldn't start correctly.

Cause: In board_config.h, the camera model was commented out:

// #define CAMERA_MODEL_AI_THINKER // Has PSRAM

Fix: Removed // so it became:

#define CAMERA_MODEL_AI_THINKER // Has PSRAM
Problem 3: Missing camera_pins.h Include

Issue: Board wasn't reading the correct pin mapping.

Cause: Include line was commented out:

// #include "camera_pins.h"

Fix: Removed // so it became:

#include "camera_pins.h"


5. What I Learned

How to flash and program the ESP32‑CAM

How to create a Wi‑Fi Access Point without a router

How to host a web server directly on the ESP32‑CAM

How to troubleshoot common ESP32‑CAM issues

6. Final Summary

This project helped me understand the ESP32‑CAM better and gave me hands‑on practice with Wi‑Fi networking, web servers, and microcontrollers. I successfully set up the ESP32‑CAM as an Access Point and streamed video to a browser. Even though I had some issues at first, fixing them taught me a lot about debugging hardware.

