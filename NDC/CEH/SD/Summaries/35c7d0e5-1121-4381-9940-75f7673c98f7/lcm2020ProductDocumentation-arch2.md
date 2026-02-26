# The UKCEH Land Cover Map for 2020

- Purpose and scope
  - User guide for LCM2020, the eighth UKCEH land cover product, produced annually to support monitoring of environmental state and change.
  - LCM2020 consists of six datasets (three for GB and Northern Ireland): 10m Classified Pixel datasets, Classified Land Parcel datasets, and 25m Rasterised Land Parcel datasets (one set for GB and one for Northern Ireland).

- Land cover classes and relationships
  - Defines 21 UKCEH Land Cover Classes based on Biodiversity Broad Habitats (BAP) concepts.
  - Classes are closely related to BAP Broad Habitats but not identical; BAP terms are italicised and capitalisation rules used for clarity.
  - Appendix 1–2 provide mappings and notes on how UKCEH Land Cover Classes relate to BAP Broad Habitats.
  - The display colour recipe (Appendix 3) provides recommended RGB values for each class.

- Data products and structure
  - 10m Classified Pixel datasets
    - Results from Classification Scenes; each pixel has a most-likely UKCEH Land Cover Class (Band 1) and a class membership probability/confidence (Band 2).
    - Do not undergo Land Parcel Spatial Framework generalisation to preserve fine features; intended for specialist users.
  - Land Parcel datasets
    - Derived by intersecting 10m Classified Pixels with the UKCEH Land Parcel Spatial Framework.
    - Parcel-level attributes include hist, mode, purity, conf, stdev, agg, n, and a unique gid.
  - 25m Rasterised Land Parcel datasets
    - Rasterise parcel-level data into 25m pixels with three bands: dominant land cover (mode), mean confidence (conf), and parcel purity (purity).
  - Datasets are prepared separately for GB and Northern Ireland (NI).

- Imagery and features used
  - Seasonal Composite Images from Sentinel-2 (winter, spring, summer, autumn) derived via Google Earth Engine.
  - Nine or more spectral bands used per season; spectral gaps due to cloud are tolerated by the classifier.
  - Context Rasters (GB: 10 rasters; NI: 7 rasters) provide terrain, proximity to features (buildings, roads, coastline, freshwater), and land cover context (foreshore, tidal water, woodland masks).

- Classification approach
  - Bootstrap Training: automatic, historical training data sampled from previous maps (LCM2017–2019) to train the classifier without new field data.
  - Random Forest classifier with balanced sampling: 10,000 samples per class drawn with replacement from training parcels.
  - Training data: >99% purity filters across three years; GB training objects ~941,027; NI ~214,833.
  - Processing workflow uses a mosaic of 100x100 km GB tiles (74 Classification Scenes) and a single NI Classification Scene.

- Validation and accuracy
  - Validated against countryside survey data (2019–2020), National Forest Inventory, IACS, and bespoke validation points (34715 points).
  - Overall accuracy: 79.2% at full thematic detail (Appendix 4 provides confusion matrices and producer/user accuracies by class).

- Data governance and comparability
  - Land Parcel Spatial Framework is shared with prior LCMs (LCM2007–2015 lineage); minor changes affect parcel identifiers, limiting direct parcel-id-based comparisons with older maps.
  - LCM2020 emphasizes annual production to distinguish random classification errors from real change; random errors are expected to flicker over time, whereas real changes persist.

- Practical considerations for users
  - 10m Classified Pixels: high detail but not generalised; best for specialist analyses of fine-scale features.
  - Land Parcel datasets: useful for time-series change detection and integration with other parcel-level data; parcel-level metrics provide insight into confidence and dominance.
  - 25m Rasterised parcels: suitable for coarser analyses where parcel structure is needed in raster form.
  - Some classes (e.g., Saltwater) can be spectrally similar to Freshwater; coastal context rasters aid discrimination, but some confusion remains, particularly near tidal areas.

- Methodology highlights
  - Classification Scenes: GB uses 36-band scenes (multiple 100x100 km tiles); NI uses a single 43-band scene per year.
  - Context Rasters and Seasonal Composite Images were designed to reduce spectral confusion and improve class separation.
  - The production pipeline integrates Weka (machine learning), PostGIS, and GDAL (open-source tools).

- Temporal and monitoring value
  - Annual LCM enables monitoring of land cover change and supports environmental objectives with a consistent, time-series product.
  - The approach differentiates random classification noise from real land cover change, aiding policy performance assessment and trend analysis.

- Appendices and datasets
  - Appendix 1–2: Detailed notes on UKCEH Land Cover Classes and BAP Broad Habitats.
  - Appendix 3: Colour recipe for displaying classes.
  - Appendix 4: Correspondence matrices and accuracy statistics by class.
  - Appendix 5: Full list of LCM2020 datasets and their geospatial scope.

- Key references and context
  - Methodological foundations include Random Forest (Breiman, 2001), Bootstrap Training concepts, and prior LCM development (LCM2007–2019).
  - Validation and interpretation guidance draw on UK countryside surveys and biodiversity habitat literature.