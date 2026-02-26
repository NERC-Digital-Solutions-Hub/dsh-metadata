# The UKCEH Land Cover Map for 2020

- Purpose and scope
  - UKCEH LCM2020 is the eighth UK land cover map, produced annually using automated methods.
  - Product suite comprises six datasets: three for Great Britain (GB) and Northern Ireland (NI) each (10m Classified Pixels, Land Parcel Spatial Framework-derived parcels, and a 25m Rasterised Land Parcel dataset).
  - Goal: describe data production, validation, and accuracy to help users apply LCM data effectively and understand limitations.

- Data products
  - 10m Classified Pixel datasets
    - Classified from Classification Scenes; each pixel gets a UKCEH Land Cover Class ID and an associated probability (confidence).
    - Does not use the Land Parcel Spatial Framework for generalisation, preserving fine landscape detail; intended for specialist users aware of implications.
  - Land Parcel datasets
    - Result from intersecting 10m Classified Pixels with the UKCEH Land Parcel Spatial Framework to create parcel attributes.
    - GB: ~6.74 million parcels; NI: ~0.90 million parcels.
  - 25m Rasterised Land Parcel datasets
    - Rasterised version of parcels (per-parcel attributes) at 25m resolution with three bands: dominant class (mode), mean confidence (conf), and purity.
  - Dataset extents and formats
    - GB and NI datasets have defined CRS: GB (EPSG:27700), NI (EPSG:29903); explicit metadata and naming in Appendix 5.

- Methods: imagery, context, and classification
  - Seasonal Composite Images
    - Sentinel-2-based seasonal composites (winter, spring, summer, autumn) using nine spectral bands; filled gaps with nulls when cloud occurs, classifier tolerates partial data.
  - Context Rasters
    - 10m context rasters to reduce spectral confusion (e.g., height, aspect, slope; distances to buildings, roads, coast, freshwater; foreshore and binary masks; woodland mask for GB; urban mask and coast/freshwater/d roads for NI).
  - Classification Scenes and training
    - GB: 100x100 km Classification Scenes (46-band) formed from overlapping tiles; 74 scenes classified independently with manual precedence for final cut.
    - NI: single 36-band Classification Scene per year using NI context rasters.
    - Bootstrap Training: automatic training data derived from historical LCMs (LCM2017–2019) filtered to >99% purity; GB ~941k objects; NI ~214k objects.
  - Random Forest classification
    - Supervised RF with balanced sampling: 10,000 samples per class (with replacement) drawn from labeled parcels to train pixel-level classifier.
    - Training integrates Bootstrap Training data with pixel-level observations to produce the 10m Classified Pixel product.
  - Software and provenance
    - Bespoke UKCEH software integrating WEKA, PostGIS, and GDAL; open-source components.

- UKCEH Land Parcel Spatial Framework and MMU
  - The Land Parcel Spatial Framework (from LCM2007 onward) provides discrete land parcels (~0.5 ha MMU) to reduce noise and enable change-detection comparisons over time.
  - Gid identifiers differ from LCM2015 due to reorganization of storage/indices; spatial overlap comparisons between 2020 and 2015 require spatial, not parcel-ID, matching.
  - Framework designed to support robust, repeatable parcel-level analysis, even as the pixel classification evolves.

- Validation and accuracy
  - Validation approach: comparison with countryside survey data (2019/2020), open-source National Forest Inventory data, IACS data, and bespoke validation points.
  - Total validation points: 34,715; overall accuracy reported at 79.2% for full thematic detail (Appendix 4).
  - Appendix 4 provides confusion matrices and per-class Producer’s and User’s accuracies, highlighting areas of higher and lower reliability.

- UKCEH Land Cover Classes and BAP Broad Habitats
  - 21 UKCEH Land Cover Classes are aligned, but not identical, to UK BAP Broad Habitats (Jackson 2000).
  - Appendices 1–2 map relationships and note when a UKCEH class corresponds to a BAP Broad Habitat (and where distinctions exist).
  - Some cells/relationships are nuanced; appendices provide detailed guidance and examples.

- Data access, display, and recommendations
  - Full thematic detail is available, with a recommended color recipe in Appendix 3 for display purposes.
  - Users should be aware that 10m Classified Pixels are not generalised and reflect fine-scale structure, but validation does not cover this dataset directly (validation is at the Land Parcel level).
  - Annual production aims to differentiate real land-cover change from random classification errors (errors are expected to flicker over time).

- Appendices and additional details (highlights)
  - Appendix 1: Notes on UKCEH Land Cover Classes (guidance and potential spectral confusions between classes).
  - Appendix 2: Biodiversity Action Plan (BAP) Broad Habitats definitions and their relationship to UKCEH Classes.
  - Appendix 3: Colour recipes for displaying UKCEH Land Cover Classes.
  - Appendix 4: Full correspondence matrices, producer/user accuracies by class (detailed validation results).
  - Appendix 5: Full list of datasets and official dataset names, extents, and metadata details for GB and NI datasets.

- Full dataset list (Appendix 5)
  - 10m Classified Raster Product (GB)
  - Land Parcel Product (GB)
  - 25m Rasterised Land Parcel Product (GB)
  - 10m Classified Raster Product (NI)
  - Land Parcel Product (NI)
  - 25m Rasterised Land Parcel Product (NI)