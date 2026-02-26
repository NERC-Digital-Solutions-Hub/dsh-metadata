# The UKCEH Land Cover Maps for 2017, 2018 and 2019 v1.5.1

## Overview
- This document is a user guide for the three UKCEH Land Cover Maps (LCMs): LCM2017, LCM2018 and LCM2019.
- Each map represents 21 UKCEH Land Cover Classes (based on Biodiversity Action Plan Broad Habitats) and matches the class framework used in LCM2015.
- Maps are produced automatically using Bootstrap Training and a Random Forest classifier to enable rapid, near-annual updates.
- The guide explains content, production decisions, validation, future plans, and how to use the data effectively.

## What the products include
- 20m Classified Pixels (new in these releases)
  - RF classification results from Sentinel-2 Seasonal Composite Images (TOA reflectance) for each season, with per-pixel class and a confidence score (0–100).
  - Not aggregated into land parcels to preserve fine detail (e.g., narrow features).
- Land Parcels
  - Attributes summarising the 20m Classified Pixels within the UKCEH Land Parcel Spatial Framework (0.5 ha MMU).
  - Key attributes: gid, hist (distribution of classes within parcel), mode, purity, conf, stdev, n.
  - Note: gid values differ from LCM2015 due to spatial framework changes.
- 25m Rasterised Land Parcels
  - Rasterised version of parcel data (3 bands: mode, conf, purity).
- 1km Raster Products (per year)
  - 1km Percent Cover (21 bands)
  - 1km Percent Aggregate Cover (10 bands)
  - 1km Dominant Cover (1 band)
  - 1km Dominant Aggregate Cover (1 band)

## Data structure and metadata
- Dataset structure for each year includes GB (Great Britain) and NI (Northern Ireland) versions, with separate coordinate systems:
  - GB: British National Grid (EPSG: 27700)
  - NI: Irish Grid TM75 (EPSG: 29903)
- Total datasets: 42 products across three years (20m Classified Pixels, Land Parcels, 25m Rasterised Land Parcels, plus three 1km products per year).

## Production approach and reasoning
- Bootstrap Training
  - Automatic sampling from historic maps (prior maps with high purity) to train the classifier.
  - The bootstrap uses the majority signal across past maps to train the RF classifier for 2017–2019.
  - Future plans: bootstrap from 2017–2019 majority signals for LCM2020 and 2021 updates.
- Random Forest classification
  - Training observations drawn from Bootstrap Training data; balanced across classes to avoid bias toward common classes.
  - Production uses bespoke UKCEH software integrating WEKA with PostGIS and GDAL.

## Satellite data and classification scenes
- Seasonal Composite Images
  - Generated from Sentinel-2 TOA reflectance, 20m resolution, median per season (winter, spring, summer, autumn).
  - Some seasons may have cloud gaps; the algorithm tolerates partial spectral information.
  - Future work may include additional input sources (e.g., Sentinel-1 SAR) to fill gaps.
- Context Rasters
  - 20m context layers to reduce spectral confusion (GB vs NI lists differ slightly):
    - GB examples: height, aspect, slope; distances to buildings, roads, sea, freshwater; foreshore and coastal masks; woodland mask.
    - NI examples: height, aspect, slope; urban mask; distance to coast, freshwater, road.
- Classification Scenes (GB and NI)
  - GB uses 100x100 km tiles, producing 36-band Seasonal Composite Images per tile combined with context layers to form 46-band GB Classification Scenes; 74 overlapping scenes classified independently and merged.
  - NI uses a single 43-band scene per year (36 spectral Bands + 7 context layers) optimized for NI’s smaller area.

## UKCEH Land Parcel Spatial Framework
- The framework was updated (matching LCM2015 geometry) but storage and indexing were reorganised for speed.
- Consequence: parcel identifiers (gid) differ from LCM2015; parcel comparisons require using gid.
- Parcellation: minimum parcel area ~0.5 ha; parcels are designed to represent discrete land units and are typically dominated by a single land cover class.
- The framework enables a fixed structure for change detection, while still allowing users to apply their own parcel boundaries if desired.

## Validation and accuracy
- Validation approach: comparison with multiple data sources (GB countryside survey 2019, National Forest Inventory, IACS, and bespoke validation points; 22,325 points total).
- Reported GB-wide accuracy (21-class maps) for the three years:
  - LCM2017: 78.6% overall
  - LCM2018: 79.6% overall
  - LCM2019: 79.4% overall
- Validation data were the same across years, with caveats about differences between validation classes and target UKCEH classes. Approximately 80% correspondence is considered strong and indicative, with expectations for improvement as methods mature.
- Appendices provide full validation tables and class-by-class confusion analyses.

## Class relationships and terminology
- LCM2017–2019 map 21 UKCEH Land Cover Classes, aligned with UK BAP Broad Habitats where possible but not a one-to-one mapping. The guide explains nuanced relationships and clarifies when BAP terms are italicised to denote exact vs. general concepts.
- Appendix details include:
  - Appendix 1: Notes on individual UKCEH Land Cover Classes
  - Appendix 2: Biodiversity Action Plan Broad Habitats definitions
  - Appendix 3: Recommended RGB color mappings for display
  - Appendix 4: Full confusion matrices and performance metrics by class
  - Appendix 5: Full list of datasets per year and their dataset names

## Usage guidance and future directions
- The three new LCMs enable annual land cover change analysis and cross-year consistency with careful interpretation of class definitions and spatial frameworks.
- No manual corrections were performed in this release to enable rapid annual updates; visual checks and formal validation were still conducted to ensure quality.
- Future plans emphasize expanding input data range (e.g., more portable input sources, radar data), refining classifications for upland and peatland habitats, and further improving validation resources.
- The datasets are designed for broad monitoring and policy-support use, with explicit attention to enabling access to underlying data and integrating with other relevant datasets for enhanced environmental monitoring.

## Appendices and supplementary information (highlights)
- Appendix 1 and 2: Detailed notes on UKCEH Land Cover Classes and BAP Broad Habitats, including detection challenges and class-level considerations.
- Appendix 3: RGB color recipes for displaying UKCEH Land Cover Classes.
- Appendix 4: Detailed validation confusion matrices and accuracy statistics by class and dataset.
- Appendix 5: Comprehensive list of datasets per LCM year (dataset names and holdings).