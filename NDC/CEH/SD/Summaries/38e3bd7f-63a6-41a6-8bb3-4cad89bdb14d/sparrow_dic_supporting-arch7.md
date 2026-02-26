# Deformation videos of 3D printed Passer sparrow skulls - house ( Passer domesticus) and F1 hybrid - and supporting interpretation scripts

## Overview
- Deformation videos of 3D printed Passer sparrow skulls (house sparrow and an F1 hybrid) with interpretation scripts to support analysis.

## Collection and generation
- Samples sourced from the Natural History Museum of Oslo under a material transfer agreement.
- Scanned with a high-resolution X-ray CT system (Waygate Technologies v|tome|x M 240kV) at 26 μA.
- STL models printed at 10x scale in Nylon Pa12 using CfAM SLS technology.
- Specimens secured at the skull base and loaded as cantilevers in a bespoke 5 kN load frame at the University of Nottingham.
- Applied loads of 2 kN; deformation tracked via motion of a reference point in the deformation plane.

## Data outputs and processing
- Raw data stored as mp4 video files; deformation stills captured at peak deformation as jpg images (e.g., GOPRO0031.jpg).
- Deformations computed by scaling jpg-derived measurements using a known frame dimension; analysis scripts run in MATLAB.
- A matlab data file (data_23_3_23.mat) central to the analyses; includes the core dataset and processing steps.

## Quality control
- Deformation measurements validated against direct measurements from the test frame.

## Data structure and organization
- Each file corresponds to the scan of a single skull under loading.
- Scripts enable combining test cases to generate comparative plots across samples.

## Reproducibility and accessibility
- The analysis is encapsulated in data_23_3_23.mat; MATLAB-based workflow is provided.
- Python access is supported via SciPy; example code shows how to load the MAT file without MATLAB.

## Software, environment, and reproducibility notes
- MATLAB is the primary software for running analyses.
- Python (SciPy) can alternatively load and process the provided MAT file, enabling broader reproducibility without MATLAB.

## GIS relevance and potential applications
- Multi-modal data (video, images, 3D STL models) with spatial references via known test-frame dimensions.
- STL 3D models and deformation data could be integrated into GIS-based 3D visualization platforms for spatial-temporal analysis or educational visualization.
- Clear data provenance and processing steps support interoperability with map-based data products and cross-dataset comparisons.