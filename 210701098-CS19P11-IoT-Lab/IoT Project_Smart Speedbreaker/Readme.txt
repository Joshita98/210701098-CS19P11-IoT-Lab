ABSTRACT:

This project introduces a novel approach to road safety by integrating intelligent technologies into speed breakers and zebra crossings. The Smart Breaker system utilizes speed sensing technology to dynamically adjust the speed breaker based on the approaching vehicle's speed. When vehicles exceed a predefined speed threshold, the speed breaker automatically elevates to slow down the traffic effectively. Furthermore, the system incorporates an advanced zebra crossing with embedded LED lights that illuminate when pedestrians stand on the crossing, enhancing their visibility to approaching vehicles. This feature significantly improves pedestrian safety, especially during low-light conditions or high traffic volumes. The Smart Breaker system is designed to promote responsible driving behavior by providing real-time feedback to motorists and encouraging compliance with speed limits. Additionally, it prioritizes pedestrian safety by ensuring they are easily discernible to drivers, thereby reducing the risk of accidents at zebra crossings. Key features of the system include speed sensing technology, variable height adjustment mechanisms, LED-equipped zebra crossings, and integration with pedestrian detection systems. These elements work synergistically to create a safer and more efficient road environment for both motorists and pedestrians.


MATERIALS REQUIRED:

Hardware Requirements:
Arduino Uno: A microcontroller board that will collect sensor data and send it to the ESP32 via serial communication.
ESP32 Board: A Wi-Fi-enabled microcontroller board that will connect to your WiFi network and send sensor data to the Blynk app. Choose a specific ESP32 board based on your project needs and available options (e.g., ESP32 Dev Module, ESP32 Dev Kit C).
LED Lights: For showing the start and stop signal while people are walking on the zebra crossing.
Breadboard: Used for prototyping and connecting various components.
Jumper Wires: Used for connecting components on the breadboard.
LCD Display: Displays sensor data locally (optional). Choose an LCD with an I2C interface for easier connection.
Power Supply: Provides power to the Arduino Uno and ESP32 board. A USB cable connected to your computer or a dedicated power supply can be used.



Software Requirements:

Arduino IDE: Integrated Development Environment (IDE) used to write and upload code to the Arduino Uno and ESP32 boards. * **Blynk App:** Mobile application for creating a user interface to visualize sensor data. Download it from the App Store or Google Play Store.
Library Library: 
IRremote Library (Arduino): Controls Infrared (IR) devices like TVs with your Arduino.
Two-way Street: Decode IR signals from remotes (understand commands) and transmit IR signals (control devices).
Protocol Savvy: Works with various IR remote protocols (NEC, Sony, etc.).
Simple Use: Easy-to-learn functions for sending and receiving IR codes.
Open Source: Free and constantly updated on GitHub.
Board Friendly: Compatible with many Arduino boards (Uno, Mega, Nano, etc.).


WORKING OF THE PROJECT:
1. Sensor Data Acquisition (Arduino Uno):

- The Arduino Uno is connected to various sensors:
-IR sensor for measuring the speed of approaching.
- RF module enables wireless connection between the speed breaker system and vehicle.
-The Arduino reads sensor data periodically and processes it.

2. Data Transmission to ESP32 (Serial Communication):

-The Arduino transmits the collected sensor data (temperature, humidity, soil moisture, and PIR detection status - optional) to the ESP32 board over serial communication.
-The data is sent in a format recognizable by the ESP32 code (e.g., comma-separated values).

3. WiFi Connection and Blynk Communication (ESP32):

-The ESP32 board connects to your WiFi network using the credentials defined in the code.
-The ESP32 code utilizes the IR library to establish communication.
-The ESP32 receives sensor data from the Arduino Uno via serial communication.

4. Smart Speed breaker and Zebra crossing:

-Using the IR sensor the speed is detected, if the speed is above the limit, the the speed breaker gets enabled.
- For this purposes we have used 2 IR sensors to calculate the distance.
- Smart Zebra crossing is also implemented, where any person who is crossing the road will be detected using an ultrasonic sensor.
- The stop-and-go signal for the vehicles approaching is displayed using LEDs.