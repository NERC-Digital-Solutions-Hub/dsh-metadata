# LIDAR QUALITY CONTROL REPORT PROJECT PM_1478

- Project scope: Processing of BAS-calibrated LIDAR data for Devon and Cornwall to produce Digital Surface Model (DSM) and Digital Terrain Model (DTM) with automated workflows and validation against ground truth.
- Objective: Deliver high-quality, automatically processed elevation products suitable for integration into GIS, with documented data processing methods and quality assessment.
- Key takeaway: Automated processing can achieve high accuracy (within 10 cm, RMSE 0.095) but carries caveats related to vegetation, automated filtering artifacts, and lack of manual editing.

## Introduction
- Data origin and purpose: LIDAR data acquired and calibrated as part of the South West TELLUS Project by BAS; Environment Agency assisted in final processing to produce DSM and DTM.
- Definitions: DSM includes ground plus above-ground features; DTM represents ground surface only.
- Processing goal: Automated processing without intensive manual interaction, with quality verification via ground truth comparisons.
- Quality framing: Height accuracy potentially affected by collection/calibration parameters; comparisons against ground truth used to comment on data quality.

## Data Processing
- Automation approach: Terrascan used to process LAS data in 1 km x 1 km blocks with standard 1 m resolution classification macros (ground vs surface objects).
- Secondary DTM: Created to retain ground points on steep slopes for coastal cliff definition.
- Mosaic and tiling: Overlapping blocks (50 m between adjacent blocks) mosaicked in ArcView using modified EA scripts and a new routine; blocks merged into regular 5 x 5 km tiles with smooth feathering.
- Gap filling: Automated routine fills no-data gaps in the DTM above a size threshold; no manual edits performed (no extra breaklines).
- Output formats: 5 x 5 km tiles exported as ESRI Binary Grid, ESRI ASCII Grid, and geo-referenced JPEG; data mosaicked into seamless DTM/DSM with hill-shading.
- Limitations: Absence of manual editing may leave residual large buildings, bridges, or trees; cliffs may be removed or false ground may appear; leaf-on conditions hinder vegetation penetration observations.

## Ground Control
- Ground truth validation: DSM and DTM compared against 74 random GPS ground truth sites; Appendix A shows coverage and ground truth locations; Appendix B provides comparison results.
- Accuracy result: RMSE of 0.095 (within stated target of less than 0.15 m); tests indicate performance in vegetation-free, low-slope areas and may not reflect absolute heights across entire survey region.
- Caveats: Vegetation can cause false ground levels; automated filtering can introduce artefacts (e.g., removing/retaining features differently than manual editing).

## Data Delivery
- Deliverables: 5 x 5 km tiles in ASCII Grid, ESRI Binary Grid, and quick-look JPEGs for each Ordnance Survey tile.
- Additional data: Resupplied LAS point cloud with classified points (ground vs surface objects) for transparency and potential reprocessing.
- Format details: ASCII Grid includes headers (ncols, nrows, xllcorner/xllcenter, yllcorner/yllcenter, cellsize, nodata_value); nodata_value defaults to -9999; LAS points carry classification codes.

## Data Quality
- Overall quality: Data accuracy within 10 cm; aligns with project specification of +/-25 cm.
- Limitations and factors: Vegetation can obscure true ground elevations leading to false ground surfaces; automated processing may produce artefacts or remove features that would be retained with manual editing.
- Ground truth context: RMSE and comparisons reflect best performance in non-vegetated, relatively flat areas; results may not generalize to all terrain types in the dataset.

## Appendices (A & B)
- Appendix A: Ground stations and coverage plot (locations of independent ground truth sites).
- Appendix B: Ground truth comparison results (detailed RMSE and comparison outcomes).