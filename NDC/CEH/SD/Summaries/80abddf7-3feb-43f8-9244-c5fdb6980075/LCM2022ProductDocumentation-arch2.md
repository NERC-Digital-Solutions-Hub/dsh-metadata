# The UKCEH Land Cover Map for 2022

- Purpose and outputs
  - User guide for the UKCEH Land Cover Map for 2022 (LCM2022), the tenth UK land cover map.
  - Produces seven datasets: three for Great Britain and three for Northern Ireland (10 m classified pixels, land parcels, and 25 m rasterised land parcels) plus a 1 km summary raster covering GB and NI.
  - Objective is to enable informed decisions about land cover state and change, with validation and data quality guidance.

- UKCEH Land Cover Classes and BAP relationship
  - LCM2022 maps 21 UKCEH Land Cover Classes based on Biodiversity Action Plan (BAP) Broad Habitats, though not identical to BAP classifications.
  - BAP Broad Habitats are italicised when referred to; main land cover classes are UKCEH-specific.
  - Appendix 1–2 explain class definitions and relationships, including where BAP and UKCEH classes diverge (e.g., saltwater vs freshwater, urban/suburban splits).

- Dataset suite and structure
  - 10 m Classified Pixel datasets (GB and NI): per-pixel classification with two bands — most likely UKCEH Land Cover Class and associated class-membership probability.
  - Land Parcel datasets: derived by intersecting 10 m classified pixels with the UKCEH Land Parcel Spatial Framework to produce parcel-level attributes (35+ fields described in Table 3).
  - 25 m Rasterised Land Parcel datasets: rasterised parcel outputs with three bands (dominant land cover, mean confidence, and parcel purity).
  - 1 km Summary rasters: four products summarising 25 m data to 1 km scale (dominant class, aggregate dominant, class percentage, aggregate percentage).
  - Coordinate systems: GB uses British National Grid (EPSG 27700); NI uses Irish Grid TM75 (EPSG 29903).
  - Pixel resolution and extents provided for GB and NI with clearly defined extents and product names.

- Data production and inputs
  - Land cover is produced by classifying Classification Scenes that combine Sentinel-2 Seasonal Composite Images with Context Rasters to reduce spectral confusion.
  - Seasonal Composite Images: four-season median reflectance derived from Sentinel-2 bands (2, 3, 4, 5, 6, 7, 8, 8A, 11, 12); occasional null data gaps are handled by the classifier without manual gap filling.
  - Context Rasters: 10 m layers to resolve spectral confusion (terrain, proximity to buildings/roads/water, foreshore, woodlands, saltmarsh, etc.). GB and NI have tailored sets of context rasters.
  - Classification Scenes: GB is partitioned into about 32 tiles; NI uses a single scene covering the land mass.
  - Bootstrapped Training: automatic Bootstrap Training uses historic LCM pixels (LCM2019–LCM2021) filtered to >80% probability and consistent class across years to train a Random Forest classifier, reducing the need for new field data.

- Machine learning and workflow
  - Random Forest classifier trained on balanced bootstrap samples to ensure rare classes are learned adequately.
  - Production software combines Weka, PostGIS, and GDAL; the pipeline is designed to enable annual map updates for temporal consistency and change detection.
  - The approach aims to differentiate real change from random classification noise as the time-series matures.

- Validation and accuracy
  - Formal validation used 33,107 reference points across all 21 classes.
  - Overall accuracy of LCM2022: 86.1% at full thematic detail.
  - Appendix 4 provides detailed confusion matrices, user’s and producer’s accuracies for each class.

- Known issues and caveats
  - A small number of polygons are missing from the vector Land Parcel products, causing nodata in some 25 m raster parcels; negligible effect on 1 km products; 10 m pixels unaffected.
  - Methodological differences across annual maps mean some changes reflect updates in production methods as well as real change; users should consider this when comparing across years.

- Citing and data access
  - Each LCM2022 dataset has a DOI; Marston et al. (2023/2024) provide production method context and previous-year overviews.
  - Data products include 10 m classified pixels (GB and NI), land parcels (GB and NI), 25 m rasterised land parcels (GB and NI), and 1 km summary rasters (GB and NI).
  - The document provides guidance on proper citation and references for the datasets.

- Practical implications for analysts monitoring the environment
  - Annual maps enhance temporal consistency, support change detection, and help distinguish real land-cover changes from classification noise.
  - The 10 m classified pixels retain fine landscape detail, while 25 m parcel products offer structured, comparable units for change analysis.
  - The 1 km rasters provide scalable summaries for broader, landscape-scale assessments.
  - Clear guidance on class definitions, their relationships to BAP habitats, and the inclusion of context layers informs classification interpretation and comparability with earlier UKCEH products.

- Appendices and supplementary resources
  - Appendices 1–2: detailed notes on UKCEH Land Cover Classes and BAP Broad Habitats.
  - Appendix 3: full list of datasets and DOIs.
  - Appendix 4: comprehensive correspondence matrices from validation.
  - Appendices 5–6: recommended color recipes (standard and color-blind friendly) for displaying the classes; accompanied by QGIS symbology files.