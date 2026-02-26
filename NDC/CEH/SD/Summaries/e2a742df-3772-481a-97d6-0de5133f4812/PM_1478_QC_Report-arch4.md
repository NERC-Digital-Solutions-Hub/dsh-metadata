# LIDAR QUALITY CONTROL REPORT PROJECT PM_1478

## 1.0 Introduction
- Report on processing of LIDAR data for Devon and Cornwall as part of the South West TELLUS Project.
- Purpose: produce automated DSM (surface including objects) and DTM (ground surface) with minimal manual editing.
- Data were acquired and calibrated by BAS; Environment Agency aided final processing.
- Ground truth surveys used to assess height accuracy; aim to comment on data quality and processing impact.

## 2.0 Data Processing
- Automated processing to generate DSM and DTM from BAS-calibrated point cloud.
- LAS data processed in Terrascan as 1 km x 1 km blocks; 1 m resolution classification macros separate ground vs. surface objects.
- Secondary DTM produced to help define coastal cliffs on steep slopes.
- Mosaicking: ArcView with modified EA scripts; overlapping 50 m between adjacent 4 km x 4 km blocks; blocks clipped/feathered into regular 5 km x 5 km tiles.
- Automated DTM gap-filling; no manual editing (unlike standard EA processes). Risks: potential retention of large buildings/bridges, unremoved tree stands, removal of some cliffs.
- Leaf-on conditions may obscure non-penetrating pulses, leading to false ground.
- Automatic cliff retrieval by merging secondary DTM with DTM near OS mean sea level within 100 m where differences exceed 0.5 m.
- Outputs exported as 5 x 5 km tiles in ESRI GRID, ESRI ASCII Grid, and geo-referenced JPEG; mosaicked into seamless DTM and DSM with hill-shading.
- Ground truth used to validate automated outputs.

## 3.0 Ground Control
- DSM/DTM compared against existing LIDAR data and 74 random GPS ground truth sites.
- Appendix A: coverage plot with ground truth locations; Appendix B: ground truth comparisons.
- Reported RMSE for the South West Tellus DTM: 0.095 (units not stated, typically meters).

## 4.0 Data Delivery
- Products delivered as 5 x 5 km tiles in:
  - ASCII Grid
  - ESRI Binary Grid
  - Quick-look JPEGs for each Ordnance Survey tile
- Point Cloud LAS data re-supplied, including per-point classifications (ground vs. surface objects).
- ASCII Grid format: header includes ncols, nrows, xll/xllcorner, yll/yllcorner, cellsize, nodata_value.
- LAS data: retains classification codes; supports ground and surface object differentiation.

## 5.0 Data Quality
- Ground truth comparisons show data accuracy within 10 cm; within project spec of ±25 cm.
- Assessments conducted in areas without vegetation, with limited slope and artefacts; not representative of absolute height across all terrain.
- Key quality considerations:
  - Vegetation can create false ground surfaces where laser pulses don’t penetrate canopy.
  - Automated DTM can retain undesired artefacts (e.g., large buildings, bridges) or remove features that a more intensive filter would preserve.
- Ground Truth Comparison notes: RMSE target of <15 cm achieved at the 74 ground truth sites; indicates high quality within tested zones.

Appendices (not detailed in the main text):
- Appendix A: Ground stations & coverage plot.
- Appendix B: Ground truth comparison results.