# Machine configuration

> **These values are from my build. Adapt them to yours.** Steps per mm depend on your motors, microstepping, screw pitch or belt/pulley ratio. Wrong values can crash the machine. See [DISCLAIMER.md](../DISCLAIMER.md).

All values below are taken from the [masdrive project pages](https://masdrive.ch/myprojects/projects/cnc-platform/) as published. Nothing has been recalculated.

## V1 / V3 – Raspberry Pi + Protoneer CNC HAT, GRBL, bCNC

| Parameter | Value (as published) |
|---|---|
| Drivers | A4988 on the Protoneer CNC HAT |
| Microstepping | 16 microsteps |
| Y-axis | Cloned (wired in opposite direction) |
| Steps/mm X/Y | 307–3072 steps/mm (depending on version) |
| Steps/mm Z | 1066.667 steps/mm |
| Control software | GRBL, bCNC |
| CAM used | HSMXpress (SolidWorks 2013), EstlCAM |

References: [GRBL wiki](https://github.com/gnea/grbl/wiki) · [bCNC wiki](https://github.com/vlachoudis/bCNC/wiki)

## V4 – UC300ETH / UB1, UCCNC (or Mach3/4)

| Parameter | Value (as published) |
|---|---|
| Controller | UC300ETH on UB1 mainboard, connected via Ethernet |
| Axes | X, Y, Y′, Z, A, C (6 channels, max. 4.2 A each) |
| Motors / drivers | NEMA 23, external DQ542MA drivers |
| Z-axis (latest) | Ball screw ⌀ 12 mm, pitch 2.5 mm, 15 mm profile rail guides |
| Software | UCCNC (or Mach3/4) on a Windows PC |

Steps per mm for V4 are not published yet.

## Rotary axes (4th axis, AC/BC table)

No numeric values are published. Set them for your build:

- **Steps per degree** – from motor steps, microstep setting and drive reduction.
- **Backlash** – measure and compensate.
- **Speed and acceleration** – rotary axes have a much higher inertia than linear axes; values that are too high cause lost steps.

## Profiles (placeholders)

| Folder | Planned content |
|---|---|
| [uccnc/](uccnc/README.md) | UCCNC profile of the V4 (to be added) |
| [grbl/](grbl/README.md) | GRBL settings of V1–V3 (to be added) |
