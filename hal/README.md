## HAL (Hardware Abstraction Layer)

This layer abstracts MCU peripherals and low-level hardware access.

### Belongs here
- GPIO abstraction
- ADC abstraction
- PWM abstraction
- Timers

### Does NOT belong here
- Device drivers
- Pin definitions
- Application logic

Rule:
HAL defines how to talk to the MCU, not why.
