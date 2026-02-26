# UKCEH Land Cover Plus: Hedgerows (20162021) England Dataset documentation

## Purpose and scope
- Provides a national-scale model of the extent and height class of woody linear features along field boundaries in England (hedgerows, tree lines, semi-natural shrubs/trees).
- Derived from Environment Agency lidar data (National LiDAR Programme) collected 2016–2021.
- Aims to enable consistent environmental health monitoring and policy performance assessment at large scales; not a precise georeferenced map of every hedgerow.
- Designed to integrate with UKCEH Land Cover Map (LCM) products and be compatible with Countryside Survey height classes.
- Excluded areas: mountain/moor/heath, open water, coastal zone, urban/suburban areas, and woodland (continuous non-linear woody cover).

## What’s in the dataset
- Output: a national-scale model of linear woody field boundaries, with presence and height class information (summarised into seven height classes).
- Format and extent:
  - 5,881 tiles of 10 km resolution (9.51 GB) in shapefile format; later provided as geopackage.
  - Aligned to British National Grid/OS grid; designed to integrate with LCM linear framework.
- Data characteristics:
  - Polyline data binned into 7 height classes (minimum height 0.5 m) for segments at least 2 m long.
  - Each feature has length (metres) and an interpretation of feature type (e.g., double hedge, single hedge).
  - Vertical accuracy ~ ±15 cm; vertical resolution 1 cm; horizontal resolution 1 m.
- Coverage limitations:
  - Extent is England; excludes woodland, urban/suburban, coastal, mountain/moor/heath, and other specified land covers.

## Data coverage and exclusions
- Filtering uses the LCM polygon boundaries as the linear framework; woody features are mapped only where lidar CHM indicates vegetation >0.5 m.
- Excludes field boundaries abutting broadleaf/coniferous woodland, mountain/moor/heath, saltwater, freshwater, coastal, urban/suburban areas.
- Coastal areas buffered by 50 m within high water mark; buildings and farmsteads masked with 5–20 m buffers to reduce misclassification.
- Overlays with field boundaries require at least 0.9 of their length to coincide within 20 m of CHM features to be retained.

## Processing environment and source data
- Processing in R on the LOTUS batch computing cluster (JASMIN).
- CHM derived from Environment Agency lidar data (5 km raster tiles; leaf-off conditions).
- Supporting datasets: UKCEH Land Cover Map 2021, OS vector/open data products.
- Output generation conducted on 5 km tiles, then assembled into 10 km tiles; multiple tiles per 10 km tile are merged.

## Methodology: from CHM to field boundaries
- Field boundaries defined by LCM; woody features populated from lidar CHM values along these boundaries.
- CHM values < 0.5 m discarded; remaining values reclassified into height classes aligned with Countryside Survey.
- Modal filtering applied to smooth raster into contiguous height-class clumps; small clumps reclassified to larger neighboring clumps.
- CHM raster converted to vector polygons and overlaid with field boundary polylines.
- Field boundaries buffered (15 m) and assigned height class if intersecting CHM features within tolerance.
- Boundaries split into segments with potentially multiple height classes; isolated segments < 2 m removed or merged.
- Two binary attributes inferred: isDouble (parallel hedgerows) and isRoadside (along roads).
  - Double features detected via ratio of 20 m to 10 m neighbourhood CHM counts.
  - Roadside hedges identified when ≥75% of a boundary’s length lies within 20 m of OS road data.
- Final labeling:
  - label derived from isDouble and isRoadside (e.g., Double hedge, Probable wide single hedge, Single hedge).
- Output: UKCEH Land Cover Plus: Hedgerows (2016-2021) England model (LCPHE) with a detailed attribute table.

## Height classification and feature typing
- Height classes mapped to Countryside Survey conventions:
  - 0.50–0.99 m → 1a
  - 1.00–1.49 m → 1b
  - 1.50–1.99 m → 1c
  - 2.00–2.99 m → 2
  - 3.00–3.99 m → 3
  - 4.00–5.99 m → 4
  - ≥6.00 m → 6
- Height class assignment applied to CHM-derived polygons; modal smoothing and clipping deliver final segmentized features.
- Attributes per segment include hghtcls, isDb, isRd, hlength (m), and label.

## Validation and accuracy
- Validation against 38 Countryside Survey test squares (1 km² each) surveyed in 2022.
- Comparison metrics (excluding non-target land covers):
  - Overall total length: 96% agreement between LCPHE and CS field data.
  - Within 20 m buffer, per-square length agreement: mean 76% (SD 15%); range 27–2798% across squares.
  - Height class comparison: exact agreement 32% for segment midpoints; 63% of LCPHE length within a single height class of adjacent CS features.
- Discrepancies attributed to timing ( lidar 2016–2021 vs field survey up to 2022), feature delimitation differences, and higher segmentation in lidar data.

## Model limitations and usage guidance
- Snapshot nature: reflects lidar capture window (2016–2021); hedgerows may have changed since.
- Exclusions reduce misclassification but also exclude some hedgerows near woodland, urban areas, and moorland.
- Distinguishing hedgerows from other field boundaries (e.g., drystone walls) imperfect; non-woody tall vegetation may be misclassified as hedgerows (primarily in lower height classes).
- No manual correction across the dataset; users may inspect and edit for area-specific accuracy.
- Alignment with LCM framework means the hedgerow midline may not coincide with ground truth; features can be a few metres offset.
- Best for large-scale summaries (national/regional/estate level) of hedgerow presence and height class distributions; can serve as a baseline for field surveys at finer scales.

## Access, licensing, and citation
- Data access subject to bespoke licensing; generally free for academic/research purposes.
- To reuse: cite Broughton et al. (2024) – UKCEH Land Cover Plus: Hedgerows 2016-2021 (England). NERC EDS Environmental Information Data Centre. DOI: 10.5285/d90a3733-2949-4dfa-8ac2-a88aef8699be
- Additional information available via the provided DOI links in the dataset documentation.

## Example output and interpretation
- Demonstrates sample polyline outputs with height-class-coded segments and associated attributes (e.g., isDouble, isRd, hlength, label) across a representative area.
- Output aids interpretation of hedgerow structure along field boundaries and facilitates integration with other Land Cover Map products.

## Acknowledgements and references
- Funded by NERC (ASSIST and AgZero+ programs); JASMIN-based analysis; Natural England-supported hedgerow evaluation project; Environment Agency collaboration.
- References include prior work on hedgerow mapping and CS field methods, and CS Technical Report No.1/07.