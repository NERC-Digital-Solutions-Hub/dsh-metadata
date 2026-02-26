# Deformation videos of 3D printed Passer sparrow skulls - house ( Passer domesticus) and F1 hybrid - and supporting interpretation scripts

## Overview
- Deformation experiments on 3D printed Passer sparrow skulls, including house sparrow and an F1 hybrid.
- Data and interpretation scripts accompany the physical experiments.

## Provenance and collection methods
- Samples derived from the Natural History Museum of Oslo under a material transfer agreement.
- High-resolution CT scans performed with Waygate Technologies v|tome|x M 240kV CT system (26 μA) at the Hounsfield Facility, University of Nottingham.
- STL print files produced at 10x scale in Nylon Pa12 using CfAM SLS at the University of Nottingham.
- Specimens mounted securely and loaded as cantilever beams in a bespoke 5 kN load frame; loads of 2 kN applied; deformation tracked via reference-point motion.

## Data formats and structure
- Primary data: mp4 video files of deformation sequences.
- Derived imagery: JPG stills captured at deformation points (e.g., GOPRO0031.jpg) for measurement.
- Deformation calculations: scale factors derived from known dimensions in the test frame; results mapped to deformation values.
- Analysis scripts: MATLAB-based workflow; MAT-file data included (e.g., data_23_3_23.mat).
- Cross-software accessibility: MAT-file can be loaded in Python via SciPy without MATLAB.

## Processing, quality control, and data quality
- Deformations validated against measured values from the test frame.
- Data structure designed so each file corresponds to a single skull scan under loading; scripts enable combining cases for comparative plots.

## Metadata, documentation, and reproducibility
- Documentation notes how data are recorded and scaled; includes the specific MAT-file used for analyses.
- Clear provenance of scans, prints, and test setup to support reproducibility.
- Instructions provided for loading MAT data in Python (SciPy), aiding reuse across environments.

## Accessibility, sharing, and reuse considerations
- Data are organized to facilitate reuse across software platforms (MATLAB and Python).
- Includes both raw video and still imagery, as well as processing scripts and data files, supporting transparency and re-analysis.
- For broader data publishing, consider providing a data dictionary, specimen identifiers, versioning, and a readme with dependencies and workflow steps.

## Practical implications for data stewardship
- Governance: track specimen provenance, transfer agreements, and instrument configurations to ensure traceability.
- Standards: maintain consistent naming, metadata fields (source, CT settings, print parameters, load conditions, scale calibrations), and file formats (video, images, MAT).
- Availability and updates: document any changes to scripts or data structure; provide guidance on extending analyses with new skull scans.
- Interoperability: ensure MATLAB and Python compatibility; supply example code and minimal environment requirements to lower barriers to reuse.
- Documentation: supply a data dictionary and readme to accompany the files, outlining units, calibration references, and interpretation notes.