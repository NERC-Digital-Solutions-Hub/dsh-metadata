# The UKCEH Land Cover Map for 2021

## Overview
- LCM2021 is the ninth UKCEH land cover map, built from 21 UKCEH Land Cover Classes (based on Biodiversity Broad Habitats, with some distinctions).
- Aims to enable users to make informed decisions by describing data production, validation, and accuracy, and by providing data products for exploration and self-service analysis.
- Produced annually using automated methods to improve temporal consistency and support change detection.

## Key Data Products
- 10 m Classified Pixel datasets (GB and NI)
  - Each pixel has:
    - Band 1: the most likely UKCEH Land Cover Class
    - Band 2: the probability/confidence for that class
  - Not generalised by the UKCEH Land Parcel Spatial Framework (preserves fine details; intended for specialist users)
- Land Parcel datasets (GB and NI)
  - Intersect 10 m classified pixels with the UKCEH Land Parcel Spatial Framework
  - Provide parcel-level attributes (Table 3 attributes such as _hist, _mode, _purity, _conf, _n, _agg)
  - Parcels have a minimum area of ~0.5 hectares (MMU)
- 25 m Rasterised Land Parcel datasets (GB and NI)
  - Rasterised from Land Parcel data into 25 m pixels
  - 3-band rasters carrying: dominant land cover (_mode), mean probability/confidence (_conf), and purity (_purity)
- 1 km raster products
  - Summary of 25 m data to 1 km pixels
  - Dominant cover at 1 km (for both classes and aggregates)
  - Percentage cover at 1 km (21 class bands and 10 aggregate bands)
  - Rounding means totals may not sum exactly to 100; coastal areas may sum to less than 100

## Seasonal and Context Information
- Seasonal Composite Images
  - Derived from Google Earth Engine using Sentinel-2 data
  - Four seasons (Jan–Mar, Apr–Jun, Jul–Sep, Oct–Dec)
  - 10 spectral bands (2, 3, 4, 5, 6, 7, 8, 8A, 11, 12)
  - Some gaps due to cloud; classification algorithms tolerate partial spectral information
- Context Rasters
  - Purpose: reduce spectral confusion between spectrally similar land covers
  - GB: 10 context rasters (height, aspect, slope, distances to buildings/roads/sea/freshwater, foreshore mask, tidal water mask, woodland mask)
  - NI: 9 context rasters (height, aspect, slope, urban mask, distance to coast/roads/freshwater, foreshore mask, tidal mask)

## Classification Framework and Scenes
- Classification Scenes
  - GB: 32 tiles (based on a modified OS 100 x 100 km grid) to classify 50-band Seasonal Composite Images plus context rasters
  - NI: single 49-band Classification Scene (40-band Sentinel-2 seasonal composite + NI context rasters)
- Bootstrap Training
  - Automatic training process that uses historic land cover maps to generate training data
  - Uses parcels with >80% purity and consistent class across LCM2018–2020
  - Enables bootstrap samples for subsequent maps without fresh field data
- Random Forest Classification
  - Supervised learning using Bootstrap Training parcels to sample pixels for RF
  - 10,000 samples per bag, with replacement to balance class representation
  - Uses bespoke UKCEH software integrating WEKA, PostGIS, and GDAL (open source)

## Land Parcel Spatial Framework
- UK Land Parcel Spatial Framework (used for LCM2021)
  - Originated for LCM2007; minor updates since LCM2015
  - Parcels are ~0.5 ha MMU and represent discrete land units (fields, parks, urban areas, etc.)
  - 10 m Classified Pixels are not generalised by the Land Parcel framework to preserve detail
  - Parcel identifiers (gid) differ from LCM2015, impacting exact cross-map parcel matching

## Data Validation and Quality
- Validation
  - 35,182 validation points across all 21 classes
  - Composite reference data from GB countryside survey, National Forest Inventory, Rural Payments Agency, and bespoke validation points
  - Overall accuracy: 82.6% (95% CI: 82.19%–82.99%)
- Class-specific notes
  - Some spectral confusion among closely related habitats (e.g., various grasslands, bog, fen, heather)
  - Saltwater vs Freshwater distinctions rely on coastal/context layers; potential coastal misclassifications exist
  - Thorough appendix-driven guidance explains interpretation of classes and potential misclassifications

## Data Access, Standards, and Notes
- Coordinate systems and extents
  - Great Britain: British National Grid (EPSG 27700)
  - Northern Ireland: Irish Grid (TM75, EPSG 29903)
  - 10 m and 25 m datasets include per-country extents and naming conventions
- Output guidance
  - 10 m Classified Pixels provide detailed spatial structure; suitable for specialists
  - Land Parcels provide a change-detection-friendly fixed spatial framework
  - 1 km products are useful for broader-scale analysis and integration with other 1 km data
- Temporal considerations
  - Annual production aims to differentiate real changes from random classification noise
  - Continuous improvements are anticipated as methods evolve

## Appendices and Reference Information
- UKCEH Land Cover Classes and BAP Broad Habitats
  - Tables outlining relationships and distinctions between UKCEH classes and BAP Broad Habitats
  - Some BAP categories are split or merged to maintain consistency with spectral information
- Notes on UK BAP Broad Habitats (Appendix 1)
  - Descriptions and potential spectral confusion highlights for several habitat types
- Biodiversity Action Plan (Appendix 2)
  - Summaries of Broad Habitats definitions and their relevance to mapping
- Dataset lists and mappings (Appendix 3)
  - Full list of LCM2021 datasets for GB and NI
- Validation and correspondence (Appendix 4)
  - Matrices showing user’s and producer’s accuracies by class
- Colour recipes (Appendices 5 and 6)
  - Default and color-blind-friendly palettes for visualising UKCEH Land Cover Classes and their accessibility considerations

## Practical Considerations for Data Support and Use
- Choose 10 m Classified Pixels for detailed, near-field analysis; use Land Parcel framework for change detection and parcel-level assessment.
- Use 1 km products for broad-scale analyses or integration with other 1 km datasets; expect small rounding-induced totals in percentage layers.
- Be mindful of potential spectral confusion in complex habitats (e.g., certain grasslands, bog, heather) and use Context Rasters to mitigate confusion.
- When cross-referencing with LCM2015 or other historic maps, note that gid identifiers may not match exactly due to framework updates.
- Validation accuracy is robust overall, but class-level accuracy varies; consult Appendix 4 for producer’s and user’s accuracy by class.