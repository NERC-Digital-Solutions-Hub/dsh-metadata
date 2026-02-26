# LIDAR QUALITY CONTROL REPORT

- Project scope: Processing of LIDAR data for Devon and Cornwall as part of the South West TELLUS Project to produce DSM (Digital Surface Model) and DTM (Digital Terrain Model) with automated processing.
- Data source and aim: BAS-acquired and calibrated LIDAR data; goal to create automated DSM/DTM while enabling ground-truth-based quality assessment.
- Key outcome: Documentation of processing steps, data delivery formats, and quality metrics to support environmental monitoring and policy evaluation.

## 1. Introduction
- LIDAR data were collected and calibrated for Devon and Cornwall; Environment Agency assisted with final automated processing.
- DSM includes ground surface plus objects; DTM includes bare ground.
- Emphasis on automated processing to minimize manual intervention; ground-truth comparisons used to assess height accuracy and data quality.

## 2. Data Processing
- Automated workflow:
  - Terrascan used on BAS-calibrated LAS data in 1 km x 1 km blocks with 1 m resolution classification macros (ground vs surface objects).
  - A secondary DTM retains ground points on steep slopes for coastal cliffs definition.
  - Data transferred to ArcView with modified EA scripts; mosaic of overlapping 4x4 km blocks (50 m overlap).
  - Automated fill of data gaps in DTM above a size threshold; no additional breaklines or manual editing applied.
  - Leaf-on summer conditions may hide pulses through vegetation; potential false ground levels.
  - Cliff retrieval: cliff features merged back into the DTM within 100 m of OS mean sea level if a 50 cm difference exists between DTMs.
  - Final mosaicking into regular 5x5 km blocks with smooth feathering; export formats: ESRI Binary Grid, ESRI ASCII Grid, and geo-referenced JPEG.
  - DTM/DSM mosaiced into one seamless dataset with hill-shading; delivered in ArcGIS GeoDatabase.
- Data handling caveats:
  - No manual editing means some large buildings/bridges may remain; some trees/cliffs may be misrepresented.
  - Potential artefacts in the DTM due to automated processing (e.g., missed features or artefacts from filtering).

## 3. Ground Control
- Validation approach:
  - DSM and DTM compared against LIDAR data and 74 random GPS ground-truth sites.
  - Appendix A: Ground stations and coverage plot.
  - Appendix B: Ground truth comparison results.
- Accuracy outcome:
  - RMSE of 0.095 (within the project’s target for accuracy).

## 4. Data Delivery
- Deliverables:
  - 5 x 5 km tiles in ASCII Grid, ESRI Binary Grid, and quick-look JPEGs for each OS tile.
  - Resupplied LAS point cloud containing all LIDAR returns and attributes with classifications (ground vs surface objects).
- ASCII Grid details (summary):
  - Includes headers with ncols, nrows, xll/yll (corner or center), cellsize, and nodata_value.
- ESRI Binary Grid:
  - Binary format equivalent to ASCII grid for quick loading in ArcGIS.
- Data organization:
  - Tiles produced and named after OS grid references; seamless mosaic across the study area.

## 5. Data Quality
- Overall quality:
  - Ground-truth comparison indicates accuracy within 10 cm, exceeding the project’s stated accuracy target of +/- 25 cm.
- Limitations and considerations:
  - Assessments performed in vegetation-free, low-slope areas; not representative of absolute height everywhere.
  - Vegetation can cause false ground surfaces where laser pulses do not penetrate canopy.
  - Automated processing may leave artefacts (e.g., large buildings/bridges) or remove features (e.g., certain cliffs) that more intensive filtering would retain.
- Ground Truth context:
  - RMSE is quantified against 74 random ground-truth sites; systematic and random errors acknowledged as part of measurement processes.

## Appendices
- Appendix A: Ground Stations & Coverage Plot (shows locations and coverage).
- Appendix B: Ground Truth Comparison (detailed comparison results).