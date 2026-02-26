# The UKCEH Land Cover Maps for 2017, 2018 and 2019 v1.6

## Overview and purpose
- Release of three UKCEH Land Cover Maps: LCM2017, LCM2018, and LCM2019.
- All maps present 21 UKCEH Land Cover Classes based on Biodiversity Action Plan (BAP) Broad Habitats, aligned with LCM2015 conventions.
- Map production is automated, using Bootstrap Training and Random Forest classification to enable annual updates.
- Sentinel-2 Seasonal Composite Images (TOA reflectance) are used, combined with 20m Context Rasters to create Classification Scenes.
- Goal: rapid, UK-wide land cover mapping with a basis for change detection, avoiding manual corrections to enable annual updates.

## Data products and structure
- 42 datasets in total (GB and Northern Ireland, year-specific): 
  - 20m Classified Pixels (new addition)
  - Land Parcels
  - 25m Rasterised Land Parcels
  - 1km Dominant Covers and Percent/Percent Aggregate Covers (both 21-band and 10-band schemes)
- Dataset specifics:
  - 20m Classified Pixels: two-band, 8-bit rasters; band 1 = most likely UKCEH Land Cover Class, band 2 = class membership probability (0–100) as a confidence indicator; preserves fine landscape detail (no parcel generalisation).
  - Land Parcels: attributes including gid, _hist, _mode, _purity, _conf, _stdev, _n; parcel-level summaries derived from intersecting 20m Classified Pixels with the UKCEH Land Parcel Spatial Framework.
  - 25m Rasterised Land Parcels: three-band rasters (band 1 = _mode, band 2 = _conf, band 3 = _purity).
  - 1km products: 1km Percent Cover (21 bands), 1km Percent Aggregate Cover (10 bands), 1km Dominant Cover (1 band), 1km Dominant Aggregate Cover (1 band).
- Spatial coverage and formats:
  - Great Britain (GB) and Northern Ireland (NI) versions; GB uses EPSG:27700, NI uses EPSG:29903.
  - 21 UKCEH Land Cover Classes; 10 UKCEH Aggregate Classes.
  - Appendix 6 lists the full dataset names and structures.

## Production approach and methodology
- Bootstrap Training:
  - Training data derived from UKCEH LCM2015 training observations; selects high-purity parcels (≥99% _purity) to bootstrap the classifier.
  - Bootstrap training sets provide large, majority-signal data to train the RF classifier.
- Random Forest classification:
  - Pixel-level classification across Classification Scenes; 10,000 samples per class per scene; balancing across 21 classes via sampling with replacement.
  - Production relies on bespoke UKCEH software integrating WEKA, PostGIS, and GDAL (open source).
- Classification Scenes and tiling:
  - Great Britain: 74 overlapping 100x100 km GB Classification Scenes; NI: single 43-band scene per year for the NI extent.
  - Scenes combine 46-band data (spectral bands + context layers) per scene.
- Context rasters:
  - 20m GB rasters: height, aspect, slope, distances to buildings/roads/sea/freshwater, foreshore, tidal water, woodland.
  - NI rasters: height, aspect, slope, urban mask, distance to coast/freshwater/road.
- Seasonal data:
  - Seasonal Composite Images derived from four 3-band Sentinel-2 polars per season (TOA reflectance), using 9 bands; some seasons may have cloud gaps, which are handled by the classifier.

## Validation and quality
- Validation against GB countryside survey (2019), National Forest Inventory, IACS, and bespoke validation points (≈22,325 points).
- UK-scale accuracy:
  - LCM2017: 78.6%
  - LCM2018: 79.6%
  - LCM2019: 79.4%
- Notes:
  - Validation uses crosswalks from multiple data sources; not a perfect ground truth due to class definitional differences and potential misclassification.
  - The same validation data were used across products; 80% correspondence is considered a strong indicator given automatic, annual maps.
  - Appendix 5 contains detailed confusion matrices and per-class metrics.

## Key technical details and caveats
- Classification outputs are automatically generated; no manual corrections were applied this cycle to enable annual updates. Visual checks and validation were performed.
- Gids (gid) for Land Parcels differ from LCM2015; cross-year parcel comparisons should use gid-based matching, not parcel geometry overlap, for LCM2017–2019 comparisons.
- 20m Classified Pixels preserve detail; Land Parcels provide a fixed structure for change detection but may introduce attribute changes due to framework updates.
- 1km products provide area-aggregated perspectives (Percent Cover, Dominant, etc.); percentages are rounded to integers; coastal sums may be slightly less than 100%.
- The 20m Classified Pixels are not generalised by the Land Parcel Spatial Framework, allowing finer features (e.g., narrow patches) to remain visible.
- TOA-based Sentinel-2 data were used (not SR) due to lack of observed improvement with SR at current thematic resolution; potential future enhancements may test broader input data.

## Relationship to BAP Broad Habitats and display
- 21 UKCEH Land Cover Classes are tied to BAP Broad Habitats; Appendix 2 provides summaries and cross-relationships; some classes are refined (e.g., Heather vs Heather Grassland) to reflect detection challenges.
- Display color schemes and color-blind friendly variants are provided (Appendix 3 and Appendix 4) with QGIS symbology files.

## Practical usage and guidance for data support
- Outputs enable self-serve exploration of UK land cover dynamics, with multi-scale summaries (pixel-level to parcel-level to 1km grids).
- For temporal change analysis, prefer using Land Parcels with gid-based comparisons or 20m Classified Pixels over time, acknowledging minor attribute changes due to framework updates.
- When integrating with other datasets, be aware of the class mappings to BAP Broad Habitats and the potential need for reclassification or harmonisation.
- For applications requiring up-to-date thematic detail, note the annual cycle and the lack of manual corrections in 2017–2019; consider supplementary validation where high precision is required.

## Appendices and resources
- Appendix 1–2: BAP Broad Habitat definitions and mappings to UKCEH Land Cover Classes.
- Appendix 3–4: Recommended color schemes for display; color-blind friendly variants; accompanying QGIS symbology files.
- Appendix 5: Detailed confusion matrices and accuracy statistics by year and class.
- Appendix 6: Full list of datasets per year and per product, with GB/NI distinctions.