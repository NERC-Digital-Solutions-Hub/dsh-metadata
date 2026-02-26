# XTekCT

- Purpose: A CT scan configuration for Skate 3 pt1, detailing voxel grid, imaging geometry, projection settings, and processing parameters to produce and manage CT-derived data.

## Data Model and Metadata Highlights

- Spatial and voxel information:
  - Voxel grid: 2000 × 2000 × 2000
  - Voxel size: ~0.0738 mm in X, Y, Z
  - Region of interest: RegionStartX/Y = 0; RegionPixelsX/Y = 2000
- Imaging geometry:
  - SrcToObject = 433.125
  - SrcToDetector = 1173.528
  - Centre of rotation: Top/Bottom = 0, auto-centre enabled
  - MaskRadius = 73.816
- Detector and image properties:
  - DetectorPixelsX/Y = 2000
  - DetectorPixelSizeX/Y = 0.2
  - DetectorOffsetX/Y = 0
  - WhiteLevel = 60000
- Data processing and scaling:
  - Scale = 1.32
  - Coefficients: X4=0, X3=0, X2=0.25, X1=0.75, X0=0
  - Normalisation = 1.0
  - Filter/processing: FilterType=0, CutOffFrequency≈2.5, Exponent=1.0, MedianFilterKernelSize=1
  - InterpolationType = 1
  - Output scaling/units: Scaling = 1000.0; OutputUnits=/m; Units=mm
- Projections and reconstruction:
  - Projections = 1080
  - InitialAngle = 205.514755..., AngularStep = 0.3333111849
- Data output and organization:
  - OutputType = 0; TIFFScaling = 1
  - OutputFolderName = Skate 3 pt1
  - RegionStart/RegionPixels define the processing window
- Quality controls and percentile normalization:
  - LowPercentile = 0.2; HighPercentile = 99.8
  - Shuttling = False
- Data provenance and materials:
  - [CTPro] FilterPreset = 0; Filter_ThicknessMM = 0.000; Filter_Material = None
- X-ray source settings:
  - [Xrays] XraykV = 120; XrayuA = 145

## Data Access, Discovery, and Governance

- Naming and folder conventions:
  - Output folder named Skate 3 pt1; input/output separators configurable
- Clear separation of configuration and data output to aid discoverability and reproducibility
- CT workflow parameters embedded in a single config file to support consistent processing

## Data Quality, Reproducibility, and Risk

- Reproducibility hinges on fixed parameters: voxel size, region, projection count, angles, and processing settings
- Potential risks if parameters drift without versioning or documentation (scaling, normalization, rotation centers, and projections are critical)
- Absence of explicit metadata like creator, date, and dataset version in the snippet highlights the need for richer metadata for governance

## Recommendations for Data Leaders

- Establish a metadata schema for CT configurations including dataset title, creation date, author, version, and a changelog
- Version-control configuration files and link them to dataset artifacts to support reproducibility
- Catalog CT datasets with explicit metadata fields: voxel size, region, geometry distances, projections, initial angle, angular step, processing parameters, output format, and units
- Implement data quality checks and QA gates for critical parameters (e.g., center of rotation, scaling, normalization) to ensure consistent results
- Promote discoverability by associating configuration metadata with output data in a data catalog, enabling easier reuse across projects and partners
- Define access and sharing policies for CT data and ensure proper documentation of any processing that could affect results
- Encourage cross-team collaboration to standardize CT parameter conventions and metadata across similar projects to reduce duplication and improve data stewardship