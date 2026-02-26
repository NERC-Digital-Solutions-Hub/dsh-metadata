# Overall description Deformation videos of 3D printed Passer sparrow skulls - house ( Passer domesticus) and F1 hybrid - and supporting interpretation scripts.

## Collection and generation methods
- Samples sourced from the Natural History Museum of Oslo under a material transfer agreement.
- High-resolution X-ray CT scanning performed with Waygate Technologies v|tome|x M 240kV at 26μA, at the Hounsfield Facility, University of Nottingham.
- STL reconstructions printed at 10x scale in Nylon Pa12 using CfAM SLS machines.
- Specimens secured at the base of the skull and loaded as cantilever beams in a bespoke 5 kN load frame; 2 kN loads applied with deformation measured via reference point motion in the plane.

## Nature and units of record values
- Primary data stored as mp4 video files.
- Deformation points captured as still jpg images at deformation moments (e.g., GOPRO0031.jpg).
- Deformations computed from jpgs using a scale factor derived from a known test-frame dimension.
- Analysis scripts are executed in MATLAB.

## Quality control
- Deformations validated by comparison with measured values from the test frame.

## Details of data structure
- Each file corresponds to the scan of a single skull under loading.
- Scripts aggregate multiple test cases to enable comparative plotting.

## Loading .mat file using python
- Data includes data_23_3_23.mat, which can be analyzed in MATLAB or, without MATLAB, via Python’s SciPy.
- Example: Python code to load the file using scipy.io.loadmat.