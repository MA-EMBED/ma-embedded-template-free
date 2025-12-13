# MA Embedded Firmware Template (Free Edition)

Author: Mark Agius

A clean and modular firmware folder structure for embedded systems projects.

This template provides a practical starting point for organising embedded firmware in a clear and scalable way, independent of a specific microcontroller or vendor.

It is intended to help engineers avoid starting from an unstructured project layout and instead begin with a proven foundation.

---

## What This Template Provides

The Free Edition focuses on:
- Project organisation
- Layered folder structure
- Clear separation of responsibilities
- Consistent naming and layout

It is intentionally generic and can be adapted to:
- ESP32
- STM32
- PIC / dsPIC
- Nordic
- NXP
- Bare metal or RTOS based projects

No board specific code or hardware drivers are included.

---

## Folder Structure Overview

```
bsp      - Board specific configuration
hal      - Hardware abstraction helpers
bus      - Communication buses
drivers  - External device drivers
services - System level logic
system   - Core system setup
utils    - Shared utilities
app      - Application logic
main     - Application entry point
```

Each folder contains a short README.md describing its role.

---

## Usage

1. Clone the repository

```
git clone https://github.com/MA-EMBED/ma-embedded-template-free.git
```

2. Use this structure as the base for your firmware project

3. Populate the folders according to your target MCU, hardware, and application needs

---

## Free Edition vs Extended Edition

The Free Edition focuses on structure and layout.

An extended edition builds on this foundation with:
- Detailed architectural guidelines
- Reference HAL and bus implementations
- Code and function "shells" for you to populate with your code
- Example services and application flows
- Practical, production oriented examples

---

## Note

This repository provides structure only.

Design decisions, rules, and implementation strategies are intentionally kept minimal in this edition.
