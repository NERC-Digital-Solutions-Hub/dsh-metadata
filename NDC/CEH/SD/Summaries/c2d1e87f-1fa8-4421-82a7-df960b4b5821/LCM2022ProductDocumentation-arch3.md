# The UKCEH Land Cover Map for 2022

- Purpose: User guide for UKCEH Land Cover Map 2022 (LCM2022). Describes production, validation, data accuracy, and guidance for appropriate use to inform current and future environmental decisions.

- Product scope: LCM2022 consists of seven geospatial datasets (GB and Northern Ireland) plus a 1 km summary raster:
  - 10 m Classified Pixels (GB and NI)
  - Land Parcel datasets (GB and NI)
  - 25 m Rasterised Land Parcels (GB and NI)
  - 1 km Summary rasters (GB and NI)
  - Additional contextual data and metadata discussed in the guide

- Datasets at a glance
  - 10 m Classified Pixel datasets: Pixel-level land cover class (UKCEH Land Cover Class) with a second band giving the classification probability; not generalised by the Land Parcel Spatial Framework to preserve fine detail.
  - Land Parcel datasets: Land parcel attributes created by intersecting 10 m pixels with the UKCEH Land Parcel Spatial Framework; include gid, hist, mode, purity, conf, stdev, agg, n; MMU ~0.5 ha; used for change detection.
  - 25 m Rasterised Land Parcel datasets: 3-band rasters (dominant class mode, conf, purity) derived from rasterising the Land Parcel data.
  - 1 km Summary rasters: Summaries of 25 m data to provide dominant class, aggregate classes, and percentage cover (with rounding; coastal areas may sum to less than 100%).
  - Seasonal Composite Images: Derived from Sentinel-2 (10 m resampled) across four seasons; used with Context Rasters to form Classification Scenes.
  - Context Rasters: 10 m layers to reduce spectral confusion (GB and NI differ slightly in content).
  - Classification Scenes: GB uses 32 tiles (~100 x 100 km), NI uses a single scene; each scene is trained/classified independently.

- Classification and data production
  - Seasonal Composite Images + Context Rasters create Classification Scenes for automatic classification.
  - Bootstrap Training: Automatic sampling of training observations from historical LCM maps (LCM2019–LCM2021) to train the classifier, reducing need for new field data. Pixels with >80% probability and consistent class across three years are used.
  - Random Forest classifier: Trains on bootstrap samples (10,000 per bag) with balanced class representation; majority class is assigned to each pixel; classifier is implemented with bespoke software integrating Weka, PostGIS, and GDAL (open source).
  - Validation: Formal validation using 33,107 reference points across all 21 classes; overall accuracy 86.1% for full thematic detail (LCM2022).
  - Data quality notes: The 10 m classified pixels preserve fine features; formal validation focused on the 25 m Rasterised Land Parcel dataset. Some misclassification occurs where spectral confusion exists (documented in appendices).

- UKCEH Land Parcel Spatial Framework
  - Framework originated for LCM2007; minor changes since LCM2015 for processing efficiency.
  - Parcellization: Parcels are ~0.5 ha MMU; designed to represent discrete land units (fields, parks, urban areas, etc.).
  - GIDs: Unique identifiers (gid) differ from LCM2015; direct parcel ID mapping across versions may not be possible.

- Relationship to Biodiversity Action Plan (BAP)
  - The 21 UKCEH Land Cover Classes are related to BAP Broad Habitats but not identical; BAP definitions are included in appendices to guide interpretation and to address potential ambiguities in cross-referencing. In some cases, BAP and UKCEH classes are distinguished or subdivided (e.g., Urban vs Suburban; Heather vs Heather Grassland).

- Data access and citations
  - Each LCM2022 dataset has a DOI; references to Marston et al. (2023, 2024) provide production methods and dataset-specific details.
  - DOIs provided for 10 m classified pixels, 25 m rasterised land parcels, land parcels (GB/NI), 1 km summary rasters, etc.
  - Disclaimer: Method variations across years may cause small changes beyond real land-cover change.

- Known issues
  - Occasional missing polygons in vector land parcel products; negligible impact on 1 km rasters; 10 m classified pixels remain unaffected.

- Appendices and supplementary materials
  - Appendix 1: Notes on UKCEH Land Cover Classes (descriptions and training considerations, with emphasis on spectral confusion and context)
  - Appendix 2: Biodiversity Action Plan (BAP) Broad Habitats (definitions and crosswalk details)
  - Appendix 3: Full list of LCM2022 datasets and DOIs
  - Appendix 4: Correspondence/validation matrices (producer/user accuracies by class)
  - Appendix 5 & 6: Recommended colour recipes for displaying land cover classes (including colour-blind friendly version) and QGIS symbology files

- Practical implications for monitoring and decision-making
  - Annual production supports change detection by distinguishing real land-cover change from random classifier noise.
  - High-resolution (10 m) data enables detailed habitat mapping, while 25 m parcels and 1 km summaries support broader policy and national-scale monitoring.
  - Bootstrap Training leverages historical maps to minimize field data needs, but some classes (e.g., arable and improved grassland) may require alternative training sources.
  - Clear documentation of class definitions, color schemes, and validation metrics supports reproducibility and governance in monitoring frameworks.