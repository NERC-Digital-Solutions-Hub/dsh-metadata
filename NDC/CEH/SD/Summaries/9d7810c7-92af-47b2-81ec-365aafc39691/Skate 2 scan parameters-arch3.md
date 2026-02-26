# Skate 2 Input Configuration

- Overview
  - Configuration for Skate 2 CT tomography data acquisition and processing, covering geometry, detector setup, projection parameters, reconstruction/processing, and X-ray settings.

- Data inputs and outputs
  - InputSeparator and OutputSeparator: underscores
  - InputFolderName and OutputFolderName: Skate 2
  - RegionStartX/Y and RegionPixelsX/Y define the region of interest (0,0) with 2000x2000 pixels
  - Projections: 1080
  - InitialAngle: 109.6045 degrees
  - AngularStep: 0.3333 degrees

- Geometry and calibration
  - SrcToObject: 733.9188
  - SrcToDetector: 1173.528
  - CentreOfRotationTop/Bottom: 0
  - AutomaticCentreOfRotation: 1 (enabled)
  - AutomaticCentreOfRotationOffsetZ1/Z2: 0
  - Offsets (X/Y/Z): 0

- Voxel and region configuration
  - VoxelsX/Y/Z: 2000 each
  - VoxelSizeX/Y/Z: 0.125079 mm
  - RegionStartX/Y: 0
  - RegionPixelsX/Y: 2000

- Detector and imaging geometry
  - DetectorPixelsX/Y: 2000 each
  - DetectorPixelSizeX/Y: 0.2 mm
  - MaskRadius: 125.079 mm
  - WhiteLevel: 60000.0

- Scaling, normalization, and data processing
  - Scale: 1.32
  - Normalisation: 1.0
  - InterpolationType: 1
  - MedianFilterKernelSize: 1
  - CoefX4/CoefX3/CoefX0: values indicate a weighted pixel/region processing model; CoefX2: 0.25; CoefX1: 0.75; CoefX0: 0
  - Scaling (global): 1000.0

- Reconstruction and processing parameters
  - FilterType: 0
  - CutOffFrequency: 2.5
  - Exponent: 1.0
  - Normalisation: 1.0 (also listed under processing)

- Output settings and units
  - OutputType: 0
  - OutputUnits: /m
  - Units: mm
  - TIFFScaling: 1
  - RegionStart/RegionPixels repeated under region configuration

- X-ray source parameters
  - XraykV: 120 kV
  - XrayuA: 120 μA

- CT processing presets
  - FilterPreset: 0
  - Filter_ThicknessMM: 0.000
  - Filter_Material: None

- Operational controls
  - Shuttling: False

- Data governance and monitoring relevance (for authors of monitoring frameworks)
  - The configuration encapsulates comprehensive, machine-readable metadata for a CT workflow, including geometry, detectors, projection sampling, and processing parameters.
  - Strengths relevant to monitoring: explicit definitions of spatial/temporal sampling (projections, angles), geometry (SrcToObject, SrcToDetector, center of rotation), detector characteristics, and processing coefficients, which support reproducibility and traceability.
  - Metadata considerations for governance:
    - Consistency of units (e.g., voxel sizes in mm, detector pixel sizes) and clear naming conventions.
    - Provenance gaps: no explicit dataset origin, date, or lineage information is shown; may need to be captured alongside such configurations for full traceability.
    - Data sharing and openness: the configuration implies data and results can be produced, but there’s no explicit linkage to dataset accessible metadata or data governance standards.
    - Data quality and verification: presence of quality-related fields (e.g., WhiteLevel, CutOffFrequency) suggests potential quality controls, but no explicit QA metrics or validation hooks are defined.
  - Recommendations for authors of monitoring frameworks:
    - Encourage embedding standardized metadata schemas (e.g., dataset origin, version, date, responsible party) alongside such parameter configurations.
    - Support reproducibility by enforcing versioning and exportable configuration logs with outputs.
    - Define data provenance and governance hooks to facilitate data sharing, metadata completeness, and lineage tracking for complex imaging pipelines.