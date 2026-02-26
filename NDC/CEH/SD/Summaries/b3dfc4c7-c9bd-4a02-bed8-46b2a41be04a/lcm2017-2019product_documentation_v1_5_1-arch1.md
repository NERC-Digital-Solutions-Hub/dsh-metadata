# The UKCEH Land Cover Maps for 2017, 2018 and 2019 v1.5.1

- Purpose and scope
  - Release of three new UKCEH Land Cover Maps: LCM2017, LCM2018, and LCM2019.
  - Each map comprises a suite of geospatial datasets with 21 UKCEH Land Cover Classes based on Biodiversity Action Plan (BAP) Broad Habitats.
  - Maps produced automatically using Bootstrap Training combined with a Random Forest classifier; annual updates planned.
  - Seasonal Sentinel-2 data (TOA) processed into 20 m classified pixels, then summarised into land parcels and other products.
  - Context rasters and Seasonal Composite Images used to reduce spectral confusion.
  - No manual corrections applied this cycle; visual checks and formal validation performed; maps deemed of similar quality to LCM2015.

- Data structure and datasets
  - 20 m Classified Pixels: new RF classification results with per-pixel class and a confidence score (0–100).
  - Land Parcels: 20 m classified pixels linked to a UKCEH Land Parcel Spatial Framework; includes parcel-level attributes.
  - 25 m Rasterised Land Parcels: summary rasters (band 1: modal class; band 2: confidence; band 3: purity).
  - 1 km rasters: three products summarising parcel data at 1 km scale:
    - 1 km Percent Cover (21-band)
    - 1 km Percent Aggregate Cover (10-band)
    - 1 km Dominant Cover (1-band)
    - 1 km Dominant Aggregate Cover (1-band)
  - Each dataset has GB (EPSG:27700) and NI (EPSG:29903) versions.

- Production methodology
  - Bootstrap Training: automatic generation of training data from historic UKCEH LCMs (starting with LCM2015) to bootstrap new maps.
  - Training set construction: >99% purity parcels from LCM2015 used to train RF classifier; balanced sampling (10,000 samples per class) to ensure rarer classes are learned.
  - Random Forest classification: bespoke UKCEH software integrating WEKA, PostGIS, and GDAL; outputs 20 m Classified Pixels.
  - Classification Scenes and tiling: Great Britain classified with overlapping 100 x 100 km tiles (36-band Seasonal Composite Images + 20 m Context Rasters; 46-band GB Classification Scenes); NI classified with a single 43-band Scene per year.
  - Context Rasters (20 m): include terrain (height, aspect, slope), distances to roads/buildings/coast, and land/water masks to reduce spectral confusion.

- Seasonal and spectral inputs
  - Seasonal Composite Images: median TOA reflectance per season (winter, spring, summer, autumn) from Sentinel-2; nine bands (2, 3, 4, 5, 6, 7, 8, 11, 12); gaps due to cloud handled by RF tolerance.
  - Sentinel-2 bands and resolutions summarized; choice of TOA over surface reflectance (SR) after testing potential gains.

- UKCEH Land Parcel Spatial Framework
  - Framework unchanged in geometry from LCM2015 but re-ordered storage and new indices for faster processing.
  - gid remains a stable parcel identifier within this framework, but new products’ gid values do not match LCM2015 for direct parcel-to-parcel comparison.
  - Minimum Mapping Unit (MMU) ~0.5 ha; parcels represent discrete real-world units (fields, parks, etc.).
  - Framework supports summation and comparison across time; users may supply their own parcel structures if desired.

- Dataset specifics and metadata
  - 20 m Classified Pixels: two-band raster (class, confidence 0–100) preserving fine detail, not generalised by parcel framework.
  - Land Parcels: parcel-level attributes including hist (class frequency per parcel), mode, purity, conf (mean class membership probability), stdev, and npix.
  - 25 m Rasterised Land Parcels: three-band raster (mode, conf, purity).
  - 1 km rasters: 21-band Percent Cover; 10-band Percent Aggregate Cover; single-band Dominant Cover; 1 km Dominant Aggregate Cover.
  - Tables and appendices describe class mappings to UK BAP Broad Habitats and relationships to Aggregate/Standard Classes.

- Classification validity and caveats
  - Validation: UK-wide validation using GB countryside survey 2019 data, open data like National Forest Inventory, IACS, and bespoke LCM validation points (22,325 points total).
  - Reported accuracies (GB scale):
    - LCM2017: 78.6%
    - LCM2018: 79.6%
    - LCM2019: 79.4%
  - Validation data currency and class conversion introduce some uncertainty; results are best-available indicators rather than absolute truth.
  - Notable limitations: some classes show inter-class confusion (e.g., acid vs. neutral grassland, bog vs. heath-related classes); upland peatland mapping remains challenging.
  - No manual corrections were applied this cycle to maintain rapid annual production; visual checks and formal validation still performed.

- Geographic scope and formats
  - Great Britain and Northern Ireland coverage; GB uses British National Grid (EPSG:27700), NI uses Irish Grid (EPSG:29903).
  - 100 x 100 km tile strategy for GB; single NI tile approach due to smaller area.
  - Output formats include 8-bit rasters with explicit class IDs, per-pixel confidence, and parcel-level attributes.

- Appendix highlights and usage guidance
  - Appendix 1 and 2: detailed notes on UKCEH Land Cover Classes and their relationship to BAP Broad Habitats; clarifications of classification nuances and detection limits.
  - Appendix 3: recommended color scheme for displaying UKCEH classes.
  - Appendix 4: validation results and confusion matrices (summary across 21 classes).
  - Appendix 5: full list of datasets per year and per product (20 m Classified Pixels, Land Parcels, 25 m Rasterised Land Parcels, 1 km products) and their GB/NI holdings.
  - Emphasis on comparing like-for-like across maps for change detection and awareness of spatial framework differences when comparing to LCM2015.

- Future directions and plans
  - Intent to release a new LCM annually; plan to extend to additional data sources and may consider deeper use of surface reflectance data or other platforms to improve thematic detail.
  - LCM2020 planned for 2021 release; ongoing evaluation of training data sources and classification approaches to enhance accuracy and timeliness.