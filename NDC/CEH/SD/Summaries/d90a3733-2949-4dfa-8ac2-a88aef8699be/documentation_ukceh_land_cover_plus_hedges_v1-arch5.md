# UKCEH Land Cover Plus: Hedgerows (20162021) England Dataset documentation

## Overview
- A national-scale model of the extent and height class of woody linear features along field boundaries in England, including hedgerows, tree lines, and semi-natural shrub/tree thickets.
- Derived from Environment Agency National LiDAR Programme data (2016–2021) and aligned with UKCEH Land Cover Map (LCM) frameworks and Countryside Survey height classes.
- Intended as a representation of presence and height of woody linear features along LCM boundaries, not a pixel-perfect georeferenced hedgerow map.

## Data content and product specification
- Product: UKCEH Land Cover Plus: Hedgerows (2016-2021) England (LCPHE) in 5,881 tiles of 10 km, total ~9.51 GB; provided as shapefile tiles, then consolidated to geopackage for download.
- Representation: Polylines for field boundaries with 7 height classes (minimum 0.5 m), plus attributes for length (metres) and feature type (e.g., single/double hedge).
- Extent and exclusions: England-wide, excluding woodland (continuous non-linear), urban/suburban, coastal, mountain/moor/heath, and areas near high water; 50 m coastal buffer; 5 m buffer for certain non-boundary features.
- Data alignment: Aligned to UKCEH LCM linear framework (parcel boundaries) and to OS grid; height class mapping compatible with Countryside Survey.
- Key attributes and interpretation: hghtcls (height class), isDb (double features), is Rd (roadside), hlength (feature length), label (derived category). Height classes align with Countryside Survey:
  - 0.50–0.99 m = 1a
  - 1.00–1.49 m = 1b
  - 1.50–1.99 m = 1c
  - 2.00–2.99 m = 2
  - 3.00–3.99 m = 3
  - 4.00–5.99 m = 4
  - 6.00 m and above = 6

## Processing environment and source data
- Processing in R on the LOTUS cluster (JASMIN).
- Input canopy height model (CHM) at 1 m resolution, derived from EA LiDAR (DTM subtracted from first-return DSM); leaf-off acquisition (autumn/winter).
- Additional masking data: LCM 2021 and OS vector data (DistrictMap Vector, OpenMap, OpenRoad).
- Tile strategy: output generated 5×5 km tiles, then assembled into 10×10 km tiles.

## Data processing workflow
- Ground framework: LCM polygon boundaries serve as the primary linear framework; woody features populated from CHM values where present.
- Height filtering and classification: CHM values <0.5 m removed; remaining values reclassified into CS-compatible height classes; 11-pixel modal filtering to smooth raster; raster-to-vector conversion.
- Boundary filtering: exclude boundaries abutting excluded land covers (woodland, urban, coastal, mountain/moor/heath, etc.); 50 m coastal buffer; 5 m buffer for garden-related features; retain boundaries that coincide with CHM features within 0.9 length within 20 m.
- Feature typing: compute local 10 m and 20 m pixel counts around each CHM cell to derive a ratio raster; ratio indicates double features (2 parallel hedgerows) vs single; assign isDb accordingly; buffer field boundaries by 15 m to assign isDb/isRd via modal values.
- Roadside attribution: buffer OS road network by 20 m; if boundary length within 20 m road buffer ≥ 0.75, tag as roadside (isRd).
- Final attribute assignment: intersect vector CHM polygons with boundary polylines within 20 m; segment boundaries by height class; merge tiles; create a label field based on isDb and isRd.
- Output structure: a comprehensive 10 km field boundary tile dataset with per-segment height class, length, and interpretation label (Single hedge, Double hedge, Probable wide single hedge, etc.).

## Validation and accuracy
- Validation dataset: 38 Countryside Survey test squares (1 km² each) surveyed in 2022.
- Overall findings:
  - 96% agreement in total feature length between LCPHE and CS field survey across all squares (within masked exclusions).
  - For individual features within a 20 m buffer, mean agreement ~76% (SD ~15%); per-square agreement varied (up to 2798% in some cases, due to scaling and counting methods).
  - Height class comparison: exact agreement ~32%; within one height class ~63%.
- Interpretation: greater discrepancy in precise geometry and height class due to difference in data capture timing (2016–2021 LiDAR vs 2022 field surveys), feature delineation, and methodological differences; CHM-based height classes capture finer segmentation than field CS outlines.

## Model limitations and caveats
- Temporal snapshot: LiDAR data from 2016–2021; hedgerows may have changed since.
- Coverage gaps: moorland/heath and urbanized areas largely excluded; North Yorkshire Moors area (~24×25 km) not mapped due to LiDAR absence.
- Feature discrimination limitations: difficulty distinguishing woody hedgerows from other field boundaries (e.g., drystone walls) and tall non-woody vegetation (nettles, reeds, bracken); taller structures (bridges, solar panels) may be misclassified.
- Ground-truth alignment: exact field positions may not align perfectly with mapped linear framework; hedgerow midlines and canopy widths may deviate from mapped polylines.
- Scale suitability: best for national/regional summaries of total hedgerow lengths by height class; field-level precision is limited; can serve as a baseline for targeted field updates.

## Licensing, access, and attribution
- Licensing: bespoke licensing; licensing generally free for academic and research purposes; licensing handled by UKCEH Data Licensing.
- Citation: must cite Broughton et al. (2024) and the NERC/EDS references; DOI provided for dataset.
- Version: v1.0; published 11/12/2023.
- Usage guidance: consider spatial tolerances when comparing with other datasets; acknowledge potential location and attribute discrepancies; for high-precision needs, supplement with field surveys.

## Practical implications for Data Stewards
- Governance and discovery: dataset comes with a clear licensing path, versioning, and citation requirements; metadata should document temporal extent (2016–2021 LiDAR), processing steps, and limitations.
- Data quality and interoperability: strong alignment with LCM framework and Countryside Survey height classes enhances interoperability, but users should anticipate georeferencing tolerances of meters to tens of meters and scale-focused analyses.
- Stewardship recommendations: provide guidance to users on appropriate use scales (national/regional) and caution for field-level substitution; consider updating the model with new LiDAR data or field validations to improve accuracy in target areas.
- Data access strategy: ensure licence negotiation workflow is documented and accessible; provide direct links to DOIs and licensing terms; maintain provenance with processing steps for reproducibility.