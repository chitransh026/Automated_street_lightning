# 🌙 Smart Street Light System using STM32F103C6

## 📌 Overview

This project implements a **Smart Street Light System** using the STM32F103C6 microcontroller.
The system automatically controls a street light based on:

* 🌑 Ambient light (using LDR)
* 🚶 Motion detection (using PIR sensor)

The goal is to **save energy and improve efficiency** by ensuring lights turn ON only when needed.

---

## ⚙️ Features

* Automatic ON/OFF control
* Motion-based lighting system
* Energy-efficient design
* Real-time sensor monitoring
* Simple and scalable architecture

---

## 🧠 Working Principle

The system follows this logic:

1. LDR senses ambient light intensity
2. If it is **dark (night condition)**:

   * System checks PIR sensor
   * If motion is detected → Light turns ON
   * Else → Light remains OFF
3. If it is **daytime**:

   * Light remains OFF regardless of motion

---

## 🔌 Hardware Components

* STM32F103C6 Microcontroller
* LDR (Light Dependent Resistor)
* PIR Motion Sensor
* LED (Street Light Simulation)
* Resistors (10kΩ, 220Ω)
* Breadboard / Proteus Simulation

---

## 🔗 Pin Configuration

| Component           | STM32 Pin      |
| ------------------- | -------------- |
| LDR (Analog Output) | PA0 (ADC1_IN0) |
| PIR Sensor Output   | PA1            |
| LED                 | PA5            |

---

## ⚡ Circuit Description

### LDR Connection (Voltage Divider)

* LDR connected to 3.3V/5V
* Middle node → PA0

### PIR Sensor

* VCC → 5V
* GND → GND
* OUT → PA1

### LED

* PA5 → LED → GND

---

## 💻 Software Requirements

* STM32CubeIDE
* STM32 HAL Drivers
* Proteus (for simulation)

---

## 🚀 How to Run

1. Configure peripherals using CubeMX:

   * ADC1 → Channel 0 (PA0)
   * GPIO:

     * PA1 → Input (PIR)
     * PA5 → Output (LED)

2. Build the project in STM32CubeIDE

3. Flash to STM32 or load HEX file in Proteus

4. Run simulation / hardware

---

## 🧪 Testing Procedure

* Cover LDR → simulate night
* Move hand near PIR → LED should turn ON
* Remove motion → LED turns OFF
* Apply light → LED remains OFF

---

## ⚠️ Common Issues

* Incorrect LDR wiring → unstable ADC values
* PIR sensor delay → requires warm-up (~30 sec)
* Wrong threshold → improper switching

---

## 🔮 Future Scope

* PWM-based brightness control
* IoT integration (remote monitoring)
* Solar-powered system
* Smart city deployment
* Machine learning for traffic-based lighting

---

## 📊 Applications

* Smart street lighting
* Parking areas
* Highways
* Campus lighting systems
* Home automation

---

## ✅ Conclusion

This project demonstrates an efficient and intelligent lighting system using embedded systems.
By combining sensor data and control logic, it significantly reduces power consumption and improves automation.

---

## 📚 References

1. STM32F1 Reference Manual (RM0008)
2. STM32CubeIDE Documentation
3. PIR Sensor Datasheet (HC-SR501)
4. LDR Working Principle – Electronics Tutorials
5. Embedded Systems Design Resources

---

## 👨‍💻 Author

Developed as part of an embedded systems learning project.
