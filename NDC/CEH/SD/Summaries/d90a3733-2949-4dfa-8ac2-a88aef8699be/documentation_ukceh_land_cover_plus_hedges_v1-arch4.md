# UKCEH Land Cover Plus: Hedgerows (20162021) England Dataset documentation

## Overview
- Provides a national-scale model of woody linear features along field boundaries in England, including hedgerows, tree lines, and semi-natural shrub/tree stands.
- Derived from Environment Agency lidar data collected 2016–2021; captures extent and height class (7 height classes) but excludes woodland, urban/suburban, coastal, mountain/moor/heath, and open water areas.
- Ground-truth validated with 38 Countryside Survey test squares (1 km² each) in 2022.
  - Summary feature-length agreement: 96% across all squares.
  - Per-square agreement within 20 m buffer: average 76% (range up to 2798% across squares).
  - Height-class agreement: 32% exact; 63% within one height class.
- Intended for large-scale analysis (national/regional/large-farm scale); exact ground-positioning may differ from other datasets due to modeling approach.

## Data details and product specification
- Output format: polyline-based data (classifications) aligned to UKCEH Land Cover linear framework; provided as geopackages, organized in 5x5 km and 10x10 km tiles.
- Spatial coverage: England; excludes woodland parcels, urban/suburban areas, coastal zones, mountains/moor/heath.
- Geometry and attributes:
  - Polyline features with 7 height classes (minimum 0.5 m; segments ≥ 2 m).
  - Attributes include: length (metres), height class, feature type (e.g., single/double hedge), and flags isDouble (parallel features) and isRoadside (along roads).
  - Height-class interpolation tied to a CHM (Canopy Height Model) derived from lidar; vertical accuracy ±15 cm, 1 cm vertical resolution, 1 m horizontal resolution.
- Data specifics:
  - Created from 5,881 tiles at 10 km resolution (total ~9.51 GB); later combined into 5x5 km tiles and then aggregated to 10x10 km tiles for delivery.
  - Excluded land-cover types are masked to reduce misclassification (e.g., walls, buildings); coastal areas buffered by 50 m; buildings buffered by 5 m.
- Processing environment:
  - Processed in R on the LOTUS batch cluster (JASMIN) using a 1 m CHM raster supplied by Environment Agency.
  - Input data include 2021 UKCEH Land Cover Map (LCM) boundaries and OS open data for masking.
  - Output is designed to be interoperable with LCM products and Countryside Survey height-class schemes.

## Processing and data lineage
- Linear framework: LCM polygon boundaries define field boundaries; woody features populated from lidar CHM within this framework.
- CHM processing:
  - Filter CHM values below 0.5 m; reclassify to Countryside Survey-compatible height classes.
  - Apply modal filtering (11-pixel) to smooth raster; convert raster clumps to vector polygons.
- Field-boundary filtering:
  - Exclude boundaries abutting woodland, urban, coastal, mountainous areas; apply 50 m coastal buffer; 5 m buffer around non-boundary buildings.
  - Retain field boundaries that coincide with CHM features within 20 m and at least 0.9 of their length.
- Feature attribution:
  - Use 10 m and 20 m radius pixel-count filters to identify double features (parallel hedges) vs single features.
  - Buffer field boundaries by 15 m to assign isDouble and isRoadside attributes; derive a label for interpretation (e.g., Double hedge, Probable wide single hedge, Single hedge).
- Finalization:
  - Intersect vector CHM polygons with field-boundary lines within a 20 m tolerance; split lines by height-class segments; clip to EA 5 km tiles; merge into 10 km tiles.
  - Clean geometries by removing very short segments (<2 m) and merging connected segments with identical attributes.
  - Output includes a label column to aid interpretation and a detailed attribute table (Table 1 in the report).

## Licensing, access, and usage considerations
- Licensing: bespoke licensing; licensing typically free for academic and research purposes; coordination by UKCEH Data Licensing team.
- Citation: required citation of the dataset with provided DOIs.
- Accessibility: licensing and download coordination handled by UKCEH; further information via the dataset DOI links.

## Validation, limitations, and guidance for use
- Validation results:
  - Strong agreement with Countryside Survey data at the overall length level (96%).
  - Moderate-to-good per-square length agreement within a 20 m buffer (mean ~76%).
  - Height-class agreement: exact 32%; within one class 63%.
- Limitations:
  - Snapshot of lidar data from 2016–2021; hedgerows may have changed since capture.
  - Excludes moorland/heath, urbanized regions, and woodland; not validated in these areas.
  - Difficulty distinguishing woody linear features from other field boundaries (e.g., drystone walls); misclassification risk mainly in lower height classes (1a/1b).
  - Distinguishing tall non-woody vegetation and large infrastructure (bridges, solar panels) can introduce errors; manual cleaning not performed.
  - Spatial accuracy: the modeled midline may not align precisely with ground-truth features; expect a tolerance of several metres to tens of metres when comparing with other datasets.
- Scale guidance:
  - Best suited for national, regional, or farm-estate level summaries of total hedgerow length by height class.
  - For field-level accuracy, use as a baseline and supplement with targeted field surveys or higher-resolution checks.

## Example outputs and interpretation
- Example outputs illustrate polyline features color-coded by height class with accompanying attribute tables.
- Attributes include: hghtcls (height class), isDb (is double), isRd (is roadside), hlength (feature length), and label (interpretive type).

## Acknowledgements, funding, and references
- Funded by NERC through ASSIST and AgZero+ programs; UKCEH and JASMIN supported computing.
- Hedgerow data collection supported by Natural England project ITT9718.
- Acknowledges Environment Agency contributions and OS data.
- References to related methodological and validation works provided in the document.