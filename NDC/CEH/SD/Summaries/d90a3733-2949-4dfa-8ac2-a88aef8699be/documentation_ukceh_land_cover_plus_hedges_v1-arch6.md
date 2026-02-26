UKCEH Land Cover Plus: Hedgerows (20162021) England Dataset documentation

## Summary
- A national-scale model of the extent and height class of woody linear features along field boundaries in England (hedgerows, tree lines, semi-natural shrub/wooded thickets).
- Derived from Environment Agency lidar (National LiDAR Programme) data collected 2016–2021.
- Excludes mountain/moor/heath, open water, coastal zone, urban/suburban areas, and woodland (continuous non-linear woody cover).
- Validated against 38 Countryside Survey test squares (1 km2 each) in 2022, showing:
  - 96% agreement in total woody feature lengths at summary scale.
  - Average 76% agreement within a 20 m buffer for individual squares.
  - Height-class exact agreement for 32% of length and 63% within one class.
- Outputs represent presence and height of woody linear features associated with the Land Cover Map (LCM) linear framework, not a precise georeferenced hedge map.
- Data licensing is bespoke; generally free for academic/research use with citation.

## Data access and licensing
- Bespoke licensing; license typically negotiated by UKCEH Data Licensing team; generally free for academic and research purposes.
- Reuse requires citation: Broughton et al. (2024) NERC EDS Environmental Information Data Centre dataset.
- Further information and access via the provided DOIs.

## Background
- Hedgerows and linear woody features are important but challenging to map at large scales.
- Lidar enables three-dimensional assessment but historically limited by extent/resolution; EA lidar coverage enables nationwide scope for England.
- Output aligns with LCM linear boundary framework and is designed for interoperability with UKCEH data products and Countryside Survey height classes.

## Product specification
- Format and coverage:
  - 5,881 tiles of 10 km resolution (total ~9.51 GB) in shapefile format; provided as a combined geopackage.
  - Aligned to British National Grid and OS grid; classified polylines derived from 1 m lidar CHM data (height classes).
  - 7 height classes (minimum 0.5 m) for segments ≥ 2 m long.
  - Attributes include length (metres) and feature type (e.g., double hedge, single hedge).
  - Vertical accuracy about ±15 cm; vertical resolution 1 cm; horizontal resolution 1 m.
  - Extent: England; exclusions apply to woodland, urban/suburban, coastal, mountain/moor/heath.
- Data are tied to lidar-derived CHM values and the LCM linear framework for field boundaries.

## Processing environment and source data
- Processing performed in R on the LOTUS batch computing cluster (JASMIN facility).
- CHM data: 1 m resolution (ground and canopy height), leaf-off season; pre-processed by Environment Agency (DSM minus DTM).
- Supporting data: LCM 2021 (land parcels), OS DistrictMap/OpenMap/Open Road for masking.
- Output assembled on 5 km tiles, then merged into 10 km tiles.

## Data processing
- Start from LCM polygon boundaries as the linear framework; fill woody features from CHM where present.
- Height filtering and classification:
  - Remove CHM values < 0.5 m.
  - Reclassify to Countryside Survey-compatible height classes (CS equivalents listed below).
- Smoothing: apply modal filter (11-pixel width) to produce raster clumps; reclass small adjacent clumps to larger ones; convert CHM raster to vectors.
- Boundary filtering: exclude field boundaries abutting excluded land covers (woodland, urban, coastal, water bodies, etc.); apply a coastal 50 m buffer and a 5 m buffer around buildings; retain boundaries within 20 m of CHM features (requiring 0.9 length overlap).
- Woody feature attribution:
  - Compute local pixel counts within 10 m and 20 m radii to derive a ratio raster (filter20/filter10).
  - Ratios 2.5–4 indicate double features (e.g., parallel hedgerows); assign isDouble accordingly.
  - Buffer field boundaries by 15 m and assign isDouble/isRoadside; road proximity uses 20 m buffer and 0.75 length overlap with OS Open Road to flag roadside hedges.
- Final attribute assignment:
  - Intersect CHM-based polygons with field boundary polylines within 20 m; split line segments by height class; clip to EA 5 km tiles and merge into 10 km tiles.
  - Remove very short segments and merge contiguous segments with identical attributes; generate a label from isDouble/isRoadside values (e.g., Double hedge, Probable wide single hedge, Single hedge).
  - Output attributes table (Table 1 in the document).

## Filtering field boundaries
- Excluded land cover classes to minimize misclassification (e.g., drystone walls) and a coastal buffer to avoid coastal topography.
- 0.9 of a boundary length within 20 m of CHM features required for retention.
- Buildings masked with 5 m buffer; farmsteads excluded via OS data unless already in LCM classes.

## Attributing woody feature types
- Double features identified by ratio of surrounding CHM pixel counts (2.5–4 range): labeled as isDouble.
- Roadside hedges identified via alignment with road network (0.75 length overlap within 20 m road buffer): labeled as isRoadside.

## Final steps
- Intersections and attribute propagation; creation of segment-level height classes; tile clipping and merging into 10 km tiles.
- Segment cleaning and consolidation; label generation; full attribute set described in Table 1.

## Validation
- 38 Countryside Survey test squares assessed in 2022 using CS standard methods.
- Comparisons:
  - Total length: 96% agreement between LCPHE and CS data across squares.
  - Within 20 m buffer: mean 76% agreement per square (SD ~15%).
  - Height class comparison: exact agreement 32%; within one class 63%.
- Ground-truthing differences attributed to timing, surveyor variability, and model granularity.

## Model limitations
- Snapshot limited to 2016–2021 lidar data; hedgerows may have changed since.
- Exclusion zones apply to moorland, heathland, urban areas, and woodland; ~ North Yorkshire Moors area (~24x25 km) not mapped due to EA lidar gaps.
- Difficult to distinguish woody linear features from non-woody or tall non-woody vegetation (e.g., nettles, reeds); misclassifications typically in lower height classes (≤1.5 m).
- Potential misalignment with ground truth due to georeferencing and digitizing variances; hedgerow midlines may not coincide with mapped field boundaries.
- Best used for large-scale summaries (national/ regional/ farm-estate) rather than precise field-level mapping; can serve as a baseline for enhancements with field surveys.

## Example output
- Illustrative figures show color-coded height classes along field boundaries and an attribute table detailing each polyline feature’s characteristics.

## Acknowledgements and funding
- Funded by NERC (ASSIST and AgZero+) with collaborative support from BBSRC; JASMIN data analysis facility used.
- Hedgerow data collection supported by Natural England; significant contributions from Environment Agency and OS data sources.

## References
- Key references to prior work on hedgerows, remote sensing applications, and Countryside Survey methodology are provided.