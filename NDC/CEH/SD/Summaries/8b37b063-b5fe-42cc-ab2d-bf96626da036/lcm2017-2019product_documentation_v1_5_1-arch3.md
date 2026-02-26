# The UKCEH Land Cover Maps for 2017, 2018 and 2019 v1.5.1 30/06/2020

## Overview
- Presents three new UKCEH land cover maps: LCM2017, LCM2018, and LCM2019, extending a UK-wide series based on 21 UKCEH Land Cover Classes linked to Biodiversity Action Plan (BAP) Broad Habitats.
- Production is automated, using Bootstrap Training combined with Random Forest (RF); aims for annual updates to track land cover change.
- Output suite includes multiple data products at 20 m, 25 m, and 1 km scales to support monitoring and policy evaluation.

## Data and Products
- 20 m Classified Pixels: RF-derived per-pixel classification with band 1 as the most likely class and band 2 as a per-pixel confidence (0–100).
- Land Parcels: fixed spatial framework (~0.5 ha minimum) linking 20 m pixels to parcels; attributes include hist, mode, purity, conf, stdev, and n (with naming adjusted from LCM2015).
- 25 m Rasterised Land Parcels: three-band rasters (mode, conf, purity) summarising parcel data.
- 1 km Datasets: 
  - 1 km Percent Cover (21 bands)
  - 1 km Percent Aggregate Cover (10 bands)
  - 1 km Dominant Cover (1 band)
  - 1 km Dominant Aggregate Cover (1 band)

## Production Approach and Data Sources
- Bootstrap Training: historic LCM2015 used to bootstrap training data for 2017–2019; parcels with ≥99% purity selected to form the training set.
- Random Forest: balanced training (10,000 samples per bag) to classify pixels; production uses bespoke open-source tools (Weka, PostGIS, GDAL).
- Datasets and Scenes:
  - Sentinel-2 Seasonal Composite Images (TOA reflectance, median per season) plus 20 m Context Rasters to form Classification Scenes.
  - Great Britain: 74 overlapping 100 x 100 km Classification Scenes; Northern Ireland: a single 43-band scene per year.
- Seasonal and Context Information:
  - Four seasons (winter, spring, summer, autumn); some cloud gaps tolerated; context rasters include height, aspect, slope, distance to buildings/roads/coast, and other proximity masks.

## UKCEH Land Parcel Spatial Framework
- Maintains 0.5 ha MMU and a long-standing parcel framework; parcel identifiers (gid) differ from LCM2015 but can be used for cross-year comparisons via gid.
- Framework supports summarising 20 m pixel data and provides a fixed structure for change detection.

## Methodology Details
- Bootstrap Training builds a large, historically grounded training set to bootstrap new maps; koristi majority signal across years to improve robustness.
- Random Forest classification produces the 20 m Classified Pixels product; outputs include per-pixel class and associated confidence.
- Training data and validation emphasize balancing classes to avoid domination by common classes.

## Dataset Structure and Attributes
- 20 m Classified Pixels: two-band 8-bit rasters; band 1 = class, band 2 = probability (0–100).
- Land Parcels: parcel-level attributes (gid, hist, mode, purity, conf, stdev, n); clarifications on naming and minor attribute changes from LCM2015.
- 25 m Rasterised Land Parcels: three-band rasters (mode, conf, purity).
- 1 km Rasters: Percent Cover (21 bands), Percent Aggregate Cover (10 bands), Dominant Cover (1 band), Dominant Aggregate Cover (1 band).

## Classification Tiles and Coverage
- Great Britain: 100 x 100 km tiles; 74 GB Classification Scenes at 46-band resolution.
- Northern Ireland: single 43-band Classification Scene per year; coverage designed for full UK state-wide application.

## Validation and Accuracy
- UK-wide validation against countryside survey (2019), National Forest Inventory, IACS, plus bespoke validation points (22,325 total).
- Reported overall accuracy:
  - LCM2017: 78.6%
  - LCM2018: 79.6%
  - LCM2019: 79.4%
- Validation caveats: data sources differ from map classes; translation to UKCEH classes introduces potential misalignment; per-class confusion matrices provided in Appendix 4.

## Appendices and Class Relationships
- Appendix 1: Notes on UKCEH Land Cover Classes and mapping challenges (including upland peat, Bracken, and spectral limitations).
- Appendix 2: Biodiversity Action Plan (BAP) Broad Habitats and crosswalk to UKCEH classes.
- Appendix 3: Recommended RGB color recipes for display of UKCEH Land Cover Classes.
- Appendix 4: Detailed confusion matrices for LCM2017–LCM2019 (per-class producer and user accuracies).
- Appendix 5: Full list of datasets included for LCM2017, LCM2018, and LCM2019.

## Practical Considerations for Monitoring Frameworks
- Class system: 21 UKCEH Land Cover Classes (not a direct one-to-one with BAP Broad Habitats; careful cross-walking recommended for policy contexts).
- Temporal comparability: annual products enable change assessment, but parcel IDs (gid) differ from LCM2015; cross-year comparisons more robust via parcel-level hist/mode/purity or the gid crosswalk.
- Data availability and governance: emphasis on data provenance, openness, and metadata; validation remains an indicator rather than an absolute truth due to dataset differences.
- Future directions: plans to increase automation, broaden input satellite sources (including potential use of Sentinel-1 SAR), and refine the Land Parcel Spatial Framework for higher-resolution future data.