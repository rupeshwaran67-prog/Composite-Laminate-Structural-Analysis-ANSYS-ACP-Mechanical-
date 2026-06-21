# Composite-Laminate-Structural-Analysis-ANSYS-ACP-Mechanical-
Static structural FEA of a composite sandwich laminate panel, using ANSYS Composite PrepPost (ACP) for ply-wise layup definition and ANSYS Mechanical for deformation analysis under applied loading.

Overview

This project models a tapered composite panel using ANSYS ACP (Pre) to define the ply stack-up and ANSYS Mechanical (Static Structural) to evaluate total and directional deformation under load. The workflow demonstrates a full composite analysis pipeline: material definition → ply layup → solid model generation → structural solve → results post-processing.

Setup

ParameterValueSolverANSYS Mechanical (Static Structural)Layup toolANSYS Composite PrepPost (ACP Pre)MaterialsEpoxy Carbon Woven (230 GPa) Wet, Epoxy Carbon UD (230 GPa) Wet, Structural SteelBoundary conditionsFixed Support ×2, Applied ForceGeometryTapered laminate panel (SolidModel.1)Unitsmm, kg, N, s, mV, mA

Ply Layup (ACP)

The laminate was defined using ANSYS ACP with element-wise thickness assignment across multiple modeling plies (ModelingPly.1, .2, .4, .5) within a single Modeling Group. Ply thickness was set via element-wise extrusion guides referencing the full element set (All_Elements). The solid model was generated using the inside-ply drop-off type and shell-normal offset, with a maximum thickness of 1.0 mm.

[Add specific ply stacking sequence / fibre orientation angles here if available, e.g. [0°/90°/±45°]ₙ]

Results

Total Deformation

ValueMinimum0 mmMaximum4.6981 × 10⁻³ mmAverage1.8965 × 10⁻³ mm

Total deformation is concentrated at the unsupported/free end of the panel, with deformation increasing progressively along the span away from the fixed supports — consistent with expected bending behaviour under the applied load.

Directional Deformation (X-Axis)

ValueMinimum-1.0436 × 10⁻⁵ mmMaximum1.0436 × 10⁻⁵ mmAverage4.991 × 10⁻¹¹ mm

The near-zero average directional deformation in X confirms the structure is primarily deforming in the through-thickness/bending direction rather than axially, as expected for this loading configuration.


Note: results were captured at two animation/load-step frames (0.89 s and 1.0 s) during post-processing — values are consistent across both, confirming a stable converged solution rather than a discrepancy.



Tools Used


ANSYS Mechanical (Static Structural)
ANSYS Composite PrepPost (ACP Pre)
Python scripting (ACP automation/logging, via ACP's embedded Python console)


Repository Contents


Deformation contours, ACP ply layup screenshots
This file


Notes

CAD and solver result files are not included in this repository due to file size. Available on request.

Author

Rupeshwaran Paranthaman — MSc Automotive Engineering, University of Hertfordshire
github.com/rupeshwaran67-prog
