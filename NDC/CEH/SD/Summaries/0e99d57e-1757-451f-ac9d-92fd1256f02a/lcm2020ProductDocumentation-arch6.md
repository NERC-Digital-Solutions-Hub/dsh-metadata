# The UKCEH Land Cover Map for 2020

- Objective and scope
  - UKCEH LCM2020 comprises six datasets (three for GB and Northern Ireland): 10m classified pixel dataset, land parcel dataset, and a higher-resolution rasterised land parcels dataset (GB: 10m and 25m; NI: 10m and 20m for classification with corresponding parcel products).
  - 21 UKCEH Land Cover Classes tied to Biodiversity Action Plan (BAP) Broad Habitats; classes are mapped to BAP concepts but are not exact equivalents.
  - Purpose is to enable informed decisions with an annually updated, remotely sensed land cover map and associated data products.

- Product suite and resolutions
  - GB:
    - 10m Classified Pixel dataset: best-guess land cover class per pixel plus a confidence/probability band; preserves high detail (no generalisation to land parcel framework).
    - Land Parcel dataset: attributes derived by intersecting 10m pixels with the UKCEH Land Parcel Spatial Framework; 0.5 ha minimum mapping unit (MMU).
    - 25m Rasterised Land Parcel dataset: three-band raster with per-parcel mode (land cover), mean conf, and purity.
  - Northern Ireland (NI):
    - 10m Classified Pixel dataset (20m classification not used here; NI uses a 20m reference in Appendix notes for certain internal metrics, but classification outputs named here are 10m, with NI-specific schema).
    - Land Parcel dataset (NI) with corresponding 20m pixel context in some internal steps.
    - 25m Rasterised Land Parcel dataset (NI).
  - Datasets listed in Appendix 5 with official names; GB products generally at 10m and 25m, NI products include 10m classification and 20m classification variants in the documentation.

- Data production framework
  - Seasonal information
    - Seasonal Composite Images derived from Google Earth Engine using Sentinel-2 data, with four seasons (winter, spring, summer, autumn) across nine Sentinel-2 bands.
    - Some seasonal gaps due to clouds are allowed; classification can tolerate partial spectral information.
  - Context rasters
    - 10m Context Rasters used to reduce spectral confusion; GB context rasters include terrain (Height, Aspect, Slope), distance to buildings/roads/sea/freshwater, foreshore mask, tidal water mask, and a woodland mask.
    - NI context rasters include terrain plus urban mask and distance to coast, freshwater, roads.
  - Classification Scenes
    - GB: 100x100 km tiles used to select 36-band Seasonal Composite Images; combined with 10 Context Rasters to form 46-band Classification Scenes; 74 overlapping scenes classified independently; visual precedence resolves overlaps for final cut.
    - NI: single 100x100 km tile (minimum bounding rectangle) used with 36-band seasonal data plus 7 NI context rasters to create a 43-band Classification Scene for the year.
  - Bootstrap Training
    - A fully automatic training approach that uses historical LCMs (Bootstrap Training) to sample training observations without new field data.
    - Training data derived from LCM2017–2019; filtered to parcels with >99% purity across three years.
    - GB training objects: 941,027; NI: 214,833.
  - Random Forest classification
    - Random Forest classifier trained on bootstrap training samples; 10,000 samples per class drawn with replacement to balance classes.
    - Processed with bespoke UKCEH software integrating WEKA, PostGIS, and GDAL.
  - Validation and accuracy
    - Validation against GB countryside survey (2019-2020), open-source National Forest Inventory, IACS data, and bespoke validation points (34715 points).
    - Overall accuracy: 79.2% for full thematic detail (Appendix 4).

- Data structure, formats, and metadata
  - 10m Classified Pixel datasets (GB and NI)
    - Band 1: most likely UKCEH Land Cover Class (integer).
    - Band 2: associated classification probability/confidence.
    - Note: 10m pixels are not generalised by the Land Parcel Spatial Framework to preserve fine landscape features; target users should be aware validation was performed against the Land Parcel dataset, not the 10m pixels.
  - Land Parcel datasets
    - Attributes per parcel including:
      - _hist: frequency of 20m pixels per land cover class within parcel
      - _mode: most frequent land cover class in parcel
      - _purity: percentage of the modal class within parcel
      - _conf: mean class membership probability (0–100)
      - _stdev: standard deviation of _conf
      - _n: number of 10m pixels intersecting the parcel
    - Identifiers: ogc_fid, gid; note that parcel IDs differ from LCM2015, so cross-map comparisons by gid may not be direct.
  - 25m Rasterised Land Parcel datasets
    - 3-band rasters per parcel: dominant land cover class (_mode), mean confidence (_conf), and purity (_purity).
  - Coordinate systems and extents
    - Great Britain: EPSG 27700 (OSGB36 / British National Grid)
    - Northern Ireland: EPSG 29903 (Irish Grid)
  - Datasets and naming
    - Appendix 5 enumerates official dataset names and formats for LCM2020 (GB and NI across 10m, 20m/25m raster products, and land parcel products).

- Class definitions and alignment with BAP Broad Habitats
  - UKCEH Land Cover Classes (21 classes) align with BAP Broad Habitats but are not exact equivalents.
  - Appendices detail mappings and notes on potential spectral confusion, e.g., between Arable and Improved Grassland, Neutral Grassland detection aids, and Saltwater vs Freshwater distinctions in coastal zones.
  - General guidance and color recipes for display provided (Appendix 3).

- Practical usage notes
  - Annual production increases the ability to distinguish real land cover change from random classification errors (errors are expected to be random and not persistent year-to-year).
  - Validation shows strong performance for many classes but varying accuracies by class (detailed producer’s and user’s accuracies available in Appendix 4 confusion matrices).
  - Users should be aware that the 10m pixel data preserves fine features, while parcel-based products enable consistent temporal comparison and change detection at the MMU level.

- Access, updates, and iteration
  - LCM2020 is positioned as the eighth UK land cover map with annual updates; method developments continue to seek improvements in accuracy and temporal consistency.
  - If new methods yield significant accuracy improvements, the entire catalogue may be updated or re-applied to improve comparability and change detection.

- Additional references and appendices
  - Appendix 1 and 2: detailed notes on UKCEH Land Cover Classes and BAP Broad Habitats definitions and relationships.
  - Appendix 3: recommended color prescriptions for displaying Land Cover Classes.
  - Appendix 4: comprehensive correspondence matrices (confusion matrices) and accuracies for each class (producer’s and user’s accuracies).
  - Appendix 5: full list of LCM2020 datasets with official dataset names and formats.