# Project 01 - From A to B

## Overview

Developed a basic conveyor control system using Siemens TIA Portal V16, PLCSIM and Factory I/O.

The conveyor transports a box until it reaches a photoelectric sensor.

The project demonstrates industrial start/stop control using a seal-in circuit.

---

## Features

- Start Button
- Stop Button
- Seal-in Circuit
- Conveyor Control
- Photoelectric Sensor Stop
- Factory I/O Integration

---

## Software

| Software | Version |
|----------|---------|
| TIA Portal | V16 Update 8 |
| S7-PLCSIM | V16 Update 4 |
| Factory I/O | 2.5.6 |

---

## PLC

CPU1211C DC/DC/DC

---

## Ladder Logic

Network 1
Start / Stop Seal-in

Network 2
Conveyor Control

---

## Lessons Learned

- Factory I/O Stop Button is Active Low.
- Factory I/O Photo Sensor is Active Low.
- Official Factory I/O Template simplifies PLCSIM communication.
