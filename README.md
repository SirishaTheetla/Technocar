# 🚗 Safe Driving System using Arduino Uno

This project implements a **Safe Driving System** designed to improve road safety by detecting **alcohol consumption**, **driver drowsiness**, and **overspeeding**, and providing **real-time alerts and speed control** using an Arduino Uno.

---

##  Features

➤  **Alcohol Detection**
  - Detects presence of alcohol using the MQ-3 sensor.
  - Prevents vehicle from starting if alcohol is detected.
  - Gradually decreases vehicle speed if alcohol is detected while driving.

➤  **Drowsiness Monitoring**
  - Uses a PIR sensor to detect eye blinking or driver movement.
  - Triggers a buzzer alert if no motion is detected (driver might be sleepy).

➤  **Overspeed Control**
  - Monitors vehicle speed through a potentiometer.
  - Automatically limits speed to a safe threshold.
  - Applies gradual speed correction after a delay when overspeeding is detected.

➤  **Real-time Feedback**
  - Outputs system status and alerts to the Serial Monitor (e.g., "alcohol detected", "sleep detected", "overspeed alert").

---

##  Technologies Used

- Arduino Uno
- C/C++ for Embedded Systems
- Serial Communication
- Analog and Digital I/O
- PWM Motor Control

---

##  Hardware Components

| Component           | Description                              |
|--------------------|------------------------------------------|
| Arduino Uno         | Main microcontroller                     |
| MQ-3 Sensor         | Alcohol detection sensor       |
| PIR Sensor          | Motion sensor for eye blink detection  |
| Potentiometer       | Simulates vehicle speed        |
| Buzzer              | Sound alert system             |
| DC Motor / LED      | Represents vehicle movement   |
| Breadboard, Jumper Wires, USB Cable, etc. |

---

##  System Workflow

1. **Startup Phase**:
    - Alcohol level is checked.
    - If alcohol is detected, the car won’t start.

2. **Normal Driving**:
    - Vehicle speed is controlled via potentiometer.
    - If gas level is safe, normal driving is allowed.

3. **Overspeed Check**:
    - Speed is compared with predefined limit.
    - If exceeded, speed is automatically adjusted over time.

4. **Drowsiness Detection**:
    - PIR sensor checks for driver motion.
    - If inactive for >500ms, buzzer rings as a warning.

5. **Alcohol During Drive**:
    - If detected, speed is reduced in steps until the car stops.

