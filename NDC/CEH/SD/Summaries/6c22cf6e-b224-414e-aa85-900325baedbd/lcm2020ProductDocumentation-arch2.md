# The UKCEH Land Cover Map for 2020

- Purpose and scope
  - User guide for LCM2020, the UKCEH land cover map for 2020.
  - Produces six datasets for GB and Northern Ireland, including multiple resolutions of land cover information.
  - Aims to help users apply UKCEH LCM data consistently, with attention to data production, validation, and accuracy to support environmental decisions and monitoring over time.

- Land cover classes and relationships
  - Defines 21 UKCEH Land Cover Classes based on Biodiversity Action Plan (BAP) Broad Habitats.
  - Classes are closely related to BAP Broad Habitats but not identical; BAP terms are italicised when referenced.
  - Appendix 1–2 provide detailed notes on class definitions and their relationship to BAP Broad Habitats, including examples and caveats for spectral separation.

- Data products (datasets and outputs)
  - 10m Classified Pixel datasets: classification results at 10 m resolution with two bands per pixel (class identifier and associated probability/confidence).
  - 25m Rasterised Land Parcel datasets: per-parcel results derived by intersecting 10m pixels with the UKCEH Land Parcel Spatial Framework; three-band rasters (mode, conf, purity) to summarize parcel-level land cover.
  - Land Parcel Spatial Framework: fixed land parcel objects (minimum ~0.5 ha) used to reduce noise and enable change detection; parcels are designed to reflect discrete real-world units (fields, parks, urban areas, etc.).
  - 20m Classified Raster Product (Great Britain): an additional GB-only 20m classified raster product (alongside 10m products) for GB-scale analyses.
  - 8-bit Raster Products: per-parcel rasters and related outputs at 8-bit resolution for some components.
  - Output formats and metadata are aligned with official dataset names and Extent/CRS details (GB: EPSG: 27700; NI: EPSG: 29903).

- Data production and inputs
  - Classification Scenes and inputs
    - Seasonal Composite Images: Sentinel-2 data (winter, spring, summer, autumn) processed to provide temporal information for classification.
    - Context Rasters: 10 GB context rasters (height, aspect, slope, distance to buildings/roads/sea/freshwater, foreshore, tidal water, woodland) and 7 NI context rasters (similar but NI-specific masks and urban/shore features).
    - Classification Scenes: GB uses a mosaic of 100×100 km tiles to extract 36-band Seasonal Composite Images, combined with Context Rasters to form 46-band GB Classification Scenes; NI uses a single 36/43-band scene per year.
  - Bootstrap Training
    - Fully automatic training that uses historic LCM data (LCM2017–2019) as training observations, reducing the need for new field data.
    - Training parcels filtered to >99% purity across three years; GB training set ~941,027 objects; NI ~214,833.
  - Random Forest classification
    - Balanced sampling: from each class, 10,000 pixel samples drawn with replacement to train the RF classifier.
    - Classifier output: 10m Classified Pixel product with the most likely class and the probability/confidence for that class.
  - Production approach
    - Fully automated, with minimal manual corrections to preserve annual production cadence and differentiate genuine change from random errors.
    - Visual checks used only to determine final precedence when overlapping Classification Scenes exist.
    - Aim to maximise temporal consistency and enable robust change detection over time.

- Validation and accuracy
  - Validation performed against GB countryside survey data (2019–2020), open-source National Forest Inventory data, IACS, and bespoke validation points (34715 points total).
  - Overall accuracy reported at just over 79% (specifically 79.2%).
  - Appendix 4 provides detailed confusion matrices and producer/user accuracies by class, illustrating how well each class is detected and where confusions occur.

- Practical implications for analysts
  - The annual production supports monitoring state and change of the UK countryside and underpins environmental objectives, policy performance tracking, and change detection.
  - The 10m classified pixels preserve fine landscape detail (e.g., narrow linear features) not generalized by the Land Parcel Framework; this is targeted at specialist users who understand the implications of non-generalized pixel-level data.
  - The Land Parcel datasets and spatial framework enable standardized parcel-based comparison over time, aiding change detection and integration with other datasets.
  - The relationship with BAP Broad Habitats ensures compatibility with historical classifications while acknowledging spectral limitations and the need for ancillary context layers.

- Temporal aspects and data management
  - UKCEH aims to produce annual maps to maximize temporal comparability and to distinguish errors from real-world change (random errors tend to flicker year-to-year; real changes persist).
  - Because of automated processing, there is no retroactive/manual re-editing across the entire catalog; instead, improvements are integrated in future releases as methods evolve.
  - The spatial identifiers (gid) for Land Parcels may shift between LCM2015 and LCM2020 due to back-end structural changes; most users will not be impacted, but cross-year parcel ID matching may not be straightforward.

- Methodological notes and appendices
  - Appendix 3 provides recommended color mappings for displaying each UKCEH Land Cover Class.
  - Appendix 4 contains full correspondence matrices and class-level accuracy details (confusion matrices, user/producer accuracies by class).
  - Appendix 5 lists official dataset names and extents, clarifying data products and resolutions (including GB NI distinctions and GB 20m product).

- Key takeaways for monitoring and decision-making
  - LCM2020 offers a robust, annually updated land cover dataset with 21 UKCEH classes, enabling monitoring of land cover extent and change at both pixel and parcel levels.
  - The combination of Sentinel-2 seasonal information, context rasters, and Bootstrap Training with Random Forest provides a reproducible, scalable approach to land cover mapping.
  - Validation indicates strong overall accuracy (~79%), with detailed class-level performance documented in the appendices.
  - Users should be aware of differences between UKCEH Land Cover Classes and historical BAP Broad Habitats, and of potential misclassifications in spectrally similar or patchy land cover types, particularly near coastlines and upland peat areas.