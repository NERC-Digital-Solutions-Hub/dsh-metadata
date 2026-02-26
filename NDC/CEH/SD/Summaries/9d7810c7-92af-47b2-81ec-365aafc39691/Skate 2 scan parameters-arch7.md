# Skate 2 CT Configuration

## Overview
- Configuration for Skate 2 CT data processing, defining a 3D voxel grid and related imaging parameters.
- Voxel grid: 2000 x 2000 x 2000 with voxel size ≈ 0.125 mm in all directions.
- Output settings indicate TIFF outputs with a scaling factor of 1000 and units reference in meters per internal mm units (Units: mm; OutputUnits: /m).

## Data and File Management
- Input/Output naming: InputSeparator and OutputSeparator are underscores; InputFolderName and OutputFolderName are both Skate 2.
- Shuttling is disabled (Shuttling=False).
- Import conversion is disabled (ImportConversion=0).
- CT data organization region defined from RegionStartX=0, RegionStartY=0 with RegionPixelsX=2000, RegionPixelsY=2000.

## Geometry and Coordinate Setup
- Source-to-object and source-to-detector distances: SrcToObject=733.9188; SrcToDetector=1173.528.
- Detector: 2000 x 2000 pixels with detector pixel size 0.2 mm.
- Center of rotation: flags indicate automatic calculation (AutomaticCentreOfRotation=1) with offsets (AutomaticCentreOfRotationOffsetZ1=0, AutomaticCentreOfRotationOffsetZ2=0).
- CentreOfRotationTop and CentreOfRotationBottom both 0.0.

## Projections and Angles
- Projections: 1080 total projections.
- InitialAngle: 109.6045 degrees; AngularStep: 0.3333131605 degrees between projections.

## Image Formation and Processing
- White level: 60000.0; Scattering: 0.0.
- Coefficient blending (CoefX4..CoefX0): X4=0, X3=0, X2=0.25, X1=0.75, X0=0.
- Filter and normalization: FilterType=0, CutOffFrequency≈2.5, Exponent=1.0, Normalisation=1.0.
- Interpolation: Type 1; MedianFilterKernelSize=1; Scaling=1000.0.
- Region and region processing: RegionStartX=0, RegionStartY=0, RegionPixelsX=2000, RegionPixelsY=2000.
- CTPro: FilterPreset=0, Filter_ThicknessMM=0.000, Filter_Material=None.

## Output and Scaling
- OutputType=0; TIFFScaling=1.
- AutoScalingType=0; LowPercentile=0.2; HighPercentile=99.8.
- OutputUnits=/m with internal Distance Scaling 1000.0 (facilitates unit conversion to meters).

## X-ray Source Settings
- X-ray tube voltage: 120 kV; X-ray current: 120 µA.

## Additional Details
- Region and voxel region mapping align with the 2000x2000x2000 grid centered around the defined region.
- Data path includes the explicit Skate 2 naming for both input and output folders.