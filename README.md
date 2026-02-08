# Ultra-Precision Current and Voltage Measurement System

##  Project Overview
This project is a collaborative effort to design and implement an **ultra-precision embedded measurement system** capable of accurately measuring very small currents and voltages without significantly affecting the Device Under Test (DUT).

The system uses the **STM32F411 microcontroller** for high-performance, real-time data acquisition. Measurements are transmitted via **UART** and can be logged using **PuTTY** for further analysis.

---

##  Project Objectives
- Measure current from **1 µA to 100 mA**  
- Measure voltage from **1 V to 12 V**  
- Minimize loading effect on the DUT  
- Enable real-time data acquisition  
- Log measurement data via serial communication  

---

##  System Architecture
The system consists of:  
- Ultra-Precision Current Sensing Circuit  
- Precision Voltage Sensing Circuit  
- STM32F411 Microcontroller  
- UART-based communication for data logging  

---

##  Ultra-Precision Current Sensing Circuit
- Uses **precision shunt resistors** to convert current into a small voltage  
- Amplified with **LM358N operational amplifier** before ADC measurement  

**Current Measurement Ranges:**

| Range           | Shunt Resistor |
|-----------------|----------------|
| Micro-amp range | 100 Ω          |
| Milli-amp range | 1 Ω            |

---

##  Precision Voltage Sensing Circuit
- Uses a **resistive voltage divider** to safely scale voltages from 1 V to 12 V for the STM32 ADC  

---

##  Microcontroller Unit
**Microcontroller:** STM32F411  
- Performs ADC sampling  
- Processes and scales measurements  
- Sends data via UART  
- Supports real-time operation  

---

##  Components Used

**Hardware:**  
- STM32F411 Development Board  
- ST-Link Debugger  
- UART TTL Serial Converter  
- Operational Amplifier (LM358N)  
- Shunt Resistors: 1 Ω, 100 Ω  
- Capacitors: 220 µF  
- Resistors: 1 MΩ, 3.3 MΩ, 330 Ω, 10 Ω  
- Breadboard & Jumper Wires  
- 3 Toggle Switches  

**Software & Tools:**  
- STM32CubeIDE – Firmware development  
- PuTTY – Serial communication and data logging  
- UART Protocol – Data transmission  

---

##  Data Storage & Logging
- Data is transmitted via **UART**  
- **PuTTY** is used for:  
  - Viewing real-time measurements  
  - Logging data for analysis  

---

##  How to Run the Project
1. Assemble the current and voltage sensing circuits  
2. Connect circuits to the STM32F411 board  
3. Program the microcontroller using **STM32CubeIDE**  
4. Connect UART TTL converter to the PC  
5. Open PuTTY and configure the COM port and baud rate  
6. Power the system and observe real-time measurements  

---

##  Applications
- Precision laboratory measurements  
- Low-power electronics testing  
- Sensor characterization  
- Embedded measurement systems  
