# The UKCEH Land Cover Maps for 2017, 2018 and 2019 v1.5.1

## Purpose and scope
- User guide for three new UKCEH Land Cover Maps: LCM2017, LCM2018, and LCM2019.
- Map content: 21 UKCEH Land Cover Classes based on Biodiversity Action Plan (BAP) Broad Habitats; compatible with but not identical to historical BAP classifications.
- Production emphasizes automated methods (Bootstrap Training + Random Forest) to enable rapid, coast-to-coast UK coverage.
- Annual release planned to track land cover change; visual checks and formal validation performed to assess quality.

## Data products and structure
- Dataset families (GB and NI each):
  - 20m Classified Pixels: new RF classifications with per-pixel class and a second band indicating membership probability (0–100) for confidence; preserves fine detail (not generalised).
  - Land Parcels: attributes linking 20m pixels to UKCEH Land Parcel Spatial Framework; includes per-parcel histories, modal class, purity, confidence, and other summary stats.
  - 25m Rasterised Land Parcels: rasterised summary (3 bands: modal class, confidence, purity) with partial generalisation from parcel data.
  - 1km Percent Cover: 21-band raster showing percent cover by each class per 1km square.
  - 1km Percent Aggregate Cover: 10-band raster showing percent cover by UKCEH Aggregate Classes per 1km.
  - 1km Dominant Cover: single-band raster of dominant class per 1km.
  - 1km Dominant Aggregate Cover: single-band raster of dominant Aggregate Class per 1km.
- Dataset count: total of 42 datasets (GB and NI for each year).
- Spatial framework: Land Parcel Spatial Framework retained (MMU ~0.5 ha); gid identifiers do not match LCM2015 for cross-year comparisons (use gid for cross-year linkage).
- Coordinate systems and extents:
  - Great Britain: British National Grid (EPSG 27700) for GB datasets.
  - Northern Ireland: Irish Grid (TM75 / EPSG 29903) for NI datasets.
- Pixel/lineage details:
  - 20m Classified Pixels provide class with a probability band (0–100) to indicate classification confidence.
  - 25m Rasterised Parcels and 1km rasters aggregate 20m results through the Land Parcel Spatial Framework.

## Production methodology and data sources
- Classification approach:
  - Bootstrap Training: automatic generation of training data from historic UKCEH LCMs (starting from LCM2015) to train the RF classifier for 2017–2019.
  - For 2017–2019, 99% purity parcels from LCM2015 were used to bootstrap training; future bootstraps planned around majority signals over multi-year windows.
  - RF classifier trained with balanced samples (10,000 per class per training bag) to ensure rarer classes are well represented.
- Imagery and features:
  - Seasonal Composite Images derived from Sentinel-2 (TOA reflectance; 20m resolution) per season (winter, spring, summer, autumn) using Google Earth Engine.
  - Context Rasters (20m) to reduce spectral confusion (terrain, proximity to urban features, roads, water, etc.).
  - Classification Scenes: GB classified in 100x100 km tiles (46-band scenes: 36 spectral + 10 context); NI uses a single 43-band scene per year guided by the minimum bounding rectangle of NI land mass.
- Data processing and quality checks:
  - No manual corrections were applied to LCM2017–LCM2019; production relies on automated classification with spatial and temporal validation.
  - Visual inspection and formal validation (Appendix 4) conducted to ensure maps are of comparable quality to LCM2015.
- Tools and software:
  - Production pipeline integrates Weka machine learning with PostGIS and GDAL; all tools are open source.

## The UKCEH Land Parcel Spatial Framework and data governance
- Spatial framework:
  - Framework unchanged in geometry and count from LCM2015, but stored with different indices for faster processing; gid values do not match LCM2015 but can be used for cross-year parcel comparisons.
  - Framework ensures parcels are approximately 0.5 ha MMU and are designed to represent discrete land units (fields, parks, urban areas, etc.) to support change detection.
- Data governance and interoperability:
  - Acknowledges potential use of alternative parcel boundaries by users; 20m Classified Pixels are provided to support user-defined parcel schemes.
  - Notes potential future refinement of the Land Parcel Spatial Framework as higher-resolution data and new training data become available.
- Data availability and documentation:
  - Full dataset descriptions, appendices, and a complete dataset list provided (Appendix 5).
  - Class descriptions and mappings to BAP Broad Habitats documented in Appendices 1 and 2.

## Data quality, validation, and caveats
- Validation results (UK scale):
  - LCM2017: 78.6% overall accuracy
  - LCM2018: 79.6% overall accuracy
  - LCM2019: 79.4% overall accuracy
- Validation data:
  - 22,325 points from GB countryside survey, National Forest Inventory, IACS, and bespoke validation points; intersection with Land Parcel datasets used to derive accuracy metrics.
- Considerations and caveats:
  - Validation points are not absolute truth; class definitions differ from validation sources and had to be mapped to UKCEH classes.
  - Around 80% correspondence is notable given automatic classification and class definition differences.
  - Seasonal gaps due to cloud: some seasons may be incomplete; algorithm tolerates partial spectral information, reducing need for manual gap filling.
  - Cross-year comparability caveat: gid-based cross-year comparisons are possible, but direct parcel identifier matches with LCM2015 are not guaranteed.
- Appendices and detailed matrices:
  - Appendix 4 contains confusion matrices and class-level accuracy metrics (Producer’s and User’s accuracies by year and class).

## Practical considerations for data stewards and governance
- Data structure and metadata:
  - Rich metadata for each dataset, including class definitions, attribute schemas (gathered in Table/Appendix references), and changes from LCM2015.
  - 20m Classified Pixels provide per-pixel confidence; notable for uncertainty assessment and downstream decision-making.
- Data update and maintenance:
  - Intent to release an LCM annually (LCM2020 planned for 2021; subsequent updates planned on majority signals from recent years).
  - Ongoing evaluation of input data types (e.g., consideration of Sentinel-1 SAR to fill seasonal gaps) and expansion of classification inputs.
- Governance and usage guidance:
  - Emphasis on using like-with-like comparisons across years due to class definitions and parcel framework nuances.
  - Clear notes on gid changes and the need to use gid for longitudinal parcel-tracking; cross-year parcel comparison with 2015 identifiers may be unreliable.
- Access and use rights:
  - Data is distributed with multiple product formats and scales (20m, 25m, 1km) to support varied workflows.
  - Users may implement their own parcel frameworks using the 20m Classified Pixels, enabling bespoke analyses while maintaining the original parcel-derived summaries.

## Where to find details
- Appendix 1–4: Class definitions, vocabulary, methodological notes, and validation details.
- Appendix 5: Full list of datasets per year and product type (GB and NI, by year).
- Dataset examples and figures illustrating dataset structures and interrelations are described in the main text (e.g., Figures 1–5).