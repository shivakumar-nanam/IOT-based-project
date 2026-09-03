# ☁️ Cloud-Connected Environmental Data Logger with Excel Reporting

## 📌 Project Overview

Environmental conditions such as temperature and smoke concentration play a critical role in industries, warehouses, laboratories, hospitals, and smart agriculture. Manual monitoring of these parameters is time-consuming and may lead to delayed responses during abnormal conditions.

This project presents a **Cloud-Connected Environmental Data Logger with Excel Reporting**, developed using the **LPC2148 ARM7 Microcontroller**. The system continuously monitors **temperature** using the **LM35 sensor** and **smoke concentration** using the **MQ2 gas sensor**. The measured values are displayed on a **16×2 LCD**, uploaded to the **ThingSpeak Cloud** through the **ESP-01 Wi-Fi module**, and automatically recorded in **Microsoft Excel** for future analysis.

The system also utilizes **interrupts** to handle user inputs and periodic operations efficiently, ensuring faster response and better system performance. By integrating **Embedded Systems**, **IoT**, **Cloud Connectivity**, **Interrupt-driven Processing**, and **Data Logging**, this project provides a reliable real-time environmental monitoring solution.

---

## 🎯 Objectives

| Objective | Description |
|------------|-------------|
| 🌡️ Temperature Monitoring | Continuously monitor environmental temperature using the LM35 sensor |
| 🔥 Smoke Detection | Detect smoke concentration using the MQ2 gas sensor |
| ☁️ Cloud Connectivity | Upload environmental data to the ThingSpeak cloud using the ESP-01 Wi-Fi module |
| 📊 Excel Reporting | Store sensor readings with timestamps in Microsoft Excel |
| 🖥️ LCD Display | Display real-time temperature and smoke values on a 16×2 LCD |
| ⏰ Time Stamping | Record accurate date and time using the RTC module |
| 🚨 Alert System | Activate the buzzer whenever the smoke level exceeds the threshold |
| ⚡ Interrupt Handling | Use interrupts for quick response to user inputs and periodic operations |
| 🌐 Remote Monitoring | Monitor environmental conditions remotely through the cloud |

---

## 🧰 Hardware Components

| Component | Quantity | Purpose |
|-----------|:--------:|---------|
| LPC2148 ARM7 Microcontroller | 1 | Central controller of the system |
| LM35 Temperature Sensor | 1 | Measures environmental temperature |
| MQ2 Gas Sensor | 1 | Detects smoke concentration |
| ESP-01 (ESP8266) Wi-Fi Module | 1 | Uploads data to ThingSpeak cloud |
| DS1307 RTC Module | 1 | Provides date and time for logging |
| 16×2 LCD Display | 1 | Displays live sensor readings |
| Matrix Keypad | 1 | Allows user to set the temperature threshold |
| Buzzer | 1 | Generates an alert during abnormal conditions |
| Crystal Oscillator | 1 | Provides system clock for LPC2148 |
| Regulated Power Supply | 1 | Supplies stable power to the circuit |

---

## 💻 Software Requirements

| Software | Purpose |
|-----------|---------|
| Keil µVision 4 | Embedded C code development and debugging |
| Flash Magic | Upload firmware into LPC2148 |
| Embedded C | Firmware development |
| ThingSpeak | Cloud platform for IoT monitoring |
| Microsoft Excel | Stores and analyzes logged sensor data |

---

## 🏗️ System Architecture

<p align="center">
  <img src="./Block digram.png" alt="System Architecture" width="900">
</p>

The **LPC2148 ARM7 Microcontroller** acts as the central processing unit of the system. It acquires environmental data from the **LM35 temperature sensor** and **MQ2 gas sensor**, processes the readings, and displays them on a **16×2 LCD**.

The **DS1307 RTC module** provides accurate date and time information for timestamping every sensor reading. The **ESP-01 Wi-Fi module** communicates with the ThingSpeak cloud through UART and uploads the environmental data for remote monitoring. The uploaded information is also stored in **Microsoft Excel** for analysis and report generation.

The system uses **interrupts** to improve responsiveness. User inputs from the keypad and other event-driven operations are handled through interrupt service routines (ISRs), allowing critical events to be processed immediately without affecting the continuous environmental monitoring process.

Whenever the smoke level exceeds the predefined threshold, the LPC2148 activates the **buzzer** to alert nearby users.

---

## 🔄 Working Principle

<p align="center">
  <img src="./Working Principle.png" alt="Working Principle" width="1000">
</p>

The system starts by initializing the LPC2148 microcontroller, LCD, RTC, ADC, UART, ESP-01 Wi-Fi module, sensors, and external interrupt. The LM35 temperature sensor and MQ2 gas sensor continuously monitor the environmental conditions.

The measured values are displayed on the 16×2 LCD. If the smoke level exceeds the predefined threshold, the buzzer is activated to alert the user.

When the **External Interrupt (EINT0)** is triggered through the matrix keypad, the system enters **Edit Mode**, allowing the user to modify the **Date, Time, Day, Month, Year, and Temperature Setpoint**. After saving the updated values, the program returns to normal monitoring.

Finally, the sensor readings, along with the RTC timestamp, are uploaded to the ThingSpeak cloud through the ESP-01 Wi-Fi module and simultaneously stored in Microsoft Excel for future analysis. This process repeats continuously.


---

## ⭐ Key Features

| Feature | Description |
|---------|-------------|
| 🌡️ Real-Time Temperature Monitoring | Continuously measures ambient temperature using the LM35 sensor |
| 🔥 Smoke Detection | Detects smoke concentration using the MQ2 gas sensor |
| ☁️ Cloud Connectivity | Uploads environmental data to the ThingSpeak cloud using the ESP-01 Wi-Fi module |
| 📊 Excel Reporting | Automatically stores sensor data with timestamps in Microsoft Excel |
| 🖥️ LCD Display | Displays real-time temperature and smoke readings locally |
| ⏰ RTC-Based Data Logging | Records accurate date and time for every sensor reading |
| ⚡ External Interrupt Support | Enters Edit Mode through **EINT0** to modify **Date, Time, Day, Month, Year, and Temperature Setpoint** |
| 🚨 Buzzer Alert | Activates a buzzer whenever the smoke level exceeds the configured threshold |
| 🌐 Remote Monitoring | Allows users to monitor environmental conditions from anywhere using the Internet |
| 🛠️ Modular Design | Separate drivers for LCD, ADC, RTC, UART, ESP-01, MQ2, Keypad, and Interrupts for easy maintenance |``

---

## 🚀 Advantages

| Advantage | Description |
|-----------|-------------|
| 📡 Remote Monitoring | Monitor environmental conditions from anywhere through the ThingSpeak cloud platform |
| ⚡ Real-Time Monitoring | Continuously measures temperature and smoke levels without manual intervention |
| 🔔 Immediate Alerts | Activates the buzzer instantly when smoke exceeds the configured threshold |
| ⏱️ Accurate Data Logging | Uses the RTC module to record precise date and time for every reading |
| 📊 Historical Data Analysis | Stores sensor data in Microsoft Excel for trend analysis and reporting |
| ☁️ IoT Enabled | Supports cloud-based monitoring using the ESP-01 Wi-Fi module |
| 🛠️ User Configurable | External Interrupt (EINT0) allows users to edit Date, Time, Day, Month, Year, and Temperature Setpoint |
| 🔄 Reliable Operation | Continuously monitors the environment with interrupt-driven user configuration |
| 📈 Scalable Design | Additional sensors and cloud features can be integrated with minimal modifications |
| 💰 Low-Cost Solution | Built using affordable embedded hardware while providing advanced IoT functionality |

---

## 🏭 Applications

| Application | Description |
|------------|-------------|
| 🏭 Industrial Safety | Monitor temperature and smoke levels in manufacturing industries |
| 🏢 Smart Buildings | Track environmental conditions in offices, malls, and commercial buildings |
| 🧪 Laboratories | Monitor laboratory environments and detect hazardous smoke conditions |
| 🏥 Hospitals | Ensure safe environmental conditions in patient care areas and laboratories |
| 🌾 Smart Agriculture | Monitor greenhouse and farm environments remotely through the cloud |
| 📦 Warehouses | Protect stored goods by detecting abnormal temperature and smoke levels |
| 🏫 Educational Institutions | Demonstrate Embedded Systems, IoT, Cloud Computing, and Interrupt-based applications |
| 🏠 Home Automation | Monitor indoor environmental conditions and receive cloud-based updates |
| 🌍 Environmental Monitoring | Collect and analyze environmental data for research and reporting |
| 🌐 IoT-Based Monitoring Systems | Serve as a foundation for cloud-connected environmental monitoring solutions |

---
## 📂 Project Folder Structure

```text
Cloud Connected Environmental Data Logger with Excel Reporting/
│
├── README.md
├── BLOCK_DIAGRAM_V2.png
├── WORKING PRINCIPLE.png
│
├── Excel File/
├── HEX File/
├── images/
└── Source Code/
    ├── .c source files
    └── .h header files
```
---

## 📸 Project Output

### 🖥️ Normal Monitoring

During normal operation, the system continuously monitors the environmental conditions and displays the **temperature and smoke level** on the 16×2 LCD.

<p align="center">
  <img src="./cloud%20connected%20environmental%20data%20logger%20with%20excel%20reporting/images/normal_monitoring.jpeg" alt="Normal Monitoring" width="700">
</p>

### 🌡️ Temperature Monitoring

When the measured temperature exceeds the configured temperature setpoint, the system detects the abnormal condition and provides an alert.

<p align="center">
  <img src="./temperature monitoring.jpng" alt="System Architecture" width="900">
</p>

### ⚙️ Temperature Setpoint Configuration

The user can configure the required temperature setpoint through the keypad.

<p align="center">
  <img src="./cloud%20connected%20environmental%20data%20logger%20with%20excel%20reporting/images/temperature_setpoint.jpeg" alt="Temperature Setpoint Configuration" width="700">
</p>

### ⌨️ Keypad Interface

The keypad is used to enter the editing mode and configure parameters such as **date, time, and temperature setpoint**.

<p align="center">
  <img src="./cloud%20connected%20environmental%20data%20logger%20with%20excel%20reporting/images/keypad_interface.jpeg" alt="Keypad Interface" width="700">
</p>

### ☁️ ThingSpeak Cloud Monitoring

The sensor data is uploaded to the **ThingSpeak cloud** through the ESP-01 Wi-Fi module, enabling remote monitoring of environmental parameters.

<p align="center">
  <img src="./cloud%20connected%20environmental%20data%20logger%20with%20excel%20reporting/images/thinkspeakimage.jpeg" alt="ThinkSpeak Cloud Monitoring" width="900">
</p>

### 📊 Excel Data Logging

The collected environmental data is stored in **Microsoft Excel** with timestamps for historical analysis and reporting.


<p align="center">
  <img src="./cloud%20connected%20environmental%20data%20logger%20with%20excel%20reporting/images/excel.jpeg" alt="excel" width="900">
</p>

### 🔌 Hardware Connections

The project integrates the LPC2148 microcontroller with the LM35 temperature sensor, MQ2 gas sensor, RTC module, ESP-01 Wi-Fi module, LCD, keypad, and buzzer.

<p align="center">
  <img src="./cloud%20connected%20environmental%20data%20logger%20with%20excel%20reporting/images/hardware%20connections.png" alt="Hardware Connections" width="900">
</p>

### 📡 ESP-01 Wi-Fi Interface

The ESP-01 Wi-Fi module communicates with the LPC2148 through UART and provides connectivity to the ThingSpeak cloud platform.

<p align="center">
  <img src="./cloud%20connected%20environmental%20data%20logger%20with%20excel%20reporting/images/esp01%20connection.jpeg" alt="ESP-01 Wi-Fi Interface" width="700">
</p>

---

## 👩‍💻 Author

**Shiva Kumar**

Electronics and Communication Engineering (ECE)

### 🔧 Technical Skills

- C / Embedded C
- ARM7 / LPC2148
- UART, SPI, I2C, ADC
- RTC and External Interrupts
- ESP-01 / Wi-Fi Communication
- ThingSpeak IoT
- Embedded Systems

### 📌 Project Focus

**Embedded Systems | IoT | Cloud Connectivity | Real-Time Data Logging**
