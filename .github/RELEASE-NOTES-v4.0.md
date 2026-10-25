# MyCNC v4.0 – first public release

**MyCNC** is an open-source hardware DIY CNC router with a 4th axis, a 4th/5th-axis AC/BC rotary table for 5-axis machining and a self-built 6-axis CNC controller. This is the first public release of the repository, documenting the current machine version **V4**.

## Highlights

- **V4 DIY CNC router:** rigid aluminium frame (profiles and plates), 16 mm ball screws, linear guides, NEMA 23 stepper motors with DQ542MA drivers. Working area 550 × 700 × 80 mm, repeatability and backlash 0.01 mm. Mills aluminium. → [docs/01-cnc-router](https://github.com/mallemann/mycnc/blob/main/docs/01-cnc-router/README.md)
- **Bills of materials:** BOMs for V1, V3 and V4 as PDF, plus the new **V4 structured BOM with costs** (237 items, total as stated in the BOM: **$4,238.30**):
  - [Markdown view](https://github.com/mallemann/mycnc/blob/main/bom/v4-structured-bom.md) (collapsible, readable on GitHub)
  - [Excel download](https://github.com/mallemann/mycnc/raw/main/bom/v4-structured-bom-with-costs.xlsx)
  - [Interactive view on masdrive](https://masdrive.ch/myprojects/projects/cnc-platform/#stueckliste)
- **Extensions:**
  - [6-axis CNC controller](https://github.com/mallemann/mycnc/blob/main/docs/02-6-axis-controller/README.md) (UC300ETH + UB1, UCCNC or Mach4), with the [schematic](https://github.com/mallemann/mycnc/blob/main/electronics/README.md)
  - [4th axis for CNC routers](https://github.com/mallemann/mycnc/blob/main/docs/03-4th-axis/README.md): rotary and indexing axis with an 80 mm 4-jaw chuck
  - [4th/5th-axis AC/BC rotary table](https://github.com/mallemann/mycnc/blob/main/docs/04-ac-bc-rotary-table/README.md): two rotary axes for 4- and 5-axis machining
- **CAD:** complete V4 model as SolidWorks and Fusion 360 downloads (see *CAD downloads* below); individual models on GrabCAD, including the Z-axis variants 1–3 for V4. See [cad/README.md](https://github.com/mallemann/mycnc/blob/main/cad/README.md).
- **Config:** machine parameters from my build, see [config/](https://github.com/mallemann/mycnc/blob/main/config/README.md) ([GRBL](https://github.com/mallemann/mycnc/blob/main/config/grbl/README.md) for V1/V3, [UCCNC](https://github.com/mallemann/mycnc/blob/main/config/uccnc/README.md) for V4).

## CAD downloads

The native CAD files of the complete V4 are attached to this release:

- [MyCNC_V4_SolidWorks.zip](https://github.com/mallemann/mycnc/releases/download/v4.0/MyCNC_V4_SolidWorks.zip) – SolidWorks, top assembly `MyCNC_V4-REV-Isel.SLDASM`, 44 assemblies and 135 parts (about 170 MB). Unzip and open the top assembly.
- [MyCNC_V4_Fusion360.f3z](https://github.com/mallemann/mycnc/releases/download/v4.0/MyCNC_V4_Fusion360.f3z) – Fusion 360 archive (about 35 MB). Upload or open it in Fusion 360.
- A neutral STEP export (`cad/step/MyCNC_V4.step`) will follow in the repository.

Some vendor models (motors, ball screws, bearings, rails, electronics and similar) are included for completeness only. They remain the property of their owners and are not covered by CERN-OHL-S-2.0. Details: [cad/README.md](https://github.com/mallemann/mycnc/blob/main/cad/README.md).

## Links

- Repository: https://github.com/mallemann/mycnc
- Project website (German, with videos): https://masdrive.ch/myprojects/
- CAD models: https://grabcad.com/martin.allemann-1/models
- Related: [Mas5ACAM](https://github.com/mallemann/Mas5ACAM) (5-axis CAM for the AC table) · [MasViewer](https://github.com/mallemann/MasViewer) (3D G-code simulation)

## License

- Hardware design (mechanical design, schematic, BOMs): [CERN-OHL-S-2.0](https://github.com/mallemann/mycnc/blob/main/LICENSE)
- Documentation, text and images: [CC BY-SA 4.0](https://github.com/mallemann/mycnc/blob/main/LICENSE-docs)

## Safety notice

This is a hobby project, published as-is. It is **not** a tested or certified product. Building and operating a CNC machine involves mains voltage, rotating spindles and strong motors that can cause serious injury, fire or damage. **You build and use anything from this repository entirely at your own risk**, without warranty or liability. Please read [DISCLAIMER.md](https://github.com/mallemann/mycnc/blob/main/DISCLAIMER.md) first.
