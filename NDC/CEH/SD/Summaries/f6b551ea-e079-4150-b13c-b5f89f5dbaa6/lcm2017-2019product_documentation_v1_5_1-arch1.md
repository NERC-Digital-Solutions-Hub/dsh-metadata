# The UKCEH Land Cover Maps for 2017, 2018 and 2019 v1.5.1

- Purpose and scope
  - Release of three new UKCEH Land Cover Maps: LCM2017, LCM2018, and LCM2019.
  - All maps use 21 UKCEH Land Cover Classes (based on Biodiversity Action Plan Broad Habitats) and are produced automatically.
  - Production combines Bootstrap Training with a Random Forest classifier, using Sentinel-2 Seasonal Composite Images (TOA reflectance) and 20m Context Rasters to create Classification Scenes.
  - Aims to deliver annual UK-wide maps with rapid production and minimal manual correction.

- Key data products and structure
  - 20m Classified Pixels (core product; GB and NI)
    - Each pixel receives a predicted class (Band 1) and a per-pixel confidence (Band 2, 0–100).
    - Preserves fine landscape detail; not generalized by land parcels.
  - Land Parcels
    - Intersects 20m Classified Pixels with the UKCEH Land Parcel Spatial Framework.
    - Attributes include gid (parcel ID), _hist (class frequency per parcel as tuples), _mode (dominant class), _purity (percentage of modal class), _conf (mean class probability), _stdev, _n (number of pixels).
    - Note: gid values differ from LCM2015; used for temporal comparison via spatial overlap or, preferably, parcel overlap.
  - 25m Rasterised Land Parcels
    - 3-band raster: band 1 = _mode, band 2 = _conf, band 3 = _purity.
  - 1km Raster datasets
    - 1km Percent Cover: 21-band, 8-bit raster (percentage cover per class).
    - 1km Percent Aggregate Cover: 10-band, 8-bit raster (percentage cover per UKCEH Aggregate Class).
    - 1km Dominant Cover: 1-band raster (dominant class per 1km grid).
    - 1km Dominant Aggregate Cover: 1-band raster (dominant aggregate class per 1km grid).

- Spatial scope and coordinate systems
  - Great Britain: British National Grid (EPSG: 27700)
  - Northern Ireland: Irish Grid (TM75; EPSG: 29903)
  - Datasets include GB and NI versions of each product (GB 6,736,652 land parcels; NI 902,248 parcels).

- Production methodology
  - Bootstrap Training
    - Uses historic UKCEH LCM observations (LCM2015) to automatically sample training data for current satellite imagery.
    - Selection: parcels with ≥99% purity from LCM2015 to bootstrap the training set.
    - Purpose: exploit the majority signal over time to generate robust spectral training observations.
  - Random Forest classification
    - Balanced learning: 10,000 samples per class drawn with replacement from each training bag.
    - Production software integrates Weka with PostGIS and GDAL.
  - Classification Scenes and tiling
    - Great Britain: 100x100 km tiles; 36-band Seasonal Composite Images combined with 20m context rasters to form 46-band Classification Scenes; 74 overlapping GB scenes classified independently; visual checks resolve overlaps.
    - Northern Ireland: single 43-band Classification Scene per year (36 spectral + 7 context layers).
  - Land Parcel Spatial Framework
    - Maintains ~0.5 ha minimum parcel size (MMU); designed to provide discrete real-world units for change detection.
    - Parcel framework is unchanged from LCM2015, but IDs (gid) are not identical; allows cross-year comparisons via gid or parcel overlap.
  - Data lineage and future plans
    - All maps are generated automatically with limited manual intervention; annual updates are planned (LCM2020 for 2021 onward to use 2017–2019 majority signals).

- Validation and accuracy
  - UK-scale validation used: GB countryside survey (2019 data), National Forest Inventory, IACS, and bespoke interpretation points (22,325 locations).
  - Reported overall accuracy (relative to validation points):
    - LCM2017: 78.6%
    - LCM2018: 79.6%
    - LCM2019: 79.4%
  - Validation data are a best-available indicator; notes acknowledge potential mismatches in class translations and the non-absolute nature of ground truth.

- Notable considerations and caveats
  - Automatic classification introduces random yet usually spatially uncorrelated errors; time-series maps should reveal genuine land cover changes against noise.
  - No manual corrections were applied in this release; improvements anticipated with future data and methods.
  - Some classes are spectrally confusable (e.g., various grasslands, peatland indicators); contextual rasters and training data help mitigate confusion.
  - The study emphasises consistency by maintaining similar class definitions to LCM2015/LCM2007 while updating detection capabilities with modern sensors.

- Glossary and class relationships (summary)
  - 21 UKCEH Land Cover Classes aligned with BAP Broad Habitats; Some terms are italicised when referring to BAP Broad Habitats.
  - A mapping framework exists between UKCEH Land Cover Classes and BAP Broad Habitats; Tables and Appendices provide detailed correspondences and detection notes (e.g., distinctions for Arable, Improved Grassland, Neutral Grassland, Calcareous Grassland, etc.).

- Appendix and references (highlights)
  - Appendix outlines UK BAP Broad Habitats definitions and their relation to UKCEH classes; notes on detection challenges (upland peatland, bracken, linear features, etc.).
  - References include foundational works on Random Forests, bootstrap training, and earlier LCM production methods for contextual background.

- Practical takeaway for analysts
  - LCM2017–LCM2019 provide a consistent, annual suite of 21-class land cover maps at multiple spatial resolutions, with detailed parcel-level and 1km aggregated products.
  - The 20m Classified Pixels dataset retains fine-scale landscape features; parcel-based summaries enable robust change detection and integration with administrative or catchment boundaries.
  - Users should account for gid changes across years when comparing with LCM2015 or earlier products; cross-year comparisons can rely on the Land Parcel Spatial Framework (gid) for LCM2017–LCM2019.
  - Validation accuracy around 78–80% suggests good overall performance, with class-level accuracy varying; consider class-specific confusion notes when interpreting results.