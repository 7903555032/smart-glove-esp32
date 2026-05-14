# Smart Gesture-Based Communication and Health Monitoring Glove Using ESP32

## Overview

This project is a wearable smart glove designed for gesture-based communication and real-time health monitoring using ESP32 microcontrollers.

The system detects hand gestures using flex sensors and converts them into predefined messages. These messages are transmitted wirelessly to a central unit using ESP-NOW communication.

The project also integrates:
- body temperature monitoring
- pulse and SpO2 monitoring
- audio feedback
- LCD/OLED display
- emergency SOS alert system using GSM

---

# Features

- Gesture recognition using 5 flex sensors
- Wireless ESP-NOW communication
- OLED display on glove unit
- LCD display on central unit
- DS18B20 temperature monitoring
- MAX30102 pulse and SpO2 monitoring
- DFPlayer Mini audio playback
- SIM800L GSM emergency alerts
- Buzzer alert system
- Rechargeable battery-powered design

---

# System Architecture

## Glove Unit
- ESP32
- 5 Flex Sensors
- DS18B20 Temperature Sensor
- MAX30102 Pulse Sensor
- OLED Display
- ESP-NOW transmitter

## Central Unit
- ESP32
- LCD Display
- DFPlayer Mini
- Speaker
- SIM800L GSM Module
- Buzzer
- ESP-NOW receiver

---

# Working Principle

1. Flex sensors detect finger bending.
2. ESP32 reads analog values from sensors.
3. Finger states are converted into binary patterns.
4. Binary patterns are mapped to predefined messages.
5. Data is transmitted wirelessly using ESP-NOW.
6. Central unit receives and processes data.
7. LCD, speaker, buzzer, and GSM modules generate output.

---

# Gesture Mapping

| Gesture Pattern | Message |
|---|---|
| 00000 | Normal / OK |
| 11111 | SOS |
| 01111 | YES |
| 10111 | NO |
| 00111 | Need Water |
| 11110 | Washroom |
| 10011 | Need Food |
| 00011 | Call / Attention |

---

# Hardware Components

| Component | Quantity |
|---|---|
| ESP32 | 2 |
| Flex Sensor | 5 |
| DS18B20 | 1 |
| MAX30102 | 1 |
| OLED Display | 1 |
| LCD 16x2 I2C | 1 |
| DFPlayer Mini | 1 |
| SIM800L | 1 |
| Speaker | 1 |
| Buzzer | 1 |

---

# Folder Structure

```text
docs/          -> Reports and project documents
firmware/      -> ESP32 source code
hardware/      -> Circuit and hardware files
media/         -> Images and demo videos
BOM/           -> Bill of Materials
```

---

# Power System

## Glove Unit
- Li-ion Battery
- TP4056 Charging Module
- Boost Converter for ESP32

## Central Unit
- 18650 Battery
- MT3608 Boost Converter
- Dedicated 4V supply for SIM800L

---

# Communication Protocol

The project uses ESP-NOW communication between two ESP32 boards for low-latency wireless data transmission.

---

# Future Improvements

- Machine learning gesture recognition
- Mobile application support
- Cloud-based health monitoring
- Custom PCB development
- Improved gesture calibration algorithms

---

# Authors

- Rohit Kumar
- Ashutosh Gupta
- Polukonda Sai Satwik
- Alok Raj

Department of Electronics and Communication Engineering  
BIT Mesra, Off-Campus Patna

---

# Mentor

Dr. Nilay Pandey

---

# License

This project is licensed under the MIT License.
