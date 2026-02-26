# 01_Filtering_specimens_generating_FA.R

## Purpose
- Generate fluctuating asymmetry (FA) values and perform quality control (QC) on bumblebee wing landmark data.
- Process landmark data for each species by aligning left and right wings and correcting upside-down wings.

## Data inputs and outputs
- Required inputs: TPS files for all specimens; CSV file listing specimens with upside-down wings (Orientation data).
- Outputs: CSVs of Procrustes distances (wing shape FA) for each specimen under different QC cut-offs.

## Key processing steps
- Read landmark data for each species.
- Flip left wings to align with right wings; correct any upside-down wings.
- Apply QC checks:
  - Measure angular difference between wings (based on y-coordinates of landmarks 1 and 10).
  - Compare each wing to the species-wide mean wing shape after Procrustes alignment.
- Test multiple QC cut-offs to balance quality and sample retention.
- Remove low-quality specimens, perform Procrustes alignment, compute FA (Procrustes distance), and export results.

## Quality control and data curation
- Uses two QC criteria to filter data before FA calculation.
- Explores multiple cut-offs to maximize data quality while minimizing sample loss.

## Reproducibility and provenance considerations
- Clearly defines inputs and outputs, enabling reproducibility and traceability of FA calculations across species and QC conditions.

## Relationship to other scripts in the suite
- Part of a broader workflow that includes directionality assessment (02_...), repeatability analysis (03_...), temporal rarefaction (04_...), and GAM-based analysis/plotting (05_...).

## Data stewardship implications
- Highlights the importance of accurate orientation data and consistent QC criteria to ensure reliable FA estimates.
- Emphasizes documenting QC cut-offs and processing steps to support auditability and reuse by others.
- Underlines the need for standardized input formats (TPS and orientation data) and versioning of processed outputs for dataset discoverability and integration.