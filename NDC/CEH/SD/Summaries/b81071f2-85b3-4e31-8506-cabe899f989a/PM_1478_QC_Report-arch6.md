# LIDAR QUALITY CONTROL REPORT PROJECT PM_1478

## Introduction
- Relates to processing of LIDAR data for Devon and Cornwall, acquired and calibrated for the South West TELLUS Project by BAS.
- Environment Agency assisted in final processing to produce DSM (surface) and DTM (ground).
- Aim: automated processing with minimal manual interaction; assess how processing parameters affect height accuracy via ground truth comparisons.
- Report describes basic processing steps and the achieved data quality.

## Data Processing
- Automated processing of LAS data (Terrascan) in 1 km x 1 km blocks using standard 1 m resolution classification macros (ground vs surface objects).
- Generated a secondary DTM preserving ground points on steep slopes for coastal cliff definition.
- Data assembled in ArcView using modified Agency scripts; mosaicked overlapping 4x4 km blocks with 50 m overlap.
- Automated filling of small gaps in the DTM; no manual editing were applied (results reflect Terrascan outputs).
- Leaf-on summer data may obscure laser penetration through vegetation, potentially causing false ground surfaces.
- Automatic cliff retrieval: merged cliffs within 100 m of OS mean sea level when DTM and secondary DTM differed by >50 cm.
- Overlaps merged into regular 5x5 km blocks; outputs exported as ESRI Binary GRID, ESRI ASCII Grid, and geo-referenced JPEG, named by OS grid reference.
- Final products imported into an ArcGIS GeoDatabase and mosaicked into seamless DTM and DSM with hill-shading.

## Ground Control
- Compared DSM and DTM to existing LIDAR data and 74 random GPS ground truth sites.
- Appendix A provides coverage plot with ground truth locations; Appendix B shows comparison results.
- RMSE (Average across 74 random sites) = 0.095 m.

## Data Delivery
- Deliverables: Digital Terrain Model (DTM) and Digital Surface Model (DSM) as 5x5 km tiles in:
  - ASCII Grid
  - ESRI Binary Grid
  - Quick-look JPEGs for each OS tile
- LAS point cloud (full LAS dataset) also resupplied.
- ASCII Grid details: header lines (ncols, nrows, xllcorner/xllcenter, yllcorner/yllcenter, cellsize, nodata_value) and example cell values.
- ESRI Binary Grid: binary format for rapid loading in ArcGIS.
- LAS: contains all LIDAR returns with classifications (ground vs surface) and attributes.

## Data Quality
- Ground truth comparison indicates data accuracy within 10 cm; aligns with high-quality output.
- Measurements meet the project specification of +/- 25 cm.
- Limitations:
  - Vegetation presence can yield false ground surfaces where laser pulses don’t penetrate canopy.
  - Automated DTMs may retain large buildings/bridges or remove features that manual filtering would preserve.
  - Lack of manual editing means some artefacts may remain or some features may be misrepresented.

## Appendices
- Appendix A: Ground Stations & Coverage Plot (locations of independent ground truth sites).
- Appendix B: Ground Truth Comparison results.