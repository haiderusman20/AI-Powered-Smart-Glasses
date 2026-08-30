# AI-Powered Smart Glasses

## 📌 Overview

This repository contains the hardware design of an **AI-powered smart glasses platform** developed around the **Qualcomm Open-Q 610 μSOM**.

The design integrates camera, audio, power management, security, USB, debugging, and haptic-feedback subsystems into a compact wearable embedded platform.

The complete schematic is designed in **Altium Designer** and is organized into six functional sheets covering the system, SOM interface, power, camera, audio, and I/O peripherals.

---

## 🧠 System Architecture

The platform is based on:

- **Qualcomm Open-Q 610 μSOM** — Primary processing platform
- **Sony IMX219** — Camera interface
- **ATSHA204A-MAHCZ-S** — Hardware security / SHA-256 cryptography
- **BQ25895RTWR** — Battery charging and power management
- **SPH0645LM4H-1-8** — Digital microphones
- **MAX98357AEWL+** — Digital audio amplifiers
- **8 Ω / 2 W speakers** — Audio output
- **DC vibration motor** — Haptic feedback
- **USB Type-C** — USB and power interface
- **Dedicated debug connector** — UART, reset, and forced USB boot

---

## 📷 Camera Interface

The camera subsystem is built around the **Sony IMX219** and provides a MIPI CSI interface to the Open-Q 610 platform.

Key features include:

- 4-lane MIPI CSI interface
- MIPI CSI clock pair
- CCI I²C control interface
- 24 MHz camera clock
- 2.85 V camera supply
- 1.8 V camera I/O supply
- 1.2 V camera supply
- Dedicated camera power regulation
- I²C level shifting
- Local power decoupling

---

## 🎙️ Audio System

The audio subsystem provides dual digital microphones and stereo speaker output.

### Microphones

- **2 × SPH0645LM4H-1-8**
- Digital audio interface
- BCLK
- WS
- DATA
- Channel selection
- Local decoupling and filtering

### Speaker Amplifiers

- **2 × MAX98357AEWL+**
- I²S digital audio interface
- Left and right audio channels
- 8 Ω / 2 W speaker outputs
- SD_MODE control
- Gain configuration
- Output filtering

---

## 🔋 Power Architecture

The power system is built around the **BQ25895RTWR** battery-management IC.

The design includes:

- USB VBUS input
- Battery input
- VSYS power rail
- PMID
- REGN
- Switching power stage
- Battery charging
- I²C control
- Battery-status indication
- Multiple regulated power rails
- Dedicated power test points

The power architecture provides the required rails for the processor, camera, audio, sensors, and peripheral circuitry.

> **Note:** Final battery configuration and protection requirements should be verified against the selected battery pack before hardware release.

---

## 🔌 I/O & Peripherals

### USB Type-C

- USB 2.0 High-Speed interface
- VBUS
- CC1 / CC2
- USB ESD protection
- Power-control circuitry
- Interface to the Open-Q 610

### Debug Interface

A dedicated debug connector provides:

- `DEBUG_UART_TX`
- `DEBUG_UART_RX`
- `RESET`
- `FORCED_USB_BOOT`
- 1.8 V
- GND

This interface is intended for board bring-up, debugging, and system development.

### Haptic Feedback

A DC vibration motor is controlled through a MOSFET-based driver stage using:

- `VM_CTRL`
- AO3407A
- 1N5819HW-7-F
- Gate pull-up
- Dedicated motor supply

---

## 🛠️ Hardware Design Highlights

The design focuses on:

- Compact wearable electronics
- High-density component placement
- Multi-layer PCB architecture
- High-speed digital interfaces
- MIPI CSI routing
- Differential pair routing
- Dedicated ground references
- Multiple regulated power domains
- USB 2.0 High-Speed connectivity
- Digital audio interfaces
- Hardware security
- Dedicated debugging
- Haptic feedback
- Design-for-manufacturing considerations

---

## 📂 Repository Contents

The repository contains the engineering design and documentation for the project:

- Altium Designer schematic files
- PCB design files
- Gerber / manufacturing files
- Bill of Materials (BOM)
- Schematic PDF
- PCB layout views
- 3D board views
- System block diagrams
- Hardware documentation
- Design notes
- Prototype and validation documentation

---

## 📑 Schematic Organization

The current schematic is organized into six main sections:

| Sheet | Description |
|---|---|
| 01 | Title Page / System Overview |
| 02 | Open-Q 610 μSOM |
| 03 | Power Section |
| 04 | Camera |
| 05 | Audio |
| 06 | I/O Peripherals |

The hardware design is developed in **Altium Designer**.

---

## 🎯 Design Focus

This project focuses on developing a **compact AI-enabled wearable hardware platform** by integrating:

- Embedded processing
- Computer vision
- Digital audio
- Power management
- Hardware security
- USB connectivity
- Debug interfaces
- Haptic feedback

The design emphasizes **compact hardware integration, reliable power architecture, high-speed interface design, and practical wearable implementation**.

---

## 🚧 Project Status

**Status: Hardware Development / Prototype**

The project is currently under active hardware development. PCB implementation, prototype fabrication, hardware bring-up, testing, and subsequent design revisions are part of the development process.

---

## 👨‍💻 Author

**Usman Haider**

Hardware Design Engineer

**TraceForge Technologies**
