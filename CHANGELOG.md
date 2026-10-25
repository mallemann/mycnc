# Changelog

Version history of the machine, based on the [masdrive project pages](https://masdrive.ch/myprojects/).

## Repository

- **2026-10-25** – V4 structured BOM with costs added (Excel + Markdown view), linked prominently in the README.
- **2026-10-25** – V4 bills of materials replaced with the revised versions from masdrive (revised layout).
- **2026-10-25** – V4 bills of materials added (single-level, multi-level, quantities).
- **2026-10-25** – Z-axis variants 1–3 and specs synced with masdrive.
- **2026-10-25** – GrabCAD links updated to the authoritative model list; specs synced with the corrected masdrive pages.
- **2026-10-25** – Initial import of the documentation, BOMs, schematic, images and CAD links into this repository.

## 3-axis CNC router

### V4 – New control and larger working area (ongoing)

- Much more stable and rigid construction, working area 550 × 700 × 80 mm; milling aluminium possible.
- Aluminium plates in the frame; aluminium worktop instead of hardwood.
- Raspberry Pi electronics replaced by the self-built 6-axis controller (UC300ETH + UB1) with UCCNC or Mach4 on a Windows PC, connected via Ethernet.
- NEMA 23 stepper motors with external DQ542MA drivers (replacing the internal DRV8825 drivers).
- Z-axis reworked several times (Z-axis variants 1–3 for V4 on GrabCAD, variant 3 is the newest); latest version with ball screw ⌀ 12 mm, pitch 2.5 mm, and 15 mm profile rail guides. New Z-axis made from solid aluminium.
- Minimum quantity lubrication with solenoid valve, switchable from the program.
- Repeatability 0.01 mm, backlash 0.01 mm.

### V3 – Ball screws and more rigidity (2016)

- Toothed belts replaced by 16 mm ball screws; linear guides.
- Printed parts redesigned for more rigidity.
- Repeatability approx. 0.01 mm, backlash approx. 0.02 mm.
- Used for drilling wood and milling POM.

### V1 – First version (2016)

- Toothed belts, NEMA 17 stepper motors, A4988 drivers (later DRV8825) on a Raspberry Pi CNC HAT with GRBL/bCNC.
- Suitable for engraving, drilling and contour milling in wood.
- Known weakness: stability of the toothed belts under load.

## Extensions

- **6-axis CNC controller** – UC300ETH + UB1, up to 6 stepper motors (4.2 A each); built in several stages up to the current cabinet version V3; in use for a long time.
- **4th CNC axis** – NEMA 23, 80 mm 4-jaw chuck, usable as A- or B-axis.
- **AC/BC rotary table** – two rotary axes for 4- and 5-axis machining; prototype in use.
