# The UKCEH Land Cover Map for 2020

- LCM2020 is the eighth UKCEH land cover map, produced annually with automated methods to enable near-real-time monitoring of the UK countryside.
- Product comprises six datasets across GB and Northern Ireland: three datasets per region (10 m Classified Pixels, Land Parcel Dataset, and 25 m Rasterised Land Parcels). In total, datasets cover Great Britain and Northern Ireland with differing pixel and parcel representations.
- The map uses 21 UKCEH Land Cover Classes aligned with Biodiversity Action Plan (BAP) Broad Habitats, with careful attention to consistency and comparability with earlier products.

## Data assets and structure

- 10 m Classified Pixel datasets
  - Generated from Classification Scenes; each pixel is assigned a UKCEH Land Cover Class plus a confidence probability.
  - For GB, 46-band Classification Scenes are produced by combining Sentinel-2 Seasonal Composite Images with 10 Context Rasters.
- Land Parcel datasets
  - Result from intersecting 10 m Classified Pixels with the UKCEH Land Parcel Spatial Framework (MMU ~0.5 ha).
  - Provide parcel-level attributes for change detection and aggregation.
- 25 m Rasterised Land Parcel datasets
  - Rasterised version of land parcels with three attributes carried per parcel (mode, conf, purity).
- Datasets per region
  - Great Britain: 10 m Classified Pixels, Land Parcel Product, 25 m Rasterised Parcel Product.
  - Northern Ireland: 10 m Classified Pixels, Land Parcel Product, 25 m Rasterised Parcel Product.
- Dataset metadata
  - Official dataset names and extents are documented; GB and NI use respective coordinate systems (GB: EPSG 27700; NI: EPSG 29903).

## Methodology and data production

- Seasonal imagery and contextual data
  - Seasonal Composite Images derived from Sentinel-2 across four seasons (winter, spring, summer, autumn) using a multi-band approach.
  - 10 Context Rasters (e.g., height, slope, proximity to buildings/roads/coast, urban mask) are incorporated to reduce spectral confusion.
- Classification Scenes and tile approach
  - GB uses overlapping 100 x 100 km tiles to extract 36-band Seasonal Composite Images and 10 context layers, creating 46-band GB Classification Scenes.
  - NI uses a single 36-band Seasonal Composite Image combined with 7 Context Rasters to create 43-band NI Classification Scenes.
- Bootstrap Training and Random Forest (RF)
  - Bootstrap Training: automatic generation of training data from historic LCM maps (LCM2017–2019) to train the classifier, reducing the need for new field data.
  - Training data filtered for high purity (>99%) across three years; GB training objects ~941,027; NI ~214,833.
  - Random Forest classifier trained with 10,000 pixel samples per class (bag sampling with replacement) to balance classes.
- Land Parcel Spatial Framework
  - Framework provides discrete land parcel units for aggregation and comparison over time; parcels help reduce classification noise and enable change detection.
- Validation and accuracy
  - Validation performed against GB countryside survey data (2019–2020), National Forest Inventory, IACS, and bespoke LCM validation points (34,715 locations).
  - Overall accuracy: 79.2% at full thematic detail (Appendix 4).
- Temporal intent
  - Annual production aims to separate genuine land cover change from classification noise, leveraging the time-series nature of the data.

## Product details and class mapping

- UKCEH Land Cover Classes: 21 classes derived from UKBAP Broad Habitats; relations to BAP Broad Habitats are described with emphasis on consistency and cross-referencing (Appendices 1–2).
- Display and interpretation
  - A recommended color recipe is provided for displaying UKCEH Land Cover Classes.
  - Tables and correspondence matrices illustrate relationships between UKCEH Classes and BAP Broad Habitats, including typical confusions and notes on detection challenges (Appendix 4).
- Special considerations
  - Some spectral confusions are anticipated (e.g., Saltwater vs Freshwater, upland peat vegetation), but context layers help improve discrimination.
  - Linear features (boundaries/linear features) are not classified as a separate UKCEH Land Cover Class due to spectral limitations, though they may appear in higher-resolution 20 m data.

## Data quality, limitations, and use

- Accuracy and validation
  - Overall accuracy around 79.2%; validation highlights producer and user accuracies by class, with some variability among rare vs common classes.
- Scaling and MMU
  - Land Parcel MMU ~0.5 ha; 10 m pixel data preserves fine features not captured in parcel-aggregated products.
- Limitations
  - Some classes (e.g., Bracken, upland peat vegetation) may require updated training data or refined methods due to spectral similarity and training data limitations.
  - Annual updates may still exhibit some classification noise; the time series helps distinguish persistent changes from random errors.
- Practical implications for Data Leaders
  - Provides a robust, annually updated data asset for monitoring land cover change, supporting environmental objectives and policy analysis.
  - Rich metadata, provenance, and validation enable integration with wider datasets and governance frameworks.
  - Emphasizes the need for data discoverability, standardization, and alignment with historical maps for comparability.

## Appendix highlights (context for governance and strategy)

- Appendix 1–2: Notes on UKCEH Land Cover Classes and the Biodiversity Action Plan Broad Habitats, including mappings, interpretation nuances, and reported limitations.
- Appendix 3: Color recipes for display of Land Cover Classes.
- Appendix 4: Detailed correspondence matrices and class-level accuracy statistics.
- Appendix 5: Full list of datasets and their official naming for LCM2020 (GB and NI).