# LIDAR QUALITY CONTROL REPORT PROJECT PM_1478 Processing of LIDAR data for the South West TELLUS Project Integrated spatial solutions

- Aims to process BAS-calibrated LIDAR data for Devon and Cornwall to produce automated DSM (Digital Surface Model) and DTM (Digital Terrain Model) products for GIS use.
- Assesses height accuracy by comparing LIDAR-derived surfaces against ground truth surveys.

## 1.0 Introduction
- Data scope: Devon and Cornwall LIDAR data collected for the South West TELLUS Project; Environment Agency assisted in final processing.
- Products: DSM (surface + objects) and DTM (bare ground).
- Processing goal: Automated workflow with minimal manual intervention; evaluate potential height accuracy impacts due to collection/calibration parameters.

## 2.0 Data Processing
- Processing workflow:
  - Use Terrascan to process BAS-calibrated LAS data in 1 km x 1 km blocks.
  - Apply standard 1 m resolution classification macros to separate ground points from surface objects.
  - Create a secondary DTM to capture ground on steep slopes, useful for coastal cliffs.
  - Import into ArcView with modified EA scripts; mosaic overlapping 4x4 km blocks with 50 m overlap.
  - Automated gap filling in the DTM for gaps above a size threshold; no manual editing performed.
  - Automated cliff retrieval by merging coastal cliff features within 100 m of OS mean sea level line where DTM-Secondary DTM difference > 50 cm.
  - Merge overlapping blocks into regular 5x5 km blocks with smooth feathering; export in ESRI Binary Grid, ESRI ASCII Grid, and georeferenced JPEG; name by OS grid reference.
  - Import into ArcGIS GeoDatabase and mosaic into seamless DTM and DSM with hill-shading.
- Notes on data handling:
  - No manual editing means some large buildings/bridges may remain; some trees may not be removed; some cliffs may be removed.
  - Summer (leaf-on) capture limits canopy penetration visibility, potentially causing false ground values.
  - Cliff retrieval relies on thresholding with the secondary DTM near the mean sea level line.
  - Data delivery includes both raster products and the original LAS point cloud.

## 3.0 Ground Control
- Validation approach: Compare DSM/DTM against existing LIDAR data and 74 random GPS ground truth sites.
- Deliverables referenced in appendices:
  - Appendix A: Ground stations & coverage plot.
  - Appendix B: Ground truth comparison results.
- Quality result: Average RMSE of 0.095 m for the ground truth comparison (within the project’s stated requirements).

## 4.0 Data Delivery
- Deliverables:
  - 5 x 5 km tiles of DTM and DSM in:
    - ASCII Grid
    - ESRI Binary Grid
    - Quick-look JPEGs (for each Ordnance Survey tile)
  - The resupplied LAS point cloud containing all LIDAR returns with classifications (ground vs surface objects).
- Data formats explained:
  - ASCII Grid: header keywords (ncols, nrows, xllcorner/xllcenter, yllcorner/yllcenter, cellsize, nodata_value) and grid of Z values.
  - ESRI Binary Grid: binary format compatible with ArcGIS for fast loading.
  - LAS: standardized point cloud with classification codes.

## 5.0 Data Quality
- Overall accuracy: Data are within 10 cm of ground truth surveys and within the project specification of +/- 25 cm.
- Limitations and caveats:
  - Vegetation canopy can cause false ground surfaces due to limited laser penetration.
  - Automated filtering may produce artefacts in the DTM (e.g., residual buildings/bridges) or remove features that a more thorough filtering would retain.
- Ground truth metrics:
  - RMSE target: less than 0.15 m (15 cm) as per project specification; reported RMSE = 0.095 m.
  - Distinguishes systematic biases from random errors in ground truth comparisons.

## Appendices
- Appendix A: Ground Stations & Coverage Plot.
- Appendix B: Ground Truth Comparison.