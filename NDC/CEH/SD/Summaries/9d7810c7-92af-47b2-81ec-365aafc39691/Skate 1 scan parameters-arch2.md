# XTekCT

## Overview
- Configuration for a CT imaging run named Skate 1, using a 3D voxel grid and reconstruction workflow.
- Core parameters define a high-resolution 3D volume (2000 × 2000 × 2000 voxels) with approximately 0.125 mm isotropic voxel size.
- Detector setup: 2000 × 2000 pixels with 0.2 mm pixel size.
- Acquisition: 1080 projections with an initial angle of 132.173 degrees and an angular step of ~0.3333 degrees.
- Automatic centre of rotation enabled, with rotation offsets provided.
- Output is configured for TIFF-like scaling and units in millimeters, with a scaling factor of 1000.0 applied.
- X-ray source settings included: 120 kV and 145 µA.
- Filtering and image processing parameters present (FilterType, CutOffFrequency, Normalisation, InterpolationType, MedianFilterKernelSize, etc.).

## Imaging Setup and Resolution
- Voxel dimensions: 0.125079 mm in X, Y, and Z.
- Region of interest: 2000 × 2000 pixels (RegionStart 0, RegionPixels 2000).
- Source-to-object distance: 733.92 units; Source-to-detector distance: 1173.53 units.
- Detectors: 2000 × 2000 with detector pixel size 0.2 mm.
- Projections: 1080, with angular sampling at 0.333314 degrees.
- Centre of Rotation: Automatic, with specified offsets (Z axis offsets set to 0.0).

## Data Output and Calibration
- Output type: 0 (unspecified in this context).
- TIFF scaling: enabled (1).
- White level: 60000.0; Scattering: 0.0; Coefficient set (CoefX0–CoefX4) with a notable emphasis on CoefX2 = 0.25 and CoefX1 = 0.75.
- Normalisation: 1.0; InterpolationType: 1; MedianFilterKernelSize: 1.
- Output units: /m (OutputUnits) and millimeters (Units); Scaling: 1000.0.
- Filter and pre-processing: FilterPreset 0, CutOffFrequency 2.5, Exponent 1.0, and AutomaticCentreOfRotation enabled.

## Processing and Metadata
- ImportConversion: 0 (no automatic conversion applied on import).
- AutoScalingType: 0 (default or manual scaling pathway).
- Shuttling: False (no automated sample shuttle operation during run).
- Region and projection data mapped to standardized coordinates for reproducibility and traceability.

## Data Management and Accessibility
- Emphasizes storage and uploading of created datasets to appropriate data portals.
- Aligns with standardized data handling to facilitate reuse and long-term accessibility.
- Includes explicit provenance through parameterized configuration for repeatable monitoring and analysis.

## Relevance to Environmental Monitoring and Policy
- Provides a reproducible, standardized imaging workflow that can be used to characterize environmental samples (e.g., microstructure, porosity, contaminant distribution) in a consistent format.
- The explicit metadata (voxel size, detector geometry, projection count, angular sampling, output scaling) supports cross-study comparisons and trend analysis over time.
- Highlights the importance of making underlying data accessible and interoperable to maximize the value of monitoring datasets and enable integration with other environmental data streams.