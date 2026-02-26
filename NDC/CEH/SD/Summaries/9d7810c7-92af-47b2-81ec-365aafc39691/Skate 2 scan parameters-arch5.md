# Skate 2 Input

- This document is a configuration file (XTekCT) for Skate 2 CT data processing, specifying the input geometry, projection settings, processing parameters, and X-ray imaging conditions used to generate a 3D CT dataset. It also implies subsequent data handling steps such as output formatting and potential metadata governance.

## Dataset and processing context

- 3D voxel grid: 2000 × 2000 × 2000
- Voxel sizes: X/Y/Z = 0.125079 mm
- Region of interest: RegionStartX/Y = 0; RegionPixelsX/Y = 2000
- Projection geometry: 1080 projections
- Angular configuration: InitialAngle ≈ 109.60 degrees; AngularStep ≈ 0.3333 degrees
- Detector: 2000 × 2000 pixels; DetectorPixelSize = 0.2 mm
- Center of rotation: Top and Bottom set to 0.0
- Source-to-object / source-to-detector distances provided (SrcToObject ≈ 733.92; SrcToDetector ≈ 1173.53)
- Mask and material/physics hints: MaskRadius ≈ 125.08; WhiteLevel = 60000.0; Scattering = 0.0
- Region and scaling controls: Scale = 1.32; Scaling = 1000.0; OutputUnits = /m; Units = mm
- Output type and scaling: OutputType = 0; TIFFScaling = 1; ImportConversion = 0; AutoScalingType = 0
- Percentile-based normalization: LowPercentile = 0.2; HighPercentile = 99.8

## Processing and data conditioning parameters

- Filtering and reconstruction controls:
  - FilterType, CutOffFrequency, Exponent, Normalisation
  - InterpolationType = 1
  - MedianFilterKernelSize = 1
  - CTPro section: FilterPreset = 0; Filter_ThicknessMM = 0.000; Filter_Material = None
- Data quality and reproducibility:
  - Normalisation and scaling enable reproducible outputs
  - Region and region pixel definitions ensure consistent ROI across datasets
- Data handling and provenance:
  - Shuttling = False (no data shuttle)
  - AutomaticCentreOfRotation = 1 (with offsets set to 0)
  - AutomaticCentreOfRotationOffsetZ1/2 = 0
  - OutputUnits = /m; Units = mm

## Imaging settings

- X-ray source: XraykV = 120 kV; XrayuA = 120 μA
- Other imaging parameters integrated into the configuration (e.g., Detector pixel size, WhiteLevel, Scattering, CoefX series)

## Metadata, provenance, and potential governance notes

- The file embeds a rich set of processing and geometry parameters, which support reproducibility if captured as metadata.
- However, explicit governance metadata is minimal; there is no visible authorship, date, license, version, or dataset DOI.
- The document references multiple internal sections ([XTekCT], [CTPro], [Xrays]) and a large, complex parameter set that would benefit from standardized metadata for discovery and sharing.

## Data stewardship considerations and recommendations

- Ensure descriptive metadata is added to accompany the configuration, including:
  - Dataset title, creator/owner, contact, and date of creation
  - Version and change history
  - Licensing or usage restrictions
  - Provenance details linking to raw data and processing steps
  - Mapping of each parameter to a data dictionary (types, allowed ranges, units)
- Align with a standard metadata schema suitable for imaging data (e.g., DataCite for datasets, plus domain-specific imaging metadata conventions).
- Improve interoperability by:
  - Providing explicit unit consistency notes (confirm that OutputUnits and Units remain compatible)
  - Documenting accepted data formats and file outputs (e.g., TIFF conventions)
  - Including a data dictionary that explains every parameter (e.g., what each CoefXn parameter represents in reconstruction)
- Manage dataset discoverability and sharing:
  - Record data access policies, potential embargo periods, and transfer considerations for large 3D datasets
  - Ensure the dataset is deposited in a catalog with a stable identifier and link to the parameter/configuration file
- Data quality and governance practices:
  - Maintain an immutable, versioned configuration for each dataset generation
  - Track updates to processing pipelines and their impact on outputs
  - Validate that all necessary metadata are captured before sharing or publication

## Summary

- The Skate 2 Input configuration provides comprehensive geometric, projection, and processing parameters for a large-scale CT dataset, including voxel grid, detector setup, projection details, normalization, filtering, and X-ray settings.
- For Data Stewards, the document demonstrates clear reproducibility potential but requires enriched governance metadata (authors, date, license, version, provenance) and standardized metadata to ensure discoverability, interoperability, and responsible data sharing.