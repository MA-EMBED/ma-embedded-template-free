## Bus Layer

This layer provides shared communication interfaces.

### Belongs here
- I2C bus wrappers
- SPI bus wrappers
- UART bus wrappers

### Does NOT belong here
- Device-specific logic
- Application state

Rule:
Drivers must communicate through this layer.
