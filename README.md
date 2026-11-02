# Smart Home Automation & IoT Monitoring System

An integrated Smart Home automation ecosystem developed using **Raspberry Pi 4**, combining four mechatronic subsystems with centralized communication, data acquisition, automation, time-series storage, and real-time monitoring.

The project demonstrates the integration of embedded systems, sensors, actuators, communication protocols, and IoT data infrastructure into one unified automation ecosystem.

## Project Overview

The system consists of four independent but interconnected automation subsystems:

1. Climate Control
2. Presence-Based Smart Lighting
3. Automated Parking Barrier
4. Automated Water Management

All subsystems communicate through MQTT, while sensor data is stored in InfluxDB and visualized through a centralized Grafana dashboard.

## 1. Climate Control

* Integrated a DHT11 temperature and humidity sensor with Raspberry Pi GPIO.
* Implemented live temperature and humidity monitoring.
* Developed threshold-based automated cooling simulation.

## 2. Presence-Based Smart Lighting

* Integrated an HC-SR501 PIR motion sensor.
* Implemented motion-triggered multi-LED lighting control.
* Used MQTT event messages for communication between components.

## 3. Automated Parking Barrier

* Integrated an HC-SR04 ultrasonic distance sensor.
* Implemented proximity-based vehicle detection.
* Controlled a micro-servo motor using PWM.
* Incorporated voltage-level shifting for safe interfacing with Raspberry Pi 3.3V logic.

## 4. Automated Water Management

* Integrated a water-level sensor.
* Used a PCF8591 analog-to-digital converter through I²C communication.
* Implemented water-level measurement and monitoring.
* Developed relay-based pump control.

## System Architecture & Data Infrastructure

A centralized IoT monitoring pipeline connects the different subsystems.

| Technology       | Purpose                                    |
| ---------------- | ------------------------------------------ |
| Raspberry Pi 4   | Main embedded computing platform           |
| Python           | Hardware control and subsystem programming |
| GPIO             | Sensor and actuator interfacing            |
| I²C              | Communication with PCF8591 ADC             |
| PWM              | Servo motor control                        |
| MQTT (Mosquitto) | Inter-process and subsystem communication  |
| InfluxDB         | Time-series sensor data storage            |
| Grafana          | Real-time monitoring and visualization     |

## Project Gallery

### 1. Hardware Implementation

Physical Raspberry Pi setup with integrated sensors, actuators, and electronic components.

![Hardware Setup](images/hardware_setup.jpg)

### 2. Live Grafana Monitoring Dashboard

Centralized dashboard displaying temperature measurements, lighting status, parking barrier status, and water-level readings.

![Grafana Dashboard](images/grafana_dashboard.png)

### 3. Running System – Raspberry Pi 4

Multiple subsystem programs running simultaneously, processing sensor measurements and exchanging real-time data through MQTT.

![Running System](images/running_system.png)

## Key Engineering Concepts

* Embedded Systems Development
* Mechatronic System Integration
* IoT Architecture
* Sensor Data Acquisition
* Actuator Control
* Analog-to-Digital Conversion
* GPIO and I²C Communication
* PWM-Based Motor Control
* MQTT Messaging
* Time-Series Data Management
* Real-Time Monitoring
* Hardware-Software Integration

## Project Objectives

* Integrate multiple mechatronic subsystems into one automation ecosystem.
* Enable communication between independent hardware components.
* Acquire and process real-time sensor data.
* Automate physical processes based on sensor measurements.
* Store and visualize system telemetry through a centralized monitoring platform.

## Technologies & Components

**Platform:** Raspberry Pi 4

**Programming:** Python

**Communication:** MQTT, Mosquitto, I²C

**Data Infrastructure:** InfluxDB, Grafana

**Sensors:** DHT11, HC-SR501, HC-SR04, Water-Level Sensor

**Other Components:** PCF8591 ADC, Servo Motor, Relay, LEDs, Cooling Simulation Components
