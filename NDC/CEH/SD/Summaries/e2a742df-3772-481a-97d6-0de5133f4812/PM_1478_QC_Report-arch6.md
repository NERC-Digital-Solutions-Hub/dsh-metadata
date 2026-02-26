# LIDAR QUALITY CONTROL REPORT PROJECT: PM_1478

## Overview
- LIDAR data processing for Devon and Cornwall as part of the South West TELLUS Project to produce Digital Surface Model (DSM) and Digital Terrain Model (DTM).
- Automated processing aim: minimize manual interaction; assess potential height accuracy by comparing to ground truth surveys.
- Outputs include DSM, DTM, and associated data products for end-user access and potential further analysis.

## Data Processing Approach
- Automated processing of BAS-calibrated LAS data in Terrascan, organized in 1 km x 1 km blocks with 1 m resolution classification macros (ground vs surface objects).
- A secondary DTM retained on steep slopes for coastal cliff definition.
- Data mosaic: ArcView workflow with modified EA scripts; overlapping 4x4 km blocks with 50 m overlap; automatic gap filling in DTMs above a size threshold.
- No manual editing applied (unlike standard EA LIDAR products), which may leave large buildings/bridges or vegetation-related artifacts in the outputs.
- Cliff retrieval: automatic integration from the secondary DTM with the main DTM where within 100 m of OS mean sea level line and a 50 cm difference threshold.
- Final tiling and delivery: overlapping blocks clipped and merged using smooth feathering into regular 5x5 km tiles; outputs in ESRI Binary GRID, ESRI ASCII Grid, and geo-referenced JPEG; mosaicked into a single DSM/DTM with hill-shading.
- Data integration: Imported into an ArcGIS Geodatabase and delivered alongside resupplied LAS point cloud.

## Ground Control and Validation
- Validation against DSM/DTM and 74 random GPS ground truth sites.
- Appendix A: Ground truth coverage plot; Appendix B: Ground truth comparison results.
- Overall RMSE: 0.095 m (within the project’s < 0.15 m requirement).
- Observations: Accuracy evaluated in vegetation-free, low-slope areas; vegetation can cause false ground surfaces; automated filtering may introduce artefacts (e.g., leaving buildings/bridges in or removing cliffs) due to the lack of manual editing.

## Data Delivery and Formats
- Deliverables: 5x5 km tiles in ASCII Grid, ESRI Binary Grid, quick-look JPEGs, plus the original LAS point cloud.
- ASCII Grid: describes raster structure (ncols, nrows, xll/yll corner, cellsize, nodata); columns of Z-values with optional nodata value.
- ESRI Binary Grid: same cell values as ASCII, stored in a binary format for quick loading in ArcGIS.
- LAS Point Cloud: contains all LIDAR returns with classifications (ground vs surface objects).

## Data Quality and Limitations
- High data quality demonstrated by RMSE well below the specification and in line with reported 10 cm- to 15 cm-scale accuracy discussions.
- Limitations to consider:
  - Leaf-on (summer) data obscures laser penetration through vegetation; potential false ground where pulses do not reach the true ground.
  - Automated processing may produce artefacts in DTMs (e.g., large structures retained, vegetation not fully removed, cliffs or coastal features misrepresented) due to lack of manual editing.
  - No manual editing means some features may not be optimally filtered in this project variant.
- Overall suitability: robust for regional analyses in non-vegetated, low-slope areas; users should be aware of vegetation and artefact caveats in coastal/cliff or heavily built environments.

## Appendices (Referenced)
- Appendix A: Ground Stations & Coverage Plot
- Appendix B: Ground Truth Comparison