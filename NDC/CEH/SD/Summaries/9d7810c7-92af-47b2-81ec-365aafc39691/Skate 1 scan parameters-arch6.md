# [XTekCT]

## Overview
- Configuration for Skate 1 CT data, embedding full geometry, projection, and acquisition parameters used to reconstruct a 3D volume.
- Defines a large voxel grid and detector geometry, projection count, and angles along with scaling and output settings.

## Key data fields

- Voxel and region
  - VoxelsX/Y/Z: 2000 each; RegionPixelsX/Y: 2000 each; RegionStartX/Y: 0
  - VoxelSizeX/Y/Z: ~0.12508 (units implied by VoxelSize fields)
  - Region size aligns with region pixels (2000x2000)

- Geometry and alignment
  - SrcToObject: 733.92
  - SrcToDetector: 1173.53
  - CentreOfRotationTop/Bottom: 0.0
  - AutomaticCentreOfRotation: 1 (enabled)

- Detector and sampling
  - DetectorPixelsX/Y: 2000
  - DetectorPixelSizeX/Y: 0.2
  - DetectorOffsetX/Y: 0.0
  - WhiteLevel: 60000.0
  - Scattering: 0.0

- Projection and acquisition
  - Projections: 1080
  - InitialAngle: 132.173°
  - AngularStep: 0.333314456° per projection

- Scaling and normalization
  - Scale: 1.32
  - Normalisation: 1.0
  - OutputUnits: /m
  - Units: mm
  - Scaling: 1000.0

- Filtering and interpolation
  - FilterType: 0
  - CutOffFrequency: 2.4999999627471
  - Exponent: 1.0
  - InterpolationType: 1
  - MedianFilterKernelSize: 1
  - CTPro: FilterPreset 0, Filter_ThicknessMM 0.000, Filter_Material None

- Region and output
  - RegionStartX/Y: 0
  - RegionPixelsX/Y: 2000
  - OutputType: 0
  - TIFFScaling: 1

- Shuttling and X-ray settings
  - Shuttling: False
  - [Xrays] XraykV: 120 kV, XrayuA: 145 μA

## What this means for data work

- Provides a complete, self-contained setup to reproduce the CT data processing pipeline for Skate 1, from acquisition geometry through reconstruction parameters to final output formatting.
- Automatic centre of rotation suggests an emphasis on simplifying alignment and reducing manual calibration steps.
- Detailed detector geometry and projection sampling enable reproducible data products (volumes, slices, or 2D projections) with defined units and scaling.

## Data quality and usability considerations

- Large voxel grid with a defined region ensures high-resolution reconstruction but may impact storage and compute needs.
- White level and scaling values should be validated against actual detector response to prevent incorrect intensity interpretation.
- Regional consistency (RegionStart 0 and RegionPixels 2000) should be verified against the actual data extent to avoid truncation or padding artifacts.
- Zero or neutral values for CTPro parameters indicate no special material or thickness filtering applied; consider validating if material-based corrections are required in downstream analyses.

## Potential data products and usage

- Reconstructed 3D volume in units of mm with intensity scaling defined by the configuration.
- 2D projections or slices derived from the projection geometry for inspection or QA.
- Self-serve outputs via the defined output units and TIFF scaling for easy sharing and visualization.