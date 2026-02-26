# Deformation videos of 3D printed Passer sparrow skulls - house ( Passer domesticus) and F1 hybrid - and supporting interpretation scripts.

## Overview
- Deformation videos of 3D printed Passer sparrow skulls (house sparrow and F1 hybrid) with accompanying interpretation scripts.

## Collection and generation methods
- Source: Natural History Museum of Oslo specimen collection under a material transfer agreement.
- Imaging: high-resolution X-ray CT using Waygate Technologies v|tome|x M 240kV at 26 μA, conducted at the Hounsfield Facility, University of Nottingham.
- 3D printing: STL files printed at 10x scale in Nylon Pa12 using CfAM SLS at the University of Nottingham.
- Mechanical testing: specimens secured at the base of the skull and loaded as a cantilever beam in a bespoke 5 kN load frame; loads of 2 kN applied; deformation tracked via reference point motion in the plane.

## Nature and units of record values
- Data formats: mp4 videos; deformation points captured as still images (jpg, e.g., GOPRO0031.jpg) at the point of deformation.
- Deformation calculation: derived from jpgs by applying a scale factor from a known dimension in the test frame.
- Analysis tools: MATLAB scripts used for processing.

## Quality control
- Deformations validated against measured values from the test frame.

## Details of data structure
- Each file corresponds to a scan of a single skull under loading.
- Scripts compile multiple test cases to generate comparative plots.

## Data access and usage notes
- Includes data_23_3_23.mat containing analyses; MATLAB is not strictly required—can be loaded in Python via SciPy.
- Python usage example:
  - import scipy.io
  - mat = scipy.io.loadmat('data_23_3_23.mat')