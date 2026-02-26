# The UKCEH Land Cover Maps for 2017, 2018 and 2019 v1.5.1

- Purpose and scope
  - Release of three new UKCEH land cover maps: LCM2017, LCM2018 and LCM2019.
  - Each map represents 21 UKCEH Land Cover Classes derived from Biodiversity Action Plan (BAP) Broad Habitats.
  - Maps produced automatically using Bootstrap Training with a Random Forest classifier; aim to release a new LCM annually.
  - Emphasis on enabling rapid UK-wide mapping while acknowledging that complex data requires careful application.

- Data products and structure
  - 20m Classified Pixels (new)
    - Pixel-level RF classification results from Sentinel-2 Seasonal Composite Images; two-band raster per pixel (class, confidence 0–100).
    - Preserves fine landscape detail; not generalised by parcel framework.
  - Land Parcels
    - 20m Classified Pixels intersected with UKCEH Land Parcel Spatial Framework; parcel-level attributes.
    - Gid: unique parcel ID; _hist: list of class frequencies; _mode: dominant class; _purity: modal proportion; _conf: mean class probability; _stdev: confidence variability; _n: number of pixels.
    - 21-class structure; Great Britain (GB) and Northern Ireland (NI) versions; parcel identifiers do not match LCM2015 but gid enables cross-year comparisons 2017–2019.
  - 25m Rasterised Land Parcels
    - Rasterised version of parcel data with 3 bands: _mode, _conf, _purity.
  - 1km Raster Datasets
    - 1km Percent Cover (21-band)
    - 1km Percent Aggregate Cover (10-band)
    - 1km Dominant Cover (1-band)
    - 1km Dominant Aggregate Cover (1-band)
  - Dataset extents and formats
    - GB: British National Grid (EPSG:27700); NI: Irish grid (EPSG:29903); each year released for GB and NI.
    - Pixel sizes and band counts align with Appendix 4 metadata (20m classified pixels, 25m land parcels, 1km rasters).

- Methodology and data sources
  - Seasonal information
    - Seasonal Composite Images derived from Google Earth Engine with median TOA reflectance for four seasons (winter, spring, summer, autumn) using Sentinel-2 bands 2,3,4,5,6,7,8,11,12.
    - Context Rasters (20m) added to reduce spectral confusion (terrain, urban proximity, distance layers, etc.).
  - Classification approach
    - Bootstrap Training: training set drawn from UKCEH LCM2015 with high-purity parcels (≥99%); used to bootstrap training for 2017–2019 maps; future bootstraps based on majority signal across years.
    - Random Forest: balanced sampling (10,000 samples per class per patch) to train the classifier; implemented with bespoke UKCEH software integrating WEKA, PostGIS, and GDAL.
  - Land Parcel Spatial Framework
    - Framework retained from LCM2007/LCM2015 lineage; 0.5 ha minimum parcel (MMU); parcels designed to represent discrete land units (fields, parks, woodlands, etc.).
    - The spatial framework is fixed; changes affect comparability mainly via gid; future refinements may occur as higher-resolution data become available.
  - Validation and accuracy
    - UK-scale validation against GB countryside survey 2019, National Forest Inventory, IACS, and bespoke validation points (22,325 points).
    - Reported overall accuracy (producer’s accuracy context): LCM2017 78.6%; LCM2018 79.6%; LCM2019 79.4%.
    - Validation results include detailed confusion matrices (Appendix 4); note that validation data are not perfect truth and were harmonised to UKCEH classes.
  - Data quality and limitations
    - No manual corrections were applied this release to enable annual mapping; errors are treated as random until seen persistently over time.
    - Some known confusions (e.g., Saltwater vs Freshwater near coasts; upland peatland and Bracken distinctions) remain, but context layers and seasonality help.

- Class framework and interpretation
  - 21 UKCEH Land Cover Classes
    - Based on UK BAP Broad Habitats; designed for remote-sensing detection rather than strict field-identified BAP categories.
    - Appendix 1 and Appendix 2 provide class notes and biodiversity habitat definitions; crosswalks to UK BAP Broad Habitats (with some refinements and private notes on detectability).
  - Practical guidance for analysts
    - Use 20m Classified Pixels for high-detail mapping and bespoke parcel summarisation.
    - Use Land Parcels to examine per-parcel composition and confidence; use _hist, _mode, _purity, _conf for interpretation and change detection.
    - Use 1km rasters for coarser-scale summary statistics (percent cover, dominant class) and for integrating with other coarse grids.
  - Visualization and color coding
    - Appendix 3 provides recommended RGB color recipes for displaying UKCEH Land Cover Classes; consistent visual interpretation across products.

- Practical considerations for monitoring environmental health
  - Consistent, automated annual maps enable near-real-time monitoring of land cover change across Great Britain and Northern Ireland.
  - The 20m Classified Pixels dataset preserves fine features that may be critical for habitat and land-use change analyses; however, parcel-based summaries (Land Parcels) can simplify time-series comparisons.
  - Validation suggests robust automatic classification at the ~80% accuracy level, with room for improvement as bootstrap strategies and training data evolve.
  - The framework supports cross-year change detection but requires careful alignment of parcel identifiers and class definitions when comparing with older maps (gid-based comparison recommended for 2017–2019).
  - Acknowledges ongoing evolution toward higher-resolution inputs and expanded data sources; planning to explore augmented data (e.g., alternative optical sources, SAR) to fill seasonal gaps.

- Future plans and data access
  - A new LCM is planned annually (LCM2020 in 2021 planning context) with continued Bootstrap Training evolution.
  - Appendix 5 lists the full set of datasets and their GB/NI scope for each year; data are available as 20m classified pixels, land parcels, 25m rasterised parcels, and 1km rasters (with year-specific naming).
  - The methodology emphasizes reproducibility, transparency, and a clear lineage from earlier maps (LCM1990, LCM2000, LCM2007, LCM2015) to the current 2017–2019 suite.

- Quick reference: key numbers
  - Years covered: 2017, 2018, 2019
  - Classes: 21 UKCEH Land Cover Classes
  - Spatial resolutions: 20m (pixels and parcels); 25m (parcels); 1km rasters
  - Validation accuracy: ~78.6% (2017), ~79.6% (2018), ~79.4% (2019)
  - Coverage: GB and NI; GB uses 100x100 km classification tiles; NI uses a single 43-band scene
  - Data structure: 20m Classified Pixels, Land Parcels, 25m Rasterised Land Parcels, 1km Dominant/Percent/Percentage datasets

- Appendix and references
  - Appendix 1–2: UKCEH Land Cover Classes and BAP Broad Habitat mappings and notes
  - Appendix 3: RGB color recipes for display
  - Appendix 4: Validation details and confusion matrices
  - Appendix 5: Detailed dataset list by year and product type
  - References: foundational works on RF, bootstrap training, and land cover mapping methodologies