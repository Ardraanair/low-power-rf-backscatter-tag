
# ESP32-Based Low-Power RF Backscatter Tag

A compact RF backscatter tag designed in **KiCad**, combining an **ESP32 microcontroller**, low-power power management, RF switching, antenna interfacing, and load-modulation techniques for low-power wireless sensing applications.

---

## 📌 Project Overview

This project focuses on the design and development of a **low-power RF backscatter communication tag**.

Instead of generating a high-power RF carrier directly, the tag uses **RF backscatter/load modulation**, where the impedance presented to the antenna is changed electronically to modulate an incident RF signal.

The **ESP32** acts as the main controller and provides the digital control signals required for the RF modulation stage.

The hardware has been designed and documented using **KiCad**, with the PCB, schematic, component interfaces, and manufacturing files maintained as part of the project.

---

## 🎯 Objectives

- Design a compact RF backscatter tag PCB.
- Use an **ESP32 MCU** for system control and modulation logic.
- Implement RF load modulation using an RF switch.
- Provide a low-power regulated supply for the electronics.
- Interface the digital control system with the RF front-end.
- Provide antenna/RF interfaces suitable for RF characterization.
- Develop a hardware platform that can later be validated using RF laboratory equipment.
- Explore the use of backscatter communication for low-power IoT and wireless sensing applications.

---

## 🏗️ System Architecture

```text
                    ┌─────────────────────┐
                    │     Power Supply    │
                    │   Regulation Stage  │
                    └──────────┬──────────┘
                               │
                               ▼
                    ┌─────────────────────┐
                    │       ESP32         │
                    │        MCU          │
                    │                     │
                    │ • System Control    │
                    │ • GPIO Control      │
                    │ • Sensor Interface  │
                    │ • Modulation Logic  │
                    └──────────┬──────────┘
                               │
                       Modulation Control
                               │
                               ▼
                    ┌─────────────────────┐
                    │     ADG902 RF       │
                    │       Switch        │
                    └──────────┬──────────┘
                               │
                               ▼
                    ┌─────────────────────┐
                    │     RF Front-End    │
                    │                     │
                    │ RF Switching        │
                    │ Matching / Routing  │
                    │ Antenna Interface   │
                    └──────────┬──────────┘
                               │
                               ▼
                           Antenna
                               │
                               ▼
                     Backscattered RF Signal
                               │
                               ▼
                         RF / SDR Reader
