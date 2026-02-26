# Skate 3 pt1

## Overview
- CT reconstruction configuration for a dataset named Skate 3 pt1.
- Voxel grid: 2000 × 2000 × 2000 with voxel size ~0.0738 mm.
- Region of interest: starts at 0,0 with 2000 × 2000 region pixels.
- Projections: 1080; Initial angle: 205.514755… degrees; Angular step: ~0.3333 degrees.
- Output units: /m; general units: mm; TIFF scaling enabled.
- Shuttling: False; Automatic Centre of Rotation enabled (with offsets = 0).
- White level: 60000.0; overall scaling and normalization parameters defined.

## Key parameters and data lineage
- Geometry and source-detector
  - SrcToObject: ~433.125; SrcToDetector: ~1173.528
  - Mask radius: ~73.816
  - Detector: 2000 × 2000 pixels; detector pixel size: 0.2 mm
  - CentreOfRotationTop/Bottom: 0.0
- Imaging and processing settings
  - X-ray: 120 kV, 145 μA
  - Filter/physics: FilterType=0; CutOffFrequency≈2.5; Exponent=1.0; Normalisation=1.0
  - Image processing: InterpolationType=1; MedianFilterKernelSize=1; Coefficients: X4=0, X3=0, X2=0.25, X1=0.75, X0=0
  - Scaling: Scale=1.32; RegionStartX=0; RegionStartY=0; RegionPixelsX=2000; RegionPixelsY=2000
  - Projections/angles: Projections=1080; InitialAngle≈205.515; AngularStep≈0.3333
- Output and data management
  - OutputType=0; TIFFScaling=1
  - ImportConversion=0; AutoScalingType=0
  - LowPercentile=0.2; HighPercentile=99.8
  - OutputUnits=/m; Units=mm
  - Coefficients and normalization indicate a published processing pipeline
- Data sections and provenance indicators
  - [XTekCT] and [CTPro] blocks imply configuration and processing presets
  - Shuttling=False; AutomaticCentreOfRotation flags present
  - Xrays section: XraykV=120; XrayuA=145

## Metadata and provenance considerations for Data Stewards
- Metadata completeness
  - Current file captures geometry, acquisition, and processing parameters, but no acquisition date, operator, instrument model, or dataset version.
  - Key provenance fields to add: datasetId, version, creation date, creator, contact, license, and references to the processing pipeline version.
- Schema and standardization
  - Ensure consistent naming (e.g., kV vs XraykV) and unit definitions across datasets.
  - Capture input/output mapping, source-to-object/detector transforms, and any calibration data used.
- Reproducibility and lineage
  - Preserve processing parameters (filters, normalization, coefficients) and the exact values used for a given reconstruction to enable full replication.
  - Record any decisions or deviations from defaults (e.g., AutoCentreOfRotation usage and offsets).
- Data quality and interoperability
  - Document any gaps or non-interoperable elements (e.g., bespoke handling for large 3D datasets).
  - Ensure that the dataset, including configuration and resulting outputs, can be ingested by standard catalogues and viewers.

## Sharing, access, and governance implications
- Data sharing readiness
  - Dataset appears ready for cataloguing but requires governance metadata (license, access controls, embargo status if any).
- Formats and storage
  - TIFF scaling indicates image outputs; confirm companion metadata files and raw/processed data versions are stored together.
- Access policy
  - Define who may view/use the dataset, version control, and any Embargo/Usage terms.

## Challenges and recommendations (aligned with Data Stewards)
- Incomplete view of user needs
  - Add a concise dataset description and intended use-case to improve discoverability.
- Timely data availability
  - Establish clear data handoff timelines and responsibilities for ingesting configuration and outputs.
- Metadata quality and standardization
  - Enforce a metadata schema across datasets to capture geometry, acquisition settings, processing steps, and provenance.
- Interoperability of formats and large data volumes
  - Plan for scalable storage and transfer strategies; document any non-standard fields or bespoke parameters to aid interoperability.
- Updating and versioning
  - Implement versioning for the configuration and outputs; track changes to parameters like angles, scaling, and processing coefficients.

## Next steps for adoption and governance
- Catalogue Skate 3 pt1 with a complete metadata record including provenance, license, and contact.
- Add missing contextual metadata (acquisition date, instrument model, operator).
- Ensure reproducibility by storing the exact configuration, processing pipeline version, and any related calibration files.
- Define access permissions and data-sharing terms; confirm embargo status if applicable.
- Align naming and units across related datasets to support interoperability and efficient discovery.