# The UKCEH Land Cover Map for 2020

- Purpose and scope
  - A user guide for LCM2020, the eighth UKCEH land cover map, produced annually.
  - Consists of six datasets across GB and Northern Ireland: for each region, a 10 m classified pixel dataset, a land parcel dataset, and a 25 m pixel rasterised land parcel dataset.
  - Aims to maximise temporal consistency, enable change detection, and support environmental decision-making.
  - Overall validation accuracy is just over 79% at full thematic detail (about 79.2%).

- Land cover classes and relationships
  - 21 UKCEH Land Cover Classes, aligned with Biodiversity Action Plan (BAP) Broad Habitats but not identical; authors note differences and preserve consistency with earlier products.
  - Appendices map relationships between UKCEH classes and UK BAP Broad Habitats, including notes on potential spectral confusion and training data limitations.
  - Generalised UK CEH Aggregate Classes are provided for the Land Parcel product, with explicit crosswalks to BAP Broad Habitats.

- Datasets and formats
  - 10 m Classified Pixel datasets (GB and NI)
    - Per-pixel classification from Classification Scenes; first band = most likely UKCEH Land Cover Class, second band = class membership probability.
    - Not generalised by the Land Parcel Spatial Framework to preserve fine landscape detail (e.g., narrow features below MMU).
    - Recommended for specialist users who understand the implications of high-resolution outputs.
  - Land Parcel datasets (GB and NI)
    - Created by intersecting 10 m classified pixels with the UKCEH Land Parcel Spatial Framework.
    - Provide parcel-level attributes and summary statistics; includes a fixed MMU (~0.5 ha) and discrete land parcels representing real-world units (fields, parks, urban areas, etc.).
    - Parcel identifiers (gid) differ from those in LCM2015 due to framework changes, affecting direct year-to-year gid-based comparisons.
  - 25 m Rasterised Land Parcel datasets (GB and NI)
    - Raster representation of parcels with three bands: dominant land cover (mode), mean confidence (conf), and parcel purity (purity).
  - Seasonality and spectral information
    - Seasonal Composite Images (Sentinel-2) used to create 46-band Classification Scenes for GB (36-band Sentinel-2 plus 10 Context Rasters) and a 43-band scene for NI.
    - Seasonal bands cover winter, spring, summer, and autumn (using bands 2, 3, 4, 5, 6, 7, 8, 11, 12); cloud gaps are handled with null data.
  - Context Rasters (10 m)
    - Added to reduce spectral confusion (e.g., height, aspect, slope, distances to roads/buildings/coast, urban masks, water, woodlands, etc.).
  - UK Land Parcel Spatial Framework
    - A long-standing framework (MMU ~0.5 ha) used to generalise national cartography; changes since 2015 affect parcel identifiers and some comparability.

- Methodology
  - Bootstrap Training
    - Automatic, self-starting training approach that uses historical LCM data (2017–2019) as training data for current classification.
    - Training dataset for GB: ~941k objects; for NI: ~214k.
    - Filters training parcels to high-purity examples (>99%) across years to build large, stable training samples.
  - Random Forest classification
    - Supervised learning using Bootstrap Training parcels to sample pixels from Classification Scenes; 10,000 samples per class with replacement to balance training.
    - Produces the 10 m Classified Pixel product; uses a bespoke pipeline combining Weka, PostGIS, and GDAL (open source).
  - Validation and accuracy
    - Validated against GB countryside survey data (2019–2020), National Forest Inventory data, IACS data, and bespoke validation points (34715 points total).
    - Overall accuracy reported as 79.2% (Appendix 4).
  - Change detection and temporal consistency
    - Annual production aims to separate real-world change from random classification noise (random errors expected to flicker over time).
    - The rich time-series supports monitoring change in the UK countryside and informing environmental objectives.

- Practical considerations for analysts
  - Data scale and accessibility
    - The 10 m pixel outputs preserve detailed landscape features but require careful interpretation and domain knowledge.
    - The Land Parcel datasets enable consistent change detection and aggregation despite higher-resolution noise in pixel data.
  - Spatial scale, boundaries, and comparability
    - LCM2020 uses a fixed spatial framework with MMU ~0.5 ha, which may exclude small features; coastal and upland areas present particular mapping challenges noted in appendices.
    - GID-based year-to-year comparisons with LCM2015 are not straightforward due to changes in the Land Parcel Spatial Framework identifiers.
  - Uncertainties and known issues
    - Spectral confusion persists among certain habitats (e.g., Neutral Grassland, Bracken, upland peat vegetation).
    - Saltwater vs Freshwater mapping can be ambiguous in tidal/coastal zones; Saltmarsh and Littoral classifications may have commission/interpretation errors.
    - Linear features and narrow boundaries are not reliably classified as separate land cover types; linear features are acknowledged but not explicitly classified as distinct classes.
  - Data usage and outputs
    - 10 m Classified Pixels: best for detailed analyses, custom maps, and change detection at fine scales; requires caution due to lack of MMU generalisation.
    - 25 m Rasterised Land Parcels: suitable for parcel-based analyses and change detection; includes per-parcel confidence measures.
    - Land Parcel Datasets: essential for aggregated analyses, trend detection, and linking land cover to spatial frameworks.
  - Data access and metadata
    - Appendix 5 lists official dataset names and geographic scope (GB and NI) and associated coordinate reference systems (GB: EPSG 27700; NI: EPSG 29903).
    - Document emphasizes the importance of metadata for discoverability and reuse.

- Appendices and supplementary guidance
  - Appendix 1: Notes on UKCEH Land Cover Classes with detailed species/habitat notes and potential misclassification scenarios.
  - Appendix 2: Biodiversity Action Plan (BAP) Broad Habitats – definitions and cross-walk to UKCEH classes.
  - Appendix 3: Recommended colour recipes for displaying UKCEH Land Cover Classes (for visualization).
  - Appendix 4: Correspondence matrices and accuracy metrics by class (producer’s and user’s accuracy; confusion matrices).
  - Appendix 5: Full list of LCM2020 datasets by region and data type.
  - The guide explains that while BAP Broad Habitat definitions informed the classes, satellite-based mapping cannot perfectly reproduce field-level classifications, and ongoing refinements are planned as methods improve.

- Use cases for analysts
  - Correlation and trend analyses of land cover types over time to assess policy and management impacts.
  - Predictive modeling of land cover change using the time-series dataset (annual maps).
  - Change detection in environmental planning, habitat restoration, or urban-rural expansion contexts.
  - Data fusion opportunities by combining 10 m pixel detail with parcel-based attributes for high-resolution, policy-relevant insights.
  - Spatial planning and environmental monitoring at national, regional, and local scales, with explicit awareness of scale-related limitations and classification uncertainties.