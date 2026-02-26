# LIDAR QUALITY CONTROL REPORT PROJECT: PM_1478

## Introduction
- Reports on processing LIDAR data for Devon and Cornwall as part of the South West TELLUS Project, produced by BAS and assisted by Environment Agency Geomatics.
- Objective: create automated DSM (surface) and DTM (ground) products; assess height accuracy via ground truth surveys.
- Data captured under summer, leaf-on conditions; potential vegetation-related limitations acknowledged.

## Data Processing
- Automated processing of BAS-calibrated LAS data into DSM and DTM using Terrascan in 1 km x 1 km blocks with standard 1 m resolution classification macros (ground vs surface objects).
- A secondary DTM retaining ground points on steep slopes used later for coastal cliff definition.
- Data moved into ArcView with modified Environment Agency scripts; mosaicked overlapping 4 km x 4 km blocks with 50 m overlap.
- Automated no-data gap filling in the DTM (no breaklines used), which may cause triangulation artifacts.
- No manual editing applied (unlike standard EA LIDAR products); potential residuals include large buildings/bridges, incomplete removal of some trees, and some cliffs removed that should remain.
- Automatic cliff retrieval from the secondary DTM merged back into the DTM within 100 m of the Ordnance Survey mean sea level line, with a 50 cm difference threshold.
- Overlaps clipped and merged into regular 5 x 5 km blocks; feathered edges; exports in ESRI Binary Grid, ESRI ASCII Grid, and geo-referenced JPEG; files named by OS grid reference.
- Data assembled into a seamless DSM and DTM with hill-shading in an ArcGIS GeoDatabase.

## Ground Control
- DSM and DTM compared against 74 random GPS ground truth sites.
- Appendix A provides coverage plots; Appendix B shows ground truth comparison.
- Reported RMSE for ground truth comparison: 0.095 m.

## Data Delivery
- Products delivered as 5 x 5 km tiles in:
  - ASCII Grid (human-readable raster with header including ncols, nrows, xll/x yll/x, cellsize, nodata_value).
  - ESRI Binary Grid (fast-loading ESRI format).
  - Quick-look JPEGs for each Ordnance Survey tile.
- LAS point cloud of all LIDAR returns and their attributes also supplied.
- Summary of ASCII Grid format included to aid transfer between applications.

## Data Quality
- Overall accuracy: data accuracy within 10 cm, surpassing the project’s target of ±25 cm.
- Limitations and caveats:
  - Accuracy assessments are in vegetation-free, low-slope areas with minimal surface artefacts; not indicative of absolute height across the entire survey.
  - Vegetation can cause false ground surfaces where laser pulses do not penetrate canopy.
  - Automated routines may leave artefacts (e.g., large buildings/bridges) or remove features (e.g., cliffs) that a more intensive filtering process would preserve.
  - Leaf-on conditions reduce pulse penetration, affecting ground determination in forested regions.
  - Cliff retrieval relies on secondary DTM and proximity to sea-level reference; results may be uncertain near coastal features.
  - No manual editing means some features may be misclassified or omitted.

## Appendices (References)
- Appendix A: Ground Stations & Coverage Plot (locations of independent ground truth sites).
- Appendix B: Ground Truth Comparison (detailed comparison results).