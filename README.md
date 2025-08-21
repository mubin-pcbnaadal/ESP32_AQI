This repository contains the hardware design files and schematics for the Blower PCB, a custom board built around the ESP32-S3-WROOM-1 module with integrated sensor, display, and blower control interfaces. The board is designed for embedded IoT applications that require environmental sensing, wireless connectivity, and actuator control.

🚀 Features

Point 1: The microcontroller is ESP32-S3-WROOM-1-N16R8 with Wi-Fi and Bluetooth 5.0 support.
Point 2: USB-UART bridge (CP2102-GMR) is included for programming and debugging.
Point 3: Multiple BME688 environmental sensors (temperature, humidity, gas, pressure) are connected via SPI, each with its own chip select line.
Point 4: E-paper display connector is available with a dedicated SPI interface (MOSI, MISO, SCLK, CS).
Point 5: External SPI flash (W25Q16DVSSIG) is included for extended storage.
Point 6: Blower control is achieved using a MOSFET-based driver stage with external connectors J2 and J3.
Point 7: Power management includes a Li-ion battery charger (MCP73831T), a boost converter (TPS61200), and a buck-boost regulator (TPS63070).
Point 8: Battery protection circuit integrates DW01A with FS8205A dual MOSFET.
Point 9: RGB LED (SK6805-2427) is provided for status indication.
Point 10: Reset and enable circuitry is included with push-button control.
Point 11: I²C expander (TCA6408ARGTR) provides additional GPIOs.
Point 12: Real-time clock (PCF8523T) with 32.768 kHz crystal and coin-cell backup ensures timekeeping even without main power.

📂 Repository Structure

Step 1: The folder /schematics contains PDF schematic files such as Blower_PCB.pdf.
Step 2: The folder /pcb contains PCB layout design files (Altium or KiCad if available).
Step 3: The folder /firmware will include ESP32 firmware examples.
Step 4: The folder /docs stores documentation and datasheets.

🔌 Connectors and Interfaces

Connector 1: USB-C connector (J1) provides power input and programming interface with VBUS, D+, and D-.
Connector 2: Blower connectors (J2 and J3) allow interfacing with the blower motor.
Connector 3: Display connector (J4) is a 24-pin FPC interface for e-paper display.
Connector 4: Battery connector (J6) accepts a Li-ion battery and integrates protection circuitry.

⚡ Power Options

Option 1: USB power input from VBUS at 5V.
Option 2: Li-ion battery input with nominal voltage of 3.7V.
Option 3: On-board regulation provides stable 3.3V and 5V rails.

🛠️ Getting Started

Step 1: Connect the board via USB-C to program the ESP32-S3.
Step 2: Flash the firmware using ESP-IDF or Arduino-ESP32 framework.
Step 3: Power the board through USB or a Li-ion battery.
Step 4: Attach blower and sensors to begin testing and development.

📜 License

Note 1: This project is licensed under the MIT License.
Note 2: You are free to use, modify, and distribute the design files.
