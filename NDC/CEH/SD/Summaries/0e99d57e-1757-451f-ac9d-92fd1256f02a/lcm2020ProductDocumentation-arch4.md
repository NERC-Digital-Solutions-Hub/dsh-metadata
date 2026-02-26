# The UKCEH Land Cover Map for 2020

- Purpose and scope
  - User guide for the LCM2020, the eighth UK land cover map produced by UKCEH.
  - Product consists of six datasets for GB and Northern Ireland: for each area, a 10m Classified Pixel dataset, a Land Parcel dataset, and a 25m Pixel Rasterised Land Parcel dataset (or 25m rasterised land parcel dataset).
  - UKCEH Land Cover Classes total 21, aligned with Biodiversity Action Plan (BAP) Broad Habitats; aims to enable annual production, improve temporal consistency, and support change detection.
  - Validation shows an overall accuracy of about 79.2% at full thematic detail.

- Data products (dataset suite)
  - 10m Classified Pixel datasets: per-location classified pixels with two bands (class identifier + associated probability/confidence). Not generalised by the Land Parcel Spatial Framework to preserve fine landscape details.
  - Land Parcel datasets: land parcel attributes derived by intersecting 10m Classified Pixels with the UKCEH Land Parcel Spatial Framework.
  - 25m Rasterised Land Parcel datasets: three-band rasters carrying per-parcel information (dominant class _mode, mean confidence _conf, and parcel purity _purity).
  - Separate datasets exist for Great Britain and Northern Ireland; Appendix 5 lists official dataset names.

- Data production and methodology
  - Classification scenes and inputs
    - Seasonal Composite Images: Sentinel-2 data (0.443–2.190 μm bands) resampled to various resolutions; four seasons (winter, spring, summer, autumn) used to capture phenology.
    - Context Rasters (10m): include terrain (height, aspect, slope) and proximity/context features (distance to buildings/roads/coast/water, foreshore and tidal masks, woodland).
  - Classification scenes
    - GB: 100x100 km tiles used to extract 36-band Seasonal Composite Images; combined with 10 Context Rasters to form 46-band Classification Scenes; 74 overlapping scenes created and classified independently; visual prioritisation used to select final results in overlaps.
    - NI: single Classification Scene per year (36-band Sentinel-2 plus context rasters) resulting in a 43-band scene.
  - Land Parcel Spatial Framework
    - Framework designed to generalise national cartography into discrete parcels (minimum ~0.5 ha MMU) to reduce noise and enable change detection.
    - 10m Classified Pixels are later associated with parcels; gid identifiers differ from LCM2015 due to system changes.
  - Bootstrap Training
    - Fully automatic training process that uses historic LCM data (LCM2017–2019) to derive training observations (Bootstrap Training) without new field data.
    - Training data: parcels with >99% purity across three years; GB: 941,027 objects; NI: 214,833 objects.
    - Purpose: leverage wall-to-wall historic data to train the Random Forest classifier for current imagery.
  - Random Forest classification
    - Supervised RF model trained on Bootstrap Training data; 10,000 samples drawn per class with replacement to balance training across all UKCEH Land Cover Classes.
    - Output: 10m Classified Pixel product with class identifier and confidence for each pixel.
    - Software: bespoke UKCEH tool integrating WEKA, PostGIS, and GDAL (open source).
  - Validation and accuracy
    - Validation against GB countryside survey 2019/2020 data, National Forest Inventory, IACS, and bespoke validation points (34,715 locations).
    - Overall accuracy reported as 79.2% (Appendix 4).
  - Data quality and limitations
    - 10m classified pixels are highly detailed but not subjected to Land Parcel spatial framework generalisation; some limitations acknowledged in Appendix 4 related to distribution of classes and spectral similarities.
    - Saltwater vs Freshwater distinctions can be affected by coastal context rasters and tidal timing; some misclassifications possible near coasts.

- Data access, metadata, and formats
  - Datasets include:
    - 10m Classified Pixels (GB and NI)
    - Land Parcel attributes (GB and NI)
    - 25m Rasterised Land Parcels (GB and NI)
  - Dataset names and full metadata are provided in Appendix 5.
  - Extents and coordinate systems differ by region (OSGB for GB, Irish Grid for NI).

- Spatial and thematic relationships
  - UKCEH Land Cover Classes are related to, but not identical with, BAP Broad Habitats; clear crosswalks and notes are provided to maintain consistency with historical products.
  - Appendices detail class definitions, crosswalks with BAP Broad Habitats, and recommended color schemes for display.
  - Some upland and mosaic habitats (e.g., peatlands, bracken, mosses) are discussed with notes on spectral limitations and training data needs.

- Practical implications for data leaders
  - Strategic value: provides an annual, nationally consistent land cover dataset enabling change detection and long-term monitoring of the UK countryside.
  - Data governance: clear data lineage, from Seasonal Composites and Context Rasters through Classification Scenes to 10m Pixel and Land Parcel products; robust validation framework and explicit caveats on generalisation and accuracy per class.
  - Interoperability: uses open-source tools (WEKA, PostGIS, GDAL) and standard geospatial formats; Appendix 5 lists official dataset names for cataloguing and integration.
  - User needs and uptake: 10m Pixels preserve fine landscape features useful to specialized analyses; Land Parcel products support change detection, aggregation, and temporal comparison; guidance notes on when to use high-detail vs parcel-generalised outputs.
  - Future direction: annual automation reduces labour costs, supports timeliness and change detection; ongoing method development and potential improvements for underrepresented habitats and upland vegetation.