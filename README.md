# IoT-FingCtrl
## PROPOSAL VIDEO
[![video](https://img.youtube.com/vi/q_JButZIfpA/hqdefault.jpg)](https://www.youtube.com/watch?v=q_JButZIfpA)

## System Concept 
This project implements a wearable input device that enables users to control a smart device using hand gestures, without touching a screen or using void commands.
By detecting the bending status of each finger, the system translates physical finger movements into a 5 bit bianry gesture code, which is mapped to a corresponding key input and sent via BLE.
The device is recognized by android smartphones as a bluetooth keyboard, allowing for direct interaction without a dedecated app.

## Objectives
- Build a wearalbe system using ESP32 and MPU6050 sensors to detect finger movement in real time.
- Interpret finger gestures as 5 bit binary values representing each finger's bending state.
- Use a TCA9548A I2C multiplexer to manage multiple MPU6050 sensors (in this project, it may be 5) with the same I2C address
- Transmit gesture information using BLE, so that smartphones recognize it as key input
	- ex. media control, certain operations, 
- Power the system using a lightweight and rechargeable Lipo battery through aLipo Rider module.
- Demonstrate seamless integration with Android devices without requiring a separate mobile application.

## Use cases 
- Smartphone media control: play/pause, next/previous track, volume up/down using hand gestures.
- Presentation controller: Navigate slides and perform some actions on screen with simple gestures.
- Accessibility tool: assist user with limited mobility to control devices via hand movements
- Smart home automation: trigger predefined action in automation apps via gesture-key mapping.
	- we want to develop the application to control actions of the smartphone from our gestures, maybe.

## Required Components
- MPU6050  $\times$ 5: 6 axis accelerometer/gyrscope modules to detect finger bending.
- TCA9548A I2C Multiplexer: allows control of multiple MPU6050s with the same address.
- ESP32 WROOM 32: Core microcontroller with BLE capability.
- Lipo Rider: Battery management module to charge and boost voltage from 3.7V to 5V
- Lipo Battery 3.7V: Rechargeable battery providing  
