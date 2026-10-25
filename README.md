# MyCNC – Open-Source DIY CNC Router with 4th Axis and 4th/5th-Axis AC/BC Rotary Table

![MyCNC V4 with the AC rotary table on the machine bed (CAD view)](images/cnc-router/v4-overview-cad-with-ac-table.jpg)

**MyCNC** is an open-source hardware **DIY CNC router**: a self-designed and self-built 3-axis CNC router with an aluminium frame (aluminium profiles and plates), 3D-printed parts and linear guides, developed through versions V1–V4 since 2016. Around it are three extensions that turn it into a multi-axis machine: a **4th axis for CNC routers** (rotary and indexing axis with an 80 mm chuck), a **4th/5th-axis AC/BC rotary table** as a 5-axis upgrade for 4- and 5-axis machining, and a self-built **6-axis CNC controller** (UC300ETH + UB1) running UCCNC or Mach4. Earlier versions ran GRBL on a Raspberry Pi.

Over several versions the machine became steadily more rigid, more precise and more capable: from the first version, suitable for engraving, to the current V4, which mills aluminium without problems.

This repository collects the documentation, bills of materials, the electronics schematic and links to the CAD models, so that anyone interested can **rebuild the machine or simply use it as a source of ideas**.

> **⚠️ Safety and liability – please read first.**
> This is a hobby project, published as-is for inspiration and personal experiments. It is **not** a tested or certified product. Building and operating a CNC machine involves mains voltage, rotating spindles and strong motors that can cause serious injury, fire or damage. **You build and use anything from this repository entirely at your own risk.** There is no warranty and no liability. See [DISCLAIMER.md](DISCLAIMER.md).

## 📋 Full structured BOM with costs (V4)

Every assembly and every single part of the current V4, exported directly from the CAD model, with costs (total as stated in the BOM: **$4,238.30**).

- **[Interactive view on masdrive](https://masdrive.ch/myprojects/projects/cnc-platform/#stueckliste)** – expand and collapse the structure, with thumbnails
- **[Markdown view in this repo](bom/v4-structured-bom.md)** – collapsible structure, readable directly on GitHub
- **[Excel download](bom/v4-structured-bom-with-costs.xlsx)** – grouped rows with costs

## Project overview

| Part | What it is | Docs | CAD (GrabCAD) | Source page |
|---|---|---|---|---|
| **3-axis CNC router** (main project) | Self-built router, versions V1, V3 and V4 (current) | [docs/01-cnc-router](docs/01-cnc-router/README.md) | [MyCNC V1](https://grabcad.com/library/mycnc-v1-1) · [My CNC V3](https://grabcad.com/library/my-cnc-v3-1) · [MyCNC V4](https://grabcad.com/library/mycnc-v4-3-axis-cnc-platform-router-1) | [masdrive](https://masdrive.ch/myprojects/projects/cnc-platform/) |
| **6-axis CNC controller** | UC300ETH + UB1 based controller for up to 6 stepper motors | [docs/02-6-axis-controller](docs/02-6-axis-controller/README.md) | [Generic 6 Axis CNC / Robotics Controller](https://grabcad.com/library/generic-6-axis-cnc-robotics-controller-1) | [masdrive](https://masdrive.ch/myprojects/projects/6-axis-controller/) |
| **4th axis for CNC router** | Rotary/indexing axis with 80 mm 4-jaw chuck, NEMA 23 | [docs/03-4th-axis](docs/03-4th-axis/README.md) | [4th Axis for CNC Router](https://grabcad.com/library/4th-axis-for-cnc-router-1) | [masdrive](https://masdrive.ch/myprojects/projects/4th-cnc-axis/) |
| **4th/5th-axis AC/BC rotary table** | Table with two rotary axes for 4- and 5-axis machining | [docs/04-ac-bc-rotary-table](docs/04-ac-bc-rotary-table/README.md) | [Table for 5 Axis CNC with 2 Rotary Axis](https://grabcad.com/library/table-for-5-axis-cnc-with-2-rotary-axis-1) | [masdrive](https://masdrive.ch/myprojects/projects/ac-table/) |

**CAD files:** the complete V4 model is available as a neutral [STEP export](cad/step/MyCNC_V4.step) in this repository and as native SolidWorks and Fusion 360 downloads on the [v4.0 release](https://github.com/mallemann/mycnc/releases/tag/v4.0); individual models are on GrabCAD. See [cad/README.md](cad/README.md) for downloads, how to open them, and the complete GrabCAD list including the Z-axis variants 1–3 for V4 (variant 3 is the newest).

## Key specifications (V4)

| | |
|---|---|
| Working area | 550 × 700 × 80 mm |
| Repeatability | 0.01 mm |
| Backlash | 0.01 mm |
| Frame | Aluminium profiles, aluminium plates |
| Guides / drive | Linear guides, 16 mm ball screws, NEMA 23 stepper motors, DQ542MA drivers |
| Control | UC300ETH / UB1 6-axis controller, UCCNC / Mach4 on a Windows PC |

Values as published on the [masdrive project page](https://masdrive.ch/myprojects/projects/cnc-platform/). Details per version in [docs/01-cnc-router](docs/01-cnc-router/README.md).

### Current control setup

The machine currently runs on the self-built **6-axis controller (UC300ETH + UB1)** with **UCCNC** (or Mach4) on Windows, connected via Ethernet. Versions V1–V3 used a Raspberry Pi with a Protoneer CNC HAT, GRBL and bCNC.

## Repository layout

| Folder | Content |
|---|---|
| [docs/](docs/) | Documentation of the four parts, translated from the masdrive pages |
| [bom/](bom/README.md) | Bills of materials (V1, V3, V4) and purchased-parts lists (PDF, originals from masdrive) |
| [electronics/](electronics/README.md) | Schematic of the 6-axis controller (V4) and axis mapping |
| [config/](config/README.md) | Machine parameters from my build (steps/mm etc.) |
| [cad/](cad/README.md) | CAD files: SolidWorks/Fusion 360 downloads, STEP export, GrabCAD links |
| [images/](images/) | Photos and renderings, organised per part |
| [CHANGELOG.md](CHANGELOG.md) | Version history of the machine |

## Related projects

- **Mas5ACAM** – 5-axis CAM for X, Y, Z, A, C, developed for the AC table: [GitHub](https://github.com/mallemann/Mas5ACAM) · [masdrive](https://masdrive.ch/myprojects/projects/mas5acam/)
- **MasViewer** – 3D G-code simulation to check tool paths before they run on the machine: [GitHub](https://github.com/mallemann/MasViewer) · [masdrive](https://masdrive.ch/myprojects/projects/gcode-viewer/)

## More information

- Project website (German): [myDIYprojects on masdrive.ch](https://masdrive.ch/myprojects/) – including videos of the machine in action
- All my CAD models: [GrabCAD profile](https://grabcad.com/martin.allemann-1/models)

## Licensing

| What | License |
|---|---|
| Hardware design (mechanical design, schematic, BOMs) | [CERN-OHL-S-2.0](LICENSE) – CERN Open Hardware Licence Version 2, Strongly Reciprocal |
| Documentation, text and images | [CC BY-SA 4.0](LICENSE-docs) – Creative Commons Attribution-ShareAlike 4.0 International |

In short: you may build, modify and share the design, also in modified form, as long as you credit the original and publish your changes under the same terms. Both licenses exclude any warranty and liability. The native CAD files are distributed as release downloads and via GrabCAD (GrabCAD terms apply there). Third-party vendor models included in the CAD files remain the property of their owners and are not covered by these licenses – see [cad/README.md](cad/README.md#third-party-parts).

## Author

Martin Allemann, Switzerland – [masdrive.ch/myprojects](https://masdrive.ch/myprojects/) · [GrabCAD](https://grabcad.com/martin.allemann-1/models) · [GitHub](https://github.com/mallemann)
