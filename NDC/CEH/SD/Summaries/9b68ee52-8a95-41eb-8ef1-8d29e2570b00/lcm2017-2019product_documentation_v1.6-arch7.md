# The UKCEH Land Cover Maps for 2017, 2018 and 2019 v1.6 18/06/2020

## Purpose and scope
- Provides user guide for three new UKCEH Land Cover Maps: LCM2017, LCM2018, LCM2019.
- Maps 21 UKCEH Land Cover Classes (based on BAP Broad Habitats) and an accompanying UKCEH Aggregate Classes set.
- All three maps produced automatically using Bootstrap Training with a Random Forest classifier; no manual corrections in this release.
- Aims to enable rapid, annual UK-wide land cover mapping and support informed use in current and future work.
- Visual checks and formal validation performed; quality judged similar to LCM2015.

## Data and conceptual framework
- 21 UKCEH Land Cover Classes (mapped from BAP Broad Habitats) with careful terminology used to reduce ambiguity; UKCEH Aggregate Classes (10 classes) available for generalized use.
- Terminology and class relationships explained; some notes on differences between BAP Broad Habitats and UKCEH Land Cover Classes.
- Land Parcel Spatial Framework used to summarise 20m classified pixels into parcels; gid identifiers differ from LCM2015 for cross-year consistency.

## Production workflow and data structure
- Sentinel-2 Seasonal Composite Images (TOA reflectance) used per season; nine Sentinel-2 bands; seasonal gaps represented as nulls.
- Seasonal composites combined with 20m Context Rasters (contextual information) to form Classification Scenes.
- Bootstrap Training: historical LCM2015 data used to generate training observations; majority signal across years guides bootstrap for subsequent maps.
- Random Forest classification trained on 10,000 samples per class; balanced sampling to handle rare classes.
- GB production: 74 overlapping Classification Scenes (100x100 km tiles) classified independently; NI production: a single 43-band Classification Scene per year.
- 20m Classified Pixels: new addition; two-band rasters (Band 1 = predicted class; Band 2 = per-pixel class membership probability 0–100).
- 25m Rasterised Land Parcels: rasterised version of Land Parcels, 3 bands: _mode, _conf, _purity.
- Land Parcels: attributes include gid, _hist (pixel distribution per class), _mode (dominant class), _purity, _conf, _stdev, _n; some attribute names changed from LCM2015.
- 1km rasters: Summaries derived per 1km square from 25m parcels:
  - 1km Percent Cover: 21-band, 8-bit rasters (per-class percent cover).
  - 1km Percent Aggregate Cover: 10-band, 8-bit rasters (aggregate classes).
  - 1km Dominant Cover: 1-band, 8-bit (dominant class).
  - 1km Dominant Aggregate Cover: 1-band, 8-bit (dominant aggregate class).
- Datasets are produced for GB (Great Britain) in British National Grid (EPSG:27700) and NI (Northern Ireland) in Irish Grid (EPSG:29903); 42 datasets per year, duplicated across years (total 126 across three years).

## Data contents and examples
- 20m Classified Pixels preserve detailed landscape features; 25m Rasterised Land Parcels generalise features (parcels dissolve to 25m).
- 1km products provide coarser summaries and fast overviews; sums may not equal exactly 100% due to rounding.
- Visualization aids: dataset examples show how 20m pixels retain detail versus 25m parcels and 1km summaries.

## Validation and accuracy
- UK-wide validation against countryside survey 2019 data, National Forest Inventory, IACS, and bespoke validation points (22,325 locations).
- Reported accuracies (proportional correspondence with UKCEH classes):
  - LCM2017: 78.6%
  - LCM2018: 79.6%
  - LCM2019: 79.4%
- Validation uses a common set of points; some correspondences are approximate due to class-definition differences; overall near 80% correspondence is strong for automatic mapping.

## Spatial framework and year-to-year considerations
- UKCEH Land Parcel Spatial Framework geometry unchanged since LCM2015; indices re-ordered for performance, so parcel identifiers (gid) differ from LCM2015 (cross-year parcel comparisons require gid-based linking).
- Land Parcels generally ~0.5 ha minimum (minimum mappable unit); designed to stabilise change detection and provide discrete real-world units.
- Bootstrap Training and annual updates rely on majority signals across years; changes to class definitions are careful to maintain comparability.

## Class definitions and biodiversity context
- Appendix and accompanying notes provide in-depth definitions for UK BAP Broad Habitats (e.g., Broadleaved Woodland, Coniferous Woodland, Arable, Improved Grassland, Neutral Grassland, Calcareous Grassland, Acid Grassland, Bracken, Heather, Bog, Fen/Marsh/Swamp, Inland Rock, Urban, Suburban, Saltmarsh, etc.).
- Discussion of detection limitations and spectral variability; context rasters improve discrimination for some difficult classes (e.g., Neutral Grassland, Bracken).
- Notes on potential future refinements (upland habitats, peatland vegetation) as training data improve.

## Visualization and data styling
- Appendix includes recommended color recipes for displaying UKCEH Land Cover Classes (standard and color-blind friendly options).
- QGIS symbol files provided (lcm_raster.qml and lcm_raster_cb_friendly.qml) to assist mapping.

## Product validation and cross-year considerations
- Confusion matrices (LCMs2017, 2018, 2019) illustrate per-class accuracies and common misclassifications; producer’s and user’s accuracy figures indicate overall reliability and class-specific performance.
- Validation data and class mappings may require translation when comparing to older products; Appendix provides translation guidance and mapping notes.

## Future directions and usage notes
- UKCEH plans annual LCM releases going forward; exploration of additional data sources (e.g., Sentinel-1, alternative optical sources) to fill potential seasonal gaps.
- The new 20m Classified Pixels enable richer downstream analyses and bespoke parcel-based summaries; the Land Parcels and 25m Rasterised Parcels provide stable, switchable structures for time-series analysis.
- Users should consider class-definition nuances and validation caveats when performing change detection or cross-product comparisons.