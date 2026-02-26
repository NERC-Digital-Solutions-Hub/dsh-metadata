# The UKCEH Land Cover Maps for 2017, 2018 and 2019 v1.5.1

- Purpose and scope
  - User guide for three new UKCEH Land Cover Maps: LCM2017, LCM2018, and LCM2019.
  - Each map comprises a suite of geospatial datasets at 21 UKCEH Land Cover Classes (based on Biodiversity Action Plan Broad Habitats) with coverage across Great Britain and Northern Ireland.
  - Data produced automatically (Bootstrap Training + Random Forest); no manual corrections applied this time. Visual checks and formal validation confirm map quality comparable to LCM2015.
  - Intention to release a new LCM annually to track land cover change.

- Core data products (per year)
  - 20m Classified Pixels: per-pixel land cover class with a second band indicating classification confidence (0–100). Preserves fine detail (not generalised by parcels).
  - Land Parcels: attributes derived from the 20m Classified Pixels via the UKCEH Land Parcel Spatial Framework (LP Framework). Key fields include _hist (class frequencies per parcel), _mode (dominant class), _purity (modal proportion), _conf (mean class membership probability), _stdev, and _n (number of pixels). gid links parcels to geometry; potential extra identifiers may appear due to file formats.
  - 25m Rasterised Land Parcels: three-band raster (band 1: modal class; band 2: parcel-averaged confidence; band 3: parcel purity).
  - 1km datasets (GB and NI): 
    - 1km Percent Cover (21-band)
    - 1km Percent Aggregate Cover (10-band)
    - 1km Dominant Cover (single-band)
    - 1km Dominant Aggregate Cover (single-band)
  - Dataset duplication: for each year, GB and NI products produce a total of 42 datasets (20m, land parcels, 25m raster parcels, and 1km products).

- Production methodology and data inputs
  - Seasonal spectral inputs: Sentinel-2 Seasonal Composite Images (TOA reflectance, median per season across four seasons) at 20m resolution.
  - Classification Scenes: classification uses 46-band GB Scenes (36 spectral bands + 10 context layers) and 43-band NI Scenes; scenes are trained and classified independently in overlapping tiles (GB uses 100x100 km tiles).
  - Context rasters (20m): include terrain (height, aspect, slope) and proximity masks (distance to buildings, roads, coast, freshwater) plus foreshore/urban/etc.
  - Contextual/landscape disambiguation helps address spectral confusion between similar classes (e.g., coastal vs inland features).
  - Google Earth Engine (GEE) provides data and processing; determination to use TOA due to incomplete SR availability and because SR did not improve classification for current land cover classes.

- Training and classification approach
  - Bootstrap Training: fully automatic training that doesn't require new field data.
  - Training sets derived from UKCEH LCM2015 (and prior stable mappings) using parcels with ≥99% purity to sample current seasonal imagery; bootstrap builds a majority signal over time for subsequent maps.
  - Random Forest classifier: 10,000 samples per class (with replacement) used to balance learning across 21 classes.

- UKCEH Land Parcel Spatial Framework
  - Parcel geometry unchanged from LCM2015; minor storage and indexing changes for performance.
  - gid identifiers for LCM2017–2019 do not match LCM2015 parcel IDs; parcel comparisons should be via gid.
  - Minimum mapping unit (MMU) ~0.5 hectares; parcels represent discrete real-world units (fields, parks, etc.) and help reduce classification noise and support change detection.
  - The framework allows users to summarise 20m pixels with other parcel structures beyond the UKCEH framework.

- Validation and accuracy
  - UK-wide validation using 22,325 points from GB countryside survey (2019), National Forest Inventory, IACS, and manual interpretation data.
  - Accuracy results (UK scale, 21-class):
    - LCM2017: 78.6%
    - LCM2018: 79.6%
    - LCM2019: 79.4%
  - Validation recognizes potential misalignment between validation data and UKCEH class definitions; results are robust indicators of quality but not absolute truth. Full correspondence tables are provided in Appendix 4.

- Data structure notes and usage guidance
  - 21 UKCEH Land Cover Classes; GB and NI data and legends align with Appendix 1–3 mappings and color recipes.
  - Class definitions reflect BAP Broad Habitats language with careful notation to avoid ambiguity between UKCEH Classes and BAP Broad Habitats.
  - The 20m Classified Pixels dataset preserves detail (e.g., narrow features) that are dissolved in parcel-based products.
  - The 1km products provide aggregated summaries suitable for broader-scale analyses and compatibility with commonly used gridded datasets.

- Technical metadata and geographic scope
  - Coordinate systems:
    - Great Britain: British National Grid, EPSG 27700
    - Northern Ireland: Irish Grid, EPSG 29903
  - Dataset extents and pixel resolutions:
    - 20m Classified Pixels: 20 m pixels
    - 25m Rasterised Land Parcels: 25 m pixels
    - 1km rasters: 1 km grid with parcel-derived statistics
  - Yearly dataset replication across GB and NI yields a comprehensive, annually updated UK-wide land cover time series.

- Appendix highlights and future plans
  - Appendix 1–2: detailed notes on UKCEH Land Cover Classes and BAP Broad Habitats with detection considerations and potential confusions.
  - Appendix 3: recommended RGB color recipe for displaying UKCEH Land Cover Classes.
  - Appendix 4: validation confusion matrices and accuracy statistics per year.
  - Appendix 5: full list of datasets per year and their data products.
  - Future directions: continued annual releases; exploration of gap filling with alternative optical/SAR data sources (e.g., Sentinel-1) if needed; potential refinements to the Land Parcel Spatial Framework to adapt to higher-resolution data and new training data.