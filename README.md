# 🚀 STM32-Based Obstacle Avoiding and Line Following Robot  

This project implements an STM32-based autonomous robot that combines line following and obstacle avoidance using IR sensors, an ultrasonic sensor, and a gas/flame sensor. The robot is programmed to detect obstacles, follow a black line, and respond to gas or flame detection by activating an alarm system.

---

## 🛠️ Features  
✅ **Line Following:**  
- Uses two IR sensors to detect and follow a black line.  
- Adjusts motor directions based on sensor input to maintain the line.  

✅ **Obstacle Detection:**  
- Ultrasonic sensor measures distance to obstacles.  
- Stops and alerts when an obstacle is detected within 50 cm.  

✅ **Gas and Flame Detection:**  
- Gas sensor triggers a buzzer and LED when gas or flame is detected.  
- The buzzer and LED are deactivated automatically after 2 seconds.  

✅ **LDR-Based Light Detection:**  
- An LDR (Light Dependent Resistor) controls an LED based on ambient light levels.  

---

## 📌 Hardware Components  
- STM32 microcontroller  
- Ultrasonic sensor (HC-SR04)  
- IR sensors  
- Gas sensor  
- Buzzer  
- LEDs  
- LDR  
- Motors and motor driver  

---

## 🏗️ Code Overview  
### 1. **Ultrasonic Sensor Logic**  
- Trigger pin sends a pulse.  
- Echo pin measures the pulse duration to calculate distance.  

### 2. **Line Following Logic**  
- Left and right IR sensors detect black or white surfaces.  
- Adjusts motor directions based on sensor input.  

### 3. **Obstacle Detection and Alert**  
- If an obstacle is within 50 cm:  
    - Robot stops.  
    - 7-segment display shows alert.  
    - Buzzer activates.  

### 4. **Gas and Flame Detection**  
- If gas is detected:  
    - Buzzer and LED turn ON for 2 seconds.  

### 5. **LDR Detection**  
- If dark, turn ON an LED.  

---

## 🔌 Pin Configuration  
| Pin | Function | Description |  
|------|----------|-------------|  
| PA0 | LDR Output | Controls LED based on light levels |  
| PA1 | Right IR Sensor | Detects line |  
| PA6 | Left IR Sensor | Detects line |  
| PA10 | Buzzer | Activates on gas/flame detection |  
| PA11 | Gas Sensor | Detects gas/flame |  
| PA15 | 7-Segment Display | Displays obstacle alert |  
| PB0 | LDR Input | Reads light intensity |  
| PB1 | LED | Alert LED |  
| PB3, PB4 | Counting LEDs | Displays alert sequence |  
| PB5 | Trigger Pin (Ultrasonic) | Triggers ultrasonic sensor |  
| PB6 | Echo Pin (Ultrasonic) | Receives ultrasonic pulse |  

---

## 🚀 How It Works  
1. The robot starts by checking for line signals using IR sensors.  
2. If an obstacle is detected, the robot stops and alerts.  
3. If gas or flame is detected, the buzzer and LED are activated for safety.  
4. Light levels are monitored using an LDR, controlling an LED based on brightness.  

---

## 🏆 Outcome  
This project demonstrates real-time robot movement, obstacle detection, and environmental awareness using STM32 microcontrollers and sensors. 🚀  

---

## ✨ Author  
**[Bhoomika H Salian](https://github.com/Bhoomika-Sahyadri-ECE)**  
