# DIY 3-Axis CNC Router (main project)

*Self-built aluminium DIY CNC router – from the first version (2016) to the stable V4.*

Source: [3-Achsen-CNC-Fräse im Eigenbau (masdrive.ch, German)](https://masdrive.ch/myprojects/projects/cnc-platform/) · CAD: [MyCNC V1](https://grabcad.com/library/mycnc-v1-1) · [My CNC V3](https://grabcad.com/library/my-cnc-v3-1) · [MyCNC V4, 3 Axis CNC Platform/Router](https://grabcad.com/library/mycnc-v4-3-axis-cnc-platform-router-1) · Schematic: [electronics/](../../electronics/README.md)

![MyCNC V4 with AC rotary table (CAD view)](../../images/cnc-router/v4-overview-cad-with-ac-table.jpg)

This project has been with me for years: a completely self-designed and self-built 3-axis CNC router based on aluminium profiles, 3D-printed parts and linear guides. Over several versions the machine became steadily more rigid, more precise and more capable – from the first version capable of engraving to the current V4, which mills aluminium without problems. The machine currently runs with my new [6-axis controller](../02-6-axis-controller/README.md) (UC300ETH + UB1) and UCCNC or Mach4 under Windows.

The picture above shows the CAD model of the current configuration, including the [AC rotary table](../04-ac-bc-rotary-table/README.md) on the machine bed, which adds two rotary axes and makes 4- and 5-axis machining possible.

## Technical data

The table is reproduced as published on the source page.

| Item | Value |
|---|---|
| Working area (V4) | 550 × 700 × 80 mm |
| Repeatability (V4) | 0.01 mm |
| Backlash (V4) | 0.01 mm |
| Frame material | Aluminium profiles, hardwood worktop, aluminium plates (V4) |
| Drive V1 | Toothed belts, NEMA 17 stepper motors, A4988 drivers (later DRV8825) |
| Guides from V3 | Linear guides |
| Drive from V3 | 16 mm ball screws instead of toothed belts |
| Control V1–V3 | Raspberry Pi + Protoneer CNC HAT, GRBL, bCNC |
| Control V4 | UC300ETH / UB1 6-axis controller, UCCNC / Mach4, NEMA 23 + external DQ542MA drivers |

## Version history

### V1 – First version (2016)

The first working machine, driven by toothed belts with NEMA 17 stepper motors (A4988 and DRV8825 drivers) on a Raspberry Pi CNC HAT with GRBL/bCNC. Suitable for engraving, drilling and contour milling in wood. Known weakness: stability of the toothed belts under load.

### V3 – Ball screws and more rigidity (2016)

The toothed belts were replaced by 16 mm ball screws, and the printed parts were redesigned for more rigidity. With this the machine was fully built and reached a repeatability of approx. 0.01 mm and a backlash of approx. 0.02 mm. This version was already used to drill wood and to mill POM (polyacetal).

### V4 – New control and larger working area (ongoing)

Much more stable and rigid construction with a working area of 550 × 700 × 80 mm – milling aluminium is no problem. The original Raspberry Pi electronics were replaced by a [6-axis controller](../02-6-axis-controller/README.md) based on UC300ETH and UB1, running UCCNC or Mach4 on a Windows PC. The Z-axis was reworked several times (most recently with a ball screw ⌀ 12 mm, pitch 2.5 mm, and 15 mm profile rail guides) and gives a much better repeatability.

## Complete bill of materials of the V4

This is the complete structured bill of materials of the latest version V4 – every assembly and every single part of the machine, exported directly from the CAD model, with all costs. The structure levels can be expanded and collapsed: a click on an assembly shows its sub-assemblies and parts; the cost of an assembly is always the sum of its parts. The total price of the machine is at the very bottom.

The same BOM is also available as an Excel file with grouped rows to expand and collapse, and as PDF.

- **[Interactive view on masdrive](https://masdrive.ch/myprojects/projects/cnc-platform/#stueckliste)**
- [Markdown view in this repo](../../bom/v4-structured-bom.md)
- [Structured BOM V4 as Excel (with costs and grouping)](../../bom/v4-structured-bom-with-costs.xlsx)
- [Structured BOM V4 (PDF, multi-level)](../../bom/v4-bom-multi-level.pdf)
- [Assembly overview V4 (PDF, single-level)](../../bom/v4-bom-single-level.pdf)
- [Quantity BOM V4 (PDF)](../../bom/v4-bom-quantities.pdf)

## The real thing

Repeat precision: 0.01 mm · Reverse backlash: 0.01 mm

The complete V4 machine, followed by details of its Z-axis:

![V4 – complete machine](../../images/cnc-router/v4-detail-2.jpg)

*V4 – complete machine*

| | | |
|---|---|---|
| ![Z-axis assembly next to its CAD model on the monitor](../../images/cnc-router/v4-with-6-axis-controller.jpg) | ![Z-axis mounted on the gantry, with spindle holder](../../images/cnc-router/v4-current-build.jpg) | ![CAD rendering of the Z-axis with spindle](../../images/cnc-router/v4-cad-rendering.jpg) |
| Z-axis assembly next to its CAD model | Z-axis mounted on the gantry, with spindle holder | CAD rendering of the Z-axis with spindle |

## Assembly

The basic construction is similar for all versions:

1. Linear guides and ball screws (V4)
2. Mount the aluminium profiles on the base plate; put on the worktop made of 12 mm hardwood (V1–V3) or aluminium (V4)
3. Mount the axes – order: Y-axis, X-axis, Z-axis
4. Wire the stepper motors and limit switches (0.5 mm² stranded wire)
5. Configure electronics and software (see [Control and software](#control-and-software))

Bills of materials and wiring (originals from masdrive, German or partly German, see [bom/](../../bom/README.md)):

- [BOM structure (V1)](../../bom/v1-bom-structure.pdf)
- [BOM quantities (V1)](../../bom/v1-bom-quantities.pdf)
- [Cost of purchased parts (V1)](../../bom/v1-cost-purchased-parts.pdf)
- [BOM quantities (V3)](../../bom/v3-bom-quantities.pdf)
- [BOM structure (V3)](../../bom/v3-bom-structure.pdf)
- [Purchased parts V4 (Raspberry variant)](../../bom/v4-purchased-parts-raspberry.pdf)
- [Purchased parts V4 (UC300ETH/UB1 variant)](../../bom/v4-purchased-parts-uc300eth-ub1.pdf)
- Complete structured BOM V4 with costs: see [Complete bill of materials of the V4](#complete-bill-of-materials-of-the-v4)
- [Electronics schematic V4](../../electronics/v4-schematic-6-axis-controller.pdf)

## Control and software

**V1/V3 (Raspberry Pi):** Stepper drivers (A4988, DRV8825) on the Protoneer CNC HAT, 16 microsteps, Y-axis cloned (wired in opposite direction). Control via GRBL and bCNC. G-code was generated with HSMXpress (SolidWorks 2013).

- [Configuring GRBL](https://github.com/gnea/grbl/wiki)
- [bCNC wiki](https://github.com/vlachoudis/bCNC/wiki)
- [Converting a PC power supply for use as power source (RepRap wiki, German)](https://reprap.org/wiki/PC-Netzteil)

**V4 (UC300ETH/UB1):** NEMA 23 stepper motors with external DQ542MA drivers (replacing the internal DRV8825 drivers), controlled by UCCNC (or Mach3/4) on a Windows PC, connected via Ethernet.

- [UCCNC motion controller software (CNCdrive)](https://www.cncdrive.com/)
- [UC300ETH-UB1 interface card (CNCRoom)](https://cncroom.com/en/)

The parameters are collected in [config/](../../config/README.md).

## 3D models

**CAD files:** the complete V4 model as SolidWorks assembly and Fusion 360 archive is available as a download on the [v4.0 release](https://github.com/mallemann/mycnc/releases/tag/v4.0). A neutral STEP export is in the repository: [cad/step/MyCNC_V4.step](../../cad/step/MyCNC_V4.step). How to open the files and the third-party parts notice are described in [cad/README.md](../../cad/README.md).

Individual models are available on GrabCAD:

- [MyCNC V1](https://grabcad.com/library/mycnc-v1-1)
- [My CNC V3](https://grabcad.com/library/my-cnc-v3-1)
- [MyCNC V4, 3 Axis CNC Platform/Router](https://grabcad.com/library/mycnc-v4-3-axis-cnc-platform-router-1)
- Z-axis variant 1 (V4): [New Z Axis CNC](https://grabcad.com/library/new-z-axis-cnc-1)
- Z-axis variant 2 (V4): [New CNC Z Axis](https://grabcad.com/library/new-cnc-z-axis-1)
- Z-axis variant 3 (V4, newest): [Z Axis CNC Router](https://grabcad.com/library/z-axis-cnc-router-1)

## Videos

Videos of the machine in action – build stages of the V4, the new Z-axis, test runs, V3 in operation, a dial-gauge accuracy test and cutting wood, aluminium and brass – are on the [masdrive project page](https://masdrive.ch/myprojects/projects/cnc-platform/).

## Gallery

### V4

| | | |
|---|---|---|
| ![V4 detail 1](../../images/cnc-router/v4-detail-1.jpg) | ![V4 detail 2](../../images/cnc-router/v4-detail-2.jpg) | ![V4 detail 3](../../images/cnc-router/v4-detail-3.jpg) |
| ![V4 detail 5](../../images/cnc-router/v4-detail-5.jpg) | ![V4 detail 6](../../images/cnc-router/v4-detail-6.jpg) | |

### V3

| | | |
|---|---|---|
| ![Wiring of external drivers](../../images/cnc-router/external-driver-wiring.png) | ![External driver sockets V4](../../images/cnc-router/external-driver-socket-v4.png) | ![V3 complete](../../images/cnc-router/v3-complete-1.jpg) |
| Wiring of external drivers | External driver sockets V4 | V3 complete |
| ![V3 complete](../../images/cnc-router/v3-complete-2.jpg) | ![bCNC control client](../../images/cnc-router/v3-bcnc-control-software.jpg) | ![Z-axis detail](../../images/cnc-router/v3-z-axis-detail.jpg) |
| V3 complete | bCNC control client | Z-axis detail |
| ![Y-axis](../../images/cnc-router/v3-y-axis.jpg) | | |
| Y-axis | | |

### V1

![Parts overview](../../images/cnc-router/v1-parts-overview.png)

| | | | |
|---|---|---|---|
| ![Build detail 1](../../images/cnc-router/v1-build-detail-1.jpg) | ![Build detail 2](../../images/cnc-router/v1-build-detail-2.jpg) | ![Build detail 3](../../images/cnc-router/v1-build-detail-3.jpg) | ![Build detail 4](../../images/cnc-router/v1-build-detail-4.jpg) |

## Rebuilding the Z-axis

Over several versions the Z-axis was the weak point of the machine. It carries the spindle and takes up the forces that push the tool sideways during milling – any compliance here shows up directly on the workpiece.

The rebuild therefore uses solid aluminium instead of bolted profiles. The pictures show the manufacturing of the individual parts: spindle mount, guide plates and bearing blocks, all milled from solid. With such parts the effort lies less in the milling itself than in the alignment – a mount whose bore is a tenth off will transfer this error to every later workpiece.

| | | |
|---|---|---|
| ![Spindle mount](../../images/cnc-router/z-axis-rebuild-1.jpg) | ![Part after machining](../../images/cnc-router/z-axis-rebuild-2.jpg) | ![Guide plate](../../images/cnc-router/z-axis-rebuild-3.jpg) |
| Milled spindle mount of the new Z-axis, solid aluminium | Part of the new Z-axis after machining on the CNC router | Aluminium guide plate of the new Z-axis |
| ![Bearing block](../../images/cnc-router/z-axis-rebuild-4.jpg) | ![Parts before assembly](../../images/cnc-router/z-axis-rebuild-5.jpg) | ![Spindle mount detail](../../images/cnc-router/z-axis-rebuild-6.jpg) |
| Bearing block of the new Z-axis, raw after milling | Parts of the new Z-axis before assembly | Detail of the spindle mount with milled fit |
| ![Partly assembled](../../images/cnc-router/z-axis-rebuild-7.jpg) | ![Fully assembled](../../images/cnc-router/z-axis-rebuild-8.jpg) | |
| New Z-axis partly assembled with guides | Fully assembled new Z-axis | |

## Minimum quantity lubrication (MQL)

For milling aluminium, minimum quantity lubrication is indispensable on this machine. Without a lubricating film, aluminium sticks to the cutting edge, forms a built-up edge and the surface becomes rough – until the cutter breaks.

The system sits under the machine table: pressure regulator with gauge, solenoid valve, reservoir and a dedicated small compressor. From there the blue air line runs up to the nozzle at the spindle – the picture below shows the whole setup. Because it is switched by a solenoid valve, the lubrication can be switched on and off from the program and does not run during rapid moves.

More details, with cutting data and the reasoning behind them, are on the masdrive know-how page [Zerspanen (German)](https://masdrive.ch/myprojects/knowhow/zerspanen.php).

![MQL under the machine table: pressure regulator with gauge, solenoid valve, reservoir and small compressor, air line to the spindle](../../images/cnc-router/v4-mql-system-under-table.jpg)

## Materials

Short videos on the [masdrive page](https://masdrive.ch/myprojects/projects/cnc-platform/) show the machine working on different materials. The difference lies less in the motion than in the behaviour of the material: wood produces chips and dust and forgives high feed rates. Aluminium tends to stick to the cutting edge and needs sharp tools and a brisk feed so that the chip is carried away. Brass, on the other hand, almost machines by itself, but breaks into short chips and prefers a pulling rather than a pushing cutting edge.

---

*Translated from the German original on [masdrive.ch](https://masdrive.ch/myprojects/projects/cnc-platform/). Build at your own risk – see [DISCLAIMER](../../DISCLAIMER.md).*
