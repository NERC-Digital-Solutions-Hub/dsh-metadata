# The UKCEH Land Cover Maps for 2017, 2018 and 2019 v1.5.1

- Purpose and scope
  - User guide for three UKCEH land cover maps: LCM2017, LCM2018, and LCM2019.
  - Describes content, data structure, production decisions, validation, and future plans to help users make informed applications.
  - Maps use 21 UKCEH Land Cover Classes based on Biodiversity Action Plan (BAP) Broad Habitats; intensity of changes tracked over time.

- Data products and structure
  - 20m Classified Pixels (new): RF classification results with per-pixel class and a second band giving confidence (0–100).
  - Land Parcels: attributes summarising 20m classifications within UKCEH Land Parcel Spatial Framework.
    - Key fields: gid, _hist (histogram of counts per class), _mode (dominant class), _purity (modal proportion), _conf (mean class membership probability), _stdev (uncertainty), _n (pixel count).
  - 25m Rasterised Land Parcels: three-band raster (band 1: _mode, band 2: _conf, band 3: _purity).
  - 1km Raster datasets:
    - 1km Percent Cover: 21-band raster of class percentages per 1km cell.
    - 1km Percent Aggregate Cover: 10-band raster of aggregate class percentages.
    - 1km Dominant Cover: single-band raster of dominant class per 1km cell.
    - 1km Dominant Aggregate Cover: 1-band raster of dominant aggregate class per 1km cell.
  - Dataset counts: each year includes GB and NI products, yielding a total of 42 datasets across years.

- Dataset extents, coordinate systems, and access
  - Great Britain: GB British National Grid (EPSG:27700).
  - Northern Ireland: NI Irish Grid (EPSG:29903).
  - Coverage and tile structure designed to support scalable processing; GB uses 100x100 km classification tiles; NI uses a single tile per year.

- Production methodology and workflow
  - Bootstrap Training: automatic training using historical maps (starting from LCM2015) to sample spectral training observations for new maps.
  - Random Forest classification: 10,000 samples per training bag, balanced across land cover classes to prevent dominance by common classes.
  - Seasonal composite imagery: Sentinel-2 seasonal mosaics (TOA reflectance) per season (winter, spring, summer, autumn) used to form classification scenes.
  - Context rasters: 20m rasters providing terrain and proximity context (height, aspect, slope, distance to buildings/roads/coast, foreshore, tidal, woodland).
  - Classification Scenes: GB uses 74 overlapping 100x100 km tiles (36-band seasonal composites + 10 contextual bands = 46-band scenes); NI uses a single 43-band scene per year.
  - UK Land Parcel Spatial Framework: maintains exact parcel structure from LCM2015 with minor attribute evolution; gid values differ from LCM2015, affecting cross-year parcel comparisons by gid but not by spatial overlap.
  - No manual corrections in this release to enable annual generation; visual checks and formal validation still conducted.

- Data quality, validation, and limitations
  - Validation conducted against GB Countryside Survey 2019 data, National Forest Inventory, IACS, and bespoke validation points (22,325 points total).
  - UK-scale accuracy:
    - LCM2017: ~78.6%
    - LCM2018: ~79.6%
    - LCM2019: ~79.4%
  - Validation notes: same validation dataset used across products; accuracy indicators reflect currency of validation data and class mapping; approximately 80% correspondence is considered strong for a fully automatic 21-class product.
  - Appendix 4 provides full per-class confusion matrices and producer/user accuracies; acknowledged limitations due to historical class definitions, spectral similarity, and MMU constraints.
  - Some classes (e.g., upland peatland, bracken) acknowledged detection limitations; context layers mitigate some spectral confusion.

- Data interpretation, usage guidance, and accessibility
  - 20m Classified Pixels preserve fine landscape detail; 25m Land Parcels provide a consolidated summary; 1km products support broader-scale analyses and comparisons.
  - Color and display guidance provided (Appendix 3) for consistent visualization.
  - Users should be aware of nuanced relationships between UKCEH Land Cover Classes and UK BAP Broad Habitats; italicization and capitalization conventions are used for clarity.
  - Some cross-year comparability caveats due to changes in parcel identifiers (gid differs from LCM2015); year-to-year parcel comparisons should use gid-based overlap rather than direct identifier match.

- Future plans and ongoing development
  - UKCEH intends to release a new LCM annually (LCM2020 planned for 2021), with potential methodological refinements (e.g., broader use of alternative data sources to fill seasonal gaps; exploration of Sentinel-1 SAR data for cloud-robust classifications).
  - Bootstrap Training strategies are expected to evolve; future bootstraps may rely on 3-year majority signals (e.g., 2017–2019) for 2020s maps.
  - There is ongoing interest in refining upland vegetation mappings and peatland classifications as training data and methods mature.

- Appendices and supporting information (highlights)
  - Appendix 1 and 2: Notes on UKCEH Land Cover Classes and their relationship to BAP Broad Habitats; class-specific considerations and detection caveats.
  - Appendix 3: Recommended RGB color recipes for displaying each UKCEH Land Cover Class.
  - Appendix 4: Detailed confusion matrices and accuracy statistics by class for LCM2017, LCM2018, and LCM2019.
  - Appendix 5: Full dataset listing and naming conventions for LCM2017, LCM2018, and LCM2019, including GB and NI products and file-naming conventions.