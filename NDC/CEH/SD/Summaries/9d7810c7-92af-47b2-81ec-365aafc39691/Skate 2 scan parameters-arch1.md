# Skate 2

## Overview
- A configuration/parameter file for Skate 2 CT reconstruction, detailing voxel grid, geometry, detector setup, projection schedule, processing filters, and X-ray settings.

## Key Parameters

- Voxel and region
  - VoxelsX = 2000, VoxelsY = 2000, VoxelsZ = 2000
  - VoxelSizeX = VoxelSizeY = VoxelSizeZ ≈ 0.125079 mm
  - RegionStartX = 0, RegionStartY = 0
  - RegionPixelsX = 2000, RegionPixelsY = 2000
  - Projections = 1080
  - InitialAngle = 109.604499816895 degrees
  - AngularStep = 0.333313160526336 degrees

- Geometry and coordinates
  - SrcToObject ≈ 733.9188
  - SrcToDetector ≈ 1173.528
  - DetectorPixelsX = 2000, DetectorPixelsY = 2000
  - DetectorPixelSizeX = DetectorPixelSizeY = 0.2 mm
  - CentreOfRotationTop = 0.0, CentreOfRotationBottom = 0.0
  - AutomaticCentreOfRotation = 1
  - AutomaticCentreOfRotationOffsetZ1 = 0, AutomaticCentreOfRotationOffsetZ2 = 0
  - OutputUnits = /m, Units = mm
  - Shuttling = False

- Filtering, scaling, and processing
  - FilterType = 0
  - CutOffFrequency = 2.4999999627471
  - Exponent = 1.0
  - Normalisation = 1.0
  - InterpolationType = 1
  - MedianFilterKernelSize = 1
  - Scaling = 1000.0
  - OutputType = 0
  - TIFFScaling = 1
  - WhiteLevel = 60000.0
  - CoefX4 = 0, CoefX3 = 0, CoefX2 = 0.25, CoefX1 = 0.75, CoefX0 = 0

- Region, scaling, and metadata
  - RegionStartX = 0, RegionStartY = 0
  - RegionPixelsX = 2000, RegionPixelsY = 2000
  - Scale = 1.32
  - AutoScalingType = 0
  - ImportConversion = 0
  - FilterPreset = 0
  - Filter_ThicknessMM = 0.000
  - Filter_Material = None
  - CTPro: FilterPreset=0, Filter_ThicknessMM=0.000, Filter_Material=None

- X-ray source
  - XraykV = 120 kV
  - XrayuA = 120 μA

- Additional controls
  - OutputUnits = /m
  - RegionStart and RegionPixels actively define the irradiated region
  - Shuttling = False

## Data and Context for Analysis

- This file captures a full CT acquisition and reconstruction setup intended for reproducible analyses, including:
  - A high-resolution 3D voxel grid (2000^3) with ~0.125 mm voxel size
  - A 1080-projection acquisition spanning roughly 360 degrees with ~0.333-degree steps
  - A 2000×2000 detector with 0.2 mm pixels
  - Center-of-rotation handling and basic preprocessing/filtering (default or minimal filtering)
  - X-ray settings: 120 kV, 120 μA

- Potential uses for analytics
  - Reproducing reconstruction results for comparison across datasets
  - Aligning voxel grid and geometry parameters for cross-study analyses
  - Tracking metadata such as projection count, angles, and scaling factors for reproducibility

## Considerations for Analysts

- Scale and units: consistent use of millimeters and meters is required; scaling factor is 1.32 and there is a 1000.0 scaling parameter for processing
- Center of rotation: automatic enabling suggests reliance on software defaults; center offsets are set to zero
- Data accessibility: this is a detailed, self-contained parameter set suitable for input into the Skate 2 pipeline; ensure compatibility with the software version
- Filtering defaults: minimal filtering (FilterType 0, CutOffFrequency 2.5, Exponent 1.0) may influence image quality and quantitative measurements
- Data provenance: includes explicit X-ray conditions and geometric parameters essential for replication and downstream quantitative analyses