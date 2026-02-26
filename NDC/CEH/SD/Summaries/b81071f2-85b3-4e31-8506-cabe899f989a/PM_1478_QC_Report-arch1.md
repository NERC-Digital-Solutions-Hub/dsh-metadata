# LIDAR QUALITY CONTROL REPORT

## Overview
- Project: PM_1478, processing of LIDAR data for Devon and Cornwall as part of the South West TELLUS Project
- Conducted by Geomatics (Environment Agency) with BAS-calibrated LAS data
- Deliverables: Digital Surface Model (DSM) and Digital Terrain Model (DTM), plus the original point cloud
- Objective: automated processing with minimal manual editing; assess height accuracy through ground truth comparisons

## Data Processing
- Automated workflow using Terrascan on 1 km x 1 km blocks with 1 m resolution classification macros to separate ground and surface objects
- Secondary DTM produced to preserve ground points on steep slopes for coastal cliffs
- Mosaic: 4 x 4 km blocks overlapped by 50 m, clipped/merged into regular 5 x 5 km blocks; feathering used for seamless tiling
- No manual editing performed (unlike standard EA LIDAR products), which may leave residual buildings/bridges or vegetation not removed; potential cliffs may be removed or not detected
- Cliff retrieval: automatic incorporation from secondary DTM within 100 m of OS mean sea level line where DTM and secondary DTM differ by > 50 cm
- Output formats: DSM and DTM delivered as 5 x 5 km tiles in ASCII Grid, ESRI Binary Grid, and quick-look JPEGs; LAS point cloud also provided
- Data integration: mosaicked into a single GeoDatabase with hill-shading applied

## Ground Control
- Validation against 74 random GPS ground truth sites
- Ground truth comparison presented in Appendix B; coverage shown in Appendix A
- Reported RMSE for the South West Tellus DTM: 0.095 m

## Data Delivery
- Deliverables:
  - DTM and DSM: 5 x 5 km tiles in ASCII Grid, ESRI Binary Grid, and quick-look JPEGs for each OS tile
  - Resupplied: Point Cloud LAS data
- ASCII Grid details: headers include ncols, nrows, xllcorner/xllcenter, yllcorner/yllcenter, cellsize, nodata_value
- ESRI Binary Grid: binary format for rapid loading in ArcGIS
- LAS: contains all LIDAR returns with classifications (ground vs surface objects)

## Data Quality
- Overall accuracy: data within 10 cm, meeting the project specification of ±25 cm
- Caveats:
  - Vegetation effects: canopy can conceal pulses, producing false ground in vegetated areas
  - Automated filtering may leave large buildings/bridges or remove cliff features that more intensive filtering would preserve
  - Leaf-on conditions (summer capture) limit penetration through vegetation, affecting true ground levels
  - No manual editing means potential artefacts or missing features in DTMs/DSMs
- Ground truth metrics:
  - RMSE target: ≤ 0.15 m (15 cm); achieved: 0.095 m
  - Systematic biases and random errors discussed as part of interpretation of comparisons

## Appendices
- Appendix A: Ground Stations & Coverage Plot
- Appendix B: Ground Truth Comparison