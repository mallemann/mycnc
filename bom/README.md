# Bills of materials

## 📋 Full structured BOM with costs (V4)

The complete structured BOM of the current V4 – every assembly and every single part, exported directly from the CAD model, with all costs. The cost of an assembly is the sum of its parts; the total of the machine is at the bottom.

- **[Interactive view on masdrive](https://masdrive.ch/myprojects/projects/cnc-platform/#stueckliste)** – the nicest way to browse
- **[Markdown view in this repo](v4-structured-bom.md)** – collapsible, generated from the Excel file
- **[Excel download](v4-structured-bom-with-costs.xlsx)** – grouped rows to expand and collapse (original: [cnc-v4-stueckliste-mehrstufig.xlsx](https://masdrive.ch/myprojects/assets/media/2026/10/cnc-v4-stueckliste-mehrstufig.xlsx))

## All BOM files

The PDFs are the **original files** (German; the V4 BOMs have English column headers and partly German part names) from [masdrive.ch](https://masdrive.ch/myprojects/projects/cnc-platform/), renamed for clarity. Prices are historical (CHF / EUR / USD as stated in the files) and only meant as an orientation.

| File | Version | Content | Original on masdrive |
|---|---|---|---|
| [v1-bom-structure.pdf](v1-bom-structure.pdf) | V1 | Structured BOM (assemblies, parts, buy/print) | [BOM-Structure.pdf](https://masdrive.ch/myprojects/assets/media/2016/02/BOM-Structure.pdf) |
| [v1-bom-quantities.pdf](v1-bom-quantities.pdf) | V1 | Total quantities | [BOM-Quantities.pdf](https://masdrive.ch/myprojects/assets/media/2016/02/BOM-Quantities.pdf) |
| [v1-cost-purchased-parts.pdf](v1-cost-purchased-parts.pdf) | V1 | Cost of non-printed (purchased) parts | [Costs-of-Non-Printed-Parts.pdf](https://masdrive.ch/myprojects/assets/media/2016/02/Costs-of-Non-Printed-Parts.pdf) |
| [v3-bom-quantities.pdf](v3-bom-quantities.pdf) | V3 | Quantity BOM | [Mbom.pdf](https://masdrive.ch/myprojects/assets/media/2016/03/Mbom.pdf) |
| [v3-bom-structure.pdf](v3-bom-structure.pdf) | V3 | Structured BOM | [Sbom.pdf](https://masdrive.ch/myprojects/assets/media/2016/03/Sbom.pdf) |
| [v4-purchased-parts-raspberry.pdf](v4-purchased-parts-raspberry.pdf) | V4 | Purchased parts, Raspberry Pi variant | [Kaufteile.pdf (2017)](https://masdrive.ch/myprojects/assets/media/2017/04/Kaufteile.pdf) |
| [v4-purchased-parts-uc300eth-ub1.pdf](v4-purchased-parts-uc300eth-ub1.pdf) | V4 | Purchased parts, UC300ETH/UB1 variant (current) | [Kaufteile.pdf (2020)](https://masdrive.ch/myprojects/assets/media/2020/01/Kaufteile.pdf) |
| [v4-bom-single-level.pdf](v4-bom-single-level.pdf) | V4 | BOM, assembly overview (single-level). Original title: «Baugruppen-Übersicht V4 (PDF, einstufig)» | [cnc-v4-stueckliste-einstufig.pdf](https://masdrive.ch/myprojects/assets/media/2026/10/cnc-v4-stueckliste-einstufig.pdf) |
| [v4-bom-multi-level.pdf](v4-bom-multi-level.pdf) | V4 | BOM, structure (multi-level). Original title: «Strukturstückliste V4 (PDF, mehrstufig)» | [cnc-v4-stueckliste-mehrstufig.pdf](https://masdrive.ch/myprojects/assets/media/2026/10/cnc-v4-stueckliste-mehrstufig.pdf) |
| [v4-bom-quantities.pdf](v4-bom-quantities.pdf) | V4 | Quantity BOM. Original title: «Mengen-Stückliste V4 (PDF)» | [cnc-v4-mengenstueckliste.pdf](https://masdrive.ch/myprojects/assets/media/2026/10/cnc-v4-mengenstueckliste.pdf) |
| [v4-structured-bom-with-costs.xlsx](v4-structured-bom-with-costs.xlsx) | V4 | Structured BOM with costs and grouping (Excel). Original title: «Strukturstückliste V4 als Excel (mit Kosten und Gruppierung)». Markdown view: [v4-structured-bom.md](v4-structured-bom.md) | [cnc-v4-stueckliste-mehrstufig.xlsx](https://masdrive.ch/myprojects/assets/media/2026/10/cnc-v4-stueckliste-mehrstufig.xlsx) |

The electronics schematic is in [electronics/](../electronics/README.md). The CAD models (geometry of all printed and machined parts) are on GrabCAD – see [cad/](../cad/README.md).

## Common German terms

| German | English |
|---|---|
| Stückliste | Bill of materials |
| Benennung / Beschreibung / Menge | Name / Description / Quantity |
| Kaufteile | Purchased parts |
| Lieferant / Einzelpreis | Supplier / Unit price |
| Welle | Shaft |
| Linearführung / Linearwagen | Linear guide rail / Carriage |
| Kugelspindel / Gewindespindel | Ball screw |
| Trapezspindel | Trapezoidal lead screw |
| Festlager / Loslager | Fixed bearing / Floating bearing |
| Schrägkugellager | Angular-contact ball bearing |
| Wellenkupplung | Shaft coupling |
| Nutsteine | T-slot nuts |
| Zahnriemen / Riemenrad | Toothed belt / Belt pulley |
| Endschalter | Limit switch |
| Grundplatte / Bodenplatte | Base plate / Work plate |
| Schrittmotor | Stepper motor |
