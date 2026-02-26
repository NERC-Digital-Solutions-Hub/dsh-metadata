# LIDAR QUALITY CONTROL REPORT PROJECT PM_1478

- Purpose: Processing of LIDAR data for Devon and Cornwall as part of the South West TELLUS Project to produce DSM (Digital Surface Model) and DTM (Digital Terrain Model); automated processing with minimal manual intervention; assess height accuracy via ground truth comparisons.
- Context: Data acquired and calibrated by the British Antarctic Survey; Environment Agency assisted in final processing; aim to support consistent environmental monitoring outputs.

## 2.0 Data Processing
- Automated processing of BAS-calibrated LAS data to create DSM and DTM using Terrascan in 1 km x 1 km blocks with 1 m resolution classification macros (ground vs surface objects).
- Secondary DTM produced to retain ground points on steep slopes for coastal cliffs; data mosaicked in ArcView with 50 m overlap between adjacent 4x4 km blocks.
- Automated filling of no-data gaps in DTM above a size threshold; no manual editing applied (unlike standard EA products), which may leave some buildings/bridges or remove some cliff features.
- Leaf-on summer conditions may obscure vegetation penetration, potentially causing false ground elevations.
- Automatic cliff retrieval by merging cliffs from the secondary DTM within 100 m of the OS mean sea level line when differences exceed 50 cm.
- Overlapping blocks merged (5x5 km) with smooth feathering; outputs exported as ESRI Binary GRID, ESRI ASCII Grid, and geo-referenced JPEG; mosaicked into seamless DTM and DSM with hill shading.

## 3.0 Ground Control
- DSM and DTM compared against LIDAR data and 74 random GPS ground truth sites.
- Appendix A: ground truth coverage plot; Appendix B: ground truth comparison results.
- RMSE of 0.095 (about 9.5 cm) for averaged ground truth comparisons, within expectations for the South West Tellus dataset.

## 4.0 Data Delivery
- Deliverables: 5 x 5 km tiles of DTM and DSM in ASCII Grid, ESRI Binary Grid, and quick-look JPEGs per Ordnance Survey tile; LAS point cloud provided separately.
- ASCII Grid details: header includes ncols, nrows, x/y lower-left or center coordinates, cellsize, and nodata_value (-9999 default).
- ESRI Binary Grid: binary format for quick loading in ESRI ArcGIS.
- LAS: contains all LIDAR returns with classification codes (ground vs surface objects).

## 5.0 Data Quality
- Ground truth comparisons indicate data accuracy within 10 cm, well within the project specification of ±25 cm.
- Criteria limited to vegetation-free areas with limited slope and artefacts; results may not reflect absolute heights across vegetated or highly variable terrain.
- Limitations notes:
  - Vegetation canopy can cause false ground surfaces.
  - Automated filtering may produce artefacts (e.g., leaving large buildings/bridges or removing features that a more thorough filtering would retain).
  - Summer leaf-on data constrain penetration visibility, affecting completeness in some areas.

## Appendix A – Ground Stations & Coverage Plot
- Provides the geographic coverage and locations of independent ground truth sites used for validation.

## Appendix B – Ground Truth Comparison
- Details the comparison results between LIDAR-derived surfaces (DTM/DSM) and ground truth surveys, including RMSE metrics and interpretation.