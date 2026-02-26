# The UKCEH Land Cover Maps for 2017, 2018 and 2019 v1.5.1

## Overview
- User guide for three UKCEH Land Cover Maps: LCM2017, LCM2018, and LCM2019.
- 21 UKCEH Land Cover Classes based on Biodiversity Action Plan (BAP) Broad Habitats; near-continuity with earlier maps (LCM2015/2007/2000/1990).
- Fully automatic classification using Bootstrap Training and Random Forest; annual release planned.
- Classification uses Sentinel-2 Seasonal Composite Images (TOA) plus 20m Context Rasters; no manual corrections this cycle; visual checks and formal validation performed.
- ACcuracy targets around 78–80% at UK scale; recognition of limitations and ongoing method refinement.

## Data Suite and Structure
- Total of 42 datasets per year (GB and Northern Ireland, GB and NI pairings): 20m Classified Pixels, Land Parcels, 25m Rasterised Land Parcels, 1km Dominant Cover, 1km Percent Cover, and 1km Percent Aggregate Cover (plus 1km Dominant Aggregate Cover where applicable).
- Dataset specifics:
  - 20m Classified Pixels: two bands per pixel—nominated class and class membership probability (0–100). Preserves fine detail (no generalisation by parcel framework).
  - Land Parcels: parcel-level attributes including gid, histogram of class counts, modal class (_mode), purity, confidence (_conf), standard deviation (_stdev), and pixel count (_n).
  - 25m Rasterised Land Parcels: three-band rasters—_mode, _conf, and _purity.
  - 1km Datasets: 1km Percent Cover (21 bands), 1km Percent Aggregate Cover (10 bands), 1km Dominant Cover (single band), 1km Dominant Aggregate Cover (single band).
- GB NI data duplication: separate GB and NI products with corresponding coordinate systems and extents.

## Spatial Framework and Metadata
- UKCEH Land Parcel Spatial Framework used to structure the datasets; minimum mapped unit approximately 0.5 hectares.
- gid identifiers for 2017–2019 do not match LCM2015 parcel IDs; comparisons across years should use gid rather than parcel IDs.
- Coordinate systems: GB in British National Grid (EPSG:27700) and NI in Irish Grid TM75 (EPSG:29903).
- MMU and delineation concepts influence dataset composition and comparability over time.

## Production Methodology and Provenance
- Bootstrap Training: automatic, self-starting training using historic UKCEH maps (initial bootstrap from LCM2015, later plans to bootstrap from majority signals across multiple years).
- Training data: for each year, 10,000 samples per class drawn with replacement to balance classes; based on Bootstrap Training from LCM2015.
- Classifier: Random Forest (Breiman 2001); production software integrates Weka, PostGIS, and GDAL (open-source components).
- Seasonal inputs: Sentinel-2 Seasonal Composite Images generated via Google Earth Engine (TOA reflectance used in this release; SR explored but no observed gain over TOA for current task).
- Context Rasters: 20m context layers (terrain, urban proximity, roads, coastline, water, etc.) to reduce spectral confusion; tailored for GB and NI contexts.
- Classification Scenes:
  - Great Britain: 100x100 km tiles, 74 overlapping GB scenes (46-band scenes) used to train and classify.
  - Northern Ireland: single 43-band scene per year (36 spectral + 7 context layers).
- UKCEH Land Parcel Spatial Framework retained but with minor internal indexing changes; parcel updates support time-series but break in parcel IDs across years is acknowledged.

## Validation and Data Quality
- Validation dataset: 22,325 points across GB countryside survey, National Forest Inventory, IACS, and manual interpretation points.
- UK-scale accuracy (overall) estimates:
  - LCM2017: 78.6%
  - LCM2018: 79.6%
  - LCM2019: 79.4%
- Validation notes:
  - Same validation points used for all three maps; currency and exact class correspondences vary.
  - Some class label conversions required; proportions and accuracies reflect mapping to UKCEH 21-class scheme.
  - Approximately 80% correspondence regarded as strong for an automatic, cross-year, national-scale product evolution.
- Appendix 4 includes detailed confusion matrices and producer/user accuracy statistics.

## Data Management, Access, and Versioning
- Appendix 5 lists full datasets per LCM2017, LCM2018, and LCM2019; 21 UKCEH Land Cover Classes plus 21-class totals across datasets.
- Data structure designed to support monitoring change over time; however, parcel-level comparability is impacted by gid changes and spatial framework reordering.
- Aimed for rapid production and annual updates; future versions likely expand input data sources (e.g., Sentinel-1, broader SAR) and potentially adjust class definitions and training data.

## Usage Considerations and Limitations
- Class definitions and mapping: UKCEH Land Cover Classes are aligned with BAP Broad Habitats but are derived for remote sensing practicality; caution with direct field-level habitat interpretation.
- Spatial resolution and MMU: small patches can fall below MMU, affecting detection of rare or fragmented features.
- Spectral confusion and context: some coastal, upland, peatland, and aquatic classes show interclass confusion; context rasters and seasonal data mitigate but do not eliminate.
- Saltwater vs Freshwater and coastal dynamics: coastal areas may exhibit cross-class confusion due to tides and proximity effects.
- Temporal comparisons: parcel IDs (gid) ensure some consistency, but parcel-level cross-year comparisons require careful alignment; overall change detection is supported via 20m Classified Pixels and Land Parcel summaries.

## Future Plans and Opportunities
- Continue annual releases (LCM2020 planned for 2021) with bootstrap training updates and method refinements.
- Potential integration of additional data sources (e.g., Sentinel-1 SAR) and alternative input data to improve classification in cloudy or challenging regions.
- Ongoing evaluation of training data strategies, including multi-year majority signals for Bootstrap Training.

## Appendices and References (Context for Governance and Interpretation)
- Appendix 1–2: Notes on UKCEH Land Cover Classes and UK BAP Broad Habitats (definitions and mapping considerations).
- Appendix 3: Recommended RGB color mapping for visualization.
- Appendix 4: Validation confusion matrices and accuracy statistics (detailed per-class producer and user accuracies).
- Appendix 5: Full dataset inventory by year and dataset type.
- References: Key methodological sources for RF classification, bootstrap training, and satellite-derived land cover mapping.