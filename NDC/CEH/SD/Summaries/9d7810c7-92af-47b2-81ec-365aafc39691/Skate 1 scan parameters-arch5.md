# Skate 1

## Overview
- CT tomography dataset configuration for Skate 1, detailing acquisition, projection, detector, processing, and output parameters.
- Aims to ensure the dataset is stored, discoverable, and usable with clear metadata and governance.

## Dataset Metadata and Structure
- Dataset identity and location
  - Name: Skate 1
  - OutputFolderName: Skate 1
  - InputFolderName: (not provided)
  - OutputType: 0
  - TIFFScaling: 1
  - Shuttling: False
- Data dimensions and resolution
  - Voxels: 2000 × 2000 × 2000
  - VoxelSize: 0.125079 mm in X, Y, Z
  - RegionStart: 0, 0
  - RegionPixels: 2000 × 2000
  - DetectorPixels: 2000 × 2000
  - DetectorPixelSize: 0.2 mm × 0.2 mm
  - DetectorOffset: 0.0, 0
  - CentreOfRotationTop/Bottom: 0.0
  - Scale: 1.32
  - OutputUnits: /m; Units: mm
- Acquisition parameters
  - Projections: 1080
  - InitialAngle: 132.173°
  - AngularStep: 0.333314° per projection
  - Xrays: 120 kV; 145 μA
  - MaskRadius: 125.079 mm
- Data quality and normalization
  - WhiteLevel: 60000.0
  - Normalisation: 1.0
  - Coefficients: X4=0, X3=0, X2=0.25, X1=0.75, X0=0
  - Filter and processing
    - FilterType: 0
    - CutOffFrequency: 2.5
    - Exponent: 1.0
    - InterpolationType: 1
    - MedianFilterKernelSize: 1
    - OutputUnits aligned with physical units; TIFFScaling: 1
    - LowPercentile: 0.2; HighPercentile: 99.8
- Processing and reconstruction settings
  - Region and scaling: RegionStart/RegionPixels as above; Scaling: 1000.0
  - AutomaticCentreOfRotation: 1 (with zero offsets)
  - CTPro: FilterPreset: 0; Filter_ThicknessMM: 0.000; Filter_Material: None
- Data integrity and provenance
  - SrcToObject: 733.92
  - SrcToDetector: 1173.528
  - OutputFolderName reflects dataset focus; InputConversion/AutoScalingType: 0

## Access, Sharing, and Update
- Storage and discovery-oriented fields
  - InputFolderName missing (potential gap for provenance)
  - OutputFolderName present; OutputType defined
  - ImportConversion: 0; AutoScalingType: 0
  - Region and projection parameters are explicitly captured, aiding reproducibility
- Data sharing considerations
  - No explicit embargo or licensing information in this extract
  - CTPro and processing parameters are documented, enabling reprocessing

## Quality, Provenance, and Governance
- Transparency of reconstruction/processing parameters
  - Detailed geometric, detector, and projection metadata
  - Processing and scaling parameters documented for reproducibility
- Potential data quality concerns
  - Incomplete input data path (InputFolderName missing)
  - Some fields are system-specific; cross-walking to standard metadata schemas recommended
- Versioning and updates
  - Clear parameterization enables re-running or updating reconstructions, but update workflows are not specified

## Challenges and Considerations for Data Stewards
- Incomplete user needs picture
  - InputFolderName missing may impede data discovery and reuse
- Data interoperability
  - Many bespoke parameters (coefficients, region definitions, scale) require mapping to standard schemas for interoperability
- Handling of large datasets
  - Very large voxel grid and projection set imply storage, transfer, and compute considerations
- Data availability and access
  - No explicit data access controls or licensing; determine embargoes, usage rights, and sharing policy

## Recommendations for Data Stewards
- Capture complete provenance
  - Populate InputFolderName; record dataset creators, creation date, and instrument details
- Strengthen metadata alignment
  - Map metadata to a standard schema (e.g., DICOM/OME-XML or data catalog schema) including units, scales, and processing history
- Clarify access and rights
  - Specify licensing, usage restrictions, and any embargo or shuttling constraints
- Implement data validation and versioning
  - Establish quality checks for critical fields (voxel sizes, projection counts, angle, detector specs)
  - Maintain versioned records of processing steps and any reprocessing
- Facilitate discoverability and reuse
  - Provide a concise data usage note, lineage, and links to raw inputs and processed outputs
  - Ensure clear, machine-readable metadata to support search and interoperability