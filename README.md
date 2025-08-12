# Fuzzy-logic-fopid
# 🤖 Fuzzy Logic FOPID Controller for Self-Balancing Robot

## 📖 Overview
This project implements a **Fuzzy Logic-based Fractional Order PID (FOPID) controller** for a **self-balancing two-wheeled robot** using a **Raspberry Pi 4**.  
The controller uses **MPU6050 IMU sensor data** to calculate the robot’s tilt angle and adjusts the motor speeds via an **L298N motor driver** to maintain balance.  
The Fuzzy Logic layer dynamically tunes the FOPID parameters to achieve faster response and better stability.

---

## ✨ Features
- **Fuzzy Logic FOPID Control** – Combines fractional order PID with fuzzy inference for adaptive tuning.
- **Real-Time Balancing** – Reads tilt data from the MPU6050 and adjusts motor PWM accordingly.
- **Dual Operating Modes** – FOPID control and fuzzy FOPID control for comparison.
- **Motor Control** – Uses GPIO PWM to control L298N motor driver.
- **Sensor Fusion** – Uses a complementary filter to smooth IMU readings.
- **Customizable Rules** – Easy to modify fuzzy rule base for different robot behaviors.

---

## 🛠 Hardware Requirements
- **Raspberry Pi 4** (any 3B/4B will work)
- **MPU6050 IMU Sensor**
- **L298N Motor Driver**
- **Two DC Motors** with wheels
- **12V Battery Pack**
- Jumper wires & chassis

---

## 💻 Software Requirements
- Python 3.x
- `numpy` – Numerical computations
- `RPi.GPIO` – GPIO control
- `mpu6050` – MPU6050 sensor library
- `scikit-fuzzy` – Fuzzy logic implementation
- `time` – Timing operations

---

## 📂 Project Structure
fuzzy_fopid_robot/
│-- main.py # Main control loop
│-- fuzzy_controller.py # Fuzzy logic rules & membership functions
│-- fopid.py # FOPID controller implementation
│-- mpu_sensor.py # MPU6050 reading & filtering
│-- motor_driver.py # L298N motor control functions
│-- utils.py # Helper functions
│-- README.md # Documentation
---

## ⚡ Getting Started

### 1️⃣ Clone the Repository
```bash
git clone https://github.com/YourUsername/fuzzy-fopid-robot.git
cd fuzzy-fopid-robot
