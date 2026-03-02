# Flipper DIY
**Designed by enexis & dripside**

<img width="963" height="467" alt="image" src="https://github.com/user-attachments/assets/583e6a9f-6850-473e-be6f-fb18482c4aef" />

This project is an open-source, DIY-friendly replacement PCB for the Flipper Zero. It is designed to be **fully compatible** with the original Flipper Zero housing without any modifications to the plastic shell. Whether you are building from scratch or repairing a device, this board brings the full suite of Flipper capabilities to a custom PCB.

**Firmware Compatibility:**
The PCB trace routing and pinout are fully compatible with the firmware configuration used in the [GthiN89/FuckingCheapFlipperZero](https://github.com/GthiN89/FuckingCheapFlipperZero-DIY-Flipper-zero-The-real-on) project. This ensures that you can use the software and pin definitions from that repository without additional mapping.
## Features & Support

* **Sub-GHz:** Full radio support via external module.
* **NFC:** High-performance NFC read/write capabilities.
* **Infrared (IR):** Dedicated Send and Receive channels.
* **External GPIO:** Standard 0.1" headers for modules and debugging.
* **iButton:** 1-Wire protocol support for Dallas keys.
* **Peripheral Support:** Full support for original buttons and the LCD.
* **Form Factor:** 100% mechanical compatibility with the original case.

---

## Bill of Materials (BOM)

| Component | Description |
| --- | --- |
| [STM32WB55CGU6](https://ali.click/fo7d11q) | **Main MCU:** Dual-core processor with BLE support. |
| [AS07-M1101S](https://ali.click/gs7d118) | **Sub-GHz Module:** Based on CC1101 for radio communication. |
| [ST7565R 1.4 inch](https://ali.click/oz7d110) | **Screen:** 128x64 Monochrome LCD. |
| [ST25R3916](https://www.elechouse.com/product/st25r3916_nfc_reader/) | **NFC Chip:** High-performance NFC/RFID reader. |
| [SN74HC165D](https://ali.click/ph8d11m) | **Shift Register:** Manages button inputs to save GPIO pins. |
| [TP4056](https://ali.click/fu9d11d) | **Battery Charger:** Manages Li-Po charging cycles. |
| [Type-C Connector](https://ali.click/qy9d117) | **USB Interface:** For charging and PC data connection. |
| **IR LED** | **IR Send:** High-power infrared emitter. |
| **IR Receiver** | **IR Receive:** Demodulator for capturing remote signals. |
| **3.7V Battery** | **Power:** Standard Li-Po battery. |
| **SMD Resistors 0603** | **Passives:** Various values (4.7kΩ, 190Ω, 470Ω, 10kΩ). |
| **MMBT2222A** | **N-Channel Transistor:** For switching IR LEDs. |
| **1N4148W** | **SMD Diodes:** Signal protection and logic. |
| **SMD Tactile Buttons** | **Input:** Navigation and "Back" buttons. |

---

## Assembly Instructions

To ensure a successful build, follow this specific soldering order to avoid mechanical interference:

1. **Phase 1 (Low Profile):** Solder the **MicroSD slot**, the **Shift Register (SN74HC165D)**, and all **SMD Resistors**. These are difficult to access once larger components are installed.
2. **Phase 2 (Display):** Install the **LCD Screen**. Ensure it is aligned perfectly before soldering the ribbon/pins.
3. **Phase 3 (Final):** Solder all remaining components, including the MCU, NFC chip, and buttons.

### Antenna Installation

The Sub-GHz antenna requires a two-step connection:

* First, solder the antenna wire to its **dedicated pin** on the PCB.
* Then, bridge/solder the connection to the **CC1101 (AS07-M1101S)** module output.

---

## GPIO Pinout Guide

Refer to the image below for the correct pin mapping when connecting external modules or sensors.
<img width="948" height="339" alt="image" src="https://github.com/user-attachments/assets/70a5ab3a-253f-46a1-ba61-ce2fcb7322e9" />


---

> **Note:** This is a hobbyist project. Ensure you have a fine-tip soldering iron or a hot air station.
