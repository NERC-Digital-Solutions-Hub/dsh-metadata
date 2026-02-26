# The UKCEH Land Cover Map for 2020

- Purpose and scope
  - LCM2020 is the UKCEH land cover map for 2020, the eighth in the series, produced annually to monitor state and change in the UK countryside.
  - Provides 21 UKCEH Land Cover Classes, aligned with Biodiversity Action Plan (BAP) Broad Habitats, based on remote-sensing data and an automated classification approach.
  - Aims to maximise temporal consistency, comparability, and change detection, with ongoing methodological improvements.

- What’s in the product (datasets and structure)
  - Six geospatial datasets (GB and Northern Ireland), comprising:
    - 10m Classified Pixel datasets (pixel-level land cover with class and confidence)
    - Land Parcel Spatial Framework (to define discrete land parcels)
    - 25m Rasterised Land Parcel datasets (per-parcel land cover, conf, and purity)
  - For GB and NI, datasets include:
    - 10m Classified Pixels (GB and NI)
    - Land Parcel products (GB and NI)
    - Rasterised Land Parcel products (GB and NI)
  - Classification is built from:
    - Seasonal Composite Images (Sentinel-2) to provide temporal information
    - 10 Context Rasters (contextual features to resolve spectral confusion)
    - 36-band GB Classification Scenes (over 74 tiles) and 43-band NI Classification Scene (one max-extent scene)
  - Minimum mapping unit and feature detail
    - Land Parcels have a minimum area of ~0.5 ha (MMU)
    - 10m Classified Pixels preserve fine landscape features not generalised by the Land Parcel framework

- How the data were produced
  - Bootstrap Training
    - Fully automatic training that uses historical UKCEH land cover maps (LCM2017–2019) to generate training data, reducing the need for new field data.
    - Training sets: GB 941,027 objects; NI 214,833 objects (filtered to >99% purity across three years).
  - Random Forest classification
    - Pixels sampled from Classification Scenes; 10,000 samples per class per bag, with replacement to balance classes.
    - Class with highest probability becomes the pixel class; second band stores the classification confidence.
  - Data processing tools
    - Bespoke UKCEH software integrating Weka, PostGIS, and GDAL (open source).

- Data quality, validation, and accuracy
  - Validation approach
    - 34,715 validation points drawn from GB Countryside Survey data (2019/2020), National Forest Inventory, IACS, and bespoke validation points.
    - Validation intersects with Land Parcel datasets to determine correspondence.
  - Overall accuracy
    - Approximately 79.2% accuracy at full thematic detail (Appendix 4).
  - Class-level validation
    - Appendix 4 includes detailed matrices showing user’s and producer’s accuracies by UKCEH Land Cover Class, highlighting areas of confusion (e.g., between arable and various grassland classes, coastal/intertidal distinctions).

- Relationship to BAP Broad Habitats and class mappings
  - 21 UKCEH Land Cover Classes align with UK BAP Broad Habitats but are not identical (BAP designed for field botanists; remote sensing requires simplifications).
  - Appendices explain mappings between UKCEH classes, BAP Broad Habitats, and indicative notes on potential spectral confusion.
  - Special notes on specific classes (e.g., Saltwater vs Freshwater, Urban vs Suburban) and how they are captured or confused by context rasters.

- Seasonal and contextual data details
  - Seasonal Composite Images
    - Derived from Sentinel-2 data (four-season median reflectance; bands 2,3,4,5,6,7,8,11,12) via Google Earth Engine.
    - Some seasonal gaps due to cloud cover; classifier tolerates partial spectral information.
  - Context Rasters
    - GB: 10 context rasters including height, aspect, slope, distance to buildings/roads/sea/freshwater, foreshore mask, tidal mask, and woodland mask.
    - NI: 7 context rasters including height, aspect, slope, urban mask (NISRA open data), and distances to coast, freshwater, and roads.
  - Classification Scenes
    - GB uses a patchwork of overlapping 100x100 km tiles; NI uses a single 100x100 km scene (minimum bounding rectangle of NI land mass).
    - Overlaps may yield slight variations; manual visual precedence is used to finalize the cut.

- Data governance, updates, and caveats
  - Annual production
    - The map is produced annually to distinguish errors from real-world change; random classification errors are expected to flicker over time, while real changes persist.
  - Transparency and reproducibility
    - Methods described in detail (Bootstrap Training, RF approach, context layers) to enable informed use and potential methodological refinements.
  - Limitations and caveats
    - Spectral confusion remains between certain land cover types; accuracy varies by class.
    - Some features below the MMU or with narrow extents may be captured or missed depending on dataset (10m vs 25m rasters).
    - Future improvements anticipated with richer time series and refined training data.

- Accessing the data and documentation
  - Appendix 5 lists the full dataset set and official names/citations for each dataset (GB and NI variants).
  - Data presentation and color-coding recommendations provided (Appendix 3) to support visualization consistency.

- Practical takeaway for Data Leaders
  - LCM2020 provides a robust, annually updated, governance-friendly land cover product that supports monitoring state and change across the UK.
  - It balances high-detail pixel data (10m) with parcel-based summaries (Land Parcel Framework and 25m rasters) for flexible analytical applications.
  - The product is designed to be integrated with user needs across networks, while maintaining metadata, discoverability, and updated pipelines for ongoing data stewardship.