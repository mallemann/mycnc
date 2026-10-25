# CAD files

The CAD models are the main reference for dimensions and assembly. They are available in three forms:

| Form | What it is | Where |
|---|---|---|
| **SolidWorks (native)** | Complete V4 model: top assembly `MyCNC_V4-REV-Isel.SLDASM`, 44 assemblies and 135 parts (179 files) | [MyCNC_V4_SolidWorks.zip](https://github.com/mallemann/mycnc/releases/download/v4.0/MyCNC_V4_SolidWorks.zip) – GitHub release v4.0 |
| **Fusion 360 (native)** | Fusion 360 archive of the same V4 model | [MyCNC_V4_Fusion360.f3z](https://github.com/mallemann/mycnc/releases/download/v4.0/MyCNC_V4_Fusion360.f3z) – GitHub release v4.0 |
| **STEP (neutral)** | Neutral export for any CAD program | `cad/step/MyCNC_V4.step` – *coming soon* |
| **GrabCAD** | Individual models: V1, V3, V4, Z-axis variants and the extensions | [GrabCAD profile](https://grabcad.com/martin.allemann-1/models), see the list below |

The native files are large binary files, so they are published as downloads on the [v4.0 release](https://github.com/mallemann/mycnc/releases/tag/v4.0) and are not stored in the git history.

## SolidWorks

1. Download [MyCNC_V4_SolidWorks.zip](https://github.com/mallemann/mycnc/releases/download/v4.0/MyCNC_V4_SolidWorks.zip) (about 170 MB).
2. Unzip it. All files are in one flat folder, `MyCNC_V4_SolidWorks/`. Keep them together so that SolidWorks finds the references.
3. Open the top assembly **`MyCNC_V4-REV-Isel.SLDASM`**.

Besides the router itself (base frame, X, Y1/Y2 and Z axes), the folder also contains the assemblies of the AC/BC rotary table (`ABC-Table-BG.SLDASM`) and of the 6-axis controller (`Generic1 v77.SLDASM`).

## Fusion 360

1. Download [MyCNC_V4_Fusion360.f3z](https://github.com/mallemann/mycnc/releases/download/v4.0/MyCNC_V4_Fusion360.f3z) (about 35 MB).
2. In Fusion 360, open the Data Panel and use **Upload** (or **File → Open → Open from my computer…**) to import the `.f3z` archive into a project.
3. Open the uploaded design `MyCNC_V4-REV-Isel`.

## STEP export (coming soon)

> **Not yet available.** A neutral STEP export of the complete V4 will be added to this repository at `cad/step/MyCNC_V4.step`. Until then, please use the SolidWorks or Fusion 360 downloads above.

STEP files can be opened in practically every CAD program (FreeCAD, Fusion 360, Onshape, SolidWorks, Inventor and others). They contain geometry only, without the feature history.

## Third-party parts

Some purchased components in the model – for example stepper motors, ball screws, bearings, profile rail guides, couplings, power supplies, controller boards, connectors and standard fasteners – are vendor models or models downloaded from other sources. They are included **for completeness only**, so that the assembly is complete. They **remain the property of their respective owners** and are **not covered by the CERN-OHL-S-2.0** licence of this project. Check the terms of the respective vendor before reusing them, and get the original models from the vendor where possible.

## GrabCAD models

All my models on GrabCAD: <https://grabcad.com/martin.allemann-1/models>. The terms shown on GrabCAD apply to the files downloaded there.

### 3-axis CNC router

| Model | Description | Link |
|---|---|---|
| MyCNC V1 | First version (2016), belt-driven | <https://grabcad.com/library/mycnc-v1-1> |
| My CNC V3 | Ball screws, more rigid printed parts (2016) | <https://grabcad.com/library/my-cnc-v3-1> |
| MyCNC V4, 3 Axis CNC Platform/Router | Current machine, 550 × 700 × 80 mm | <https://grabcad.com/library/mycnc-v4-3-axis-cnc-platform-router-1> |
| New Z Axis CNC | Z-axis variant 1 (V4), oldest | <https://grabcad.com/library/new-z-axis-cnc-1> |
| New CNC Z Axis | Z-axis variant 2 (V4) | <https://grabcad.com/library/new-cnc-z-axis-1> |
| Z Axis CNC Router | Z-axis variant 3 (V4), newest: ball screw ⌀ 12 mm, pitch 2.5 mm, 15 mm profile rails | <https://grabcad.com/library/z-axis-cnc-router-1> |

Documentation: [docs/01-cnc-router](../docs/01-cnc-router/README.md)

### Extensions

| Model | Description | Link | Docs |
|---|---|---|---|
| Generic 6 Axis CNC / Robotics Controller | Enclosure of the UC300ETH/UB1 controller | <https://grabcad.com/library/generic-6-axis-cnc-robotics-controller-1> | [02-6-axis-controller](../docs/02-6-axis-controller/README.md) |
| 4th Axis for CNC Router | NEMA 23, 80 mm 4-jaw chuck | <https://grabcad.com/library/4th-axis-for-cnc-router-1> | [03-4th-axis](../docs/03-4th-axis/README.md) |
| Table for 5 Axis CNC with 2 Rotary Axis | AC/BC rotary table | <https://grabcad.com/library/table-for-5-axis-cnc-with-2-rotary-axis-1> | [04-ac-bc-rotary-table](../docs/04-ac-bc-rotary-table/README.md) |
