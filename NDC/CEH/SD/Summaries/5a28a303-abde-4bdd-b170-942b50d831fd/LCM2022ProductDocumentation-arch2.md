# The UKCEH Land Cover Map for 2022

- Purpose and scope
  - UKCEH LCM2022 is the tenth land cover map in the series, produced annually to monitor state and change of the UK countryside.
  - 21 UKCEH Land Cover Classes aligned with Biodiversity Broad Habitats (BAP) concepts; classification uses Sentinel-2 Seasonal Composite Images plus Context Rasters to reduce spectral confusion.
  - The document describes data production, validation, accuracy, and guidance for informed use; continuous improvement with potential re-application of new methods to maintain temporal consistency and support change detection.

- Data products (dataset suite)
  - 10 m Classified Pixel datasets
    - Available for Great Britain (GB) and Northern Ireland (NI); two bands: most likely UKCEH Land Cover Class and associated classification probability (confidence).
    - High spatial detail; not generalised by the UKCEH Land Parcel Spatial Framework to preserve fine features.
  - Land Parcel datasets (25 m rasterised)
    - GB and NI; rasterised 25 m representation of Land Parcels with per-parcel attributes (mode, confidence, purity, etc.) and linkage to the UKCEH Land Parcel Spatial Framework (MMU ~0.5 ha).
  - Land Parcel Vector products (vector land parcels)
    - GB and NI versions; include per-parcel identifiers and attributes; intended for analyses requiring parcel-level units.
  - 1 km summary rasters
    - GB and NI; dominant class per 1 km pixel and percentage cover by class (both 21 UKCEH classes and 10 aggregated classes); summary statistics deliberately rounded; coastal areas may sum to less than 100% due to coast delineation.
  - Seasonal Composite Images
    - Derived from Google Earth Engine; four seasonal composites (Jan–Mar, Apr–Jun, Jul–Sep, Oct–Dec) using Sentinel-2 bands; occasional cloud gaps represented as nulls; classifier tolerant of partial data.
  - Context Rasters
    - 10 m context rasters to reduce spectral confusion; GB includes terrain (height, aspect, slope) and proximity masks (buildings, roads, tidal water, freshwater, foreshore, woodland, saltmarsh); NI includes similar context plus urban mask and additional proximities.
  - Classification Scenes
    - GB split into 32 tiles (~100 x 100 km) for localized training/classification; NI uses a single scene; independent classification per scene to manage regional phenology variation.
  - The UKCEH Land Parcel Spatial Framework
    - Framework for generalising land parcels to stable units; used to create the 25 m rasterised parcel products and to enable change detection; note that gid identifiers differ from LCM2015 if you compare parcel IDs across versions.
  - Metadata and DOIs
    - Each LCM2022 dataset has a DOI; citations provided (including Marston et al. 2023/2024) for production methods and validation.

- Data production and methods
  - Bootstrap Training
    - Automatic training data generation using historic LCMs (2019–2021) filtered to pixels with >80% probability and consistent class across three years; enables large, wall-to-wall training data without new field collection.
  - Random Forest classification
    - RF classifier trained on Bootstrap Training samples (10,000 per bag, balanced across classes); uses bespoke UKCEH software integrating WEKA, PostGIS, and GDAL.
  - Prediction outputs
    - 10 m classified pixels: two-band output (class ID and confidence), preserved at full 10 m resolution to retain fine landscape features.
  - Validation and accuracy
    - Formal validation against 33,107 reference points across all 21 classes; overall accuracy 86.1% for LCM2022 (full thematic detail).
  - Data governance and updates
    - Annual production aims for temporal consistency; known issues may arise from methodology changes between editions; methods may be refined or re-applied for improvements.

- Relationship to land cover classes and BAP Broad Habitats
  - 21 UKCEH Land Cover Classes are closely related to BAP Broad Habitats but not identical; some mappings are nuanced and explained in Appendices.
  - Appendices provide guidance on class meanings, potential spectral confusion, and how BAP Broad Habitats relate to UKCEH classes (with specific notes on difficult-to-separate types like various grasses, bogs, heather, and fen-related habitats).

- Known issues and caveats
  - A small number of polygons are missing from vector land parcel products, with corresponding nodata areas in the 25 m rasterised parcel dataset; negligible impact on 1 km products; 10 m classified pixels are unaffected.
  - Differences in methods year-to-year may produce real changes as well as methodological differences; users should interpret changes with this in mind.

- How to use and interpret
  - Data are designed for monitoring land cover state and change over time, enabling change detection by comparing across annual LCM editions.
  - The 10 m classified pixels provide detailed land cover classification with a confidence metric to inform uncertainty.
  - The 25 m parcel products and 1 km rasters offer scalable, area-based summaries suitable for integration with other datasets and regional analyses.
  - The mapping to BAP Broad Habitats supports habitat-related assessments, while highlighting areas where spectral separation is challenging.

- Access, citation, and further information
  - DOIs are provided for all LCM2022 data products; users should cite the corresponding dataset DOIs and Marston et al. (2024) for production methods.
  - Appendices include extensive technical detail on class definitions, correspondence matrices, and colour schemes (including color-blind friendly variants) for display in GIS applications.

- Appendix highlights (quick reference)
  - Appendix 1–2: Notes on UKCEH Land Cover Classes and their relationship to UK BAP Broad Habitats; guidance on interpretation and potential spectral confusion.
  - Appendix 3: Full list of LCM2022 datasets and their DOIs.
  - Appendix 4: Correspondence matrices and accuracy metrics by class (Producer’s and User’s Accuracy).
  - Appendix 5–6: Recommended colour schemes (standard and color-blind friendly) with corresponding QGIS symbology files.