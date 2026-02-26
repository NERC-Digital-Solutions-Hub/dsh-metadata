# Skate 3 pt1

## What this document is
- A standardized configuration for acquiring and reconstructing computed tomography (CT) data, with explicit geometry, detector, processing, and output settings.
- Produces reproducible datasets (name: Skate 3 pt1) suitable for quality assurance, longitudinal monitoring, and data sharing through appropriate portals.

## Key configuration details
- Output dataset name: Skate 3 pt1
- Output folder: Skate 3 pt1
- Voxel grid: 2000 × 2000 × 2000
- Voxel size: 0.0738 mm (X, Y, Z)
- Region of interest: RegionStartX=0, RegionStartY=0, RegionPixelsX=2000, RegionPixelsY=2000
- Projections: 1080
- Initial angle: 205.5148 degrees
- Angular step: 0.3333 degrees
- Output scaling: 1000.0
- Output units: 1) OutputUnits=/m, 2) Units=mm
- Center of rotation: AutomaticCentreOfRotation enabled
- Scale factor: 1.32
- Detector: 2000 × 2000 pixels, pixel size 0.2 mm, detector offset 0
- Source-to-object distance: ~433.125
- Source-to-detector distance: ~1173.528
- Mask radius: ~73.816
- White level: 60000.0
- Shuttling: False
- Coefficients for X-space reconstruction: CoefX4=0, CoefX3=0, CoefX2=0.25, CoefX1=0.75, CoefX0=0
- Region and processing controls: FilterType=0, CutOffFrequency≈2.5, Exponent=1.0, Normalisation=1.0, InterpolationType=1, MedianFilterKernelSize=1
- TIFF/Output controls: TIFFScaling=1, OutputType=0, ImportConversion=0, AutoScalingType=0
- Percentiles for data handling: LowPercentile=0.2, HighPercentile=99.8

## Imaging and acquisition parameters
- X-ray settings: kV=120, μA=145
- Geometry: SrcToObject≈433.125, SrcToDetector≈1173.528
- Detector details: 2000 × 2000 pixels, each 0.2 mm
- Masking and rotation: Centre of rotation values present but set to 0, with automatic rotation enabled

## Processing and reconstruction specifics
- Reconstruction normalization and scaling: Normalisation=1.0, Scale=1.32
- Filtering and interpolation: FilterType=0, CutOffFrequency≈2.5, Exponent=1.0, InterpolationType=1
- Data quality and handling: Median filter size=1, Low/High percentile bounds defined for data scaling
- Miscellaneous: Region and region pixels aligned to full voxel grid, OutputUnits in meters, units in millimeters

## Data management and accessibility
- Dataset and outputs are prepared for standard storage and portal upload (OutputFolderName specified, TIFF scaling, and unit specifications)
- Clear metadata through explicit voxel, geometric, and processing parameters to support verification and reuse

## Relevance to environmental monitoring (analyst perspective)
- Demonstrates a rigorous, standardized workflow for acquiring and reconstructing 3D imaging data, enabling consistent temporal comparisons and policy-relevant assessments.
- Emphasizes reproducibility, data quality assurance, and clear metadata, facilitating data sharing and integration with other environmental datasets.
- Addresses data value and accessibility by detailing parameter transparency and dataset packaging suitable for adoption across monitoring programs.