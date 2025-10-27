Jurgen Smart Oven - Microcontroller Based System Design
📋 Project Overview
The Jurgen Smart Oven is a comprehensive microcontroller-based embedded system project developed for the EEE 4705: Microcontroller Based System Design course at the Islamic University of Technology (IUT). This project implements a fully functional smart oven prototype using the AT89S52/AT89C51 microcontroller, featuring advanced user interface capabilities, safety mechanisms, and intelligent cooking modes.


✨ Key Features
🕒 Advanced Timer System
User-Defined Timing: Set cooking duration from 5 to 300 seconds via keypad input

Input Validation: Automatically rejects inputs outside the valid range (<5s or >300s)

Real-time Countdown: Three 7-segment displays show remaining time in seconds

📊 Intelligent Display System
Dual-Mode LCD Messaging:

Quick Cook Mode (Time < 60s): Displays fixed cooking messages

Extended Cook Mode (Time > 60s): Shows rotating random facts about food and cooking

Dynamic Content: 11 different cooking facts that rotate during operation

🔔 Multi-Modal Notifications
Audible Alert: Buzzer sounds when countdown completes

Visual Indicators: LED status lights show oven operational state

LCD Feedback: Real-time status messages and error notifications

🛡️ Safety & Control Features
Emergency Stop: Instant oven shutdown in any situation

Restart Capability: Dedicated restart button after operation completion

Input Validation: Comprehensive error checking for user inputs

Heating Control: Precise control of heating element with safety protocols

🛠️ Technical Specifications
🎛️ Hardware Components
Microcontroller: AT89S52/AT89C51

Clock Frequency: 13.00021247 MHz (custom calculated)

Display System:

16x2 LCD for text messages and status

Three 7-segment displays for countdown timer

Input System: 4x4 Matrix Keypad (0-9, A-F)

Output Indicators:

Buzzer for audio notification

LED status indicators

Heating element control

Control Buttons:

Start button

Restart button

Emergency stop button

💾 Memory Organization
Program Memory: Organized assembly code with structured subroutines

Data Memory: Efficient use of internal RAM for:

Timer values storage (40H, 44H, 53H)

Counter variables (R0-R7)

System flags and status registers

🔧 System Architecture
🏗️ Code Structure
The system is built using 8051 assembly language with modular architecture:

assembly
; Main Program Flow
1. INITIALIZE        - System initialization and port configuration
2. LCD_INIT          - LCD display setup and calibration
3. TIME_INPUT_LOOP   - User input handling and validation
4. COOKING_LOOP_1/2  - Main cooking routines (two modes)
5. DECREMENT_TIMER   - Real-time timer management
6. DISPLAY_MANAGER   - Multi-display coordination
🔄 Operational Modes
Mode 1: Quick Cooking (<60 seconds)
Fixed power setting

Continuous cooking tip display

Simplified countdown display

Mode 2: Extended Cooking (>60 seconds)
Enhanced power management

Rotating cooking facts display

Advanced display updates

⌨️ Keypad Mapping
text
[1] [2] [3] [A]
[4] [5] [6] [B]
[7] [8] [9] [C]
[0] [F] [E] [D]

Special Functions:
- F: Start cooking
- A-F: Reserved for future expansion
📁 Project Structure
text
Jurgen-Smart-Oven/
├── Documentation/
│   └── JURGEN_OVEN_REPORT_monir.pdf
├── Source Code/
│   └── jargon_oven.asm
├── Simulation/
│   ├── Proteus Schematic Files
│   └── Component Configuration
├── Resources/
│   └── Features.PNG
└── README.md
🚀 Implementation Details
🔢 Timer Management System
Three-Digit Input: Hundreds, tens, and ones places stored separately

Mathematical Conversion: Converts keypad input to actual seconds

Range Validation: Comprehensive checking for 5-300 second range

Real-time Decrement: Smooth countdown with underflow handling

🎮 User Interface Flow
Initial Prompt: "ENTER TIME IN s:"

Digit-by-Digit Input: Three-digit time entry with real-time display

Mode Selection: Automatic based on time duration

Cooking Phase: Real-time countdown with dynamic messaging

Completion: Buzzer notification and reset options

🔄 Random Fact System
Pseudo-Random Generation: Uses timer values for fact selection

11 Unique Facts: Food-related tips and cooking information

Rotating Display: Changes facts during extended cooking sessions

⚙️ Technical Implementation
🔧 Port Configuration
assembly
P0 - Keypad scanning interface
P1 - LCD data port
P2 - Control signals (RS, EN, Buzzer, Heating, Display select)
P3 - 7-segment display output
⏰ Timing Subroutines
DELAY_1S: Precise 1-second delay using Timer 0

SHORT_DELAY: Keypad debouncing (∼10ms)

LONG_DELAY: Extended delays (∼5 seconds)

DISPLAY_DELAY: 7-segment display refresh timing

🖥️ Display Management
LCD Commands: Standard HD44780 command set

7-Segment Patterns: Common cathode display patterns

Multiplexing: Time-division multiplexing for three displays

🛠️ Development Tools
💻 Software Requirements
Assembler: ASEM-51 or equivalent 8051 assembler

Simulator: Proteus Design Suite

Programming Tool: Suitable AT89S52 programmer

Editor: Any text editor with assembly syntax support

🔌 Hardware Setup
AT89S52/AT89C51 Development Board

16x2 LCD Display

Three 7-segment Common Cathode Displays

4x4 Matrix Keypad

Buzzer and LED indicators

Heating element with driver circuit

Power supply unit

📊 Performance Characteristics
⚡ System Performance
Response Time: Immediate keypad response with debouncing

Display Refresh: Smooth 7-segment multiplexing

Timer Accuracy: Precise 1-second intervals

Power Management: Efficient heating element control

🎯 Reliability Features
Input Validation: Comprehensive error checking

Safe Shutdown: Emergency stop functionality

Memory Management: Proper register initialization

Error Recovery: Automatic reset and retry mechanisms

🔍 Code Highlights
🎪 Innovative Features
Dynamic Message System: Context-aware display messages

Semi-Random Fact Generator: Creative use of timer for randomness

Dual-Mode Operation: Adaptive behavior based on cooking duration

Comprehensive Error Handling: User-friendly error messages

💡 Technical Achievements
Efficient Memory Usage: Optimal use of limited 8051 resources

Real-time Multi-tasking: Simultaneous display updates and timing

Robust Input Handling: Debounced keypad with validation

Structured Programming: Modular, maintainable assembly code

🚀 Getting Started
📋 Prerequisites
Basic knowledge of 8051 microcontroller architecture

Proteus simulator for circuit simulation

8051 assembler for code compilation

Hardware components for physical implementation

🔧 Installation Steps
Assemble the Code: Use ASEM-51 or compatible assembler

Load HEX File: Program the microcontroller with generated HEX file

Setup Hardware: Connect all components as per schematic

Power On: Apply 5V power supply to the system

Test Functionality: Verify all features working correctly

🎮 Operation Guide
Power on the system

Enter desired cooking time (3 digits)

Press 'F' to start cooking

Monitor countdown on 7-segment displays

View cooking messages/facts on LCD

System alerts when cooking completes

Use restart or emergency stop as needed

🐛 Known Limitations & Future Enhancements
⚠️ Current Limitations
Fixed 5-300 second timer range

Limited to 11 cooking facts

Basic pseudo-random number generation

No temperature sensing capability

🔮 Potential Improvements
Temperature monitoring and control

Recipe storage and recall

Wireless connectivity for remote control

Power level adjustment

Expanded fact database

Graphical display interface

👨‍💻 Developer Information
Developer: K. M. Sirazul Monir
Student ID: 200021247
Institution: Islamic University of Technology (IUT)
Department: Electrical and Electronic Engineering
Course: EEE 4705 - Microcontroller Based System Design

📄 License & Acknowledgments
This project is developed as part of academic coursework at IUT. All rights reserved by the developer. The code and design may be used for educational purposes with proper attribution.

🙏 Special Thanks
Islamic University of Technology for resources and support

Department of Electrical and Electronic Engineering

Course instructors for guidance and evaluation

Note: This project demonstrates comprehensive embedded systems design principles and serves as an excellent example of microcontroller-based product development for educational and professional reference.

For any queries or contributions, please contact the developer through the university channels.
