# The UKCEH Land Cover Maps for 2017, 2018 and 2019 v1.5.1 30/06/2020

## Purpose and Overview
- User guide for three new UKCEH Land Cover Maps: LCM2017, LCM2018, and LCM2019.
- Each map provides a set of geospatial datasets mapping 21 UKCEH Land Cover Classes based on Biodiversity Action Plan (BAP) Broad Habitats.
- Maps produced automatically using Bootstrap Training plus Random Forest; aims to release annually.
- Classification used Sentinel-2 Seasonal Composite Images (TOA reflectance) per season, combined with 20m Context Rasters to create Classification Scenes.
- No manual corrections were applied this time; visual checks and formal validation performed to ensure quality comparable to LCM2015.
- Outputs include both high-detail 20m products and aggregated 1km products, with GB and Northern Ireland (NI) versions.

## Data Products (Dataset Suite)
- 20m Classified Pixels (new in 2017–2019): per-pixel class with membership probability (band 2) and class (band 1); preserves fine detail down to narrow features.
- Land Parcels: parcel-level attributes derived from the UKCEH Land Parcel Spatial Framework (gid, hist, mode, purity, conf, stdev, n).
- 25m Rasterised Land Parcels: three-band rasters (band 1: modal class; band 2: class confidence; band 3: parcel purity).
- 1km Raster Datasets (derived by aggregating 25m parcels): 
  - 1km Percent Cover (21-band)
  - 1km Percent Aggregate Cover (10-band)
  - 1km Dominant Cover (1-band)
  - 1km Dominant Aggregate Cover (1-band)
- Output structure: a total of 42 datasets (GB and NI, across three years).

## Geographic and Data Structure Details
- Great Britain (GB) extents: British National Grid (EPSG:27700); min East 0, max East 700000; min North 0, max North 1300000.
- Northern Ireland (NI) extents: Irish Grid (EPSG:29903); localized extents provided in dataset specifications.
- Pixel and dataset metadata:
  - 20m Classified Pixels: 21 classes with per-pixel confidence (0–100).
  - 25m Land Parcels: attributes including gid, hist, mode, purity, conf, stdev, n.
  - 1km rasters: derived by aggregating 25m parcels to 1km grids.
- Dataset descriptions are provided with detailed attribute definitions and changes from LCM2015 (see Appendix notes in the guide).

## Production Methodology
- Bootstrap Training: automatic training data sampled from UKCEH LCM2015 (high-purity parcels) to bootstrap 2017–2019; uses majority signal over time for training data.
- Random Forest Classification: balanced sampling (10,000 samples per training bag per class) using bespoke UKCEH software integrated with WEKA, PostGIS, and GDAL.
- Sentinel-2 Seasonal Composite Images: four-season, 20m TOA reflectance; bands 2,3,4,5,6,7,8,11,12 used for classification; gaps modelled as nulls and handled by the RF algorithm.
- Context Rasters: 20m context layers (GB: height, aspect, slope, proximity to buildings/roads/sea/freshwater, foreshore, tidal water, woodland; NI: height, aspect, slope, urban mask, distance to coast/freshwater/road).
- Classification Scenes and Tile Strategy:
  - GB: 100x100 km overlapping tiles, total of 74 classification scenes (46-band GB scenes per tile, including 36 spectral bands plus 10 context bands).
  - NI: single 43-band scene per year (36 spectral + 7 context).
- UKCEH Land Parcel Spatial Framework:
  - Maintains ~0.5 ha minimum parcel size (MMU); geometry unchanged from LCM2015, but with reindexed storage for speed.
  - gid identifiers for 2017–2019 parcels do not match LCM2015; cross-year comparisons should use gid within 2017–2019.
  - The framework allows users to summarize 20m classified pixels over alternative parcel boundaries if desired.
- Bootstrap Training and Validation:
  - Bootstrap Training uses majority signal from historic maps (LCM2015) to generate spectral training data for 2017–2019.
  - Validation involved 22,325 points from GB countryside survey 2019, NFI, IACS, and bespoke interpretation points.
  - Reported overall accuracy (GB scale) around 78.6% (LCM2017), 79.6% (LCM2018), and 79.4% (LCM2019).
  - Validation data are not absolute truth and may require interpretation, but results indicate strong performance for automatic 21-class maps.

## Class System and Canonical Colours
- LCM2017–2019 map 21 UKCEH Land Cover Classes, tied to UK BAP Broad Habitats definitions (Appendix 1 and 2 provide mappings and detection notes).
- Appendix 3 provides recommended RGB colour mappings for display of classes.
- Distinctions and potential spectral confusions between classes are discussed, with context rasters helping reduce misclassification (e.g., Neutral Grassland, Fern/Bog confusion, upland vegetation).

## Practical Considerations and caveats
- Manual corrections were not performed this release; the maps rely on automated classification with validation indicating comparable quality to earlier maps.
- Classification errors are generally randomly distributed; persistent real land cover changes should emerge over time as the time series develops.
- Outputs are designed to support broad applications, including policy support, environmental monitoring, and landscape change analysis, with an emphasis on enabling self-serve data exploration.
- For cross-year comparisons with LCM2015, gid-based comparisons are not possible; instead, use year-to-year gid references within 2017–2019 or align via spatial overlap.

## Appendix and Dataset Details
- Appendix 5 lists the full set of datasets by year, including GB and NI distinctions and the exact dataset naming conventions.
- References cited cover core methods and related land-cover mapping literature (Bootstrap Training, Random Forest, Sentinel-2 seasonal analysis).

## Summary Takeaways for Data Support
- Three new UKCEH LCMs (2017–2019) are released with a comprehensive 21-class system derived from BAP Broad Habitats.
- Production combines Bootstrap Training, Random Forest, Sentinel-2 seasonal data, and context rasters to produce detailed 20m outputs plus 1km summaries.
- GB and NI assets are provided, with 42 total datasets across three years; well-documented metadata and validation indicate robust, automation-driven outputs suitable for data exploration and product development.
- Users should note gid changes relative to LCM2015 and the absence of manual corrections in this release.