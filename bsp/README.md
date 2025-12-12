## BSP (Board Support Package)

This layer contains everything that is specific to the PCB and board design.

### Belongs here
- Pin mappings
- GPIO default states
- Power enable pins
- Clock configuration
- Board revisions

### Does NOT belong here
- Application logic
- Drivers
- Business logic

Rule:
If the PCB changes, this is the only layer that should need modification.
