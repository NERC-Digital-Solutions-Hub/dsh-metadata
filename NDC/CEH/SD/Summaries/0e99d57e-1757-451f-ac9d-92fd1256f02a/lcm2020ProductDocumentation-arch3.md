# The UKCEH Land Cover Map for 2020

- Purpose and scope
  - User guide for the UKCEH Land Cover Map 2020 (LCM2020).
  - LCM2020 comprises six geospatial datasets (GB and Northern Ireland) across three core product types, with the goal of enabling informed decision-making, monitoring change, and supporting environmental objectives.
  - Provides data production details, validation, and data accuracy to help users apply LCM2020 appropriately.

- What LCM2020 is and why it matters
  - Eighth UK land cover map from UKCEH; maps 21 UKCEH Land Cover Classes based on Biodiversity Action Plan (BAP) Broad Habitats.
  - Maps are produced annually using automated methods to improve temporal consistency and enable change detection.
  - Classification mediante Classification Scenes created from Sentinel-2 Seasonal Composite Images plus 10 Context Layers; automated Bootstrap Training with a Random Forest classifier.
  - Overall validation accuracy is just over 79% at full thematic detail (79.2% reported).

- Data products and datasets
  - 10m Classified Pixel datasets: classified classification scenes; each pixel carries a class identifier and a confidence/probability.
  - 10m Classified Pixels: preserves fine landscape detail (not generalized to Land Parcel Spatial Framework) for specialist use.
  - Land Parcel datasets: attributes produced by intersecting 10m pixels with the UKCEH Land Parcel Spatial Framework (MMU ~0.5 hectares).
  - 25m Rasterised Land Parcel datasets: per-parcel land-cover, mean confidence (_conf) and purity (_purity) per parcel; three-band rasters available.
  - 20m Classified Pixel datasets and 20m Rasterised land parcels are included for Northern Ireland (NI) in the dataset suite.
  - Appendix 5 lists the full dataset catalog and naming conventions.

- Classification scenes, seasons and context information
  - Seasonal Composite Images (Sentinel-2) derived from Google Earth Engine, with four seasons (winter, spring, summer, autumn) and nine Sentinel-2 bands used for classification.
  - Context Rasters mitigate spectral confusion (e.g., terrain, proximity to features, water, and urban elements). GB uses 10 context rasters; NI uses 7 context rasters including urban mask and distance layers to coast, roads, and water.
  - Classification Scenes: GB uses overlapping 100x100 km tiles, producing 74 overlapping Classification Scenes; NI uses a single 43-band Scene for the year.
  - The UK Land Parcel Spatial Framework (used to standardize parcel geometry) remains largely unchanged in size but its parcel identifiers differ from LCM2015, affecting direct parcel-id comparisons.

- Bootstrap Training and Random Forest approach
  - Bootstrap Training: fully automatic training process that reuses historic LCM data (2017–2019) to train classifiers for new maps, reducing the need for fresh field data.
  - Training data consist of land parcels with high purity (>99% across three years) from LCM2017–2019; GB training objects ≈ 941,027; NI ≈ 214,833.
  - Random Forest classifier trained on sampled pixels from Classification Scenes; ensures balanced class representation by drawing 10,000 samples per class with replacement.

- Validation and data quality
  - Validation performed against GB countryside survey data (2019, 2020), National Forest Inventory data, IACS data, and bespoke validation points (34715 points in total).
  - Overall accuracy: 79.2% (LCM2020) on full thematic detail (Appendix 4 contains the detailed confusion matrices and class-level accuracies).
  - Validation highlights and limitations discussed, including known spectral ambiguities and the presence of confusions among certain habitat types.

- Relationship to biodiversity classifications (BAP) and interpretation guidance
  - The 21 UKCEH Land Cover Classes are closely related to BAP Broad Habitats but are not identical; BAP Broad Habitats were designed for field botanists, not satellite detection.
  - The guide provides notes on mapping between UKCEH Land Cover Classes and UK BAP Broad Habitats, including examples of where one-to-one relationships hold or where distinctions are blurred.
  - Appendices outline detailed definitions and potential confusions (e.g., Arable vs Improved Grassland, Bracken vs Acid Grassland, upland vegetation classifications).

- Practical considerations for policy monitoring and data use
  - The annual production supports separation of real change from random classification errors; persistent changes indicate genuine land cover change.
  - The 0.5 ha MMU and the lack of manual corrections in 2020 affect the detectability of small features; users should understand that very small patches may be underrepresented.
  - Data governance, metadata availability, and openness are important considerations; sharing underlying data and metadata can be a barrier for some users, a matter highlighted in the project’s approach to transparency and data use.

- Technical and implementation notes
  - Data formats include 8-bit raster products and multiple-band rasters; 10m and 25m pixel resolutions are used for different products; NI also includes 20m products.
  - Colour recipes and display guidance are provided (Appendix 3) to standardize visualization of the Land Cover Classes.
  - The data suite is designed to support change detection, temporal comparability, and integration with environmental monitoring objectives and reporting.
  - Open-source components (WEKA, PostGIS, GDAL) underpin the classification workflow.

- References and supporting material
  - Core methodological references (Random Forests, Bootstrap Training) and foundational UKCEH/Land Cover methodologies cited in the document.
  - Appendices provide detailed class definitions (Appendix 1 and 2), color mapping (Appendix 3), full validation matrices (Appendix 4), and the complete dataset listing (Appendix 5).