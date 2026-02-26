# UKCEH Land Cover Plus: Hedgerows (20162021) England Dataset documentation

## Overview
- A national-scale model of the extent and height class of woody linear features along field boundaries in England (hedgerows, tree lines, sem-natural shrub/treed thickets).
- Derived from Environment Agency lidar data collected 2016–2021 (National Lidar Programme).
- Excludes mountain/moor/heath, open water, coastal zone, urban/suburban areas, and woodland; focuses on hedgerows and similar features along farmed/open land boundaries.
- Validated against ground-truth data from Countryside Survey methods (38 test squares, 1 km2 each, surveyed in 2022).
- High overall agreement at summary scale (96% for total woody feature lengths) and reasonable per-square agreement (mean 76% within 20 m), with height-class agreement nuanced (32% exact, 63% within one class).

## What is included
- A national-scale model of woody linear field-boundary features with length and height-class attributes.
- Output aligned with UKCEH Land Cover Map (LCM) linear framework and compatible with Countryside Survey height-class schemes.
- Not a precise, field-accurate map of each hedgerow midline; position may shift relative to ground features due to framework generalization and mapping tolerances.
- Data product: 5,881 tiles of 10 km resolution (combined into 10x10 km tiles for delivery), in geopackage format; originally provided as 5 km tiles for processing.

## Data Product Specifications
- Classification: polylines representing woody features, binned into 7 height classes (minimum height 0.5 m) for segments ≥ 2 m long.
- Attributes per feature: height class (hghtcls), isDouble (two parallel features), isRd (roadside feature), hlength (length in metres), label (interpretation of feature type).
- Height classes mapped to Countryside Survey scheme:
  - 0.50–0.99 m = 1a
  - 1.00–1.49 m = 1b
  - 1.50–1.99 m = 1c
  - 2.00–2.99 m = 2
  - 3.00–3.99 m = 3
  - 4.00–5.99 m = 4
  - 6.00 m and above = 6
- Vertical accuracy about ±15 cm; horizontal resolution ~1 m; CHM vertical resolution 1 cm.
- Extent: England; exclusions apply for woodland, urban/suburban, coastal, mountain/moor/heath.

## Processing and Methodology
- Environment: processing in R on the LOTUS batch computing cluster (JASMIN).
- Input data: Canopy Height Model (CHM) derived from EA National Lidar Programme (first-return DSM minus DTM) at 1 m resolution; leaf-off data (autumn/winter).
- Supporting datasets: LCM 2021 for masking; OS Open data (DistrictMap Vector, OpenMap, Open Road).
- Processing steps (high-level):
  - Use LCM polygon boundaries as the linear framework; populate woody features from CHM where present.
  - Filter CHM values to remove sub-0.5 m values; reclassify to height classes compatible with CS.
  - Apply modal filtering to smooth raster, then convert CHM to vector polygons.
  - Exclude field boundaries abutting excluded land covers (woodland, urban, mountain/moor/heath, coastal/water) and apply a coastal buffer (50 m), plus a 5 m buffer around buildings.
  - Retain field boundaries that coincide with CHM features within 20 m and within 0.9 length overlap.
  - Attribute woody feature types using local 10 m and 20 m radii rasters to distinguish single vs double features (ratio filter 2.5–4 indicates double).
  - Classify roadside hedges by buffering OS roads and testing 0.75 length within 20 m road buffer.
  - Intersect vector CHM polygon with field boundary polylines within 20 m; segment boundaries receive height-class attributes; merge tiles into 10x10 km outputs.
  - Create a label attribute based on isDouble and isRoadside (e.g., Double hedge, Probable wide single hedge, Single hedge).
- Output structure: 10x10 km field boundary tiles composed of merged 5x5 km subtiles; included features can be split into multiple segments with different height classes.

## Attribute Details and Data Structure
- Output attributes per segment include: section, hghtcls (height class), isDb (isDouble), isRd (isRoadside), hlength (segment length), label (interpreted feature type).
- Example outputs illustrate varying segment lengths and classifications (e.g., "Double hedge," "Probable wide single hedge").

## Validation, Accuracy, and Comparability
- Validation against 38 Countryside Survey test squares (1 km2 each) conducted in 2022.
- 96% agreement for total length between LCPHE model and CS data across squares (excluding masked areas).
- Within-square comparison (2D): mean agreement in total length within 20 m tolerance ~76% (SD ~15%), with wide per-square variation.
- Height-class comparison: exact agreement ~32% across all length; 63% of length within a single height class of adjacent CS WLF height class, acknowledging higher segmentation precision in lidar data and potential timing differences (CS surveys in different years).

## Limitations and Uncertainty
- Snapshot in time (2016–2021 lidar); hedgerows may have changed since.
- Excludes moorland, heathland, urbanized areas, and woodland; gaps exist in North Yorkshire Moors (approx. 24x25 km not mapped due to lidar coverage gaps).
- Difficulty distinguishing woody linear features from other field boundaries (e.g., drystone walls) and from tall non-woody vegetation (nettles, reeds, bracken); misclassifications mainly affect lower height classes (1a/1b).
- Potential misalignment with ground truth due to generalization, digitizing, and georeferencing differences; the model aims to reflect presence and height of woody features associated with the LCM framework rather than precise ground-truth positions.
- Spatial accuracy tolerances: expect a few metres to tens of metres difference between modeled features and other georeferenced datasets.
- Best use: suitable for large-scale summaries (national/regional/farm-estate) of hedgerow lengths by height class; could serve as a baseline for field surveys to refine hedgerow maps at smaller scales.

## Practical Use for Analysts
- Data are designed for informing broad-scale assessments of hedgerow extent and structure, enhancing ecological and land-management analyses alongside other UKCEH datasets.
- Consider uncertainty and spatial tolerance when integrating with high-precision field data or fine-scale planning decisions.
- When using the data, cite the dataset and use the provided DOI; licensing is typically free for academic/research purposes with bespoke license negotiations.

## Example Output and Data Structure
- Visual examples show polyline hedgerow features color-coded by height class.
- Attribute tables accompany polyline features, with segment-level height class, length, and interpretation.

## Access, Licensing, and Reuse
- Bespoke licensing applies; licensing negotiations are conducted by the UKCEH Data Licensing team.
- Generally free for academic and research purposes.
- Reuse requires citation:
  Broughton, R.K.; Burkmar, R.; McCracken, M.; Mitschunas, N.; Norton, L.R.; Pallett, D.W.; Patton, J.; Redhead, J.W.; Staley, J.T.; Wood, C.M.; Pywell, R.F. (2024). UKCEH Land Cover Plus: Hedgerows 2016-2021 (England) . NERC EDS Environmental Information Data Centre. (Dataset). https://doi.org/10.5285/d90a3733-2949-4dfa-8ac2-a88aef8699be

## Acknowledgements and References
- Funded by NERC under ASSIST and AgZero+ programmes; JASMIN facility used for data analysis.
- Hedgerow data collection supported by Natural England under ITT9718.
- Notes on references to prior CS methodology and related lidar hedgerow work.