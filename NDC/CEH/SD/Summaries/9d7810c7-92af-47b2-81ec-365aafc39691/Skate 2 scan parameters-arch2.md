# Skate 2

## Overview
- Configuration for a computed tomography (CT) data acquisition and processing pipeline named Skate 2.
- Defines imaging geometry, detectors, projection sampling, processing filters, output formats, and data handling to produce standardized 3D voxel data.
- Aims to generate reproducible datasets suitable for environmental monitoring and subsequent analysis or policy evaluation.

## Imaging and acquisition parameters

- Image volume and voxels
  - VoxelsX = 2000, VoxelsY = 2000, VoxelsZ = 2000
  - VoxelSizeX = 0.125079 mm, VoxelSizeY = 0.125079 mm, VoxelSizeZ = 0.125079 mm
  - RegionStartX = 0, RegionStartY = 0
  - RegionPixelsX = 2000, RegionPixelsY = 2000

- Geometry and alignment
  - SrcToObject = 733.9188
  - SrcToDetector = 1173.528
  - CentreOfRotationTop = 0.0, CentreOfRotationBottom = 0.0
  - AutomaticCentreOfRotation = 1 (enabled)
  - AutomaticCentreOfRotationOffsetZ1 = 0, AutomaticCentreOfRotationOffsetZ2 = 0
  - MaskRadius = 125.0791
  - DetectorOffsetX = 0.0, DetectorOffsetY = 0

- Detector details
  - DetectorPixelsX = 2000, DetectorPixelsY = 2000
  - DetectorPixelSizeX = 0.2 mm, DetectorPixelSizeY = 0.2 mm
  - WhiteLevel = 60000.0
  - Scattering = 0.0

- Sampling and projections
  - Projections = 1080
  - InitialAngle = 109.6045 degrees
  - AngularStep = 0.3333132 degrees

- Region and processing controls
  - RegionStartX/Y and RegionPixelsX/Y as above
  - CoeffX4 = 0, CoeffX3 = 0, CoeffX2 = 0.25, CoeffX1 = 0.75, CoeffX0 = 0
  - Scale = 1.32
  - Normalisation = 1.0
  - InterpolationType = 1
  - MedianFilterKernelSize = 1
  - LowPercentile = 0.2, HighPercentile = 99.8
  - OutputUnits = /m, Units = mm
  - Scaling = 1000.0

## Processing, filtering, and output

- Filtering and normalization
  - FilterType = 0
  - CutOffFrequency = 2.5
  - Exponent = 1.0
  - Normalisation = 1.0
  - MedianFilterKernelSize = 1

- Data handling and export
  - TIFFScaling = 1
  - OutputType = 0
  - AutoScalingType = 0
  - ImportConversion = 0
  - Shuttling = False

- CTPro (filter/film-like properties)
  - FilterPreset = 0
  - Filter_ThicknessMM = 0.000
  - Filter_Material = None

- X-ray source
  - XraykV = 120 kV
  - XrayuA = 120 µA

## Environment-facing data considerations

- The configuration emphasizes standardized, QA-driven data generation to enable time-series comparisons of environmental samples.
- Outputs are designed for clear presentation (reports, maps, charts) and for storage in appropriate data portals.
- Aims to increase data value by enabling integration with other datasets and facilitating access to underlying data for broader reuse.