# The UKCEH Land Cover Map for 2021

- UKCEH Land Cover Map 2021 (LCM2021) documentation describing data production, validation, accuracy, and how to use six geospatial datasets (three per region: Great Britain and Northern Ireland): 10 m Classified Pixels, Land Parcel Spatial Framework, and 25 m Rasterised Land Parcels. Includes 1 km summary rasters for GB and NI.
- Purpose: help users understand data structure, production steps, quality/accuracy, and appropriate use for current and future work.

## Data Products and Formats

- 10 m Classified Pixel datasets (GB and NI)
  - Generated from classified Classification Scenes; Random Forest yields a most-likely class and a second band with the class confidence.
  - First band: UKCEH Land Cover Class ID; second band: classification probability.
  - Not generalised by the Land Parcel Spatial Framework to preserve fine landscape details; intended for specialist use. Validation focused on Land Parcel data, not the 10 m pixels.
- Land Parcel datasets (GB and NI)
  - Created by intersecting 10 m pixels with the UKCEH Land Parcel Spatial Framework.
  - Provide parcel-level attributes (e.g., _hist, _mode, _conf, _stdev, _agg, _n) and class-specific summaries.
- 25 m Rasterised Land Parcel datasets (GB and NI)
  - Rasterised from Land Parcel data; 3-band rasters conveying per-parcel dominant class (mode), mean confidence (_conf), and purity (_purity).
- 1 km Summary Rasters (GB and NI)
  - Summaries derived from 25 m rasters:
    - Dominant cover for LCM2021 classes (1-band)
    - Dominant cover for LCM2021 Aggregate classes (1-band)
    - Percentage cover for LCM2021 classes (21 bands)
    - Percentage cover for Aggregate classes (10 bands)
  - Percentage values are rounded; sums near coast may be slightly below 100 due to mapping resolution.
- Spatial reference and extents
  - Great Britain: British National Grid (EPSG 27700)
  - Northern Ireland: Irish Grid (TM75, EPSG 29903)
  - Datasets include extensive metadata (Table 2, Appendix 3).

## Production Pipeline and Methodology

- Seasonal Composite Images
  - Derived from Google Earth Engine; Sentinel-2 data resampled to 10 m; four seasonal medians (Jan–Mar, Apr–Jun, Jul–Sep, Oct–Dec) using bands 2,3,4,5,6,7,8,8A,11,12.
  - Some gaps may occur due to cloud; the classifier tolerates partial spectral information.
- Context Rasters
  - 10 m context layers added to reduce spectral confusion:
    - GB: height, aspect, slope; distance to buildings, roads, sea, freshwater; foreshore and tidal masks; woodland mask.
    - NI: height, aspect, slope; urban mask; distances to coast, freshwater, roads; foreshore and tidal masks.
- Classification Scenes
  - GB: a grid of roughly 100 x 100 km tiles (classification scenes); 32 scenes yield full GB coverage; some tiles enlarged to accommodate sea areas.
  - NI: single Classification Scene (40-band Sentinel-2 Seasonal Composite + NI context rasters) yielding 49-band classification scene.
- Bootstrap Training
  - Automatic training using historic LCMs (2018–2020); select land parcels with >80% purity classified consistently across three years.
  - Bootstrap Training enables sampling of current imagery without new field data; large training sets improve robustness.
- Random Forest Classification
  - Balanced sampling: 10,000 samples per class per bag; sampling with replacement ensures equal representation.
  - Custom software integrating WEKA, PostGIS, and GDAL.
- Validation
  - 35,182 validation points across 21 classes; independent composite dataset from GB countryside survey, National Forest Inventory, Rural Payments Agency, and bespoke validation points.
  - Overall accuracy: 82.6% (95% CI 82.19%–82.99%).
  - Appendix 4 contains per-class confusion matrices and accuracy metrics (producer’s and user’s accuracy).

## UKCEH Land Parcel Spatial Framework

- Parcels have a minimum area of ~0.5 ha (MMU); designed to represent discrete real-world units (fields, parks, urban areas, etc.).
- Parcels reduce classification noise and provide a stable structure for time-series change detection.
- Unique parcel identifiers (gid) do not match LCM2015 identifiers due to framework reordering and index changes.

## Relationship to Biodiversity Action Plan (BAP) Broad Habitats

- UKCEH Land Cover Classes (21) are related to BAP Broad Habitats but are not identical; a crosswalk exists (Appendices 1–2).
- Some habitats are split or aggregated to better align with satellite imagery, with careful notes on ambiguity and potential misclassification (e.g., Bracken, Heather, Bog, Saltwater vs Freshwater).
- Appendices provide detailed definitions and mapping considerations to support interpretation and cross-referencing with BAP Broad Habitats.

## Practical Guidance for Data Support

- Use-cases and interpretation
  - 10 m dataset provides fine-grained detail but may introduce classification noise; use 25 m parcels for stable, generalized outputs and robust change detection.
  1 km rasters offer consistent aggregation suitable for wide-area analyses.
- Temporal dynamics
  - Bootstrap Training enables annual updates; changes that persist across years are more likely real, whereas random errors tend to flicker.
- Coastal and water classifications
  - Saltwater vs Freshwater and Saltmarsh can be challenging near coasts; context rasters and proximity features aid differentiation but some confusion remains.
- Continuous improvement
  - UKCEH aims to improve methods; outputs may be updated across the catalog to maximize temporal consistency and change detection potential.

## Access, Visualization, and Supporting Materials

- Appendix 5 and 6 provide recommended color schemes for displaying UKCEH Land Cover Classes, including color-blind friendly options.
- QGIS symbol files (lcm_raster.qml and lcm_raster_cb_friendly.qml) accompany data products for immediate mapping use.
- Appendix 3 lists dataset names and full citations for each LCM2021 data product.
- Appendix 4 contains comprehensive correspondence matrices (confusion matrices) detailing class-level accuracy and producer’s/user’s accuracy.