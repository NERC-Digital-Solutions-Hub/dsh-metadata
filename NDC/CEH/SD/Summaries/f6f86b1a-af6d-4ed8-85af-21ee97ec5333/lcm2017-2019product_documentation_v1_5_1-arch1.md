# The UKCEH Land Cover Maps for 2017, 2018 and 2019 v1.5.1 30/06/2020

## Overview
- Release accompanying LCM2017, LCM2018 and LCM2019.
- Map 21 UKCEH Land Cover Classes based on Biodiversity Action Plan (BAP) Broad Habitats; designed for satellite detection rather than field-level classifications.
- Production is automatic using Bootstrap Training and Random Forest (RF) classifiers to enable near-annual updates.
- No manual corrections this cycle to enable annual production; visual checks and formal validation are reported.
- Validation against GB countryside survey (2019), National Forest Inventory, IACS, and validation points yields around 78–79% overall accuracy across 2017–2019 products.

## Data content and dataset structure
- Datasets (per year) include:
  - 20m Classified Pixels (new, per-pixel RF probabilities; preserves fine detail)
  - Land Parcels (attributes linked to UKCEH Land Parcel Spatial Framework)
  - 25m Rasterised Land Parcels (derived from Land Parcels)
  - 1km Percent Cover (21-band)
  - 1km Percent Aggregate Cover (10-band)
  - 1km Dominant Cover (1-band)
  - 1km Dominant Aggregate Cover (1-band)
- Land Parcel attributes (examples):
  - gid: unique parcel identifier
  - _hist: histogram of class counts within parcel
  - _mode: most frequent class in parcel
  - _purity: percentage of modal class
  - _conf: mean class membership probability (0–100)
  - _stdev: standard deviation of _conf
  - _n: number of 20m pixels intersecting parcel
- Spatial scope:
  - Great Britain and Northern Ireland (GB and NI) with separate coordinate systems: GB National Grid (EPSG:27700) and Irish Grid (EPSG:29903).
  - Total of 42 datasets (per year: GB and NI variants).

## Production methodology
- Bootstrap Training:
  - Fully automatic training using historic maps as training data (no fresh field-gathered data required).
  - For 2017–2019, Bootstrap Training samples drawn from LCM2015 parcels with purity ≥ 99%.
  - Aims to capture majority signal over time; newer maps bootstrap from older maps and update with recent observations.
- Random Forest classification:
  - Training data drawn to balance classes (10,000 samples per class, with replacement).
  - Production software combines Weka with PostGIS and GDAL (all open source).
- Classification Scenes and tiling:
  - Great Britain: 74 overlapping 100x100 km tiles; each tile yields a 46-band Classification Scene (36 spectral bands + 10 context rasters).
  - Northern Ireland: a single 43-band Classification Scene per year (36 spectral + 7 context layers).
  - Results from overlapping tiles are visually inspected to select best outcomes for the final map.
- Contextual information:
  - Context Rasters (20m) mitigate spectral confusion and include terrain, proximity to buildings/roads/sea/freshwater, foreshore, tidal influence, and land cover masks (woodland, etc.).
- Seasonal imagery:
  - Seasonal Composite Images derived from Google Earth Engine using Sentinel-2 data; four seasons (winter, spring, summer, autumn) with median TOA reflectance per season at 20m.
  - Some seasonal gaps due to cloud; the RF classifier tolerates partial data.
  - Sentinel-2 bands used span blue, green, red, NIR, red-edge bands, and related wavelengths.
- Land Parcel Spatial Framework:
  - Framework used since LCM2007; parcels ~0.5 ha MMU; parcels generalized from national cartography.
  - gid identifiers differ from LCM2015; not directly comparable by parcel ID, but gid can be used for LCM2017–LCM2019 comparisons.
  - Provides a fixed structure for change detection; users may apply their own parcel structures if desired.

## Inputs and data sources
- Imagery:
  - Sentinel-2 Seasonal Composite Images (TOA reflectance; 20m resolution); 9 bands used per seasonal composite.
  - Google Earth Engine provides Sentinel-2 data; data levels initially TOA due to limited SR availability during production.
- Context rasters:
  - Great Britain: NEXTMap terrain (height, aspect, slope); OS open data (distance to buildings, roads, sea, freshwater); foreshore and tidal masks; woodland mask.
  - Northern Ireland: height, aspect, slope; urban mask (NISRA open data); distance to coast and freshwater; distance to roads.
- Validation data sources:
  - GB countryside survey 2019
  - Open source National Forest Inventory data
  - IACS data
  - Bespoke LCM validation points (manual image interpretation)

## UKCEH Land Parcel Spatial Framework and dataset relationships
- Land Parcels summarize 20m Classified Pixels within a fixed grid of parcels.
- Attributes exportable for cross-map comparisons; changes in attribute definitions exist relative to LCM2015 but gid remains the stable parcel identifier within this release.
- Framework supports potential use of alternative parcel structures by users (e.g., administrative boundaries, catchment boundaries).

## Validation and accuracy
- Validation dataset: 22,325 points across GB, intersected with LCM Land Parcels.
- Reported overall accuracy (via validation points):
  - LCM2017: 78.6%
  - LCM2018: 79.6%
  - LCM2019: 79.4%
- Notes on validation:
  - Validation data sourced from multiple datasets with potential category conversions; therefore, accuracy figures are indicative rather than absolute truths.
  - Approximately 80% correspondence is considered strong for fully automatic, annual pre-processed LCMs.
- Appendices include full confusion matrices and class-by-class producer’s and user’s accuracy metrics.

## Display, metadata, and data access
- Appendix 3 provides recommended RGB color mappings for display of each UKCEH Land Cover Class.
- Appendix 4 contains confusion matrices and class-level accuracy details (per year).
- Appendix 5 lists the full dataset inventory and naming conventions for LCM2017, LCM2018, and LCM2019.

## Appendices: key reference material
- Appendix 1: Notes on UKCEH Land Cover Classes (interpretation, detection potential, and typical confusions).
- Appendix 2: Biodiversity Action Plan (BAP) Broad Habitats definitions and their relationships to UKCEH Classes.
- Appendix 3: Color recipes for display of each land cover class.
- Appendix 4: Yearly confusion matrices with user’s and producer’s accuracies by class.
- Appendix 5: Full dataset lists and dataset descriptors for LCM2017–LCM2019.

## Future plans and outlook
- Intent to release a new LCM annually; aims to further automate production and validation workflows.
- Potential enhancements include expanding input data (e.g., Sentinel-1 radar), improving training data through new Bootstrap Training strategies, and refining parcel frameworks or adopting alternative summaries for change detection.
- Acknowledges that annual maps require automatic processing without manual corrections, balancing between timely updates and accuracy.