# Smart Home Automation & IoT Monitoring System

An integrated Smart Home automation ecosystem built around Raspberry Pi 4, combining four mechatronic subsystems with centralized communication, data storage, and real-time monitoring.

## Project Overview

The system integrates four independent automation subsystems:

### 1. Climate Control

* DHT11 temperature and humidity sensor.
* GPIO-based sensor communication.
* Automated cooling simulation based on temperature thresholds.

### 2. Smart Lighting

* HC-SR501 PIR motion sensor.
* Automatic multi-LED lighting control.
* MQTT-based event communication.

### 3. Automated Parking Barrier

* HC-SR04 ultrasonic distance sensor.
* PWM-controlled micro-servo motor.
* Voltage-level shifting for safe hardware interfacing.

### 4. Automated Water Management

* Water-level sensor.
* PCF8591 analog-to-digital converter over I²C.
* Relay-based pump control.

## Data Infrastructure

The system uses a centralized IoT monitoring pipeline:

* **MQTT (Mosquitto):** Communication between subsystems.
* **InfluxDB:** Time-series sensor data storage.
* **Grafana:** Live monitoring and visualization dashboard.

## Technologies & Components

* Raspberry Pi 4
* Python
* GPIO
* I²C
* PWM
* MQTT / Mosquitto
* InfluxDB
* Grafana
* DHT11, HC-SR501, HC-SR04
* PCF8591 ADC
* Servo motor, relay, LEDs and water-level sensor

## System Monitoring

The Grafana dashboard provides live visualization of temperature, lighting status, parking barrier status, and water-level measurements.

## Project Objectives

* Integrate multiple mechatronic systems into one automation ecosystem.
* Enable communication between distributed hardware subsystems.
* Collect and store sensor data.
* Provide centralized real-time monitoring.
* Automate physical processes based on sensor readings.

