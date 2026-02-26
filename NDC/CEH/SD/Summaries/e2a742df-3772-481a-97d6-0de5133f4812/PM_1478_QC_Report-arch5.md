# LIDAR QUALITY CONTROL REPORT

## Introduction
- Project: Processing of LIDAR data for Devon and Cornwall as part of the South West TELLUS Project; data acquired and calibrated by the British Antarctic Survey (BAS).
- Purpose: Assist Environment Agency in final processing to produce Digital Surface Model (DSM) and Digital Terrain Model (DTM) with automated processing and minimal manual intervention.
- Outputs: DSM (surface + objects) and DTM (ground surface only); baseline used to assess height accuracy via ground truth comparisons.

## Data Processing
- Automated workflow:
  - LAS data processed in Terrascan as 1km x 1km blocks with standard 1m resolution classification macros (ground vs surface objects).
  - Secondary DTM created to retain ground points on steep slopes (coastal cliff definition later).
  - Data mosaicked in ArcView from overlapping 4x4km blocks with 50m overlap.
  - Automated no-data gap filling in the DTM; no breaklines used, which may cause triangulation artifacts.
- No manual editing:
  - Unlike standard EA LIDAR products, no manual editing was applied; potential retention of large buildings/bridges or incomplete removal of trees/cliffs.
- Vegetation impact:
  - Summer leaf-on conditions limit laser penetration, possibly leaving false ground where pulses do not reach ground.
- Cliff and coastal features:
  - Automatic cliff retrieval via the secondary DTM, merged into the DTM within 100m of OS mean sea level with a 50 cm difference threshold.
- Delivery preparation:
  - Overlapping blocks merged into regular 5x5km tiles; clipped and feathered; exported as ESRI Binary GRID, ESRI ASCII Grid, and geo-referenced JPEG.
  - DTM/DSM mosaicked into a single seamless dataset with hill-shading applied.
- Data storage and formats:
  - Data imported into an ArcGIS Geodatabase.

## Ground Control
- Validation approach:
  - DSM and DTM compared against existing LIDAR data and 74 random GPS ground truth sites.
- Documentation:
  - Appendix A: Ground truth coverage plot with site locations.
  - Appendix B: Ground truth comparison results.
- Accuracy outcome:
  - Average RMSE for the SW Tellus DTM: 0.095 m (well within the project specification of ±0.25 m).

## Data Delivery
- Deliverables:
  - DTM and DSM as 5x5 km tiles in ASCII Grid, ESRI Binary Grid, and quick-look JPEGs for each OS tile.
  - Resupplied LAS point cloud containing all LIDAR returns with classifications (ground vs surface objects; surface objects further classified by distance to ground).
- Data semantics:
  - ASCII Grid format details provided (ncols, nrows, xllcorner/xllcenter, yllcorner/yllcenter, cellsize, nodata_value).
  - ESRI Binary Grid format described as a binary equivalent of the ASCII grid for fast loading in ArcGIS.
  - LAS point cloud contains classification codes for ground and surface objects.

## Data Quality
- Overall quality:
  - Ground truth comparisons indicate data accuracy within 10 cm, exceeding the stated project target of ±25 cm.
  - Quality assessments emphasize that accuracy assessments are in non-vegetated, low-slope areas and may not reflect conditions across all survey extents.
- Key caveats:
  - Vegetation canopy can cause false ground surfaces where laser pulses do not penetrate.
  - Automated processing may leave artifacts in the DTM (e.g., large buildings/bridges) or remove features that would be retained with more intensive filtering.
- Ground truth context:
  - RMSE and potential systematic vs. random errors discussed to interpret deviations between LIDAR and ground truth measurements.

Appendices
- Appendix A: Ground Stations & Coverage Plot.
- Appendix B: Ground Truth Comparison.