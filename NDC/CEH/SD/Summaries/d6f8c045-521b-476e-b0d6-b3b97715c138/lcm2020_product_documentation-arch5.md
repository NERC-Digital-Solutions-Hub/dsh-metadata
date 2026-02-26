# The UKCEH Land Cover Map for 2020

- Purpose and scope
  - User guide for the UKCEH Land Cover Map 2020 (LCM2020), the eighth UK land cover map.
  - Product consists of six geospatial datasets (three for Great Britain and Northern Ireland) plus 1 km summary rasters; overall seven main data holdings.
  - LCM2020 uses automatic classification of Classification Scenes, combining Sentinel-2 Seasonal Composite Images with 10 Context Layers, produced annually with ongoing methodological improvements.
  - Target: enable informed decision-making and long-term monitoring of UK land cover, including change detection.

- Data products and formats
  - 10 m Classified Pixel datasets (GB and NI): per-pixel land cover class with a second band providing the class membership probability/confidence.
  - 25 m Rasterised Land Parcel datasets (GB and NI): rastered parcels tied to the UKCEH Land Parcel Spatial Framework (fixed MMU ~0.5 ha) with three bands (dominant class (_mode), mean confidence (_conf), and mean purity (_purity)).
  - Land Parcel Products (GB and NI): per-parcel attributes derived by intersecting 10 m pixels with the Land Parcel Framework (columns include _hist, _mode, _purity, _conf, _stdev, _agg, _n, gid).
  - 1 km raster summary products (GB and NI): Dominant class, percentage cover per class, and related aggregations for 1 km pixels.
  - Coordinate systems: GB (British National Grid, EPSG 27700); NI (TM75 Irish Grid, EPSG 29903).
  - Official dataset names and metadata summarized in Appendix 6.

- Dataset structure and attributes
  - 10 m Classified Pixels: two bands; first band = most likely UKCEH Land Cover Class, second band = associated probability/confidence.
  - 25 m Rasterised Land Parcel: three bands per parcel—dominant class (_mode), mean confidence (_conf), and parcel purity (_purity).
  - Land Parcel attributes: including gid, _hist, _mode, _purity, _conf, _stdev, _agg, _n, with clear definitions and example values in Table 3.

- Production methodology
  - Seasonal Composite Images: derived from Google Earth Engine; Sentinel-2 data resampled to 10 m/20 m bands (bands 2,3,4,5,6,7,8,11,12) with seasonal medians for winter, spring, summer, autumn; some seasons may have cloud gaps represented as null.
  - Context Rasters: 10 m GB rasters (height, aspect, slope, distances to buildings/roads/sea/freshwater, foreshore and tidal masks, woodland) and NI equivalents (urban mask and distance-to-coast/freshwater/roads).
  - Classification Scenes: GB uses overlapping 100x100 km tiles (74 scenes) to generate 46-band GB Classification Scenes; NI uses a single 43-band Classification Scene per year.
  - Bootstrap Training: fully automatic trainer using historical LCM observations (LCM2017–2019 filtered to >99% purity across three years) to create a large, balanced training set for Random Forest classification.
  - Random Forest: 10,000 samples per class (bagged with replacement) to train the RF classifier; aims to balance learning across all classes.
  - Software: bespoke UKCEH pipeline integrating Weka, PostGIS, and GDAL (open source).

- Validation and quality
  - Validation against GB countryside survey data (2019–2020), National Forest Inventory data, IACS data, and bespoke validation points (34715 points total).
  - Reported overall accuracy around 79.2% (Appendix 5).

- Land Cover classifications and harmonisation
  - UKCEH Land Cover Classes (21 classes) are aligned with but not identical to UK BAP Broad Habitats; BAP terms are italicised when explicitly referred to, and the UKCEH/UK BAP terms are capitalised when defined as a class.
  - Appendix 1 and 2 explain detailed class definitions and their relationships to BAP Broad Habitats; Appendix 3 and 4 provide color schemes (standard and color-blind friendly) for displaying classes.

- The UKCEH Land Parcel Spatial Framework
  - Land parcels created from generalised national cartography with a 0.5 ha MMU; reorganised storage and new indices since LCM2015 changes mean LCM2020 parcel IDs (gid) do not match LCM2015 identifiers.
  - Parcels provide a stable unit for change detection and analysis, though cross-version comparisons by parcel ID may require spatial overlap rather than exact ID matching.

- Production notes and limitations
  - Annual production enables distinguishing real land-cover change from random errors; random classification errors are expected to flicker over time.
  - Some classification errors occur due to spectral similarity and patch size; coastal and upland vegetation categories present particular challenges.
  - Seasonal gaps due to cloud are managed by the classifier’s tolerance for partial spectral information; full nationwide coverage is achieved without manual gap filling.

- Display, metadata, and accessibility
  - Appendix 3 and 4 provide recommended colour recipes for displaying UKCEH Land Cover Classes; color-blind friendly versions are provided in Appendix 4.
  - Appendix 6 lists the full dataset catalog for LCM2020 and associated metadata.
  - Documentation emphasises data availability, versioning and the provenance of training data (Bootstrap Training) for governance and reproducibility.

- Practical considerations for data stewardship
  - Care with versioning and cross-version comparisons (gid changes; LCM2015 compatibility caveat).
  - Awareness of the 0.5 ha MMU and the presence of fine-scale features in 10 m data not generalized by Land Parcel framework.
  - Acknowledgement of potential classification confusion among related habitat types; use of Context Rasters helps mitigate some spectral confusion.
  - Regular updates and improvements anticipated; if new methods improve accuracy, re-application across the entire catalogue may occur.

- Appendix references and further details
  - Appendix 1-2: Detailed UKCEH Land Cover Classes and BAP Broad Habitats
  - Appendix 3-4: Colour recipes for display (standard and color-blind)
  - Appendix 5: Validation correspondence matrices and accuracy metrics
  - Appendix 6: Full list of LCM2020 datasets and metadata

- Key challenges aligned with Data Stewards archetype
  - Managing an incomplete picture of user needs and priorities for the data.
  - Ensuring timely access to updated data and metadata.
  - Achieving and maintaining standards across multiple systems and formats.
  - Handling very large datasets and ensuring interoperability with existing data holdings.
  - Addressing legacy database constraints and ensuring robust governance for ongoing updates.