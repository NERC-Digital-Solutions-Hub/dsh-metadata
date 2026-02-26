# The UKCEH Land Cover Maps for 2017, 2018 and 2019 v1.6

- **Purpose and scope**
  - Release of three new UKCEH Land Cover Maps: LCM2017, LCM2018, and LCM2019.
  - Each map uses 21 UKCEH Land Cover Classes, aligned with Biodiversity Action Plan (BAP) Broad Habitats concept.
  - Maps are produced automatically using Bootstrap Training and a Random Forest classifier; intended for annual updates to monitor land cover change.
  - Aims to enable rapid, coast-to-coast UK mapping with formal validation and documented production decisions.

- **Key concepts and terminology**
  - 21 UKCEH Land Cover Classes (aligned with UK BAP Broad Habitats in Appendix 1 and 2; terminology capitalised for clarity).
  - Bootstrap Training: automatic sampling of training observations from historic maps to train the classifier.
  - Classification Scenes: multi-layer inputs combining Seasonal Composite Images (from Sentinel-2) and Context Rasters.
  - Land Parcel Spatial Framework: fixed polygon system (≈0.5 ha MMU) used to structure and summarize 20m classified pixels.

- **What’s in the data (product suite)**
  - 20m Classified Pixels: new 2-band, 8-bit rasters per year and region; band 1 = most likely UKCEH Land Cover Class, band 2 = class membership probability (0–100) indicating classification confidence.
  - Land Parcels: parcel-level attributes (gid, _hist, _mode, _purity, _conf, etc.); supports detailed parcel-based summaries and change detection; notes on attribute changes from LCM2015.
  - 25m Rasterised Land Parcels: three-band rasters (band 1 = _mode, band 2 = _conf, band 3 = _purity).
  - 1km rasters (GB and NI composites):
    - 1km Percent Cover: 21-band raster (percentage by class per 1km cell).
    - 1km Percent Aggregate Cover: 10-band raster (percentage by UKCEH Aggregate Classes).
    - 1km Dominant Cover: 1-band raster (dominant class per 1km cell).
    - 1km Dominant Aggregate Cover: 1-band raster (dominant aggregate class per 1km cell).
  - Coordinate systems and extent:
    - GB: British National Grid (EPSG 27700); 21 classes; multiple bands per product.
    - NI: Irish Grid (TM75; EPSG 29903); 10 classes; corresponding products.
  - Scale and duplication:
    - Datasets exist for each year (2017–2019) and are duplicated for GB and NI, resulting in 42 primary datasets.
  - Dataset structure figure (Figure 1) shows the 21-class and 10-class relationships and dataset lineage.

- **Production methodology highlights**
  - Seasonal Composite Images: Sentinel-2 median TOA reflectance per season (winter, spring, summer, autumn) at 20m resolution; 9 Sentinel-2 bands used; some seasonal gaps treated as null data.
  - Classification Scenes: GB used overlapping 100x100 km tiles (74 scenes) to produce 46-band GB scenes; NI used a single 43-band scene per year.
  - Context Rasters: 20m GB rasters (height, aspect, slope, proximity to buildings/roads/sea/freshwater, foreshore and tidal masks, vegetation masks) and NI equivalents (urban mask, distances to coast/freshwater/roads).
  - Bootstrap Training: training set drawn from LCM2015 with ≥99% purity; balanced sampling to ensure rare classes are represented; RF classifier trained with 10,000 samples per class.
  - Software stack: bespoke UKCEH pipeline integrating Weka (RF), PostGIS, and GDAL.
  - Validation approach: UK-scale validation using countryside survey 2019 data, National Forest Inventory, IACS, and bespoke validation points (≈22,325 points) to assess correspondence with LCM Land Parcels.
  - Accuracy results (UK-scale):
    - LCM2017: 78.6%
    - LCM2018: 79.6%
    - LCM2019: 79.4%
  - Important caveats:
    - No manual accuracy corrections were applied in these releases to enable rapid annual mapping; visual checks and formal validation still performed.
    - Validation uses data with different purposes and class descriptions, converted to UKCEH classes; results reflect this uncertainty.

- **Data quality, interpretation, and limitations**
  - Overall accuracy around 80% for 21-class maps; reasonable for automatic mapping and change detection, with expectations of improvement over time.
  - Common challenges and known confusions:
    - Upland vegetation types and spectral confusion between similar habitat classes.
    - Coastal environments where Saltwater, Freshwater, and Saltmarsh can be confused; Salinity-related classes rely on contextual inputs.
    - Built-up areas vs. urban/suburban distinctions can exhibit spectral mixing.
  - MMU and patch dynamics:
    - Land Parcels have a ~0.5 ha MMU; many small patches (<0.5 ha) may be underrepresented in parcel summaries.
    - 20m pixels preserve finer detail than later aggregated 25m or 1km products; however, aggregation reduces noise for broad-scale analyses.
  - Cross-year comparisons:
    - The UKCEH Land Parcel Spatial Framework is unchanged in geometry since LCM2015, but unique parcel identifiers (gid) differ between LCM2015 and 2017–2019; direct gid-based cross-year comparisons are not supported (use gid-based comparisons within the same framework or spatial overlap).

- **Usage guidance for Data Leaders**
  - Suitability:
    - Good for rapid, annual monitoring of land cover change across Great Britain and Northern Ireland at multiple spatial scales (pixel, parcel, and grid).
    - Useful for both visualization (via colour schemes and Appendix 3–4 color recipes) and quantitative change analysis (parcel and 1km products).
  - Data governance and interoperability:
    - Clear lineage from historic LCMs via Bootstrap Training; documentation of production decisions and validation context supports reproducibility.
    - Cross-year comparisons require careful handling due to gid changes; consider spatial overlap analyses or re-baselining on a common parcel framework when assessing trajectories.
  - Future-proofing and enhancements:
    - Plans to increase automation and annual release cadence; potential incorporation of additional data sources (e.g., Sentinel-1 SAR, Sentinel-2 surface reflectance; SMART transitions between TOA and SR inputs) and expanded training data for improved class separation.
    - Ongoing evaluation of training data sources and custom context layers to reduce spectral confusion, with potential for refined upland vegetation mapping.

- **Future plans and context**
  - Annual LCM releases are planned going forward; 2020 progression anticipated to use Bootstrap Training from a multi-year majority signal (2017–2019) to improve training data robustness.
  - Exploration of supplementary data sources and methods (e.g., alternative optical sources, SAR) to fill seasonal gaps and improve classification in challenging areas.
  - Commitment to continual validation and refinement of class definitions, with Appendix materials (e.g., confusion matrices in Appendix 5) providing detailed performance insights.