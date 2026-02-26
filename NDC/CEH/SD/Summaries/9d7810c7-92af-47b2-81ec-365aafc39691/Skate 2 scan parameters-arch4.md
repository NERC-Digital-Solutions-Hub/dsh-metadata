# Skate 2 CT Configuration

- Overview
  - Configuration for a Skate 2 CT imaging dataset, detailing voxel grid, detector setup, projection parameters, and X-ray imaging settings. Encapsulated in sections [XTekCT], [CTPro], and [Xrays].

- Data assets and structure
  - Dataset name: Skate 2
  - Voxel grid: 2000 × 2000 × 2000
  - Voxel sizes: X/Y/Z = 0.125079 mm
  - Region of interest: RegionStartX/Y = 0; RegionPixelsX/Y = 2000
  - Source-to-object / Source-to-detector distances: SrcToObject ≈ 733.92; SrcToDetector ≈ 1173.53
  - Detector: 2000 × 2000 pixels; detector pixel size = 0.2 × 0.2 mm
  - Center of rotation: Top/Bottom = 0.0; AutomaticCentreOfRotation = 1
  - White level: 60000.0; MaskRadius: 125.079 mm
  - Scaling: Scale = 1.32; OutputScale = 1000.0
  - Coefficients: CoefX4=0, CoefX3=0, CoefX2=0.25, CoefX1=0.75, CoefX0=0
  - Region and sampling: RegionStartX/Y = 0; RegionPixelsX/Y = 2000

- Acquisition and projection parameters
  - Projections: 1080
  - Initial angle: 109.604499816895 degrees
  - Angular step: 0.333313160526336 degrees
  - Filter and normalization: FilterType=0; CutOffFrequency=2.4999999627471; Exponent=1.0; Normalisation=1.0
  - Interpolation: Type=1; MedianFilterKernelSize=1

- Data processing and output
  - Output: OutputType=0; TIFFScaling=1; OutputUnits=/m; Units=mm
  - Data handling: ImportConversion=0; AutoScalingType=0; LowPercentile=0.2; HighPercentile=99.8
  - Shuttling: False
  - Region and scaling: RegionStartX/Y = 0; RegionPixelsX/Y = 2000

- CT processing configuration
  - [CTPro]: FilterPreset=0; Filter_ThicknessMM=0.000; Filter_Material=None

- X-ray source settings
  - [Xrays]: XraykV=120; XrayuA=120
  - Repeated under [Xrays] and within [XTekCT] block, indicating consistent kV and current settings

- Data governance and provenance considerations (inferred)
  - All critical acquisition and processing parameters are explicitly captured, enabling reproducibility of the CT configuration.
  - The configuration is organized into dedicated sections for acquisition, processing, and X-ray settings, aiding traceability.

- Key considerations for Data Leaders
  - Reproducibility: The detailed parameterization supports exact replication of scans and reconstructions.
  - Metadata completeness: Extensive numeric metadata is present; formalize into a metadata schema for discovery and cataloging.
  - Discoverability and standardization: Consider mapping fields to a standardized data dictionary to improve discoverability across systems.
  - Data quality and provenance: Capture changes over time (versioning) and link to raw data, processed outputs, and processing steps for full lineage.
  - Access and governance: Ensure appropriate access controls for raw and processed data and maintain records of processing configurations to meet data governance requirements.