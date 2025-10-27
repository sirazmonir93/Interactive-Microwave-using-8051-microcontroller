# Jurgen Smart Oven Prototype Assignment Report

## Overview

This repository contains the assignment submission for a complex engineering problem involving the design and simulation of a Jurgen Smart Oven Prototype. The project utilizes an AT89S52/AT89C51 microcontroller and was developed as part of the coursework at the Islamic University of Technology (IUT), under the Organisation of Islamic Cooperation (OIC).


## Project Description

The Jurgen Smart Oven Prototype is a simulated smart oven controller featuring a user-defined timer, countdown display, LCD messages, buzzer notifications, LED status indicators, and safety controls. The system is designed to provide an engaging user experience and was simulated using Proteus software.

### Features
1. **User-Defined Timer**: Allows setting cooking time from 5 to 300 seconds via keypad.
2. **Out of Range Input Rejection**: Rejects inputs below 5s or above 300s.
3. **Countdown Display**: Shows countdown on three 7-segment displays.
4. **LCD Message Display**:
   - Time < 60s: Displays a fixed message.
   - Time > 60s: Shows random food/cooking facts.
5. **Buzzer Notification**: Activates when countdown reaches zero.
6. **LED Status Indication**: Indicates oven working state.
7. **Start Button**: Initiates countdown after time input.
8. **Restart Button**: Resets oven post-operation.
9. **Emergency Stop Button**: Instantly halts oven operation.
<img width="895" height="799" alt="Features" src="https://github.com/user-attachments/assets/65e73bd5-4d81-4b53-bf94-2d6323f8a24b" />

**Microcontroller Frequency**: 11 + (22-12) * (Student ID / 10^9) MHz = 13.00021247 MHz

## Documentation

- **Report**: [Assignment Report](JURGEN OVEN REPORT monir.pdf) – Detailed overview, features, and code explanation.
- **Schematic**: [Proteus Schematic Screenshot](proteus_schematic.png) – Visual representation of the circuit design.
- **Code**: [Source Code](code_snippet.png) – Partial view of the 8051 Assembly code.

## Setup and Simulation
<img width="1875" height="796" alt="image" src="https://github.com/user-attachments/assets/ded13e36-8b40-4796-894c-82e590e88358" />

### Prerequisites
- Proteus Simulation Software
- 8051 Assembler (e.g., Keil uVision)

### Steps
1. Load the Proteus schematic and attach the compiled HEX file from the assembly code.
2. Compile the code using an 8051 assembler to generate the HEX file.
3. Run the simulation, input a time (e.g., 030 for 30s), and press Start (F key) to observe functionality.

## Limitations
- Simulation-only prototype; no physical hardware implementation.
- Random fact selection is based on a simple timer-based pseudo-random method.
- Timer accuracy depends on the simulated clock frequency.

## License
All rights reserved by K. M. Sirazul Monir for educational purposes.

## Acknowledgments
- Islamic University of Technology (IUT) and the Department of Electrical and Electronic Engineering.
- Proteus for simulation tools.
