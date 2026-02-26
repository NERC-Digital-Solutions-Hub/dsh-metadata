# Skate 2

- Overview
  - A configuration file for a Skate 2 CT dataset, detailing voxel/grid setup, projection geometry, detector and X-ray parameters, processing options, and output settings to enable reconstruction and data exploration.

- Key parameters
  - Geometry and grid
    - Voxel grid: 2000 × 2000 × 2000 voxels
    - Voxel size: 0.125079 mm (X/Y/Z)
    - Region: RegionStartX/Y = 0; RegionPixelsX/Y = 2000
    - Detector grid: 2000 × 2000 pixels; DetectorPixelSize = 0.2 mm
    - Center of rotation: AutomaticCentreOfRotation = 1; offsets effectively 0
    - CentreOfRotationTop/Bottom = 0.0
    - SrcToObject ≈ 733.92; SrcToDetector ≈ 1173.53
  - Imaging and data attributes
    - WhiteLevel = 60000.0; Scattering = 0.0
    - Scale = 1.32; Scaling = 1000.0; OutputUnits = /m; Units = mm
    - LowPercentile = 0.2; HighPercentile = 99.8
    - Region and interpolation: InterpolationType = 1; MedianFilterKernelSize = 1
  - Projections and angles
    - Projections = 1080
    - InitialAngle = 109.604499816895 degrees
    - AngularStep = 0.333313160526336 degrees
  - Processing and normalization
    - Normalisation = 1.0
    - Filter/denoising: FilterType = 0; CutOffFrequency = 2.4999999627471; Exponent = 1.0
    - Coefficient settings: CoefX4 = 0; CoefX3 = 0; CoefX2 = 0.25; CoefX1 = 0.75; CoefX0 = 0
    - CTPro: FilterPreset = 0; Filter_ThicknessMM = 0.000; Filter_Material = None
  - Output and formats
    - OutputType = 0
    - TIFFScaling = 1
    - OutputUnits = /m
    - Shuttling = False
  - X-ray source
    - XraykV = 120 kV; XrayuA = 120 μA

- Data interpretation and use
  - Purpose: configure CT data acquisition/processing for reconstruction and subsequent exploration (self-serve access via dashboards or reports).
  - Outputs: prepared for conversion to 3D volumes or slices, with scaling and unit consistency, and TIFF-based outputs where applicable.
  - Reproducibility: explicit initial angle, angular step, and region settings to reproduce the scan and reconstruction pipeline.

- Practical considerations for data support
  - Alignment and center-of-rotation
    - Automatic CO R with zero offsets requires validation against actual hardware alignment to ensure accurate reconstruction.
  - Data quality and consistency
    - Wide dynamic range (WhiteLevel) and percentile bounds suggest careful normalization to avoid saturation and improve contrast in downstream visualization.
  - Output accessibility
    - TIFF scaling and unit choices should align with downstream analysis tools; confirm compatibility with target dashboards or viewers.
  - Parameter visibility
    - All critical parameters (geometry, detector, exposure, processing) are explicit, enabling researchers to reproduce or modify the pipeline for related datasets.
  
- Next steps for data support
  - Validate the dataset against the configuration (geometry matches hardware, projections count matches frames).
  - Produce sample reconstructions and verify with known phantoms or reference slices.
  - Create self-serve views (dashboards or pivoted views) to allow end users to explore slices, volumes, and derived metrics.
  - Document any deviations from the configuration (e.g., real CO R offsets or different scaling) and adjust the data products accordingly.