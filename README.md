# Microcontroller Final Project – ECE 3301L (Spring 2024)

An integrated embedded system using the **PIC18F4620** microcontroller that combines sensor monitoring, real-time clock, PWM control, and display interface.

---

## Overview
This project integrates multiple peripherals and sensors into a single embedded control system.  
It uses a TFT display for real-time feedback and an IR remote + push button for user control.
<img width="926" height="610" alt="image" src="https://github.com/user-attachments/assets/78a09c49-03c7-4fd0-86a3-92a486379c23" />

---

## Features
- **TFT Display:** Shows time, date, temperature, fan status, and duty cycle  
- **Temperature Display:** Ambient temperature in °C and °F  
- **Digital Clock:** Real-time clock (DS3231) with date/time tracking  
- **Fan Control:** Automatic or manual mode using PWM speed control  
- **Alarm System:** Buzzer and RGB LED activate when alarm time is reached  
- **Light Sensor:** Silences alarm when light is blocked (above 2.5V)  
- **Remote Control:** Set time, alarm, and fan temperature via IR  
- **Push Button:** Toggle alarm mode ON/OFF  
<img width="280" height="372" alt="image" src="https://github.com/user-attachments/assets/148edb86-adf6-44bd-bcfc-1325ceb8dcd9" />

---

## ⚙️ Setup Screens
| Remote Button | Function |
|----------------|-----------|
| `CH–` | Set current time/date |
| `CH` | Set alarm time |
| `CH+` | Set fan auto temperature (16–30°C) |

---

## Code Structure
| File | Description |
|------|--------------|
| `main.c` | Main program loop and logic |
| `main_screen.c` | TFT screen drawing and updates |
| `setup_time.c` | Time setup functions |
| `setup_alarm_time.c` | Alarm setup functions |
| `setup_fan_temp.c` | Fan temperature setup |
| `interrupt.c` | Interrupts and IR remote handling |
| `i2c_soft.c` / `i2c_support.c` | I²C communication and sensor support |
| `fan_support.c` | PWM control and fan logic |
| `st7735_tft.c` | TFT driver |
| `utils.c` | Helper utilities |
| `main.h` | Pin mappings and global defines |

---

## Operation Summary
- Displays **temperature**, **time/date**, and **fan RPM/duty cycle** in real time  
- Fan adjusts speed automatically with temperature using PWM  
- Alarm triggers buzzer and RGB LED color sequence  
- Light sensor disables alarm when covered  
- All system functions are controllable via **IR remote** or **push-button**

---

## Technologies Used
- **Microcontroller:** PIC18F4620  
- **Peripherals:** DS3231 RTC, DS1621 Temperature Sensor, ST7735 TFT  
- **Protocols:** I²C, SPI, PWM, GPIO, Interrupts  
- **Control Interfaces:** IR Remote, Push Button  

---

## Skills Demonstrated
- Embedded C programming  
- Sensor integration and data display  
- Peripheral communication (I²C/SPI)  
- Real-time system control  
- Interrupt handling and modular software design  

---

**Instructor:** Felix Pinai  
**Institution:** California State Polytechnic University, Pomona – College of Engineering  
