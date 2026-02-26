# UKCEH Land Cover Plus: Hedgerows (20162021) England Dataset documentation

- The dataset provides a national-scale model of woody linear features along field boundaries in England, including hedgerows, tree lines, and semi-natural shrub/tree thickets. It derives from Environment Agency lidar data collected 2016–2021 and is designed to quantify presence and height class of these features within the UKCEH Land Cover Map (LCM) framework.
- Exclusions and scope: areas excluded due to high uncertainty or lack of relevant features include mountain/moor/heath, open water, coastal zones, urban/suburban areas, and woodland. The product focuses on hedgerows and similar boundary features associated with farmed/open land boundaries rather than continuous woodland.

- Data access and licensing
  - Bespoke licensing with UKCEH Data Licensing; generally free for academic/research use.
  - Reuse must cite the dataset (with DOI) and link to the Environmental Information Data Centre record.
  - Source citations and acknowledgements provided.

- Product specification
  - Format and coverage:
    - Created as shapefile tiles (5,881 tiles of 10 km resolution; ~9.51 Gb total) aligned to the British National Grid and OS grid; downloadable as geopackage after tile combination.
    - Extent: England. Excludes woodland, urban/suburban, coastal, mountain/moor/heath lands.
  - Geometry and attributes:
    - Polylines representing woody field boundaries derived from LiDAR CHM (Canopy Height Model) data.
    - Height classes: 7 classes, minimum feature height 0.5 m; segments minimum length 2 m.
    - Attributes include: height class (hghtcls), isDouble (two parallel features), isRoadside (along roads), feature length (hlength), and a derived label (e.g., Double hedge, Probable wide single hedge, Single hedge).
    - Spatial resolution: 1 m x-y with 0.01 m vertical precision (approx. ±15 cm vertical accuracy) and 1 m horizontal resolution; CHM height classes aligned to Countryside Survey (CS).
  - Processing tiles and output structure:
    - Output produced on 5x5 km tiles, combined into 10x10 km tiles. Features may be split into segments with differing height classes; many small segments under 2 m length are removed or merged per rules.
  - Interpretation:
    - The output represents the presence and height of woody linear features tied to the LCM linear framework, not a precise georeferenced map of every hedgerow midline. There is a spatial tolerance between modeled features and other georeferenced datasets.

- Processing workflow and data provenance
  - Data sources:
    - LiDAR: Environment Agency National LiDAR Programme (2016–2021), CHM rasters supplied as 1 m resolution with leaf-off conditions.
    - Supporting data: LCM boundaries, OS DistrictMap/OpenRoad/OpenMap data for masking, and other OS open data.
  - Key processing steps:
    - Use LCM polygon boundaries as the linear framework; populate woody features from CHM values.
    - Filter CHM values below 0.5 m; reclassify into height classes compatible with CS.
    - Apply modal filtering to smooth raster data; convert CHM raster to vector polygons.
    - Field boundary filtering: remove boundaries abutting excluded land cover classes (woody woodland, urban, coastal, water bodies, etc.); apply a 50 m coastal water buffer; apply 5 m building buffer to exclude farm buildings and associated infrastructure.
    - Overlay CHM-derived features with field boundaries; retain boundaries that coincide with CHM features within a 20 m tolerance.
    - Woody feature attribution: compute 10 m and 20 m pixel counts around each CHM pixel to identify double features (parallel hedgerows) using a ratio rule; assign isDouble accordingly.
    - Roadside detection: buffer OS Open Road by 20 m and flag field boundaries with at least 75% of length within the road buffer as roadside.
    - Final attribute assignment: intersect vector CHM polygons with boundary polylines within 20 m, splitting lines into segments with consistent height class; clip to EA tiles; merge into 10x10 km tiles; delete isolated segments < 2 m; merge connected segments with identical attributes; generate label from isDouble and isRoadside.
  - Output attributes (Table 1 in the document):
    - hghtcls: height class
    - isDb: double feature indicator
    - isRd: roadside indicator
    - hlength: feature length (m)
    - label: interpreted feature type (e.g., Double hedge, Probable wide single hedge, Single hedge)
  - Example output formats:
    - Visual example: polyline features color-coded by height class
    - Attribute example: per-curve records with hghtcls, isDb, isRd, hlength, label

- Validation and limitations
  - Validation approach:
    - 38 Countryside Survey test squares (1 km2 each) surveyed in 2022; comparison of CS woody linear features against LCPHE model features, excluding certain excluded land covers.
  - Accuracy results:
    - Overall 96% agreement in total feature lengths between LCPHE and CS (across all squares).
    - Within-squares detail: mean 76% agreement in total feature lengths within 20 m buffer (range varied by square; up to ~2800% in some cases).
    - Height-class agreement: exact agreement ~32% of LCPHE length with CS WLF height class; 63% of LCPHE length within a single CS height class (allowing for height class variation over years and survey differences).
  - Model limitations:
    - Snapshot of lidar data era (2016–2021); hedgerows may have changed since capture.
    - Excludes moorland, heathland, urbanized regions, and woodland; North Yorkshire Moors area (~24x25 km) not mapped due to lack of EA lidar coverage.
    - Difficulty distinguishing tall woody boundaries from non-woody boundaries (e.g., drystone walls); misclassifications more likely in tall non-woody vegetation (nettles, reeds, bracken).
    - Manual cleaning to correct errors was not performed; users should inspect data for area-specific cleaning as needed.
    - Alignment differences with ground truth and other datasets due to generalization and digitizing/georeferencing discrepancies; model is best suited for large-scale summaries (national/regional/farm estate) rather than precise field-by-field mapping.
  - Use-case guidance:
    - Suitable for larger-scale summarization of hedgerow length by height class and for comparative analyses across England; can serve as a baseline for enhancement with field surveys for finer-scale mapping.

- Practical use for GIS specialists
  - A ready-made, height-classed, polyline-based representation of hedgerows and woody field boundaries that can be integrated with other LCM datasets and OS data.
  - Useful for map-based data products, policy briefing, landscape analysis, and ecological modeling at regional to national scales.
  - Requires awareness of spatial offset tolerance and potential misclassifications; ideal to support high-level reporting and planning rather than precise field-level feature location.

- Background and references
  - Context on hedgerows as habitats and mapping challenges; rationale for lidar-based approaches.
  - Validation methodology and Countryside Survey benchmarks.
  - Acknowledgements of funding (NERC, ASSIST, AgZero+) and data/processing facilities (JASMIN).

- Example outputs and documentation
  - Figures illustrating a sample model output area and an example attribute table accompany the dataset documentation.
  - Detailed data table and attribute definitions provided to facilitate interpretation of the polyline features.