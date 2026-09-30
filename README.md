# Charger-Board

TP4056 Lithium-Ion Battery Charger Board

📌 Project Overview

This project presents the design and implementation of a Lithium-Ion Battery Charger Board using the TP4056 IC. The TP4056 is a complete constant-current/constant-voltage linear charger designed for charging single-cell lithium-ion and lithium-polymer batteries.

The charger board accepts 5V input through a USB Type-C connector and safely charges a 3.7V Li-ion battery with charging status indication using LEDs.

The schematic and PCB are designed using KiCad.

🔧 Components Used
Component	Value
TP4056-42-ESOP8	Battery Charging IC
USB Type-C Connector	Power Input
Battery Connector	JST-PH 2-Pin
R1	1.2 kΩ
R2	1 kΩ
R3	1 kΩ
C1	10 µF
C2	10 µF
D1	Charging LED
D2	Fully Charged LED
⚡ Features
USB Type-C input
Supports single-cell 3.7V Li-ion/Li-Po batteries
Constant Current / Constant Voltage charging
Automatic charge termination
Charging status indication
Thermal regulation
Battery protection compatibility
Compact PCB design
🔌 Circuit Description

The TP4056 charger operates using the CC/CV charging method.

Stage 1: Constant Current Charging

The battery is charged with a fixed current determined by the resistor connected to the PROG pin.

Stage 2: Constant Voltage Charging

When the battery voltage reaches 4.2V, the TP4056 maintains a constant voltage and gradually reduces the charging current.

Charge Completion

Charging stops automatically when the charging current drops to approximately 10% of the programmed value.



Charging current:

Icharge ≈ 1000 mA
💡 LED Indication
LED Status	Meaning
CHRG LED ON	Charging
STDBY LED ON	Battery Fully Charged
🛠️ Software Used
KiCad
KiCad Schematic Editor
KiCad PCB Editor
ERC (Electrical Rules Check)
DRC (Design Rule Check)
📁 Project Structure
TP4056-Charger/
│
├── README.md
├── TP4056.kicad_sch
├── TP4056.kicad_pcb
├── Gerber/
├── Images/
│   ├── Schematic.png
│   └── PCB.png
└── Datasheet/
    └── TP4056.pdf
📦 Recommended Footprints
Component	Footprint
TP4056	SOIC-8-1EP_3.9x4.9mm
Resistors	R_0805
Capacitors	C_0805
LEDs	LED_0805
USB Type-C	Depends on connector
Battery Connector	JST_PH_2Pin
🚀 Applications
Power banks
Portable electronics
DIY battery packs
IoT devices
Wearable devices
Rechargeable gadgets
📷 Circuit Diagram

Add your KiCad schematic image:

![Schematic](Images/Schematic.png)
📚 References
TP4056 Datasheet
KiCad Documentation
USB Type-C Specification
👨‍💻 Author

Manideep

Designed using KiCad for learning PCB design and battery charging circuits.
