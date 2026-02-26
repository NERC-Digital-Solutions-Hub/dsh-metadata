# LIDAR QUALITY CONTROL REPORT PROJECT PM_1478

## Introduction
- Reports on processing of LIDAR data for Devon and Cornwall as part of the South West TELLUS Project.
- Objective: produce Digital Surface Model (DSM) and Digital Terrain Model (DTM) from BAS-calibrated point cloud; aim for automated processing with minimal manual interaction.
- Validation conducted by comparing against ground truth surveys to assess height accuracy.

## Data Processing
- Automated processing pipeline:
  - Terrascan used in 1 km x 1 km blocks with standard 1 m resolution classification macros to separate ground points from surface objects.
  - A secondary DTM retaining ground points on steep slopes used for coastal cliff definition.
  - Data moved to ArcView with modified EA scripts; mosaicked overlapping 4x4 km blocks with 50 m overlap.
  - Automated gap filling in the DTM above a size threshold; no manual editing performed (risks including large buildings/bridges remaining or cliffs being removed).
  - Cliff retrieval via merging into DTM cliffs within 100 m of the Ordnance Survey mean sea level line where differences exceed 50 cm.
  - Overlaps merged into regular 5x5 km blocks, exported as ESRI Binary Grid, ESRI ASCII Grid, and geo-referenced JPEG; mosaicked into seamless DTM and DSM with hill-shading.

## Ground Control & Validation
- Ground truth validation used 74 random GPS sites; Appendix A shows coverage and independent site locations; Appendix B provides LIDAR vs ground truth comparisons.
- RMSE for the South West Tellus DTM: 0.095 m, indicating high accuracy.
- Accuracy claims are in areas with no vegetation and gentle slopes; results may not reflect absolute heights across all terrain types.

## Data Delivery & Formats
- Final products delivered as 5x5 km tiles in:
  - ASCII Grid
  - ESRI Binary Grid
  - Quick-look JPEGs for each Ordnance Survey tile
- LAS point cloud data re-supplied, with classification codes for ground vs surface objects.

## Data Quality & Considerations
- Overall data accuracy reported as within 10 cm in ground-truth comparisons; within project specification of ±25 cm.
- Key caveats:
  - Vegetation can cause false ground surfaces due to limited laser penetration (leaf-on conditions during capture).
  - Automated processing can leave artefacts (e.g., large buildings, bridges) or remove features (e.g., cliffs) that a more intensive filtering would retain.
  - Cliff features are derived via a secondary DTM and proximity-based merging, which may introduce uncertainties.
- Governance/metadata notes:
  - Emphasis on automated, reproducible processing; lack of manual editing affects feature retention.
  - Data formats are documented and data (LAS) re-supplied to support transparency and reuse.