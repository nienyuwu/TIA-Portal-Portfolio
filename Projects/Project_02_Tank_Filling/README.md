# Project 02 - Tank Filling

![TIA Portal](https://img.shields.io/badge/TIA%20Portal-V16-blue)
![Factory IO](https://img.shields.io/badge/Factory%20IO-2.5.6-green)
![PLC](https://img.shields.io/badge/PLC-S7--1200-orange)

![Scene](Images/scene.png)

Automatic tank filling and discharge control using Siemens TIA Portal, Factory I/O and PLCSIM.

---

## Overview

Developed an automatic tank filling system using **Siemens TIA Portal V16**, **S7-PLCSIM**, and **Factory I/O**.

The PLC automatically fills and discharges an analog tank by monitoring the tank level, controlling analog valves, and managing the filling sequence with timers.

This project demonstrates analog signal processing, automatic sequence control, manual override, and analog output control using Ladder Logic.

---

## Features

- Automatic Tank Filling
- Automatic Tank Discharge
- Analog Tank Level Processing
- Analog Valve Control
- Manual Fill / Discharge Override
- TON Timer Control
- Automatic Sequence Control
- Factory I/O Integration
- Siemens S7-1200 PLC Simulation

---

## Software

| Software | Version |
|----------|---------|
| Siemens TIA Portal | V16 Update 8 |
| S7-PLCSIM | V16 Update 4 |
| Factory I/O | 2.5.6 |

---

## PLC Hardware

**CPU:** Siemens S7-1200 CPU1211C DC/DC/DC

---

## I/O Mapping

### Inputs

| Tag | Address | Description |
|------|---------|-------------|
| Tank_Level | %ID30 | Analog Tank Level |
| Tank_Flow | %ID34 | Analog Tank Flow |
| Start_Button | %I0.0 | Start Pushbutton |
| Stop_Button | %I0.1 | Stop Pushbutton |
| Emergency_Stop | %I0.2 | Emergency Stop |
| Manual_Fill_Button | %I0.3 | Manual Fill |
| Manual_Discharge_Button | %I0.4 | Manual Discharge |

### Outputs

| Tag | Address | Description |
|------|---------|-------------|
| Fill_Valve | %QD30 | Analog Fill Valve |
| Discharge_Valve | %QD34 | Analog Discharge Valve |

---

## Ladder Logic

### Network 1 — Analog Signal Processing

Converts analog tank level into digital fill and discharge states.

### Network 2 — Machine Enable

Implements Start / Stop control and machine enable logic.

### Network 3 — Manual Operation

Processes manual fill and discharge requests.

### Network 4 — Automatic Sequence

Controls automatic filling and discharge using TON timers and state transitions.

### Network 5 — Command Merge

Combines manual and automatic commands with manual priority.

### Network 6 — Analog Output Control

Converts digital commands into analog valve outputs.

---

## Project Structure

```text
Project_02_Tank_Filling
│
├── FactoryIO
│   ├── Tank_Filling.factoryio
│   └── driver_config.png
│
├── Images
│   ├── scene.png
│   ├── ladder.png
│   ├── plc_tags.png
│   ├── factoryio_driver.png
│   └── ...
│
└── README.md
```

---

## Screenshots

### Ladder Logic

![Ladder](Images/ladder.png)

### PLC Tags

![PLC Tags](Images/plc_tags.png)

### Factory I/O Driver Configuration

![Driver](Images/factoryio_driver.png)

---

## Demonstration

The demonstration video, archived TIA Portal project (.zap16), and Factory I/O scene will be available in the GitHub Release.

---

## Lessons Learned

- Factory I/O Analog Tank uses REAL values from **0.0 to 10.0**.
- Analog valves accept REAL values from **0.0 (closed)** to **10.0 (fully open)**.
- Analog signals can be converted into digital states for sequence control.
- Automatic filling and discharge can be implemented using state-based logic and TON timers.
- Manual commands can safely override automatic control through command merging.
- Separating signal processing, sequence control, and output control simplifies PLC program design.

---

## PLC Concepts

- PLC Programming
- Ladder Logic (LAD)
- Analog Inputs
- Analog Outputs
- Analog Signal Processing
- TON Timers
- Set / Reset Instructions
- State-based Sequence Control
- Manual Override
- Analog Valve Control
- Factory I/O Integration
- PLC Simulation
- Industrial Automation

---

## Author

Created by **Nien-Yu Wu**

Automation Engineering Portfolio

GitHub: <https://github.com/nienyuwu>
