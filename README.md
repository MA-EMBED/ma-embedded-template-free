# ma-embedded-template-free
MA Embedded – Firmware Project Template (Free Edition)

A clean and organised project structure for embedded firmware development.
This template gives you the foundation for building scalable applications on ESP32 and other microcontrollers.

It includes:

- A modular folder layout
- Starter files for each layer
- Naming conventions and layout principles
- Clear separation between BSP, HAL, drivers, services, system and application logic

The goal of this template is simple:
Help embedded engineers start new projects with clarity and a solid architecture instead of reinventing the structure every time.

This is the free version, focused on the structure and core philosophy.
For a full, production-ready version including working GPIO, UART, I2C, device drivers, tasks and board initialization, you can check the Pro Edition.

# Overview

This template provides a clear and modular structure for embedded firmware projects.
It is designed to help engineers start new applications with a solid architectural foundation instead of a blank folder and scattered files.

You will find a clean separation between hardware layers, drivers, services and application logic.
The structure is compatible with ESP32, STM32, PIC, dsPIC and many other microcontrollers.

This Free Edition focuses on project organisation and starter files.
It does not include hardware drivers or board initialisation code.
It is meant to be a strong foundation for your next embedded project.

# Folder Structure
### /bsp
    Board Support Package.
    Holds board-specific definitions such as pin mappings and configuration.

### /bus
    Low-level communication buses such as I2C, SPI or UART.
    These modules abstract raw peripheral operations.

### /drivers
    Device drivers that sit on top of the bus layer.
    Each module represents a specific hardware component.

### /hal
    Hardware Abstraction Layer.
    Provides high-level hardware-independent APIs for the system.

### /services
    Reusable functionality such as sensor managers or communication handlers.

### /system
    System initialization and global logic.
    Responsible for project-wide configuration and boot sequences.

### /utils
    Helper modules including logging, timing utilities and common definitions.

### /app
    Main application source files, tasks, loops and project logic.

Each folder contains a minimal example file to guide you on how to structure future modules.

# Usage Instructions
1. Clone the repository : git clone https://github.com/YOUR_USERNAME/ma-embedded-template-free.git

2. Use the structure for your next firmware project

Copy the folders into your workspace and begin adding:

- Board-specific configuration
- HAL implementations
- Device drivers
- Services and logic
- Tasks or application loops

3. MCU-independent design

This template is intentionally generic. You can use it with:

- Espressif -> ESP32 etc
- ST -> STM32 etc
- Microchip -> PIC / dsPIC
- NXP
- Nordic - NRF..

Any bare-metal MCU architecture

The structure encourages reusability and keeps your project organised as it grows.

# Philosophy Behind This Template
## Modularity

Each layer has a clear purpose.
This makes individual modules easy to modify or reuse.

## Scalability

The structure supports small embedded projects and large multi-module systems.

## Separation of concerns

Drivers do not depend on the application.
The HAL does not depend on specific hardware.
The system layer ties everything together cleanly.

## Professional workflow

This layout mirrors how production-grade firmware is structured in industry.
