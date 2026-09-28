# Isolated-SPI-CAN-FD-MCP2518FD-ISO1042
Open-source isolated SPI-to-CAN FD module based on Microchip MCP2518FD CAN FD controller and Texas Instruments ISO1042 isolated CAN transceiver.
Isolated SPI-to-CAN FD Module

An open-source galvanically isolated SPI-to-CAN FD interface module based on the Microchip MCP2518FD CAN FD controller and Texas Instruments ISO1042 isolated CAN transceiver.

The module provides a practical solution for adding a reliable, isolated CAN/CAN FD interface to microcontrollers that have an available SPI interface but do not have an integrated CAN FD peripheral.

Features

- Single CAN FD channel
- Galvanic isolation
- SPI interface
- MCP2518FD CAN FD controller
- ISO1042 isolated CAN transceiver
- Supports Classical CAN (CAN 2.0B)
- Supports CAN FD
- CAN arbitration bit rate up to 1 Mbps
- CAN FD data bit rate up to 5 Mbps with ISO1042
- ±70 V DC CAN bus fault protection
- ±16 kV HBM ESD tolerance on CAN bus pins
- ±30 V common-mode voltage range
- Driver Dominant Time-Out (TXD DTO)
- High-impedance passive CAN bus terminals when unpowered
- Compact PCB design

Main Components

MCP2518FD – CAN FD Controller

The MCP2518FD is a CAN FD controller that communicates with the host microcontroller through an SPI interface.

Key capabilities:

- Classical CAN 2.0B support
- CAN FD support
- Arbitration bit rate up to 1 Mbps
- Data bit rate up to 8 Mbps
- 31 configurable FIFOs
- 32 flexible filter and mask objects
- ISO 11898-1:2015 compliant CAN protocol controller

ISO1042 – Isolated CAN Transceiver

The ISO1042 is a galvanically isolated CAN transceiver from Texas Instruments.

Key features:

- ISO 11898-2:2016 physical-layer compliance
- Classical CAN up to 1 Mbps
- CAN FD support
- CAN FD data rate up to 5 Mbps
- Low loop delay
- ±70 V bus fault protection
- ±16 kV HBM ESD protection on CAN bus pins
- ±30 V common-mode voltage range
- TXD dominant-state time-out protection

Block Diagram

             ┌──────────────────────┐
             │   Host Microcontroller│
             │                      │
             │      SPI Interface   │
             └──────────┬───────────┘
                        │
                        │ SPI
                        ▼
             ┌──────────────────────┐
             │      MCP2518FD       │
             │     CAN FD Controller│
             └──────────┬───────────┘
                        │
                        │ CAN TX/RX
                        ▼
             ┌──────────────────────┐
             │       ISO1042        │
             │ Isolated CAN Transceiver│
             └──────────┬───────────┘
                        │
                  Galvanic Isolation
                        │
                        ▼
                  ┌────────────┐
                  │  CAN Bus   │
                  │ CANH/CANL  │
                  └────────────┘

Applications

This module can be used for:

- Industrial automation
- Embedded systems
- Automotive electronics
- EV and charging applications
- Battery management systems
- Motor controllers
- Power electronics
- Industrial communication
- Data acquisition systems
- Microcontrollers without an integrated CAN FD peripheral

Repository Contents

Isolated-SPI-CAN-FD/
│
├── Hardware/
│   ├── Schematic/
│   ├── PCB/
│   ├── Gerber/
│   ├── BOM/
│   └── Manufacturing/
│
├── Documentation/
│   ├── Datasheets/
│   └── Design_Notes/
│
├── Images/
│   ├── Schematic.png
│   ├── PCB_3D.png
│   └── Board_Top.png
│
├── LICENSE
└── README.md

Design Information

Parameter| Specification
CAN Channels| 1
CAN Controller| MCP2518FD
CAN Transceiver| ISO1042
Host Interface| SPI
Isolation| Galvanic
Classical CAN| Supported
CAN FD| Supported
Arbitration Rate| Up to 1 Mbps
CAN FD Data Rate| Up to 5 Mbps with ISO1042
Bus Fault Protection| ±70 V
Bus ESD Protection| ±16 kV HBM
Common-Mode Range| ±30 V

PCB Design

The PCB has been designed with focus on:

- Compact form factor
- Proper isolation between logic and CAN domains
- CAN signal integrity
- Short high-speed signal paths
- Appropriate power decoupling
- Practical manufacturing considerations
- CAN bus termination provisions

Hardware Files

The repository includes the available hardware design files:

- Schematic
- PCB layout
- Gerber files
- Bill of Materials (BOM)
- Manufacturing files
- Design documentation

Open Source

This project is shared as an open-source hardware design for learning, experimentation, prototyping and further development.

You are welcome to:

- Study the design
- Build the hardware
- Modify the design
- Improve the design
- Use it as a reference for your own CAN/CAN FD projects

Please review the component datasheets and validate the design for your specific application before using it in a production or safety-critical system.

Disclaimer

This project is provided for educational, development and prototyping purposes. The design has not been certified for any specific automotive, industrial or safety-critical application.

Users are responsible for validating electrical performance, EMC/EMI compliance, thermal performance, isolation requirements and applicable regulatory requirements for their intended application.

References

- Microchip MCP2518FD CAN FD Controller Datasheet
- Texas Instruments ISO1042 Isolated CAN Transceiver Datasheet
- ISO 11898-1 – CAN Data Link Layer and Physical Signalling
- ISO 11898-2 – High-Speed CAN Physical Layer

Author

Vipin Dhariwal

PCB Design | Embedded Hardware | Electronics | CAN/CAN FD

---

⭐ If you find this project useful, consider starring the repository and sharing your feedback.
