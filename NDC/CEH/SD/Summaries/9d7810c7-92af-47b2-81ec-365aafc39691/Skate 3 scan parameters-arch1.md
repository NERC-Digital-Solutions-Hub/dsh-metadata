# Skate 3 pt1

## Overview
- Configuration file for a CT/X-ray imaging dataset named Skate 3 pt1 (XTekCT format).
- Encodes imaging geometry, acquisition, and processing parameters used to reconstruct a 3D volume from 1080 projections.

## Imaging and voxel geometry
- Voxel grid: 2000 × 2000 × 2000
- Voxel size: 0.0738158705594889 (units likely mm) in X, Y, and Z
- Region of interest: RegionStartX=0, RegionStartY=0, RegionPixelsX=2000, RegionPixelsY=2000
- Offsets: OffsetX=0, OffsetY=0, OffsetZ=0
- Region scaling: Scaling=1000.0
- Output units: OutputUnits=/m; Units=mm

## Acquisition geometry
- Source-to-object distance (SrcToObject)=433.124931335449
- Source-to-detector distance (SrcToDetector)=1173.528
- Detector: 2000 × 2000 pixels, detector pixel size 0.2 × 0.2
- Center of rotation: CentreOfRotationTop=0, CentreOfRotationBottom=0; AutomaticCentreOfRotation=1
- Masking: MaskRadius=73.8158705594889

## Projection and angular parameters
- Projections=1080
- Initial angle=205.514755249023 degrees
- Angular step=0.33331118491503 degrees

## Reconstruction and processing settings
- Filter and normalization: FilterType=0; CutOffFrequency=2.4999999627471; Exponent=1.0; Normalisation=1.0
- Interpolation: InterpolationType=1
- Median filtering: MedianFilterKernelSize=1
- Pre/post-processing: AutoScalingType=0; LowPercentile=0; HighPercentile=99.8
- Output/scale: TIFFScaling=1; ImportConversion=0; AutoScalingType indicates how data is scaled during processing

## Output and data handling
- OutputType=0
- Additional scaling for output: Scaling=1000.0
- Data accessibility: Region and projection parameters imply a full-volume reconstruction workflow from the specified 1080 projections

## X-ray source configuration
- X-ray voltage (kV)=120; current (µA)=145

## CTPro and materials
- FilterPreset=0; Filter_ThicknessMM=0.000; Filter_Material=None

## Miscellaneous
- Shuttling=False (no shuttle movement during acquisition)