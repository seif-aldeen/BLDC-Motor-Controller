# 3-Phase BLDC Motor Controller

A custom 3-phase BLDC motor controller designed and implemented using Arduino UNO, IR2110 high/low-side gate drivers, and a MOSFET-based inverter topology.

The project focuses on practical power electronics implementation, MOSFET gate driving, PWM switching, and real hardware debugging challenges.

---

# Project Overview

This controller converts DC input power into controlled 3-phase switching signals to drive a BLDC motor using 6-step commutation.

The system was designed and tested through:
- MATLAB Simulink simulation
- Proteus circuit verification
- Real hardware implementation using perforated PCB

---

# Features

- 3-Phase MOSFET Inverter
- IR2110 High/Low-Side Gate Drivers
- Bootstrap High-Side Driving
- PWM Speed Control
- Open-Loop 6-Step Commutation
- ACS712 Current Monitoring
- Potentiometer Speed Adjustment
- LCD Monitoring Interface
- Dead-Time Protection

---

# Hardware Components

| Component | Purpose |
|---|---|
| Arduino UNO | Main Controller |
| IR2110 | High/Low Side MOSFET Driver |
| IRLZ44N MOSFETs | 3-Phase Inverter |
| UF4004 Diodes | Bootstrap Charging |
| Bootstrap Capacitors | High-Side Supply |
| ACS712 | Current Measurement |
| Potentiometer | Speed Control |
| LCD 16x2 | System Monitoring |

---

# Working Principle

The controller operates using 6-step electronic commutation.

At every switching step:
- One phase is connected to +VDC
- One phase is connected to GND
- One phase remains floating

This creates a rotating magnetic field that drives the BLDC motor rotor.

PWM signals are used to control the effective voltage applied to the motor, which directly controls motor speed.

---

# Simulation

The inverter and BLDC operation were first verified using MATLAB Simulink.

Simulation included:
- Three-phase inverter
- PWM generation
- BLDC motor model
- Voltage measurements
- Phase switching validation

---

# Proteus Circuit Design

The full driver and inverter stages were designed and tested in Proteus before hardware implementation.

Main sections:
- Arduino PWM generation
- IR2110 gate driving
- Bootstrap circuitry
- MOSFET half-bridges
- BLDC motor interface

---

# Hardware Prototype

The hardware prototype was implemented using perforated PCB and point-to-point soldering connections.

Special attention was given to:
- Grounding
- Bootstrap routing
- Power isolation
- Noise reduction
- MOSFET gate wiring

---

# Challenges Faced

This project involved extensive practical debugging including:

- Floating ground issues
- Bootstrap capacitor polarity errors
- MOSFET overheating
- Incorrect driver pin connections
- Shoot-through risks
- High-side switching failure
- PWM timing verification

Most issues were solved through direct measurements using:
- Multimeter testing
- HO/LO signal verification
- VB-VS bootstrap measurements

---

# Project Images

## Proteus Design
<img width="1280" height="1175" alt="1779207032242" src="https://github.com/user-attachments/assets/c7a9b193-a4ad-43b2-af33-08de22c30204" />

## Simulink Model
<img width="1280" height="604" alt="1779207026253" src="https://github.com/user-attachments/assets/6c7c2084-dfda-481e-a5b1-9b254c9b5f18" />

## Hardware Prototype
<img width="480" height="951" alt="1779207027372" src="https://github.com/user-attachments/assets/7de85b40-e7d3-44b7-87ac-5c2f397dfeef" />

## Waveform Results
<img width="1280" height="725" alt="1779207027879" src="https://github.com/user-attachments/assets/f164b0af-7278-49e4-95a6-5bc4764acaa4" />

---

# Future Improvements

- Closed-loop speed control
- Hall sensor feedback
- Sensorless commutation
- PCB manufacturing
- FOC (Field Oriented Control)
- Regenerative braking

---

# Applications

- Robotics
- UAVs
- Electric Vehicles
- Industrial Automation
- Mechatronics Systems

---

# Team

Supervised by:
Dr. Shaimaa Kandil

Helwan National University

Faculty of Engineering

Mechatronics & Robotics Department

Academic Year: 2025/2026

---

# Documentation

Project documentation is included in this repository.
