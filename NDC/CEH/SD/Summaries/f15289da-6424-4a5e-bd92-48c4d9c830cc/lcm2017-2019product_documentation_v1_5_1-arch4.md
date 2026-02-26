# The UKCEH Land Cover Maps for 2017, 2018 and 2019 v1.5.1

## Overview
- User guide for three UKCEH land cover products: LCM2017, LCM2018, and LCM2019.
- 21 UKCEH Land Cover Classes derived from Biodiversity Action Plan (BAP) Broad Habitats; designed for consistent cross-year comparison.
- Automated production using Bootstrap Training and Random Forest classifiers; rapid, coast-to-coast mapping.
- Sentinel-2 Seasonal Composite Images (TOA) used with 20m Context Layers; aim to release a new map annually.
- Validation indicates ~80% correspondence with reference datasets; no manual corrections were applied in these releases.

## Data products and structure
- 20m Classified Pixels
  - GB and NI versions; 21-class classification with a second band indicating per-pixel classification confidence (0–100).
  - Preserves fine detail; not generalized by Land Parcels.

- Land Parcels
  - Attributes per parcel: gid, _hist (histogram as tuples), _mode, _purity, _conf, _stdev, _n.
  - Minimum parcel size about 0.5 ha (MMU); parcels are a fixed UKCEH Spatial Framework structure.
  - gid values do not match LCM2015; cross-year comparisons should use gid for 2017–2019.

- 25m Rasterised Land Parcels
  - 3-band raster: band 1 = _mode, band 2 = _conf, band 3 = _purity.

- 1km Raster datasets
  - 1km Percent Cover (21 bands)
  - 1km Percent Aggregate Cover (10 bands)
  - 1km Dominant Cover (1 band)
  - 1km Dominant Aggregate Cover (1 band)

- Seasonal Composite Images and Classification Scenes
  - Seasonal composites derived from Google Earth Engine (Sentinel-2 TOA, 20m resolution).
  - 20m Context Rasters used to reduce spectral confusion.
  - Great Britain: 74 overlapping 100x100 km Classification Scenes; Northern Ireland: single 43-band scene per year.

- The UKCEH Land Parcel Spatial Framework
  - Maintains ~0.5 ha MMU; unchanged parcel geometry from LCM2015, but reindexed for faster processing.
  - Parcel identifiers (gid) do not map directly to LCM2015 parcels; cross-compatibility requires spatial overlap rather than gid.

- Bootstrap Training and Random Forest
  - Bootstrap Training uses UKCEH LCM2015-derived data (high-purity parcels) to bootstrap classifiers for 2017–2019.
  - RF classifier trained with balanced sampling (10,000 samples per class per training bag).
  - Production tools are bespoke, integrating Weka, PostGIS, and GDAL (open source).

## Production methodology
- Bootstrap Training draws from historic maps to train the classifier for current Sentinel-2 data.
- Random Forest classification yields the 20m Classified Pixels product; subsequent layers (Land Parcels, 25m Parcels, 1km rasters) are derived from these pixels.
- Classification Scenes are overlapping to ensure training data balance and coverage; minimal manual intervention (visual checks used to select best results).
- Context rasters provide terrain and proximity information to aid disambiguation of spectrally similar classes.

## Data quality, validation, and limitations
- Validation against GB countryside survey 2019 data, National Forest Inventory, IACS, and bespoke points (total ~22,325 points).
- Reported overall accuracy (UK scale):
  - LCM2017: 78.6%
  - LCM2018: 79.6%
  - LCM2019: 79.4%
- Notes:
  - Validation points are not an absolute truth; some label conversions were needed between validation schemes and UKCEH classes.
  - Approximate ~80% correspondence is considered strong for fully automatic 21-class maps.
  - Some inter-class confusion remains (e.g., between upland peatland and related habitats; Saltwater vs Freshwater near coasts).
  - No manual corrections were performed this cycle to enable rapid annual updates; visual checks and validations were still conducted.

## Usage considerations and planning
- Class definitions and relationships to UK BAP Broad Habitats are provided, with care to maintain consistency over time for change detection.
- The 20m Classified Pixels retain fine features; the 25m and 1km products generalize information for broad-area analyses.
- Acknowledges limitations in detecting certain upland and peatland classes from satellite data; planned future enhancements may address these with new training data and methods.
- Data access and formats align with UKCEH production software and internal conventions; changes in parcel identifiers mean historical parcel-based comparisons to LCM2015 are not direct by gid.

## Data governance, metadata, and future plans
- Yearly release intention: LCM2020 planned for 2021, following the Bootstrap Training scheme from 2017–2019.
- Dataset descriptions include multiple geographic extents (Great Britain and Northern Ireland) and multiple spatial resolutions, with corresponding metadata (CRS, pixel sizes, bands, and attributes).
- Appendix materials (Appendix 1–5) cover detailed class definitions, mapping to BAP habitats, color schemes, and full dataset listings; confusion matrices and validation details are provided to support audit and interpretation.
- Future enhancements anticipated:
  - Potentially increasing input data range (including SAR for cloud-robust classification).
  - Possible refinement of the UKCEH Land Parcel Spatial Framework to align with higher-resolution data and new mapping needs.

## Appendix and references (highlights)
- Appendix 1–2: UKCEH Land Cover Class notes and BAP Broad Habitat mappings.
- Appendix 3: Recommended RGB color recipes for display.
- Appendix 4: Validation confusion matrices and accuracy metrics (per class).
- Appendix 5: Full dataset lists for LCM2017, LCM2018, and LCM2019 (GB and NI products).
- References to foundational works on Random Forests, Bootstrap Training, and prior LCM developments.