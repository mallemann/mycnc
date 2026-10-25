# MyCNC v4.0 – first public release

**MyCNC** is an open-source hardware DIY CNC router with a 4th axis, a 4th/5th-axis AC/BC rotary table for 5-axis machining and a self-built 6-axis CNC controller. This is the first public release of the repository, documenting the current machine version **V4**.

## Highlights

- **V4 DIY CNC router:** rigid aluminium frame (profiles and plates), 16 mm ball screws, linear guides, NEMA 23 stepper motors with DQ542MA drivers. Working area 550 × 700 × 80 mm, repeatability and backlash 0.01 mm. Mills aluminium. → [docs/01-cnc-router](../docs/01-cnc-router/README.md)
- **Bills of materials:** BOMs for V1, V3 and V4 as PDF, plus the new **V4 structured BOM with costs** (237 items, total as stated in the BOM: **$4,238.30**):
  - [Markdown view](../bom/v4-structured-bom.md) (collapsible, readable on GitHub)
  - [Excel download](../bom/v4-structured-bom-with-costs.xlsx)
  - [Interactive view on masdrive](https://masdrive.ch/myprojects/projects/cnc-platform/#stueckliste)
- **Extensions:**
  - [6-axis CNC controller](../docs/02-6-axis-controller/README.md) (UC300ETH + UB1, UCCNC or Mach4), with the [schematic](../electronics/README.md)
  - [4th axis for CNC routers](../docs/03-4th-axis/README.md): rotary and indexing axis with an 80 mm 4-jaw chuck
  - [4th/5th-axis AC/BC rotary table](../docs/04-ac-bc-rotary-table/README.md): two rotary axes for 4- and 5-axis machining
- **CAD:** all models on GrabCAD, including the Z-axis variants 1–3 for V4. See [cad/README.md](../cad/README.md).
- **Config:** machine parameters from my build, see [config/](../config/README.md) ([GRBL](../config/grbl/README.md) for V1/V3, [UCCNC](../config/uccnc/README.md) for V4).

## Links

- Repository: https://github.com/mallemann/mycnc
- Project website (German, with videos): https://masdrive.ch/myprojects/
- CAD models: https://grabcad.com/martin.allemann-1/models
- Related: [Mas5ACAM](https://github.com/mallemann/Mas5ACAM) (5-axis CAM for the AC table) · [MasViewer](https://github.com/mallemann/MasViewer) (3D G-code simulation)

## License

- Hardware design (mechanical design, schematic, BOMs): [CERN-OHL-S-2.0](../LICENSE)
- Documentation, text and images: [CC BY-SA 4.0](../LICENSE-docs)

## Safety notice

This is a hobby project, published as-is. It is **not** a tested or certified product. Building and operating a CNC machine involves mains voltage, rotating spindles and strong motors that can cause serious injury, fire or damage. **You build and use anything from this repository entirely at your own risk**, without warranty or liability. Please read [DISCLAIMER.md](../DISCLAIMER.md) first.
