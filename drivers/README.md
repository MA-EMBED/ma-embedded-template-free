## Drivers

This layer contains drivers for external ICs and peripherals.

### Belongs here
- Sensors
- Power ICs
- IO expanders
- Communication ICs

### Does NOT belong here
- Pin numbers
- Application logic
- ESP-IDF calls or other MCU manufacturer library calls (Microchip, NXP, Nordic, ST)

Rule:
Drivers must be reusable and hardware-agnostic.
