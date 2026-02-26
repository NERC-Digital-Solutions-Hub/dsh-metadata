# XTekCT

## Overview
- Defines a Skate 1 CT scan configuration with a 2000×2000×2000 voxel grid.
- Voxel size: ~0.125 mm in x, y, z; region of interest spans the full region (RegionStart 0, RegionPixels 2000 in x and y).
- Acquisition setup includes 1080 projections, initial angle 132.173°, angular step 0.333314°.
- Output is TIFF with scaling enabled, units in millimeters and meters, and a regional processing frame.

## Data Assets and Structure
- Voxel data and CT projections with detailed geometric parameters:
  - SrcToObject and SrcToDetector distances provided.
  - Detector: 2000×2000 pixels, detector pixel size 0.2 mm.
  - Centre of rotation parameters present (CentreOfRotationTop/Bottom = 0).
  - OutputFolderName: Skate 1; InputFolderName unspecified.
- Region and scaling metadata:
  - RegionStartX/Y = 0; RegionPixelsX/Y = 2000.
  - Scale = 1.32; OutputType = 0; TIFFScaling = 1.
  - OutputUnits = /m; Units = mm; AutomaticCentreOfRotation = 1.
  - LowPercentile = 0.2; HighPercentile = 99.8; Normalisation = 1.0.
- Acquisition and reconstruction controls:
  - Projections = 1080; InitialAngle = 132.173°, AngularStep = 0.333314°.
  - Shuttling = False; Region and processing parameters defined.
- X-ray source settings:
  - Xrays: kV = 120, µA = 145.
- CT processing parameters (CTPro and related):
  - FilterPreset = 0; Filter_ThicknessMM = 0.000; Filter_Material = None.

## Acquisition, Processing and Quality Parameters
- Image formation and filtering:
  - FilterType = 0; CutOffFrequency = 2.5; Exponent = 1.0; InterpolationType = 1.
  - MedianFilterKernelSize = 1; Normalisation = 1.0; Scaling = 1000.0.
  - Coefficients: CoefX4=0, CoefX3=0, CoefX2=0.25, CoefX1=0.75, CoefX0=0.
- Data scaling and output:
  - Scale = 1.32; OutputUnits = /m; Units = mm.
  - OutputType = 0; TIFFScaling = 1; AutoScalingType = 0.
- Data governance hints:
  - Region and pixel sizing, center of rotation handling, and percentile-based intensity controls indicate a defined, repeatable data processing pipeline.

## Metadata, Standards and discoverability
- Rich set of acquisition and geometry metadata (distances, detector specs, ROI, rotation, and scaling) supports reproducibility.
- Some fields are present (e.g., automatic center of rotation, region definitions, output formats) but explicit data provenance and licensing metadata are not shown.
- Clear naming for data outputs (Skate 1) aids discoverability within a compatible data ecosystem.

## Practical Implications for Data Leaders
- Data assets are well-parametrized for reproducibility but may require additional governance context (data lineage, licensing, and access policies) for broader sharing.
- Ensuring metadata completeness and alignment with organizational data standards will improve interoperability with partners and downstream analyses.
- Consider cataloging these assets with versioning, explicit access controls, and documentation of the data processing pipeline (filters, normalization, scaling, and coefficients) to support reuse.

## Next Steps and Recommendations
- Add or confirm data licensing, ownership, and access permissions for Skate 1 CT dataset.
- Document data lineage: source raw data, processing steps, and software versions used for filtering and scaling.
- Register the dataset in a data catalog with consistent metadata fields (units, ROI, projection count, rotation, detector specs).
- Standardize metadata schemas across similar datasets to facilitate cross-institution data sharing and reproducibility.