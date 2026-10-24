# Composite Laminate Structural Analysis (ANSYS ACP and Mechanical)

Static structural FEA of a tapered composite sandwich panel, using ANSYS Composite PrepPost (ACP) for ply-by-ply layup definition and ANSYS Mechanical for deformation analysis.

Search this file for `TODO` before publishing. Each one is a detail from your own model that a reviewer will look for.

## Setup

| Item | Value |
|---|---|
| Solver | ANSYS Mechanical (Static Structural) |
| Layup tool | ANSYS Composite PrepPost (ACP Pre) |
| Materials | Epoxy Carbon Woven (230 GPa, wet), Epoxy Carbon UD (230 GPa, wet). TODO: state which body uses Structural Steel, or remove it |
| Geometry | Tapered laminate panel (SolidModel.1), TODO: overall dimensions |
| Boundary conditions | Fixed Support x 2, applied force. TODO: which faces |
| Applied load | TODO: magnitude (N) and direction |
| Mesh | TODO: element type, element size and element count |
| Units | mm, kg, N, s, mV, mA |

## Layup (ACP)

The laminate was defined with element-wise thickness assignment across modelling plies (ModelingPly.1, .2, .4, .5) in a single Modeling Group. Thickness was set through element-wise extrusion guides referencing the full element set (All_Elements). The solid model used inside-ply drop-off and a shell-normal offset, with a maximum thickness of 1.0 mm.

| Ply | Material | Orientation | Thickness |
|---|---|---|---|
| TODO | TODO | TODO | TODO |

TODO: fill the table from your ACP model tree (ply order, material, fibre angle, thickness).

## Results

**Total deformation**

| Min | Max | Average |
|---|---|---|
| 0 mm | 4.6981e-3 mm | 1.8965e-3 mm |

Deformation is greatest at the free end and grows along the span away from the fixed supports, consistent with bending.

**Directional deformation (X)**

| Min | Max | Average |
|---|---|---|
| -1.0436e-5 mm | 1.0436e-5 mm | 4.991e-11 mm |

X-direction deformation is more than two orders of magnitude smaller than total deformation, consistent with a bending-dominated response.

Results are shown at two animation frames (0.89 s and 1.0 s) and are consistent across both.

## Failure Assessment

TODO: add a failure index plot from ACP Post (for example Tsai-Wu or maximum stress) with the maximum value and its location. Deformation alone does not show whether a composite part survives its load.

## Automation

TODO: attach the ACP Python script (as `acp_script.py`) and describe what it automates, or remove "Python scripting" from this README and your CV.

## Notes

- CAD and solver result files are not included because of file size. Available on request.
- TODO: add a one-line validation statement, such as a hand-calculation check of the deflection (beam or plate theory) with the percentage difference.

## Tools

ANSYS Mechanical (Static Structural), ANSYS ACP (Pre and Post), Python (ACP console)

## Author

TODO: your full name, MSc Automotive Engineering, University of Hertfordshire
GitHub: https://github.com/rupeshwaran67-prog
