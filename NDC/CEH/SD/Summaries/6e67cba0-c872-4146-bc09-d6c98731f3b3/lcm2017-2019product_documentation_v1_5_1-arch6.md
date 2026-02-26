# The UKCEH Land Cover Maps for 2017, 2018 and 2019 v1.5.1

## Purpose and scope
- User guide accompanying the release of three UKCEH Land Cover Maps: LCM2017, LCM2018, and LCM2019.
- Maps present 21 UKCEH Land Cover Classes (based on Biodiversity Action Plan Broad Habitats) and aim to support wide-scale land cover monitoring and change detection.
- Outputs are produced automatically using Bootstrap Training with a Random Forest classifier to enable rapid, nationwide updates (intended to be annual).

## Data structure and datasets
- Datasets provided for each year (GB and Northern Ireland): 20m Classified Pixels, Land Parcels, 25m Rasterised Land Parcels, and 1km raster products.
- 42 datasets in total (across GB and NI) per year, with full metadata and documentation.
- Data products and their extents:
  - 20m Classified Pixels: two-band rasters (Band 1 = most likely class, Band 2 = class membership probability 0–100). Preserves fine detail; not generalised by parcel framework.
  - Land Parcels: attributes derived by intersecting 20m Classified Pixels with the UKCEH Land Parcel Spatial Framework (MMU ~0.5 ha); includes per-parcel hist, mode, purity, confidence, and other metrics.
  - 25m Rasterised Land Parcels: three-band rasters (Band 1 = modal class, Band 2 = average confidence, Band 3 = parcel purity).
  - 1km Raster datasets: 
    - 1km Percent Cover: 21-band (per-class) percentage cover.
    - 1km Percent Aggregate Cover: 10-band (per-aggregate class) percentages.
    - 1km Dominant Cover: single-band dominant class.
    - 1km Dominant Aggregate Cover: single-band dominant aggregate class.
- GB and NI coordinate systems:
  - GB: EPSG:27700 (British National Grid)
  - NI: EPSG:29903 (Irish Grid)
- Dataset generation includes a 20m Classified Pixels layer plus subsequent summarisation into higher-level products.

## Production methodology
- Bootstrap Training: automatic generation of training data from historic UKCEH maps (primarily LCM2015) to support new classifications. Sampling focused on majority signal to mitigate changes over time.
- Random Forest classification: static training sets created to balance classes; 10,000 samples per class per Classification Scene; automatic, bespoke software integrating Weka with PostGIS and GDAL.
- Seasonal information: classification uses Sentinel-2 Seasonal Composite Images (TOA reflectance) by season (winter, spring, summer, autumn) plus 20m Context Rasters to reduce spectral confusion.
- Classification Scenes and tiling:
  - Great Britain: 100x100 km tiles; 36-band Seasonal Composite Images plus 10 Context Layers; 46-band GB Classification Scenes; 74 overlapping scenes classified independently. Visual checks resolve overlaps to select best results.
  - Northern Ireland: a single 43-band Classification Scene per year, based on minimum bounding rectangle of NI land mass.
- Context rasters (20m) used to improve discrimination between spectrally similar classes; GB and NI include different context layers (e.g., height, slope, distances to roads/coast, urban/foreshore masks).
- UKCEH Land Parcel Spatial Framework: framework to summarise 20m pixels into parcels; modifications to indices enable faster processing; gid identifiers change between LCM2015 and LCM2017–2019 (not suitable for direct cross-map parcel-id comparisons).

## Validation and accuracy
- Validation performed at UK scale against multiple sources (GB countryside survey 2019, National Forest Inventory, IACS, bespoke validation points).
- Total validation points: 22,325.
- Reported overall accuracy (per year):
  - LCM2017: 78.6%
  - LCM2018: 79.6%
  - LCM2019: 79.4%
- Notes:
  - Validation uses data with slightly different class definitions; conversions introduce subjectivity.
  - Approximately 80% correspondence indicates substantial current performance; accuracy is expected to improve as methods mature.
  - Validation datasets are not absolute truth and reflect the currency and comparability of inputs.

## Class framework and presentation
- 21 UKCEH Land Cover Classes, mapped from Biodiversity Action Plan Broad Habitats; relationships and nuances between UKCEH classes and BAP Broad Habitats are described in appendices (e.g., how some BAP classes are subdivided or merged for remote sensing detection).
- Appendix material provides guidance on interpretation, class relationships, and color-coding for visualization.
- Outputs are designed for self-service use, enabling downstream users to explore land cover dynamics and perform change detection across the annual series.

## Data usage notes and considerations
- Manual corrections: the 2017–2019 releases were produced automatically with no manual corrections (to enable annual production). Visual checks and validation still applied to ensure quality.
- Temporal consistency: annual LCMs are designed to detect land cover change, with attention to maintaining a consistent class sequence to support change detection over time.
- Cross-version comparisons: due to changes in the Land Parcel Spatial Framework, parcel identifiers (gid) do not match between LCM2015 and later maps; comparison across years is better done via spatial overlap rather than parcel-id equivalence.
- Satellite data considerations: Sentinel-2 TOA data were used for these maps; near-future iterations may incorporate additional data sources (e.g., SAR) or alternative optical inputs to fill gaps.
- Output accessibility: GB and NI data are provided with clear metadata and are suitable for a broad range of applications, including policy, planning, and environmental monitoring.

## Future plans and ongoing development
- Annual release cadence: intent to release a new LCM annually (LCM2020 planned for 2021; bootstrap approach to be based on majority signals across years).
- Method evolution: bootstrap training strategies and classifier refinements anticipated; exploration of additional data sources and methods to improve accuracy and coverage.
- Possible enhancements: broader use of alternative input data, expanded context around upland habitats, and potential fine-tuning of class delineations to improve remote-sensing detectability.