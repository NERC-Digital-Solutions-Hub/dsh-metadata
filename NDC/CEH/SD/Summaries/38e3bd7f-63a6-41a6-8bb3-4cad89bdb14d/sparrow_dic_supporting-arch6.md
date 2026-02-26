# Deformation videos of 3D printed Passer sparrow skulls - house ( Passer domesticus) and F1 hybrid - and supporting interpretation scripts.

## Overview
- A dataset of deformation videos for 3D printed Passer sparrow skulls (house sparrow and F1 hybrid) with supporting interpretation scripts.

## Collection and generation
- Samples derived from the Natural History Museum of Oslo specimen collection under a material transfer agreement.
- High-resolution CT scanning performed with a Waygate Technologies v|tome|x M 240kV CT system at 26 μA, at the Hounsfield Facility, University of Nottingham, UK.
- STL models printed at 10x scale in Nylon Pa12 using CfAM SLS machines at the University of Nottingham.
- Specimens secured at the base of the skull and loaded as a cantilever beam in a bespoke 5 kN load frame; loads of 2 kN applied; deformation recorded via reference point motion in the plane.

## Data types and recording
- Recorded as mp4 video files of deformation.
- Deformation stills captured at deformation point saved as jpg images (e.g., GOPRO0031.jpg).
- Deformations derived from jpgs by applying a scale factor based on a known dimension in the test frame.
- Analysis scripts are executed in MATLAB.

## Quality control
- Deformations are validated against measured values from the test frame.

## Data structure
- Each file corresponds to the scan of a single skull under loading.
- Scripts can combine test cases to produce comparative plots.

## Reproducibility and analysis workflow
- Includes data_23_3_23.mat which runs the analyses.
- MATLAB-based workflow; can be run without MATLAB using Python and SciPy.

### Loading the MATLAB file in Python (example)
```python
import scipy.io
mat = scipy.io.loadmat('data_23_3_23.mat')
```

## Access and usage guidance
- The dataset provides both the MATLAB analysis file and instructions for loading and using the data in Python via SciPy, enabling non-MATLAB workflows for analysis.