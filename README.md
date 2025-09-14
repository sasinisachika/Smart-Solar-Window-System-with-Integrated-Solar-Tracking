# 🌞 Smart Solar Window System with Integrated Sun Tracking & Intelligent Control

## 📖 Overview

This project presents a multi-functional Smart Solar Window System that combines the benefits of transparent photovoltaic solar technology, automatic solar tracking, and smart environmental responsiveness.

Unlike conventional solar windows (which are static and inefficient) or smart windows (which focus only on automation and comfort), this system merges both concepts into one solution:

- Generates renewable energy through integrated transparent/semi-transparent solar cells.
- Tracks the sun dynamically with a single-axis solar tracking mechanism to optimize solar capture.
- Functions as a smart window, adapting automatically to environmental and safety conditions (rain, smoke) while allowing manual and scheduled control.

This approach addresses two of the biggest challenges in urban sustainability:

- Limited rooftop space for solar panels.
- Need for energy-efficient, adaptable building components.

---

## 🏗️ What Was Done in This Work

✔️ **System Design & Implementation**

- Designed a solar window that integrates PV panels directly into window glass without compromising ventilation or visibility.
- Developed a single-axis solar tracking system (based on LDR sensors and servo motor) to continuously optimize energy capture.
- Added chain-driven actuators for smooth window opening/closing.

✔️ **Smart Automation Features**

- **Rain Sensor (YL-83):** closes the window automatically to protect interiors.
- **Smoke Sensor (MQ-2):** opens fully during smoke/fire for safety ventilation.
- **Manual & Scheduled Control:** users can override automation and set window operation schedules.

✔️ **Control Algorithm**

- Implemented a PI controller for stable, efficient solar tracking.
- Used threshold-based LDR comparison to avoid unnecessary micro-adjustments.
- Developed a workflow logic prioritizing safety (smoke > rain > solar tracking).

✔️ **Simulation & Validation**

- Built a MATLAB/Simulink model for solar tracking dynamics.
- Verified panel motion, angle response, and tracking efficiency under step changes in light conditions.
- Demonstrated stable alignment with sun position while maintaining ventilation.

✔️ **Energy Flow**

- Solar energy harvested → converted from DC to AC → stored in batteries or supplied to the grid.
- Energy used not only for building power but also to self-sustain window automation.

---

## ⚡ Key Contributions

- Dual-purpose window design – ventilation + renewable energy.
- Integrated solar tracking – increases energy generation compared to fixed PV windows.
- Smart environmental control – adapts automatically to rain, smoke, and user preferences.
- Prototype simulation & algorithm – validated using Simulink and control models.
- Urban sustainability solution – addresses both space constraints and energy efficiency in modern buildings.

---

## 🔧 System Architecture

**Components Used:**
- Arduino Uno (ATmega328P) – microcontroller brain
- Transparent Photovoltaic Solar Cells – energy harvesting
- YL-83 Rain Sensor – automatic closure during rain
- MQ-2 Smoke Sensor – automatic opening during smoke/fire
- LDR Sensors – sunlight tracking
- Servo Motor (BLDC) – panel orientation adjustment
- Chain-driven Actuator – window movement mechanism
- Energy Storage System – battery + inverter for AC output

**Control Logic Flow:**
1. Smoke check → if detected → window opens fully.
2. Rain check → if detected → window closes.
3. Normal mode → user sets ventilation → solar tracking activates.
4. Tracking → LDRs compare sunlight → motor adjusts → PI controller stabilizes position.

---

## 📊 Results & Findings

- Solar tracking improved energy capture compared to fixed PV windows.
- PI control ensured stability, preventing oscillations in panel movement.
- Simulations confirmed correct response of panel under torque inputs and light shifts.
- System demonstrated adaptability, balancing ventilation, safety, and energy harvesting simultaneously.

---

## 🚀 Future Work

- Extend to dual-axis tracking without compromising airflow.
- Integrate IoT-based monitoring and remote control.
- Optimize material costs for commercial adoption.
- Deploy in real building prototypes for field testing.
