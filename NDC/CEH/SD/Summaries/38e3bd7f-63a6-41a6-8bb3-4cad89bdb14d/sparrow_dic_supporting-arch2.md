# Deformation videos of 3D printed Passer sparrow skulls - house ( Passer domesticus) and F1 hybrid - and supporting interpretation scripts.

## Overview
- A dataset of deformation videos for 3D printed sparrow skulls (house Passer domesticus and an F1 hybrid) accompanied by scripts to interpret deformation data.
- Aimed at enabling standardized assessment of mechanical deformation under loading, with traceable data lineage and analysis workflows.

## Collection and generation methods
- Source specimens: Natural History Museum of Oslo under a material transfer agreement.
- Imaging: Scanned with a high-resolution X-ray Waygate Technologies v|tome|x M 240kV CT system at 26 μA, at the Hounsfield Facility, Sutton Bonington Campus, University of Nottingham.
- 3D models: Resulting STL files printed at 10x scale in Nylon Pa12 using CfAM SLS machines.
- Mechanical testing: Specimens secured at the skull base and loaded as a cantilever beam in a bespoke 5 kN load frame at the University of Nottingham; loads of 2 kN applied; deformation captured via reference point motion in the plane.

## Nature and units of record values
- Data formats: mp4 video files recording deformation; snapshots captured as jpg images (e.g., GOPRO0031.jpg) at deformation points.
- Deformation measurement: Calculated from jpg frames by applying a scale factor from a known dimension in the test frame.
- Analysis tools: All scripts run in MATLAB.

## Quality control
- Deformations validated against measured values obtained from the test frame.

## Details of data structure
- Each file corresponds to the scan of a single skull under loading.
- Scripts are capable of combining multiple test cases to generate comparative plots.

## Reproducibility and tooling
- Data can be loaded in Python via SciPy as an alternative to MATLAB.
- Specific example data file: data_23_3_23.mat.
- It is possible to run the analyses without MATLAB using SciPy in Python.

### Example: loading the MAT-file with Python (SciPy)
- Code to load the data:
  ```
  import scipy.io
  mat = scipy.io.loadmat(`data_23_3_23.mat`)
  ```
- Note: With the SciPy package installed, the MAT-file can be loaded without MATLAB; the following indicates the capability to run without MATLAB using SciPy.