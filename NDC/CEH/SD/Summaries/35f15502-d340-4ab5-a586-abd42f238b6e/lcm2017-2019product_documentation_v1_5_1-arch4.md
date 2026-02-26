# The UKCEH Land Cover Maps for 2017, 2018 and 2019

## Overview
- Release of three new UKCEH Land Cover Maps: LCM2017, LCM2018, and LCM2019.
- Each map presents 21 UKCEH Land Cover Classes derived from Biodiversity Action Plan (BAP) Broad Habitats, matching the LCM2015 scheme.
- Production is fully automatic (Bootstrap Training + Random Forest) to enable annual updates; aims to release a new map each year.
- UK-wide coverage including Great Britain and Northern Ireland; 42 datasets in total (per-year, per-region).

## What data are included
- 21 UKCEH Land Cover Classes (not UK BAP Broad Habitats) with a clear crosswalk to BAP where relevant; emphasis on consistency for change detection.
- Datasets include:
  - 20m Classified Pixels (new for 2017–2019): RF classification results with per-pixel class and a separate confidence score (0–100).
  - Land Parcels: intersection of 20m Classified Pixels with the UKCEH Land Parcel Spatial Framework; parcel-level attributes.
  - 25m Rasterised Land Parcels: 3-band rasters (dominant class, confidence, purity).
  - 1km Raster datasets: Percent Cover (21 bands), Percent Aggregate Cover (10 bands), Dominant Cover (1 band), Dominant Aggregate Cover (1 band).

## How data were produced
- Sentinel-2 Seasonal Composite Images (TOA reflectance, resampled to 20m) for winter, spring, summer, and autumn.
- Context Rasters (20m) used to reduce spectral confusion (terrain, proximity to buildings/roads/water, coastal masks, etc.).
- Classification Scenes:
  - Great Britain: 100x100 km tiles; 74 overlapping scenes classified independently; visual inspection resolves overlaps.
  - Northern Ireland: single 43-band Classification Scene per year.
- Bootstrap Training:
  - Automatic generation of training data from historic LCMs (bootstrap from 2015 for 2017–2019).
  - RF classifier trained with balanced sampling from training bags to avoid bias toward common classes.
- Production stack relies on open-source tools (Weka, PostGIS, GDAL).

## Data structure and formats
- Two regional scales per year: GB and NI.
- Classifications and products:
  - 20m Classified Pixels: 2-band rasters; band 1 = most likely class; band 2 = confidence (0–100).
  - Land Parcels: attributes including gid, hist (class frequencies per parcel), mode, purity, conf, stdev, n.
  - 25m Rasterised Land Parcels: 3-band rasters (mode, conf, purity).
  - 1km Percent Cover: 21-band raster (per-class cover percentage).
  - 1km Percent Aggregate Cover: 10-band raster (aggregate cover).
  - 1km Dominant Cover: 1-band raster (dominant class per 1km cell).
  - 1km Dominant Aggregate Cover: 1-band raster (dominant aggregate class).
- Coordinate systems:
  - Great Britain: British National Grid (EPSG:27700).
  - Northern Ireland: Irish Grid (EPSG:29903).
- Ground-truth/validation data and crosswalks described in Appendices.

## Classification and validation
- Validation approach:
  - UK-scale validation against GB countryside survey data, National Forest Inventory, IACS, and bespoke LCM validation points.
  - Total validation points: 22,325.
  - Reported overall accuracy: LCM2017 ≈ 78.6%; LCM2018 ≈ 79.6%; LCM2019 ≈ 79.4%.
- Notes on validation:
  - Validation points derived from sources with slightly different class definitions; conversions to UKCEH classes introduce some subjectivity.
  - Approximately 80% overall correspondence is considered highly credible for an automatic 21-class product; expected improvements as methods mature.

## Relationship to BAP Broad Habitats and class mapping
- LCM2017–LCM2019 retain the 21 UKCEH Land Cover Classes, aligned to BAP Broad Habitats definitions where relevant.
- Appendix materials provide:
  - Detailed notes on how BAP Broad Habitats map to UKCEH classes (and where mismatches occur).
  - Guidance on interpreting classes such as Broadleaved/Coniferous woodland, Arable, Various Grasslands, Fen/Marsh/Swamp, Bog, Saltmarsh, Urban/Suburban, etc.
- General aim: maintain consistency with earlier maps to facilitate change detection while adapting to improved spectral detection capabilities.

## UKCEH Land Parcel Spatial Framework
- Framework maintains minimum parcel size ~0.5 ha (MMU) and parcel-based structure for time-series consistency.
- gid identifiers are stable within a map but do not match LCM2015 parcel IDs; cross-map comparisons should use spatial overlap or use gid as linkage only within the same release series.
- The framework supports summarizing 20m Classified Pixels into parcels while preserving detail; users can also apply their own parcel structures.

## Access, limitations, and future directions
- Access:
  - GB and NI extents provided; multiple derived products across years available within each year’s dataset package.
- Limitations:
  - No manual corrections this release; classification errors are expected to be randomly distributed over time.
  - Some coastal and upland classes present detection challenges; Saltwater vs Freshwater distinctions influenced by coastal context layers.
  - The BAP-to-UKCEH mapping requires careful interpretation for some habitats; not every habitat is easily separable spectrally.
- Future directions:
  - Planned annual releases; ongoing evaluation of input data (e.g., exploring Sentinel-1 SAR, alternative imagery, or surface reflectance products).
  - Potential refinements to training data and parcel frameworks; exploration of finer parcel boundaries as higher-resolution data become available.

## Appendices and supporting documentation (in summary)
- Appendix 1–2: In-depth notes on UKCEH Land Cover Classes and their relation to BAP Broad Habitats.
- Appendix 3: Color conventions for displaying UKCEH Land Cover Classes.
- Appendix 4: Validation results and confusion matrices for 2017, 2018, 2019; summary of user and producer accuracies.
- Appendix 5: Full list of datasets included for LCM2017, LCM2018, and LCM2019 (per year, per region, per dataset type).