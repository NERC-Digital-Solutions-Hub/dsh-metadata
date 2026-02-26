# LIDAR QUALITY CONTROL REPORT PROJECT: PM_1478

## 1. Introduction
- Purpose: Process LIDAR data for Devon and Cornwall (South West TELLUS Project) to produce a Digital Surface Model (DSM) and Digital Terrain Model (DTM).
- Data origin: BAS-calibrated LIDAR data; Environment Agency assisted in final automated processing.
- Goal: Automated processing with minimal manual editing; assess how collection/calibration parameters affect height accuracy.
- Quality check: Ground truth surveys used to evaluate data quality and comment on data accuracy.

## 2. Data Processing
- Software and workflow: Automated processing using Terrascan to classify LAS point clouds into ground and surface objects; ArcView used for mosaicking and delivery.
- Block structure: Processing in 1 km × 1 km blocks with standard 1 m resolution classification macros; 50 m overlap between adjacent blocks.
- DTM and DSM: Generated from BAS-calibrated points; a secondary DTM retained ground points on steep slopes for coastal cliffs.
- Manual editing: No manual editing was performed (unlike standard EA practices), potentially leaving large buildings/bridges or removing cliffs that should remain.
- Cliff handling: Automatic cliff retrieval from the secondary DTM merged back into the primary DTM within 100 m of the OS mean sea level line when differences exceeded 50 cm.
- Block mosaicking: Overlapping 4 × 4 km blocks clipped and merged into regular 5 × 5 km blocks with smooth feathering; outputs exported as ESRI Binary Grid, ESRI ASCII Grid, and georeferenced JPEG; mosaicked into seamless DTM and DSM with hill-shading.
- Data handling: Data imported into an ArcGIS geodatabase for final delivery.

## 3. Ground Control
- Ground truth: Compared DSM/DTM against 74 random GPS ground truth sites.
- Coverage: Appendix A provides coverage locations; Appendix B presents ground truth comparisons.
- Result: RMSE of 0.095 (well within the target ±0.15 m specification).

## 4. Data Delivery
- Deliverables: DSM and DTM as 5 × 5 km tiles in ASCII Grid, ESRI Binary Grid, and quick-look JPEGs for each OS tile.
- Additional data: Resupplied the Point Cloud LAS data.
- File formats details:
  - ASCII Grid: header includes ncols, nrows, xllcorner/xllcenter, yllcorner/yllcenter, cellsize, nodata_value (default -9999).
  - ESRI Binary Grid: binary representation of the same raster values for rapid loading in ArcGIS.
  - LAS: contains all LIDAR returns with classification codes (ground vs surface objects, with surface objects further classified by height relative to ground).

## 5. Data Quality
- Overall accuracy: Data accuracy within 10 cm, exceeding the project’s stated accuracy of ±25 cm.
- Limitations and caveats:
  - Vegetation: leaf-on conditions can obscure pulses and cause false ground surfaces where vegetation blocks penetration.
  - Automated processing artefacts: Potential for residual artefacts such as leftover buildings/bridges or removal of features that would be retained with more filtering.
  - Height reliability: Results reflect areas with no vegetation and gentle slopes; may not represent absolute heights across all terrain.
- Ground truth context: RMSE target is less than 0.15 m; achieved 0.095 m in the validated areas.

Appendices
- Appendix A: Ground Stations & Coverage Plot.
- Appendix B: Ground Truth Comparison.