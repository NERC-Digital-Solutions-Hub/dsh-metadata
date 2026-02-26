# Skate 3 pt1

- This configuration defines a CT imaging dataset and reconstruction workflow named Skate 3 pt1, covering geometry, detector setup, projection sampling, filtering, scaling, and output formatting. It also includes X-ray source settings and a CTPro sub-section for optional filtering.

## Key parameters and data geometry

- Voxel grid: 2000 × 2000 × 2000 voxels; voxel size 0.0738 mm in X, Y, and Z.
- Spatial origins: RegionStartX/Y = 0; RegionPixelsX/Y = 2000 (full region used).
- Source-to-object and source-to-detector distances: SrcToObject = 433.125; SrcToDetector = 1173.528.
- Detector: 2000 × 2000 pixels; detector pixel size = 0.2 mm; detector offset X/Y = 0.
- Calibration and orientation:
  - Center of rotation: default 0 for top/bottom; AutomaticCentreOfRotation = true.
  - WhiteLevel = 60000.0; Scattering = 0.0.
- Shuttling: False (data capture path not shuttled).
- Identification: Name and OutputFolderName both indicate Skate 3 pt1.

## Projection and acquisition settings

- Projections: 1080 projections captured.
- Angular sampling: InitialAngle = 205.5148 degrees; AngularStep = 0.3333111849 degrees per projection.
- Output/units: OutputUnits = /m; Units = mm.
- Region handling: RegionStartX/Y = 0; RegionPixelsX/Y = 2000 (full region used).
- TIFF and import/export: TIFFScaling = 1; ImportConversion = 0; OutputType = 0.

## Data processing and reconstruction parameters

- Filter and reconstruction:
  - FilterType = 0; CutOffFrequency ≈ 2.5; Exponent = 1.0; Normalisation = 1.0.
  - InterpolationType = 1; MedianFilterKernelSize = 1.
  - Scaling = 1000.0 (scaling applied to output data).
- Coefficients and scaling model: CoefX4=0, CoefX3=0, CoefX2=0.25, CoefX1=0.75, CoefX0=0 (data-driven or calibration mix).
- Centering and corrections: AutomaticCentreOfRotation = 1; AutomaticCentreOfRotationOffsetZ1/2 = 0; OutputType = 0.
- Normalization and percentile controls: LowPercentile = 0.2; HighPercentile = 99.8.
- Output formatting: TIFFScaling = 1; OutputUnits = /m.

## CTPro and filtering options

- [CTPro] FilterPreset = 0; Filter_ThicknessMM = 0.000; Filter_Material = None (no CTPro filtering applied by default).

## X-ray source settings

- X-rays: kV = 120; μA = 145 (typical acquisition parameters for the scan).

## Data provenance and potential data products

- Data products likely include:
  - Reconstructed 3D CT volume at the specified voxel grid and scaling.
  - Projection data and/or sinograms may be referenced by the 1080 projections and angular sampling.
  - Calibration outputs such as center-of-rotation determination and/or quality indicators (percentile-based intensity scaling and white level).
  - Optional CTPro-filtered results if enabled in future configurations.
- Meta and provenance captured by: dataset name, input/output paths, geometry, acquisition parameters, and processing settings.

## Practical considerations for Data Support

- Reproducibility: The explicit initial angle, angular step, region, and automatic center-of-rotation enable repeatable reconstructions; preserve all parameter values for future runs.
- Data quality and consistency: Verify that the automatic center-of-rotation finding is appropriate for the dataset; confirm that the full region (RegionPixels 2000) aligns with the detector and voxel grid.
- Data integration: Ensure downstream tools can interpret the units (mm, /m) and scaling (1000.0) consistently; confirm TIFF export behavior matches downstream workflows.
- Potential enhancements:
  - Provide a summary dashboard of key parameters (projections, angular sampling, voxel size, ROIs) for quick QA.
  - Capture provenance logs to track parameter changes across reconstructions.
  - Offer alternate outputs (e.g., raw projections, reconstructed volume in common formats) to facilitate reuse.

## Recommended next steps for data support

- Validate reconstruction with current parameters and confirm output dimensions and voxel spacing match expectations.
- Create a self-serve product listing this dataset with its parameter set, enabling stakeholders to reproduce or adjust parameters for similar scans.
- Document how changes to CenterOfRotation, Filtering, or Scaling impact results to aid non-specialist users in understanding trade-offs.