# Dashboard-Implementation-using-CAN
Developed an STM32F4-based IoT monitoring system using CAN for real-time sensor communication. Interfaced INA219, HX710B, DHT22, and LIS3DSH via I2C, SPI, and GPIO. Integrated ESP8266/ESP32 with MQTT and built an HTML dashboard for live monitoring using Embedded C, STM32 HAL, timers, and watchdog timer.

# Embedded IoT-Based Real-Time Monitoring Dashboard using STM32F4, CAN & MQTT

## Project Overview

This project implements a real-time embedded IoT monitoring system using the STM32F4 Discovery board. Sensor data is collected from multiple sensors, transmitted over the CAN (Controller Area Network), forwarded through an ESP8266/ESP32 using the MQTT protocol, and displayed on a web-based dashboard for remote monitoring.

The project demonstrates Embedded C programming, STM32 HAL drivers, CAN communication, MQTT integration, sensor interfacing, and IoT dashboard development.

---

## Features

* Real-time sensor monitoring
* CAN-based communication between STM32 nodes
* MQTT-based cloud communication
* HTML dashboard for live visualization
* Multi-sensor interfacing
* Modular firmware design
* Timer-based periodic data transmission
* Watchdog timer for improved reliability

---

## Hardware Components

* STM32F407G Discovery Board (Transmitter)
* STM32F407G Discovery Board (Receiver)
* ESP8266 / ESP32 Wi-Fi Module
* INA219 Current & Voltage Sensor
* HX710B Pressure Sensor
* DHT22 Temperature & Humidity Sensor
* LIS3DSH Accelerometer (On-board)
* CAN Transceiver (SN65HVD230 / MCP2551)
* USB-UART Converter
* Power Supply

---

## Software & Technologies

### Programming Language

* Embedded C

### Development Tools

* STM32CubeIDE
* STM32CubeMX
* Git
* GitHub

### Communication Protocols

* CAN 2.0
* MQTT
* UART
* I2C
* SPI
* GPIO

### Firmware

* STM32 HAL Drivers
* Timer Interrupts
* Watchdog Timer

### Dashboard

* HTML
* CSS
* JavaScript
* MQTT over WebSocket

---

## System Architecture

Sensors
↓
STM32F407 (Transmitter)
↓
CAN Bus
↓
STM32F407 (Receiver)
↓
UART
↓
ESP8266 / ESP32
↓
MQTT Broker
↓
HTML Dashboard

---

## Sensor Details

| Sensor  | Interface | Measured Parameter     |
| ------- | --------- | ---------------------- |
| INA219  | I2C       | Current & Voltage      |
| HX710B  | GPIO      | Pressure               |
| DHT22   | GPIO      | Temperature & Humidity |
| LIS3DSH | SPI       | Acceleration           |

---

## Project Workflow

1. Initialize peripherals (CAN, UART, I2C, SPI, GPIO, Timers).
2. Read sensor data periodically.
3. Pack sensor values into CAN frames.
4. Transmit CAN messages.
5. Receive CAN frames on the receiver node.
6. Send received data to ESP8266/ESP32 via UART.
7. Publish data to the MQTT broker.
8. Dashboard subscribes to MQTT topics.
9. Display live sensor values.

---

## Technologies Used

* Embedded C
* STM32 HAL
* CAN Protocol
* MQTT
* ESP8266 / ESP32
* HTML
* CSS
* JavaScript
* Git

---

## Project Directory

```
Transmitter/
│── Core/
│── Drivers/
│── CAN/
│── Sensors/

Receiver/
│── Core/
│── Drivers/
│── CAN/
│── UART/

ESP/
│── MQTT/

Dashboard/
│── index.html
│── style.css
│── script.js
```

---

## Future Improvements

* CAN FD support
* OTA firmware updates
* TLS-secured MQTT communication
* SD card data logging
* FreeRTOS task scheduling
* Cloud database integration
* Mobile application support

---

## Author

**Pratik Kamble**

PG-Diploma in Embedded Systems Design (PG-DESD)

CDAC Sunbeam Pune

Embedded Systems | Firmware Development | IoT | CAN | Linux
