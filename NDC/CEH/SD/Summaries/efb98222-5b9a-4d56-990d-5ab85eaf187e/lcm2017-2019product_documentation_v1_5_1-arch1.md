# The UKCEH Land Cover Maps for 2017, 2018 and 2019 v1.5.1

- Purpose and scope
  - User guide accompanying the release of three new UKCEH Land Cover Maps: LCM2017, LCM2018, and LCM2019.
  - Describes content, production workflow, validation, production decisions, and future plans to help users apply the data correctly.
  - 21 UKCEH Land Cover Classes based on Biodiversity Action Plan (BAP) Broad Habitats; aligned with LCM2015 and earlier maps for comparability.
  - Class descriptions and derived relationships with UKCEH Aggregate Classes provided; emphasis on consistent change detection and interpretation.

- Data products and structure
  - Datasets produced for each year (GB and Northern Ireland):
    - 20 m Classified Pixels: RF classification results with per-pixel class and a confidence score (0–100). Preserves fine landscape detail; not generalised by Land Parcels.
    - Land Parcels: parcel-level attributes summarising 20 m pixels within the UKCEH Land Parcel Spatial Framework (min ~0.5 ha MMU). Includes gid, hist, mode, purity, conf, stdev, n.
    - 25 m Rasterised Land Parcels: three-band raster (mode, conf, purity) summarising parcels.
    - 1 km rasters: 
      - 1 km Percent Cover (21 bands)
      - 1 km Percent Aggregate Cover (10 bands)
      - 1 km Dominant Cover (single band)
      - 1 km Dominant Aggregate Cover (single band)
  - Dataset extents and coordinate systems
    - Great Britain: British National Grid (EPSG:27700)
    - Northern Ireland: Irish Grid TM75 (EPSG:29903)
    - Pixel sizes and band counts specified for each product (e.g., 20 m Classified Pixels, 25 m Land Parcels, 1 km rasters).

- Production workflow and inputs
  - Seasonal Composite Images from Sentinel-2 (TOA reflectance, median per season) used to create 20 m Classification Scenes.
  - Context rasters (20 m) added to mitigate spectral confusion; include terrain, proximity to buildings/roads/coast, foreshore, tidal water, woodland, etc.
  - Classification Scenes
    - Great Britain: 74 overlapping 100 x 100 km tiles used to generate 46-band GB Classification Scenes; each scene trained and classified independently; overlaps resolved by visual inspection to select best results.
    - Northern Ireland: single 43-band Classification Scene per year (36 spectral bands + 7 context layers) based on the minimum bounding rectangle of NI land mass.
  - UK Land Parcel Spatial Framework
    - Maintains ~0.5 ha MMU; reorganised storage and indexing for faster processing.
    - gid identifiers do not match LCM2015 parcel IDs; comparisons between 2017–2019 and 2015 require parcel overlap rather than IDs.
  - Bootstrap Training
    - Fully automatic training using Bootstrap Training: historic maps (LCM2015) provide spectral training observations for current Sentinel-2 scenes.
    - Sampling from LCM2015 land parcels with high purity (≥99%) to create balanced training sets; intended to bootstrap 2020 and 2021 maps with progressively longer majority signals.
  - Random Forest classification
    - Training uses 10,000 samples per class, drawn with replacement to balance classes.
    - Software: bespoke production tool integrating Weka, PostGIS, and GDAL.

- Satellite data and processing choices
  - Sentinel-2 Seasonal Composite Images (TOA used; SR did not improve classification for UKCEH Land Cover Classes in this release).
  - Some seasonal data gaps due to cloud; classifier designed to tolerate partial spectral information.
  - Context rasters provide additional contextual information to reduce spectral confusion (e.g., coastal proximity, urban proximity, terrain).

- Validation and accuracy
  - Validation dataset: 22,325 points from GB countryside survey (2019), open forest inventory data, IACS, and bespoke LCM validation points.
  - Reported accuracy (UK scale, 21-class automatically produced maps):
    - LCM2017: 78.6%
    - LCM2018: 79.6%
    - LCM2019: 79.4%
  - Validation notes: same validation points used across products; currency and class mapping differences mean accuracy should be interpreted as indicative rather than absolute truth. Appendix 4 provides full validation tables.

- Class definitions and related information
  - 21 UKCEH Land Cover Classes derived from BAP Broad Habitats; relationships to UKCEH Aggregate Classes provided (Tables and Appendices).
  - Appendix content includes: notes on each Broad Habitat class, translation considerations between BAP and UKCEH classes, and guidance on interpretation.

- Visualization and metadata
  - Appendix 3 provides recommended RGB color recipes for display of UKCEH Land Cover Classes.
  - Datasets are accompanied by metadata and are designed to be discoverable (e.g., through portals) with documentation and appendix references (Appendix 5 lists full dataset inventories).

- Future plans and notable decisions
  - Intention to release a new LCM annually going forward.
  - Manual accuracy corrections are not performed in this cycle to enable automation; visual checks and formal validation still occur.
  - Ongoing evaluation of input data (e.g., expansion of data inputs beyond Sentinel-2 TOA) and potential future improvements to training data and thematic resolution.

- Practical considerations for analysts
  - If comparing to LCM2015, use gid-based parcel comparisons for 2017–2019 with caution due to changes in the Land Parcel Spatial Framework.
  - The 20 m Classified Pixels dataset preserves fine features and includes a per-pixel confidence score, useful for downstream analysis and thresholding.
  - The 1 km products facilitate landscape-scale analyses with broad coverage and multiple class/aggregate metrics.
  - Validation indicates strong but not perfect accuracy; consider contextual validation for specific study areas and timeframes.
  - The methodology relies on Bootstrap Training and RF, with ongoing plans to refine bootstrap inputs for subsequent product generations.