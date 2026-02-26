# The UKCEH Land Cover Map for 2020

- Purpose and scope
  - User guide for the UKCEH Land Cover Map for 2020 (LCM2020), the eighth UK land cover map produced by UKCEH.
  - LCM2020 provides annual land cover data in a consistent format to monitor environmental state and change, with 21 UKCEH Land Cover Classes based on Biodiversity Broad Habitats (BAP) definitions.
  - Classes are aligned with BAP Broad Habitats but are not identical; BAP terms are italicised when referenced to avoid confusion.
  - The product supports monitoring and change detection across time, aiding environmental objectives.

- Product suite (datasets)
  - Six datasets in total, across GB and Northern Ireland (NI):
    - 10m Classified Pixel datasets (per geography)
    - Land Parcel datasets (per geography)
    - 25m Rasterised Land Parcel datasets (per geography)
  - For GB and NI, this results in three dataset types per geography, enabling both high-detail classification and parcel-based analyses.
  - Dataset naming and official product IDs are provided in Appendix 5.

- Data formats and spatial framework
  - 10m Classified Pixels: each pixel has two bands
    - Band 1: integer UKCEH Land Cover Class
    - Band 2: probability/confidence for the assigned class
    - These pixels preserve fine landscape detail (e.g., narrow features) and are not generalised by the Land Parcel Spatial Framework.
    - Recommended for specialist users who understand the implications of non-generalised pixels.
  - Land Parcel datasets: created by intersecting 10m pixels with the UKCEH Land Parcel Spatial Framework
    - Provides parcel-level attributes and supports change detection over time.
  - 25m Rasterised Land Parcel datasets: three-band rasters
    - Band 1: per-parcel dominant land cover (mode)
    - Band 2: mean probability/confidence (conf)
    - Band 3: per-parcel purity (purity)
  - Spatial references
    - Great Britain: EPSG 27700 (British National Grid)
    - Northern Ireland: EPSG 29903 (Irish Grid,TM75)
  - Minimum mapping unit (MMU)
    - Land Parcels have a minimum area of ~0.5 hectares.

- Data production and methodology
  - Classification approach
    - Land cover classified from Classification Scenes composed of Sentinel-2 Seasonal Composite Images plus 10 Context Rasters to reduce spectral confusion.
    - Seasonal composites represent winter, spring, summer, and autumn; nine Sentinel-2 bands used (2, 3, 4, 5, 6, 7, 8, 11, 12).
  - Context and classification scenes
    - Context Rasters include terrain, proximity to buildings/roads/seas/freshwater, foreshore, tidal water, and land cover masks (GB NI-specific sets).
  - Classification Scenes and training
    - GB: 100x100 km Classification Scenes; 74 overlapping scenes used to ensure training diversity; each scene classified independently.
    - NI: single 100x100 km Classification Scene.
    - Bootstrap Training: fully automatic training using historic LCM data (LCM2017–LCM2019) to generate training observations, reducing the need for field data.
    - Training data selection: parcels with >99% purity across three years used; GB: 941,027 training objects; NI: 214,833 training objects.
    - Random Forest (RF) classifier used; sampling with replacement to balance classes (10,000 samples per class).
    - Software: bespoke UKCEH pipeline integrating WEKA, PostGIS, and GDAL (open source).
  - Product validation
    - Validation against GB countryside survey (2019–2020), open-source National Forest Inventory, IACS data, and bespoke LCM validation points (34,715 points total).
    - Result: overall accuracy of 79.2% (full thematic detail; Appendix 4).

- Relationship to Biodiversity Action Plan (BAP) Broad Habitats
  - The 21 UKCEH Land Cover Classes are closely related to BAP Broad Habitats but are not the same; some splits and adaptations exist to better suit remote sensing.
  - Appendix 1 and 2 provide mappings and notes on differences; where appropriate, BAP terms are italicised and UKCEH class names are capitalised.
  - The relationship table shows typical one-to-one mappings, with some exceptions (e.g., Freshwater combining Standing Open Water/Canals and Rivers/Streams; Saltwater treated separately where possible).

- Practical considerations for users
  - Annual maps enable distinction between random classification noise (which flickers over time) and real land-cover change (which persists).
  - Most classification errors are random in space/time; spatial overlaps between Classification Scenes may yield slight variations, which are acceptable for change detection.
  - Validation notes highlight certain challenging classes (e.g., upland peatland, Bracken with Acid Grassland, Neutral/Calcareous grasslands) and the impact of limited training data or spectral similarity.
  - Use of Context Rasters (e.g., slope, distance to water/roads, urban masks) improves discrimination for several habitat types.

- Data quality, caveats, and future improvements
  - Acknowledges that errors occur in all land cover products; no manual corrections are performed at annual scale to enable timely production, but problem areas are noted for future method improvements.
  - Annual production aids change detection but may still show some class-confusion in spectrally similar habitats.
  - The team plans continuous methodological improvements; if significant accuracy gains arise, there is potential for re-application across the entire catalogue to maximise temporal consistency and comparability.

- Appendices and additional references
  - Appendix 1: Notes on UKCEH Land Cover Classes (class-level descriptions and training considerations)
  - Appendix 2: Biodiversity Action Plan (BAP) Broad Habitats (definitions and relationships to UKCEH classes)
  - Appendix 3: Colour mapping recommendations for displaying UKCEH Land Cover Classes
  - Appendix 4: Correspondence matrices (confusion matrices) for LCM2020 (class-by-class accuracy, user/producer accuracies)
  - Appendix 5: Full list of datasets for UKCEH LCM2020 (dataset names and citations)

- Key takeaways for analysts monitoring environmental health
  - LCM2020 provides an annual, standardized view of land cover across GB and NI with 21 detailed classes, supporting change detection and trend analysis.
  - The data blend Sentinel-2 seasonal imagery with contextual layers and a Bootstrap-trained Random Forest classifier to deliver 10m classified pixels and parcel-based products, plus 25m rasterised parcel data.
  - Validation indicates strong, but not perfect, accuracy (~79%), with clear notes on limitations and areas for future improvement.
  - The dataset infrastructure is designed to facilitate data integration, storage, and portal access, enabling users to build time-series datasets for monitoring environmental health and policy performance.