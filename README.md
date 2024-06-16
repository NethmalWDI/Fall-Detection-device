# Fall Detection Device

## Team MedMinds

This project was developed as part of our 2nd semester project at the University of Moratuwa. The objective of this project is to design and implement a device that detects falls in elderly people and sends a notification to a designated person via SMS.

## Project Overview

Falls are a major health risk for elderly people, and timely assistance is crucial in such situations. Our fall detection device aims to address this issue by detecting falls using a gyroscope and accelerometer, and notifying a caretaker through a WiFi-enabled communication system.

## Features

- **Fall Detection**: Utilizes the MPU6050 gyroscope and accelerometer to detect falls.
- **Notification System**: Sends an SMS to a predefined contact when a fall is detected.
- **WiFi Communication**: Uses the ESP8266 module to connect to a WiFi network and send notifications.
- **Custom PCB Design**: Designed using Altium.
- **Enclosure Design**: Modeled and simulated using SOLIDWORKS.

## Fall Detection Concepts

Our fall detection algorithm is based on analyzing movement patterns and accelerations using the MPU6050 sensor. Here are the key concepts:

- **Movement Indication**: 
  - Messages are sent to the HiveMQ server under the topic "Notifications" to indicate various movements.

- **Fall Detection**:
  - Falls are identified when the resultant acceleration drops near zero, then suddenly increases to a value higher than 1g, and finally decreases back to around 1g.

- **Walking Detection**:
  - Walking is identified when the longitudinal acceleration is about 1g, and the resultant acceleration has slightly higher values, approximately 1.1g.

- **Getting Up Detection**:
  - Getting up from the bed is detected when the longitudinal acceleration increases, and the turned angle approaches 90 degrees.

## Hardware Components

- **MPU6050**: Gyroscope and accelerometer module for motion detection.
- **ESP8266**: WiFi module for internet connectivity.
- **Custom PCB**: Designed with Altium for integrating the components.
- **Enclosure**: Designed with SOLIDWORKS to house the device.
