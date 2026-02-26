# The UKCEH Land Cover Maps for 2017, 2018 and 2019 v1.5.1

## Overview
- User guide accompanying LCM2017, LCM2018 and LCM2019, describing content, production, validation and planned future work.
- UKCEH maps use 21 UKCEH Land Cover Classes (based on BAP Broad Habitats) with a near one-to-one relationship to earlier LCM schemes.
- Production is automated (Bootstrap Training + Random Forest); no manual corrections were applied this release.
- Annual UK-wide maps aim to monitor land cover change; historically lag times between maps have been large.

## Content and Classification System
- 21 UKCEH Land Cover Classes (plus 10 UKCEH Aggregate Classes) defined and related to UK BAP Broad Habitats.
- Datasets per year include a 42-dataset suite (GB and NI versions), across multiple spatial grains.
- Class mapping and color scheme are specified; Appendix 3 provides RGB recipes for display.

## Data Structure and Datasets
- Datasets (per year) and extents:
  - 20m Classified Pixels (new in 2017–2019): pixel-level RF classification results with class probability per pixel.
  - Land Parcels: derived by intersecting 20m Classified Pixels with the UKCEH Land Parcel Spatial Framework; provides parcel-level attributes.
  - 25m Rasterised Land Parcels: summarises parcel data to 25m pixels; three bands retained: dominant class, confidence, and purity.
  - 1km Percent Cover: 21-band raster of per-1km class percentages.
  - 1km Percent Aggregate Cover: 10-band raster of per-1km aggregate class percentages.
  - 1km Dominant Cover: single-band raster of the dominant class per 1km grid.
  - 1km Dominant Aggregate Cover: single-band raster of the dominant aggregate class per 1km grid.
- GB and NI versions exist for each dataset; GB uses British National Grid (EPSG:27700) and NI uses Irish Grid (EPSG:29903).
- Pixel sizes and extents:
  - 20m Classified Pixels: 20 m resolution (GB and NI versions).
  - 25m Rasterised Land Parcels: 25 m resolution.
  - 1km rasters: 1 km resolution.
- Total dataset count: 42 datasets (per year across GB and NI).

## Production Process
- Sentinel-2 Seasonal Composite Images (TOA, median per season) used to create seasonal spectral information (winter, spring, summer, autumn).
- Ten Context Rasters added to seasonal images to help reduce spectral confusion (e.g., terrain, distance to features, proximity to sea, roads, etc.).
- Context rasters help RF distinguish spectrally similar classes (e.g., coastal vs inland features, urban proximity, terrain).
- Classification Scenes:
  - Great Britain: 100x100 km tiles; 36-band Seasonal Composite Images + 10 context layers = 46-band GB Classification Scenes; 74 overlapping scenes classified independently; visual inspection determines final precedence.
  - Northern Ireland: a single 43-band Classification Scene per year (36 spectral bands + 7 context layers) determined by NI land mass.
- Bootstrap Training:
  - Automatic training set derived from historic LCM2015 data (greater than 99% purity parcels) to bootstrap new maps.
  - Bootstrap Training uses majority signal across time to train RF classifier; reduces need for fresh field data.
- Random Forest classification:
  - 10,000 samples per class (with replacement) to balance training and avoid dominance by common classes.
  - Production software integrates Weka, PostGIS, and GDAL (open-source stack).
- Validation:
  - UK-scale validation against GB countryside survey (2019), National Forest Inventory, IACS and bespoke validation points (n ≈ 22,325).
  - Reported overall accuracy: LCM2017 78.6%; LCM2018 79.6%; LCM2019 79.4%.
  - Validation data are not perfect “ground truth” and involve some cross-mapping of class definitions; currency and comparability discussed in Appendix.

## Land Parcel Spatial Framework and Parcel Attributes
- Land Parcel Spatial Framework unchanged in geometry from LCM2015; gid identifiers do not match LCM2015, enabling time-based parcel comparisons via gid for 2017–2019.
- Land parcels ~0.5 ha minimum (MMU) to represent discrete real-world units (fields, parks, urban areas, etc.).
- Parcel attributes (Table 5) include:
  - gid: unique parcel identifier.
  - _hist: list of tuples (class_id:count) per parcel.
  - _mode: most frequent land cover class within parcel.
  - _purity: percentage of modal class within parcel.
  - _conf: mean class membership probability (0–100) for the modal class.
  - _stdev: standard deviation of _conf.
  - _n: number of 20m pixels intersecting parcel.
- Note: Parcel identifiers differ from LCM2015; comparisons should use gid across 2017–2019.

## Practical Usage and Considerations for GIS Specialists
- 20m Classified Pixels preserves fine spatial detail (e.g., narrow features) beyond parcel-based summaries.
- 25m Rasterised Land Parcels and 1km rasters provide progressively generalized products suitable for regional/landscape analyses and change detection at coarser scales.
- Bootstrap Training and automatic classification enable near real-time annual updates but introduce some consistency caveats with historical mappings.
- Validation indicates robust performance across major habitats, with notable difficulty in some upland and mixed habitats; user should consider class-specific accuracies in analyses.
- Spatial alignment: all GB/NI products are harmonized to their respective national grids; ensure correct CRS and extent when joining datasets across years or between GB and NI.
- Data governance: the Land Parcel Spatial Framework provides a fixed structure for time-series analysis, but 2017–2019 gid values are not directly interchangeable with LCM2015; use gid for cross-year parcel comparisons.

## Appendices and Supplementary Information
- Appendix 1–2: Notes on UKCEH Land Cover Classes and their relationship with BAP Broad Habitats; guidance on interpretation and spectral/detection limitations.
- Appendix 3: RGB color recipes for displaying each UKCEH Land Cover Class.
- Appendix 4: Validation details including confusion matrices and producer/user accuracies by class (2017–2019); caveats regarding validation data and class mappings.
- Appendix 5: Full list of datasets included for LCM2017, LCM2018 and LCM2019 (dataset names, HB/GB/NI scope, and file naming conventions).