# Deformation videos of 3D printed Passer sparrow skulls - house ( Passer domesticus) and F1 hybrid - and supporting interpretation scripts

- Overview
  - Deformation videos of 3D printed Passer sparrow skulls (house sparrow and F1 hybrid) with accompanying interpretation scripts.

- Collection and provenance
  - Samples derived from Natural History Museum of Oslo under a material transfer agreement.
  - Scanned with high-resolution X-ray CT (Waygate Technologies v|tome|x M 240kV) at 26 μA.
  - Scans conducted at Hounsfield Facility, University of Nottingham; STL prints produced at University of Nottingham at 10x scale in Nylon PA12 (CfAM SLS).
  - Specimens secured by clamps at the base of the skull and loaded as a cantilever beam in a bespoke 5 kN load frame.
  - Loads of 2 kN applied; deformation recorded by tracking reference point motion.

- Data content and formats
  - Primary recordings stored as mp4 deformation videos.
  - Still frames captured during deformation stored as JPG images (e.g., GOPRO0031.jpg).
  - Deformations computed from JPGs using a scale factor from a known dimension in the test frame; analyses run in MATLAB.
  - Includes data_23_3_23.mat (MAT-file) for analyses; can be loaded in Python via SciPy without MATLAB.

- Data structure and organization
  - Each file corresponds to the scan of a single skull under loading.
  - Scripts consolidate test cases to produce comparative plots. 

- Processing and analysis workflow
  - MATLAB scripts perform deformation calculations from JPG frames.
  - Python (SciPy) can load data_23_3_23.mat to run analyses without MATLAB.

- Quality control
  - Deformations validated against measured values from the test frame.

- Access, reuse, and interoperability
  - Data and interpretation scripts provided; MATLAB-based workflow with a Python alternative via SciPy.
  - Experimental context (CT scanning, 3D printing, loading apparatus) important for reproducibility.

- Governance, rights, and sustainability
  - Access governed by a material transfer agreement; provenance tied to multiple institutions and campus facilities.
  - Data are tied to a specific experimental setup, aiding reproducibility while informing potential limitations on generalizability.

- Practical implications for Data Leaders
  - Demonstrates end-to-end data lifecycle: acquisition, processing, validation, and interpretation.
  - Multiple tooling paths (MATLAB and Python) support diverse analytics environments.
  - Highlights needs around metadata and discoverability (detailed metadata is not described; consider expanding metadata for governance and reuse).