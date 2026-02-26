# The UKCEH Land Cover Maps for 2017, 2018 and 2019 v1.5.1

## Overview
- Three new UKCEH land cover maps: LCM2017, LCM2018, LCM2019.
- 21 UKCEH Land Cover Classes (based on BAP Broad Habitats) mapped across the UK; 21 classes align with LCM2015 and related legacy products.
- Production is automatic: Bootstrap Training combined with Random Forest (RF) classifier; uses Sentinel-2 Seasonal Composite Images (TOA reflectance) with 20m resolution, plus 20m Context Rasters.
- Aim is rapid UK-wide production with ongoing annual releases; no manual corrections were applied this cycle.
- Validation indicates maps are of similar quality to LCM2015; overall accuracy around 79% across years, with class-specific accuracies reported.

## Data sources and production approach
- Seasonal Composite Images: Sentinel-2 multispectral data from Google Earth Engine, median reflectance per season (winter, spring, summer, autumn) at 20m.
- Context Rasters (GB 20m): height, aspect, slope (from NEXTMap), distance from building/road/sea/freshwater, foreshore mask, tidal water mask, and a woodland mask.
- Classification Scenes: Great Britain uses overlapping 100x100 km tiles with 46-band scenes; Northern Ireland uses a single 43-band scene per year.
- Bootstrap Training: automatic training dataset created from historic maps (Bootstrap Training) to drive RF classification; 10,000 samples per class with replacement to balance classes.
- UKCEH Land Parcel Spatial Framework: a 0.5 ha MMU framework used to summarise 20m classified pixels into land parcels; geometry preserved across years with gid identifiers.
- No manual corrections this year; visual checks and formal validation performed.

## Datasets and products
- Dataset families (GB and NI) and yearly releases:
  - 20m Classified Pixels (GB and NI): 2-band rasters; band 1 = most likely UKCEH Land Cover Class; band 2 = class membership probability (0–100) for confidence.
  - Land Parcels: attributes derived by intersecting 20m Classified Pixels with the Land Parcel Framework; includes histogram of pixel counts per class, mode, purity, confidence, and related fields.
  - 25m Rasterised Land Parcels: 3-band rasters (mode, conf, purity) derived from Land Parcels.
  - 1km Raster Datasets: three products summarising parcel data to 1km grids:
    - 1km Percent Cover (21-band)
    - 1km Percent Aggregate Cover (10-band)
    - 1km Dominant Cover (1-band)
    - 1km Dominant Aggregate Cover (1-band)
- Extents and coordinate systems:
  - Great Britain: GB National Grid (EPSG:27700)
  - Northern Ireland: Irish Grid (EPSG:29903)
  - GB pixel extents for 8-bit rasters specify min/max coordinates; NI extents similarly defined.
- Dataset count: 42 datasets total (GB and NI, for 2017–2019).

## Classification workflow and data structure
- 20m Classified Pixels:
  - New in LCM2017–2019; RF outputs with per-pixel class probabilities.
  - Band 1: class ID; Band 2: probability (0–100) for confidence.
  - Preserves fine-scale features (e.g., narrow patches) since not generalised by the Land Parcel Framework.
- Land Parcels:
  - Attributes include gid, _hist (class-frequency tuples), _mode (dominant class), _purity (percent of modal class), _conf (mean membership probability), _stdev (uncertainty), _n (pixel count).
  - Field name changes reflect production naming conventions; gid values do not match LCM2015 parcels.
  - Aimed at reducing classification noise and enabling consistent change detection.
- 25m Rasterised Land Parcels:
  - 3-band raster: _mode, _conf, _purity.
- 1km Rasters (aggregation from 25m parcels):
  - 1km Percent Cover: 21-band raster (percentage cover per class).
  - 1km Percent Aggregate Cover: 10-band raster (aggregate classes).
  - 1km Dominant Cover: single-band raster (dominant class per 1km cell).
  - 1km Dominant Aggregate Cover: single-band raster (dominant aggregate class per 1km cell).
- Seasonal and contextual inputs:
  - Seasonal Composite Images derived from Sentinel-2 bands; 9 spectral bands used (2,3,4,5,6,7,8,11,12).
  - Context rasters help separate spectrally confusable classes (e.g., urban proximity, terrain context).
- Bootstrap Training and RF details:
  - Bootstrap Training draws from historic LCM2015 observations (99% purity threshold for parcel selection) to bootstrap the training set.
  - RF sampling: 10,000 samples per class, balanced via sampling with replacement.
  - Production software combines Weka RF, PostGIS, and GDAL (open source).

## Validation and accuracy
- Validation data sources: GB countryside survey 2019, National Forest Inventory data, IACS data, bespoke LCM validation points (22,325 points in total).
- Overall accuracy (UK scale):
  - LCM2017: 78.6%
  - LCM2018: 79.6%
  - LCM2019: 79.4%
- Class-level performance is variable; examples include producer’s and user’s accuracies across classes (document provides detailed confusion matrices and accuracy metrics per year).
- Important caveats:
  - Validation data have different purposes and class mappings; conversions between schemes introduce subjectivity.
  - No manual corrections were applied; results reflect automated classification and validation against independent datasets.

## Key notes for GIS usage and interpretation
- 20m Classified Pixels vs Land Parcels:
  - 20m pixels retain fine-scale landscape details; suitable for high-resolution mapping and detailed change detection.
  - Land Parcels provide a fixed, reusable spatial framework for time-series analysis, with associated attributes describing classification confidence and history.
- Temporal and thematic consistency:
  - Class definitions align with UKCEH Land Cover Classes; generally consistent with LCM2007, LCM2000, LCM2015, and UK BAP Broad Habitats mappings.
  - Cautious interpretation recommended where land cover classifications are spectrally ambiguous (e.g., some grassland and upland vegetation types).
- Data structure changes:
  - gid values in LCM2017–2019 land parcels do not match LCM2015; parcel-based comparisons should use gid-based matching.
  - Attribute naming changes in Land Parcels are designed for production clarity; historical comparisons may require mapping between fields.
- Future plans:
  - UKCEH aims to release a new LCM annually; LCM2020 planned for 2021, with bootstrap updates over multi-year periods.

## Appendices and additional context (highlights)
- Appendix 1: Notes on UKCEH Land Cover Classes (and how they relate to BAP Broad Habitats); detailed class-specific notes and detection caveats.
- Appendix 2: Biodiversity Action Plan (BAP) Broad Habitats definitions (detailed class descriptions and mapping implications).
- Appendix 3: Recommended RGB color recipes for displaying UKCEH Land Cover Classes (for visualization).
- Appendix 4: Validation details, confusion matrices, and accuracy metrics by class and year (detailed per-class producer’s and user’s accuracies).
- Appendix 5: Full list of datasets for LCM2017, LCM2018, and LCM2019 (dataset names, extents, and product types).