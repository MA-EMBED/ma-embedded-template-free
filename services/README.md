Part of the Mark Agius Embedded Firmware Template
## Services

This layer contains system-level logic and coordination.

### Belongs here
- State machines
- Monitoring logic
- Managers and controllers

### Does NOT belong here
- Pin definitions
- Low-level drivers

Rule:
Services orchestrate drivers and expose clean interfaces upward.
