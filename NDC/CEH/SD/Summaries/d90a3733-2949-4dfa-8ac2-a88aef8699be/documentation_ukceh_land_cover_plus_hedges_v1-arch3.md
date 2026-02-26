# UKCEH Land Cover Plus: Hedgerows (20162021) England Dataset documentation

- Purpose and scope
  - Provides a national-scale model of woody linear features along field boundaries in England, including hedgerows, tree lines, and semi-natural shrub/wooded thickets.
  - Derived from Environment Agency lidar data (National LiDAR Programme) collected during 2016–2021.
  - Outputs are aligned with UKCEH Land Cover Map (LCM) frameworks and compatible with Countryside Survey height classes.
  - Not a full georeferenced map of every hedgerow; focuses on presence and height of woody features along LCM-defined parcel boundaries, with anticipated positional tolerance.

- Data and coverage
  - Extent: England; excludes woodland (continuous non-linear woody cover), urban/suburban, coastal, mountain/moor/heath, and water bodies in the primary analysis.
  - Areas excluded due to lidar coverage gaps (e.g., North Yorkshire Moors area ~24 x 25 km) and other high-uncertainty zones.
  - Height classes are designed to correspond to Countryside Survey categories.

- Data sources and processing
  - Primary data: 1 m resolution canopy height model (CHM) derived from lidar (first-return DSM minus DTM) from 2016–2021 EA National LiDAR Programme.
  - Supporting data: UKCEH LCM 2021, OS datasets (DistrictMap Vector, OpenMap, Open Road).
  - Processing environment: performed in R on the JASMIN LOTUS cluster.
  - Key processing steps:
    - Use LCM polygon boundaries as the linear framework; populate woody features from CHM where present.
    - Filter CHM values below 0.5 m; reclassify into height classes (see mappings).
    - Modal filtering and raster-to-vector conversion to create polyline features.
    - Exclude boundaries abutting excluded land cover classes; apply coastal buffer; mask out buildings and farmsteads with buffers.
    - Attribute woody features by local density (filter10 and filter20) to identify double features (parallel hedgerows) and roadside hedges.
    - Overlay CHM-derived features onto field boundaries; split lines by height classes; generate final 10 km tiles of 5 km tile collections.
    - Add interpretation labels (e.g., Double hedge, Probable wide single hedge, Single hedge) based on isDouble and isRoadside attributes.
  - Output format: UKCEH Land Cover Plus: Hedgerows (2016-2021) England model (LCPHE) in geopackage, distributed as 5,881 tiles at 10 km resolution (total ~9.51 GB).

- Product specification and attributes
  - Data are classified polylines with:
    - hghtcls: height class (7 classes, 0.5 m+ segments)
    - isDb: boolean flag for double features
    - isRd: boolean flag for roadside hedges
    - hlength: feature length in meters
    - label: interpreted feature type
  - Attribute interpretation provided (Table 1) and examples shown in outputs.
  - Resolution and accuracy:
    - Underlying lidar vertical accuracy: ±15 cm; vertical resolution 1 cm; horizontal resolution 1 m.
    - CHM height thresholds: 0.5 m minimum to classify as woody feature.
    - Spatial alignment tolerances applied during processing (e.g., 20 m intersection tolerance with field boundaries).

- Validation and accuracy
  - Validation data: 38 Countryside Survey (CS) test squares (1 km2 each) surveyed in 2022.
  - Validation metrics:
    - Total length: 96% agreement between LCPHE and CS field surveys across squares (within masked areas).
    - Per-square length: mean 76% agreement (SD ~15%), with variability across squares.
    - Height class comparison: exact agreement 32% across total LCPHE length; 63% of length within one height class of adjacent CS WLF height class (accounting for timing differences up to ~6 years and methodological differences).
  - Notes: Higher segmentation in LCPHE vs. CS; some differences due to survey timing, boundary generalization, and potential misalignment.

- Limitations and caveats
  - Snapshot in time (2016–2021 lidar data); real-world changes after capture are not reflected.
  - Exclusion of certain environments reduces misclassification but omits many features in moorland, mountain, urban, and woodland areas.
  - Difficulty distinguishing hedgerows from drystone walls or non-woody tall vegetation (nettles, reeds); misclassifications tend to be in lower height classes (1a/1b).
  - Potential inclusion of tall infrastructure as woody features; manual cleaning not performed; users should inspect area-specific data for errors.
  - Alignment between LCPHE features and ground truth can differ due to georeferencing/digitizing errors; a multi-metre tolerance should be expected.
  - Small-scale accuracy is limited; model best suited for national/regional summaries rather than precise field-level mapping.

- Data access, licensing, and usage
  - Access: Bespoke licensing conditions; license negotiation required by UKCEH Data Licensing team; generally free for academic/research purposes.
  - Citation required when reusing: Broughton et al. (2024) UKCEH Land Cover Plus: Hedgerows 2016-2021 (England). NERC EDS Environmental Information Data Centre.
  - Purpose alignment: Data designed for integration with LCM products; intended as a baseline for monitoring and policy evaluation, and for informing future decisions.
  - Governance considerations: Emphasizes data provenance, metadata quality, and updates; users should verify data suitability for their monitoring framework and consider revalidation in target areas.

- Example outputs and accessibility
  - Example figures illustrate polyline outputs and attribute tables; the model provides a tabular summary of features and height class distribution.
  - Output suitable for large-scale summaries (national/regional) and for informing hedgerow management and ecological connectivity analyses; less suitable for precise field-level demarcation without supplementary ground truth.

- Acknowledgements
  - Funded by NERC through ASSIST and AgZero+ initiatives; JASMIN data facility used; collaboration with Environment Agency and Natural England-supported projects.