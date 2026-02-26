# The UKCEH Land Cover Maps for 2017, 2018 and 2019 v1.5.1 30/06/2020

- Purpose and scope
  - Release of three new UKCEH land cover maps: LCM2017, LCM2018, and LCM2019.
  - Each map provides 21 UKCEH Land Cover Classes, aligned with BAP Broad Habitats approach; maps are produced automatically to enable near-real-time monitoring of land cover changes.
  - Emphasizes understanding data production, validation, decisions, and future plans to inform current and future work.

- Data products (dataset suite)
  - 20m Classified Pixels (new): per-pixel classification with two bands (class, confidence 0–100); preserves fine detail, not generalised by parcel framework.
  - Land Parcels: parcel-level attributes (gid, hist, mode, purity, conf, stdev, n); built on UKCEH Land Parcel Spatial Framework; notes on gid mismatch with LCM2015.
  - 25m Rasterised Land Parcels: three-band rasters (mode, conf, purity) summarising parcel data onto 25m grid.
  - 1km rasters (derived from parcels):
    - 1km Percent Cover (21-band)
    - 1km Percent Aggregate Cover (10-band)
    - 1km Dominant Cover (1 band)
    - 1km Dominant Aggregate Cover (1 band)
  - Spatial coverage: Great Britain (GB) and Northern Ireland (NI) with corresponding coordinate systems (EPSG:27700 for GB; EPSG:29903 for NI).

- Production structure and data extents
  - GB extents use British National Grid; NI extents use Irish Grid; all datasets provided in GB and NI versions.
  - Extents and pixel/parcel details summarized in Tables 3–4 of the guide (classification pixel, parcel, 25m raster, and 1km grids).

- Seasonal imagery and contextual data
  - Seasonal Composite Images created from Sentinel-2 (TOA reflectance) for winter, spring, summer, autumn; 20m resolution; derived via Google Earth Engine (GEE).
  - Seasonal data sometimes have cloud gaps; the classification framework tolerates partial spectral information.
  - Context Rasters (20m): include height, aspect, slope (NEXTMap), distance to buildings/roads/sea/freshwater, foreshore, tidal water, and woodland.

- Classification framework
  - Classification Scenes: GB uses overlapping 100x100 km tiles to create 46-band GB Classification Scenes; NI uses a single 43-band scene per year.
  - Bootstrap Training: fully automatic training using historic LCM2015-derived data with high-purity parcels (≥99% purity) to seed training for 2017–2019; aims to bootstrap future maps from majority signal across years.
  - Random Forest (RF) classifier: built via a bespoke production pipeline integrating WEKA, PostGIS, and GDAL; balanced sampling (10,000 samples per class) to train the 21-class RF model.

- Validation and accuracy
  - UK-scale validation using GB countryside survey 2019 data, National Forest Inventory, IACS, and manual interpretation points (22,325 points total).
  - Reported overall accuracy (producer’s and user’s accuracy context) around:
    - LCM2017: ~78.6%
    - LCM2018: ~79.6%
    - LCM2019: ~79.4%
  - Notes on validation: same validation dataset used across products; accuracy treated as indicative rather than absolute truth; conversions between historical class schemes may affect exact figures.

- Class definitions and terminology
  - 21 UKCEH Land Cover Classes, based on UK BAP Broad Habitats (Appendices 1–2); not exact BAP definitions but aligned to aid consistency and change detection.
  - Appendix 3 provides recommended RGB color mapping for display.
  - Appendix 4 includes detailed confusion matrices and producer/user accuracy by class for validation.

- Data framework and comparability
  - UKCEH Land Parcel Spatial Framework unchanged in geometry since LCM2015 (min parcel ~0.5 ha MMU); gid identifiers differ from LCM2015, affecting direct parcel-id comparisons but enabling cross-year overlap at the parcel level via gid.
  - 20m Classified Pixels preserve intricate landscape features (e.g., narrow patches) not present in Land Parcels summaries.
  - Provides an option for users to apply their own parcel structures beyond the UKCEH framework.

- Data governance, availability, and future plans
  - Dataset structure designed to support time-series analysis and change detection; annual LCM releases intended going forward.
  - Future enhancements under consideration include broader satellite inputs (e.g., Sentinel-1), filling occasional seasonal gaps with alternative sources, and potential refinements to the Land Parcel Spatial Framework as higher-resolution data become available.
  - Aims to improve automation, validation resources, and lineage for cross-year comparisons.

- Appendix highlights (value for analysts)
  - Appendix 1–2: detailed notes on UKCEH Land Cover Classes and their relationship to BAP Broad Habitats, including detection considerations and known spectral ambiguities.
  - Appendix 3: color recipes for consistent map visualization.
  - Appendix 4: full validation confusion matrices and accuracy metrics by class (LCM2017–LCM2019).
  - Appendix 5: full list of datasets per year and their digital holding names.