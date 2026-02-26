# The UKCEH Land Cover Map 2023

## Overview
- UKCEH LCM2023 is the eleventh UK land cover map, providing 21 UKCEH Land Cover Classes linked to Biodiversity Action Plan (BAP) Broad Habitats.
- Produced annually using automated methods to enable change detection, aiming for temporal consistency and comparability.
- Validation shows an overall accuracy of 83%.
- Core methodology combines Sentinel-2 Seasonal Composite Images with Context Rasters, classified via Bootstrap Training and a Random Forest classifier.
- Data are organized into three primary geospatial datasets per region (Great Britain and Northern Ireland) plus a 1 km summary raster product: 10 m Classified Pixels, 25 m Rasterised Land Parcels, and Land Parcel (vector) datasets; plus 1 km summary rasters for GB and NI.

## Data Products (Dataset Descriptions)
- 10 m Classified Pixel datasets (GB and NI): mosaic of Classification Scenes; each pixel stores the most likely UKCEH Land Cover Class and the associated classification confidence.
- 25 m Rasterised Land Parcel datasets (GB and NI): blocks of 0.5 ha minimum mapping unit (MMU) aggregated from the 10 m data, carrying per-parcel attributes (dominant class, confidence, purity).
- Land Parcel products (GB and NI): vector parcels defined by the UKCEH Land Parcel Spatial Framework with fixed identifiers.
- 1 km Summary rasters (GB and NI): summarize 25 m rasters to 1 km cells, providing dominant class, aggregate dominance, and percentage cover per class/aggregate.
- Official dataset names and DOIs are provided for each product.

## Data Structure and Spatial Details
- Coordinate systems: Great Britain – British National Grid (EPSG:27700); Northern Ireland – Irish Grid TM75 (EPSG:29903).
- Pixel resolution: 10 m (pixels) and 25 m (rasters); 1 km summaries derived from 25 m data.
- Land Parcel Spatial Framework minimum mapping unit is ~0.5 ha; parcels group 10 m pixels to reduce noise and support change detection.
- Appendix 3 lists the full dataset catalogue; Appendix 5 and 6 provide colour recipes for mapping UKCEH Land Cover Classes (including color-blind friendly options).

## Methods and Production Pipeline
- Seasonal Composite Images: four-season Sentinel-2 composites (January–March, April–June, July–September, October–December) at 10 m, using bands 2,3,4,5,6,7,8,8a,11,12; gaps due to cloud are handled automatically.
- Context Rasters: 10 m layers to resolve spectral confusion (terrain, proximity to buildings/roads/coast, water, vegetation masks, etc.).
- Classification Scenes: GB uses 32 tiles; NI uses a single Scene covering the landmass; training is scene-specific.
- Bootstrap Training: automatic training set generated from historic LCMs (LCM2020–2022) by selecting pixels with >80% probability and consistent class across three years; reduces need for field data.
- Random Forest: balanced sampling (10,000 samples per bag) to train the classifier; implemented with a bespoke software stack integrating Weka, PostGIS, and GDAL.
- LCM2023 validation: 33,107 reference points across all 21 classes; overall accuracy 83%.

## Data Access and Citation
- Each LCM2023 dataset has a DOI; recommended citation provided (including Marston et al. 2023/2024 and Morton et al. 2011 references).
- Users should cite the appropriate dataset DOI(s) when using the data.
- Note: some methodological updates in newer maps may introduce small changes unrelated to actual land-cover change.

## Quality, Validation, and Known Issues
- Validation indicates 83% overall accuracy across 21 classes; class-level producer’s and user’s accuracies vary by class.
- Known issues: a small number of polygons missing from vector land parcel products, causing nodata regions in 25 m raster parcels (negligible effect on 1 km rasters; 10 m pixels unaffected).
- Caution: annual maps may reflect both real change and methodological differences; use time series to differentiate real change from methodological effects.

## How This Supports Environmental Analysis
- Standardised, time-series land cover data facilitate monitoring of environment health and policy performance over time.
- High spatial detail (10 m) plus parcel-level and 1 km summaries support detailed habitat assessments and broad-scale change detection.
- Bootstrap Training and annual production improve ability to distinguish true land cover change from classification noise, aiding trend analyses and policy evaluation.

## Appendices and Supporting Information (Highlights)
- Appendix 1: Notes on UKCEH Land Cover Classes and crosswalks with BAP Broad Habitats; nuances in class definitions and potential spectral confusions.
- Appendix 2: Summary of BAP Broad Habitats definitions to aid interpretation of classes.
- Appendix 4: Detailed correspondence matrices (class-to-class confusion) from validation.
- Appendices 5–6: Color recipes for displaying classes (including color-blind friendly options) and accompanying QGIS symbol files.