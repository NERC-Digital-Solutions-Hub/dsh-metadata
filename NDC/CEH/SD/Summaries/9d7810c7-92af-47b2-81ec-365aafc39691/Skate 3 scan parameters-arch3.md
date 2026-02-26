# XTekCT

- This document is a configuration for the XTekCT CT reconstruction system, describing a dataset named "Skate 3 pt1" and detailing imaging geometry, acquisition, and X-ray settings.

- Core imaging geometry and region
  - Voxel grid: 2000 × 2000 × 2000 with voxel size approximately 0.0738 mm in X, Y, and Z.
  - Region of interest: RegionStartX/Y = 0; RegionPixelsX/Y = 2000; Region size = 2000 × 2000 × 2000.
  - Detector: 2000 × 2000 pixels with 0.2 mm pixel size.
  - Source-to-object distance: 433.1249 units; Source-to-detector distance: 1173.528 units.
  - Centre of rotation: Top and Bottom values are 0.0 (neutral/undefined in this file).

- Acquisition parameters
  - Projections: 1080.
  - Initial angle: 205.5148 degrees.
  - Angular step: 0.3333111849 degrees.
  - Output scaling: Scaling set to 1000.0; Normalisation = 1.0.
  - Coefficient settings: CoefX2 = 0.25; CoefX1 = 0.75; others 0.
  - Interpolation: Type 1; Median filter kernel size = 1.
  - Output: OutputType = 0; OutputUnits = /m; Units = mm.
  - Automatic centre of rotation enabled, with offsets set to zero.

- CT processing and X-ray settings
  - CTPro: FilterPreset = 0; Filter_ThicknessMM = 0.000; Filter_Material = None.
  - Shuttling: False (no shuttle mechanism in this configuration).
  - X-rays: XraykV = 120 kV; XrayuA = 145 μA.

- Additional notes
  - The configuration is modular, separating core CT parameters, processing filters, and X-ray settings, facilitating reuse and governance of the dataset.
  - Metadata richness (geometry, projections, angles, scaling, and detector details) supports reproducibility and evaluation, aligning with monitoring framework practice.