# Skate 1

- This document is a configuration for a CT reconstruction/processing pipeline labeled as Skate 1, detailing voxel geometry, projection geometry, processing, and acquisition settings.
- Key purpose: specify imaging, reconstruction, and output parameters for a 1080-projection CT scan.

## Imaging and Volume Geometry

- Volume/grid
  - Voxels: 2000 × 2000 × 2000
  - Voxel sizes: X 0.12508 mm, Y 0.12508 mm, Z 0.12508 mm
  - Region: RegionStartX/Y 0; RegionPixelsX/Y 2000
- Center and scaling
  - Centre of rotation: automatic (AutomaticCentreOfRotation=1) with no offsets
  - Source-to-object distance: 733.9188
  - Source-to-detector distance: 1173.528
  - Detector: 2000 × 2000 pixels; detector pixel size 0.2 mm
  - White level: 60000.0
  - Scaling factor: 1000.0
- Regions and alignment
  - RegionStartX/Y: 0
  - RegionPixelsX/Y: 2000

## Acquisition and Geometry Details

- Projections
  - Projections: 1080
  - Initial angle: 132.1730 degrees
  - Angular step: 0.333314456403047 degrees per projection
- Output/Units
  - Output units: /m
  - Units: mm

## Reconstruction and Processing Parameters

- Filters and corrections
  - FilterType: 0
  - CutOffFrequency: 2.5
  - Exponent: 1.0
  - Normalisation: 1.0
  - MedianFilterKernelSize: 1
  - InterpolationType: 1
  - Scattering: 0.0
  - Coefficients for correction: X4=0, X3=0, X2=0.25, X1=0.75, X0=0
- Data handling and normalisation
  - Automatic centre-of-rotation: enabled
  - Shuttling: False

## Output and File Management

- Folders
  - InputFolderName: (unspecified)
  - OutputFolderName: Skate 1
- File formatting
  - InputSeparator: _
  - OutputSeparator: _
- Additional processing settings
  - FilterPreset: 0
  - RegionStartX/Y: 0
  - RegionPixelsX/Y: 2000

## X-ray Acquisition Parameters

- X-ray settings
  - XraykV: 120
  - XrayuA: 145

## Notes for Analysts

- The configuration is highly specific to a single scan setup and includes automatic center-of-rotation and a full 360°-like acquisition window (1080 projections with 0.333° steps).
- Several fields are set to 0 or left at defaults, suggesting areas where domain expertise or dataset-specific calibration could be applied if needed.
- Output scaling and unit conventions indicate the data is prepared for downstream quantitative analysis or cross-dataset comparisons.