# The UKCEH Land Cover Map for 2021

- This document is the user guide for UKCEH LCM2021, detailing data production, validation, and accuracy to help users apply the land cover data in current and future work.
- LCM2021 is the ninth UK land cover map, delivering 21 UKCEH Land Cover Classes derived from Biodiversity Broad Habitats (BAP), with annual updates to support change detection and temporal consistency.

## Product structure and datasets

- Three geospatial dataset types for Great Britain and Northern Ireland (six datasets total):
  - 10 m Classified Pixel datasets: per-pixel land cover classification with a second band indicating classification probability/confidence; first band is the most likely UKCEH Land Cover Class. These pixels are not generalised by the UKCEH Land Parcel Spatial Framework to preserve fine features.
  - Land Parcel datasets: classify an independent Land Parcel Spatial Framework, producing parcel-level attributes derived from the 10 m pixels (parcel-level statistics and metadata).
  - 25 m Rasterised Land Parcel datasets: rasterised version of parcels (3-band rasters: dominant land cover, confidence, and purity) aligned to 25 m pixels.
- 1 km raster products (derived from 25 m data): dominant class and percentage cover for both UKCEH Land Cover Classes (21 bands) and UK BAP Broad Habitats (10 bands); percentages are integer values with rounding caveats near 100%.
- Seasonal Composite Images and Context Rasters:
  - Seasonal Composite Images: four-season Sentinel-2 composites (Jan–Mar, Apr–Jun, Jul–Sep, Oct–Dec) derived from Google Earth Engine; 50-band data per Classification Scene for GB and 49-band scene for Northern Ireland.
  - Context Rasters: 10 m context layers to reduce spectral confusion (GB includes terrain, proximity to buildings/roads/coast, foreshore, tidal water, woodland mask; NI includes terrain, urban mask, and proximity layers).
- Classification Scenes:
  - GB uses a grid of roughly 100 x 100 km tiles (32 Classification Scenes) to cover GB with training and classification per scene.
  - Northern Ireland uses a single Classification Scene (minimum bounding rectangle of NI land mass) with 40 Sentinel-2 bands plus NI context rasters (49 bands total).
- Coordinate systems and extents:
  - GB: British National Grid (EPSG:27700); extent approx. 0–700000 E, 0–1300000 N.
  - NI: Irish Grid (TM75, EPSG:29903); extent truncated to NI land mass.
- Data products and naming (Appendix 3 lists official dataset names for GB and NI).

## How LCM2021 is produced

- Bootstrap Training and Random Forest:
  - Bootstrap Training uses historic land cover maps (LCM2018–LCM2020) to automatically generate training observations, reducing the need for new field data.
  - Training parcels are filtered to >80% purity and consistent class across three years to form training data.
  - A Random Forest classifier uses 10,000 samples per class (with replacement) to balance learning and produce per-pixel classifications.
  - Software stack combines Weka, PostGIS, and GDAL (all open source).
- Band composition and classification:
  - Classification Scenes combine 50-band Seasonal Composite Images with 10 Context Layers to classify pixels into UKCEH Land Cover Classes.
  - The process aims to maximize temporal consistency, support change detection, and differentiate real land cover change from random errors.
- Validation and accuracy:
  - Validation uses 35,182 points across all 21 classes, derived from GB countryside surveys, open data inventories, and bespoke validation points.
  - Overall accuracy for LCM2021 is 82.6% (95% CI: 82.19%–82.99%).

## Data context and relationships

- 21 UKCEH Land Cover Classes are linked to UK BAP Broad Habitats; some classes differ between the two schemes. Appendices provide detailed crosswalks and note that UKCEH classes are designed for satellite remote sensing, while BAP Broad Habitats were originally field-based.
- The relationship is maintained through crosswalk notes, with some Broad Habitats split or combined to align with spectral separability and mapping considerations.
- The UK Land Parcel Spatial Framework supports parcel-based change detection by aggregating 10 m pixels into discrete land parcels, typically ≥0.5 ha (the MMU).

## Data quality, limitations, and guidance

- The 10 m Classified Pixel dataset preserves detailed landscape features but has not been validated directly against the 10 m pixel data; validation was performed against the 25 m Land Parcel dataset. Users should consider this when applying the 10 m layer, particularly for non-specialist analyses.
- Validation results indicate some inter-class confusion, especially among grassland, bog, fen, and heath types; context rasters and seasonal signals help mitigate confusion but may not fully resolve all ambiguities.
- The parcel-based products provide richer metadata (e.g., _hist, _mode, _purity, _conf, _stdev, _agg, _n) to support quality assessment and change detection.
- The annual production supports distinguishing random errors from real change over time, as genuine changes persist across years while random errors flicker.

## Practical usage notes

- Use 10 m classified pixels for detailed mapping and exploratory analyses by specialists; combine with parcel data for stable change detection and time-series analyses.
- Use 1 km percentage/dominant products for broad-scale summaries and policy-level assessments where high spatial detail is less critical.
- Refer to the crosswalks with BAP Broad Habitats for interpretation when aligning with biodiversity frameworks.
- For visualization, recommended color schemes and color-blind friendly palettes are provided in Appendices 5 and 6.

## Accessibility and references

- Core datasets are available as GB and NI collections with explicit dataset names and metadata (Appendix 3).
- Key methodological references include bootstrap training concepts, random forests, and validation practices (Breiman 2001; Carrasco et al. 2019; Morton et al. 2011; Jackson 2000; Smith et al. 2007).
- LCM2021 aims to be updated with significant methodological improvements when accuracy gains are demonstrated, to improve temporal comparability and change detection.

- Overall accuracy: 82.6% (95% CI 82.19%–82.99%) across 35,182 validation points.