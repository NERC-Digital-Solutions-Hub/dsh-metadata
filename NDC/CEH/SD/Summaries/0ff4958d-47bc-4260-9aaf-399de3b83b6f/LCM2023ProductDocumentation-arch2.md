# The UKCEH Land Cover Map for 2023

- The LCM2023 is the eleventh UK Land Cover Map produced by UKCEH, intended to map the UK’s land cover annually using standardized methods to support monitoring of environmental state and change.
- Product suite includes three geospatial datasets for Great Britain and Northern Ireland (10 m classified pixels, land parcels, and 25 m rasterised land parcels) plus a 1 km summary raster product covering GB+NI.

## Purpose and scope
- Provides a consistent, validated view of land cover to support monitoring of environmental health and policy performance over time.
- Aims to maximise temporal consistency, comparability, and change detection; annual production helps distinguish real change from classification error.
- Formal validation reports an overall accuracy of 83% at full thematic detail.

## Product suite and data formats
- 10 m Classified Pixel datasets (GB and NI): per-pixel land cover class with a second band giving the class membership probability (confidence).
- Land Parcel datasets: derived by intersecting the 10 m pixels with a UKCEH Land Parcel Spatial Framework to generate parcel attributes.
- 25 m Rasterised Land Parcel datasets: raster versions of parcels with three bands (dominant land cover class, mean confidence, and purity).
- 1 km Raster Summary products: summarize 25 m data to give dominant class, percentage cover per class, and percentage cover per aggregate class.
- Appendix 3 lists official dataset names and DOIs; Table 5 provides citation information for each data product.

## Key concepts and classifications
- Land cover is described by 21 UKCEH Land Cover Classes, anchored to Biodiversity Action Plan (BAP) Broad Habitats for comparability, with careful labeling and occasional cross-referencing to BAP terminology.
- The dataset includes a broad range of land cover types: Broadleaved and Coniferous woodland, Arable, Improved/Neutral/Calcareous/Acid grasslands, Bracken, Heather and Heather grassland, Bog, Fen/Marsh/Swamp, Inland Rock, Saltwater, Freshwater, Coastal (Supralittoral/Littoral, Rock/Sediment/Saltmarsh), Urban and Suburban.

## Production methods and pipeline
- Seasonal Composite Images: Sentinel-2 data resampled to 10 m, with four seasonal composites (Jan–Mar, Apr–Jun, Jul–Sep, Oct–Dec) to capture phenology; 12-band or 13-band configurations used in classification.
- Context Rasters: 10 m context layers to reduce spectral confusion, including terrain (height, aspect, slope) and proximity masks (distance to buildings/roads, near coastal/freshwater features, foreshore, woodland, saltmarsh).
- Classification Scenes: GB classified using 32 tiles (100 x 100 km grid); NI uses a single Scene; some tiles are enlarged to accommodate coastal/sea coverage.
- Bootstrap Training: automatic training data generated from historic LCM maps (2020–2022) with pixels of >80% probability and consistent class across three years; used to train a Random Forest classifier, enabling training without fresh field data.
- Random Forest: Balanced training with 10,000 samples per class per bag; the classifier yields the most probable class and its associated probability/confidence.
- Software: bespoke UKCEH pipeline integrating Weka, PostGIS, and GDAL (open source).

## Data structure and accessibility
- 10 m Classified Pixels (GB): two-band raster; Band 1 = most likely UKCEH Land Cover Class, Band 2 = mean probability/confidence.
- 25 m Rasterised Land Parcels (GB/NI): three-band rasters—dominant land cover class (_mode), confidence (_conf), and purity (_purity).
- Land Parcel Spatial Framework: parcel geometries with a ~0.5 ha minimum area; parcels provide stable units for change detection and dataset simplification.
- 1 km Summary Rasters: include dominant class rasters (1 band) and two 1 km-layer sets for class/aggregate class percentages (21 and 10 bands respectively); area rounding can cause sums to vary slightly from 100%.

## Validation and accuracy
- Validation dataset: 33,107 points across all 21 classes; compiled from countryside surveys, open data inventories, and bespoke validation points.
- Overall accuracy: 83% for the 21-class product; validation metrics include user’s and producer’s accuracy by class and confusion matrices (Appendix 4).

## Known issues and caveats
- A small number of polygons are missing from vector land parcel products, causing nodata areas in the 25 m rasterised parcels; effect is negligible for 1 km products; 10 m classified pixels remain unaffected.
- Differences between consecutive LCMs may reflect real land cover change and methodological updates; annual maps are subject to evolving methods.

## Appendices and interpretation notes
- Appendices provide detailed notes on UKCEH Land Cover Classes and their relationship to UK BAP Broad Habitats, including guidance on interpretive nuances and potential spectral confusions (e.g., between arable and grassland, peat/dense vegetation, or coastal/water classes).
- Appendix 5 & 6 supply recommended colour recipes for displaying land cover classes (including color-blind friendly options) and accompanying QGIS symbol files.
- The document emphasises ongoing methodological evolution: improvements may be applied across the full catalogue when accuracy gains are significant, with implications for temporal comparability.

## How to cite and data access
- Each LCM2023 dataset has a DOI; citations are provided in Table 5 and corresponding references (including Marston et al. 2023, 2024a–g) for production methods and data products.
- Data availability and DOIs enable reuse for monitoring the environment, trend analysis, and policy evaluation.