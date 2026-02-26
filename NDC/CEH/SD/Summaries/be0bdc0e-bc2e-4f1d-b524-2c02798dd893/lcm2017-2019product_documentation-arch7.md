# The UKCEH Land Cover Maps for 2017, 2018 and 2019 v1.6 18/06/2020

- Purpose
  - User guide for three UKCEH Land Cover Maps: LCM2017, LCM2018, and LCM2019.
  - Describes content, production, validation, decisions, and future plans to help users apply the data correctly.

- Key content and structure
  - 21 UKCEH Land Cover Classes (based on BAP Broad Habitats) and 10 UKCEH Aggregate Classes.
  - Automatic production using Bootstrap Training with a Random Forest classifier.
  - Sentinel-2 Seasonal Composite Images (median reflectance per season) + 20m Context Rasters for Classification Scenes.
  - Annual map series with emphasis on rapid production and cross-year comparability.

- Data products and dataset suite
  - 20m Classified Pixels (GB and NI versions): new addition; per-pixel class with confidence; preserves fine landscape detail.
  - Land Parcels: attributes derived from the UKCEH Land Parcel Spatial Framework (0.5 ha MMU; fixed parcel structure).
  - 25m Rasterised Land Parcels: rasterised version with 3 bands (dominant class, confidence, purity).
  - 1km Dominant Cover: 21-band raster for per-1km grid, dominant class.
  - 1km Percent Cover: 21-band percentage cover per 1km (rounded to integers).
  - 1km Percent Aggregate Cover: 10-band percentage cover for aggregate classes.
  - 1km Dominant Aggregate Cover: single-band dominant aggregate class per 1km.
  - Spatial extent and formats
    - Great Britain: GB National Grid (EPSG:27700); 20m, 25m and 1km products.
    - Northern Ireland: Irish National Grid (EPSG:29903); 20m, 25m and 1km products.
  - Total dataset set: 42 datasets (yearly duplication for GB and NI).

- Production methodology
  - Bootstrap Training: automatic sampling from historic UKCEH maps (primarily LCM2015) to train the classifier; aims to exploit majority signal over time.
  - Random Forest classifier: trained with balanced samples; 10,000 samples per class; uses classification scenes.
  - Seasonal information: Seasonal Composite Images (winter, spring, summer, autumn) derived from Sentinel-2; TOA reflects used (SR not adopted in this release).
  - Context information: 20m Context Rasters (terrain, proximity to buildings, roads, sea, freshwater, foreshore, urban/rural masks) to reduce spectral confusion.
  - Classification Scenes: GB classified in 100x100 km tiles (36-band seasonal + 10 context = 46 bands); NI uses a single 43-band scene per year.
  - No manual corrections this release (to enable annual production); visual checks and formal validation performed.

- Validation and accuracy
  - UK-scale validation against countryside survey data, National Forest Inventory, IACS, and legend-specific points.
  - Reported overall accuracies for the three years: LCM2017 ≈ 78.6%, LCM2018 ≈ 79.6%, LCM2019 ≈ 79.4%.
  - Validation points include caveats: some class description conversions and non-exact correspondences; around 80% correspondence considered strong for automatic, annual maps.

- Data relationships and terminology
  - 21 UKCEH Land Cover Classes linked to UK BAP Broad Habitats; some refinements and notes on detection limits (e.g., wetlands, upland vegetation, bracken).
  - 20m Classified Pixels preserve finer details; Land Parcels aggregate into parcel-level attributes; 25m rasters provide coarser generalisation.
  - Appendix notes include class definitions, color schemes for display, and confusion matrices (illustrating common inter-class confusion and producer/user accuracies).

- Practical considerations for GIS use
  - Parcel identifiers: gid is consistent within the UKCEH Land Parcel Spatial Framework; gid values differ from LCM2015 for cross-year comparisons.
  - MMU and generalisation: 0.5 ha MMU for Land Parcels; 25m rasters and 1km rasters provide different summarisation scales.
  - Temporal change: Bootstrap Training uses majority signal with a plan to base future bootstraps on multi-year data (2017–2019 for 2020; 2018–2020 for 2021).
  - Output guidance: Colour recipes and QGIS symbology files provided to aid visualisation; caveats about coastal saltwater vs freshwater delineation and salinity proxies.

- Appendix highlights (high level)
  - Appendix 1–2: Relationships between UKCEH classes and BAP Broad Habitats; detection considerations and caveats.
  - Appendix 3–4: Recommended colour recipes for display; color-blind friendly versions.
  - Appendix 5: Comprehensive confusion matrices by year and class; producer and user accuracies.
  - Appendix 6: Full list of datasets by year and product type (GB/NI, year-specific naming).