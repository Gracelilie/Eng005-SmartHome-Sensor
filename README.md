# ENGR005: ECE Week #5 (Design a Smart Home)
**Grace-lilie Acheampong**
**Fall 2024**

**Date Written:** 10/9/2024
**Date Updated:** 10/9/2024

## Project Overview
This project implements a smart home system using the MSP430 microcontroller. It incorporates various sensors and actuators to create an intelligent home environment.

## Components
1. Motion Sensor (Input: P1.1)
2. Temperature Sensor (Input: P1.4)
3. Gas Sensor (Input: P1.3)
4. Photo Sensor (Input: P1.2)
5. Piezo Electronic Buzzer (Output: P1.6, P1.7)
6. LEDs (Output: P6.0, P6.1, P6.2, P6.3)
7. Serial Communication (P4.2, P4.3)

## Functionality
1. **Motion Detection**: 
   - Uses P1.1 as input
   - Activates LED on P6.0 when motion is detected
   - Triggers buzzer on P1.6 and P1.7

2. **Light Sensor**:
   - Uses P1.4 as ADC input
   - Activates LED on P6.1 when light level is below threshold

3. **Gas Sensor**:
   - Uses P1.3 as ADC input
   - Activates LED on P6.2 when gas level is above threshold

4. **Temperature Sensor**:
   - Uses ADC to measure temperature
   - LED on P6.3 indicates temperature status

## Code Structure
The project consists of three main parts:

1. **Temperature Sensing**:
   - Configures ADC for temperature sensing
   - Uses internal temperature sensor
   - Implements software trim for accuracy

2. **Light Sensing**:
   - Configures ADC for light sensing on P1.4
   - Uses interrupt-driven ADC readings

3. **Motion Detection**:
   - Configures P1.1 as input for motion sensor
   - Implements PWM on P1.6 and P1.7 for buzzer when motion is detected

4. **Gas Sensing**:
   - Configures ADC for gas sensing on P1.3
   - Uses interrupt-driven ADC readings

## Setup and Configuration
1. GPIO Configuration:
   - P6.0, P6.1, P6.2, P6.3: Configured as outputs for LEDs
   - P1.1: Configured as input with pull-up resistor for motion sensor
   - P1.4, P1.3: Configured as analog inputs for light and gas sensors
   - P1.6, P1.7: Configured as PWM outputs for buzzer

2. ADC Configuration:
   - 12-bit resolution
   - Internal reference
   - Sampling time: 16 ADC clock cycles

3. Timer Configuration:
   - Timer B0 used for PWM generation (buzzer)

## Usage
1. Compile and flash the code to your MSP430 microcontroller.
2. Connect the sensors and actuators as per the pin configuration.
3. The system will continuously monitor for motion, light levels, gas levels, and temperature.
4. LEDs will indicate the status of each sensor.
5. The buzzer will sound when motion is detected.




































































































# ENGR005: ECE Lab #3 (Transfering data to web application)
**Grace-lilie Acheampong**
**Fall 2024**

**Date Written:** 10/2/2024
**Date Updated:** 10/2/2024

## Project Overview:
This project focuses on implementing a smart home system that transfers temperature data from a sensor to the ThingSpeak web application. The experiment demonstrates the integration of IoT concepts, data processing, and web-based visualization in engineering applications.

### Objectives:
- Implement a system to transfer temperature data to ThingSpeak
- Create level 0 and level 1 block diagrams for the data transfer process
- Use C# for data calculations and processing
- Visualize and analyze the transferred data using ThingSpeak's features

### System Components:
- Temperature Sensor
- Microcontroller
- C# Application
- Wi-Fi Module
- ThingSpeak Web Application

### Data Flow:
1. Temperature Sensor collects raw data
2. Microcontroller reads sensor data
3. C# Application processes and calculates final temperature values
4. Wi-Fi Module sends processed data to ThingSpeak
5. ThingSpeak Server receives and stores the data
6. ThingSpeak Web Interface displays the data for analysis

### ThingSpeak Overview:
ThingSpeak is an IoT analytics platform service that allows users to collect, store, analyze, and visualize data in the cloud. It is commonly used for monitoring and analyzing sensor data and building IoT applications.

### Conclusion:
This lab successfully demonstrated the implementation of a smart home temperature monitoring system using IoT concepts. The integration of C# for data processing and ThingSpeak for visualization showcased the practical application of web technologies in engineering.
