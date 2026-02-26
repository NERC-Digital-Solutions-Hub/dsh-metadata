# LIDAR QUALITY CONTROL REPORT PROJECT PM_1478

## Introduction
- Purpose: processing LIDAR data for Devon and Cornwall to produce Digital Surface Model (DSM) and Digital Terrain Model (DTM); assess automated processing quality against ground truth to comment on data quality.
- Context: part of the South West TELLUS Project; BAS-acquired data with Environment Agency assisting in final processing; aim for automated processing with minimal manual intervention.

## Data Processing
- Workflow: automated production of DSM and DTM from BAS-calibrated LAS data; Terrascan used in 1 km x 1 km blocks with standard 1 m resolution classification macros to separate ground and surface objects.
- Mosaic and refinement: ArcView integration with custom scripts; 50 m overlap between adjacent blocks; automated gap filling above a size threshold; no manual editing performed (compared with standard EA practice).
- Cliffs and catchments: secondary DTM retained ground points on steep slopes for coastal cliff definition; automatic cliff retrieval merged into the DTM within 100 m of OS mean sea level where differences exceeded 50 cm.
- Tiling and formats: overlapping blocks clipped and merged into 5x5 km tiles; outputs exported as ESRI Binary Grid, ESRI ASCII Grid, and geo-referenced JPEG; data mosaicked into seamless DTM and DSM with hill-shading.
- Data handling: data imported into an ArcGIS geodatabase for final integration.

## Ground Control
- Validation: DSM and DTM compared against existing LIDAR data and 74 random GPS ground truth sites.
- Documentation: Appendix A shows coverage plots; Appendix B presents ground truth comparison results.
- Quality metric: RMSE for the South West Tellus DTM averaged across 74 random sites is 0.095 m.

## Data Delivery
- Deliverables: 5x5 km tiles in ASCII Grid, ESRI Binary Grid, and quick-look JPEGs; resupplied LAS point cloud.
- File formats explained:
  - ASCII Grid: header with ncols, nrows, xllcorner/xllcenter, yllcorner/yllcenter, cellsize, nodata_value (-9999 default); grid of Z values.
  - ESRI Binary Grid: binary format containing the same cell values as ASCII Grid for fast loading in ArcGIS.
  - LAS: contains all LIDAR returns with point classifications (ground vs surface) and sub-classes based on vertical distance to the nearest ground point.

## Data Quality
- Overall accuracy: data accuracy within 10 cm in areas without vegetation and with limited slope/artifacts; aligns with project specification of ±25 cm.
- Limitations and caveats:
  - Vegetation can cause false ground surfaces due to limited laser penetration.
  - Automated filtering may leave artifacts (e.g., large buildings, bridges) or remove features that a more intensive filtering would preserve.
  - Large-scale block processing and leaf-on conditions may affect ground truth representations beyond vegetation-free, gentle-slope areas.
- Ground truth context: RMSE within the target specification indicates high quality for the validated zones; differences and biases are discussed in terms of systematic vs. random error.

## Appendices
- Appendix A: Ground Stations & Coverage Plot.
- Appendix B: Ground Truth Comparison.