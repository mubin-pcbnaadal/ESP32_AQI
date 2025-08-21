Blower PCB

This repository contains the hardware design files and schematics for the Blower PCB, a custom board built around the ESP32-S3-WROOM-1 module with integrated sensor, display, and blower control interfaces. The board is designed for embedded IoT applications that require environmental sensing, wireless connectivity, and actuator control.

🚀 Features

Microcontroller

ESP32-S3-WROOM-1-N16R8

Dual-core Xtensa LX7 processor with Wi-Fi and Bluetooth 5.0

USB-UART bridge (CP2102-GMR) for programming and debugging

Sensors

Multiple BME688 environmental sensors (temperature, humidity, gas, pressure) on SPI bus

Individual chip select lines for multi-sensor support

Display & Storage

E-paper display connector with dedicated SPI interface (MOSI, MISO, SCLK, CS)

External SPI flash (W25Q16DVSSIG) for storage

Blower Control

MOSFET-based driver stage for blower motor control

External connectors (J2/J3) to interface with blower unit

Power Management

Li-ion battery charging circuit (MCP73831T)

Boost converter (TPS61200) and buck-boost regulator (TPS63070)

Battery protection IC (DW01A + FS8205A dual MOSFET)

Peripherals

RGB LED (SK6805-2427) for status indication

Reset & enable circuitry with push-button

I²C expander (TCA6408ARGTR) for additional GPIOs

RTC module (PCF8523T) with 32.768 kHz crystal and coin-cell backup
