# MA Embedded Firmware Template (Free Edition)

A clean, scalable, and professional firmware architecture template for embedded systems.

This template provides a clear project structure and architectural philosophy to help embedded engineers start new firmware projects with confidence, clarity, and long term maintainability in mind.

Instead of beginning with a blank folder and scattered files, this template gives you a proven foundation that scales from early prototypes to real products.

---

## What This Template Is

This Free Edition focuses on:
- Project organisation
- Layered architecture
- Clear separation of concerns
- Consistent naming and structure

It is intentionally lightweight and generic, making it suitable for:
- ESP32
- STM32
- PIC / dsPIC
- Nordic
- NXP
- Any bare metal or RTOS based MCU project

No board specific code or hardware drivers are included.  
This is about how to structure firmware, not locking you into a specific platform.

---

## Folder Structure Overview

```
bsp      - Board specific configuration
hal      - Hardware abstraction layer
bus      - Communication buses (I2C, SPI, UART)
drivers  - External device drivers
services - System level logic and managers
system   - Startup, lifecycle and global system logic
utils    - Hardware independent helpers
app      - Product specific application logic
main     - Application entry point
```

Each folder contains a small README.md describing its responsibility and boundaries.

---

## Architectural Rules

These rules are simple by design, but powerful in practice.

- Dependencies flow upward only
- Application logic never touches hardware directly
- Drivers are reusable and board agnostic
- Board changes are isolated to the BSP layer
- Each layer has a single, clear responsibility

Following these rules prevents firmware from turning into tightly coupled, unmaintainable code as projects grow.

---

## Layer Philosophy

### BSP (Board Support Package)
Contains everything that is specific to the PCB and hardware design.  
If the board changes, this should be the only layer that needs modification.

### HAL (Hardware Abstraction Layer)
Abstracts MCU peripherals and low level access.  
Defines how the system talks to hardware, not why.

### Bus
Shared communication layers such as I2C, SPI and UART.  
Drivers communicate through this layer instead of directly touching the MCU.

### Drivers
Drivers for external ICs and peripherals.  
Reusable across projects and independent of application logic.

### Services
System level logic and coordination.  
Services orchestrate drivers and expose clean interfaces upward.

### System
Startup, initialisation, reset handling and global system state.  
This layer ties everything together cleanly.

### Utils
Pure helper utilities such as logging, timing and math.  
No hardware knowledge belongs here.

### App
Product specific behaviour.  
Tasks, state machines and application logic live here.

---

## Usage Instructions

1. Clone the repository
```
git clone https://github.com/MA-EMBED/ma-embedded-template-free.git
```

2. Use the structure as the base for your next firmware project

3. Begin adding:
- Board specific configuration in bsp
- HAL implementations
- Device drivers
- Services and application logic

The structure is intentionally flexible and adapts to different MCUs and toolchains.

---

## Philosophy Behind This Template

### Modularity
Each layer has a clear purpose.  
This makes individual modules easier to understand, test, and reuse.

### Scalability
The structure works for small projects and continues to make sense as systems grow more complex.

### Separation of Concerns
Hardware, drivers, logic and application behaviour remain isolated from each other.  
This reduces coupling and long term technical debt.

### Professional Workflow
This layout mirrors how production grade firmware is structured in industry.  
It is designed to support real products, not just demos.

---

## Free Edition vs Extended Edition

This Free Edition focuses on structure, rules, and architectural clarity.

An extended edition builds on this foundation with:
- Fully implemented HAL modules
- Ready to use bus layers
- Real device drivers
- Example services and tasks
- Board initialisation flows
- Practical, production oriented examples

The goal is simple:  
Start free, learn the structure, and scale when you are ready.

---

### Closing Note

Good firmware is not just about writing code.  
It is about setting boundaries early and respecting them as the system grows.

This template exists to help you do exactly that.
