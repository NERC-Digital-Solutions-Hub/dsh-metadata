# The UKCEH Land Cover Maps for 2017, 2018 and 2019 v1.5.1

- Purpose and scope
  - Release of three UKCEH Land Cover Maps: LCM2017, LCM2018, and LCM2019.
  - Each map contains 21 UKCEH Land Cover Classes (based on BAP Broad Habitats) and matches the class scheme used in LCM2015.
  - Maps produced automatically using Bootstrap Training + Random Forest; intended to enable rapid, annual UK-wide land cover mapping.
  - Data produced from Sentinel-2 Seasonal Composite Images (TOA reflectance) plus 20m context rasters; created for Great Britain and Northern Ireland; 42 datasets in total (3 years × GB/NI × data products).

- How outputs are generated
  - Bootstrap Training
    - Automatic, no fresh field data required.
    - Bootstraps from historic LCM2015 data (≥99% purity) to create training sets for classification.
    - Builds a majority-signal training dataset for subsequent maps; future bootstraps planned from 3-year signals (2017–2019, then 2018–2020, etc.).
  - Random Forest classification
    - Balanced sampling: 10,000 samples per class per Classification Scene.
    - Uses Bootstrap Training data to classify 20m Classified Pixels.
    - GB uses 36-band Seasonal Composite Images + 10 Context Layers to form 46-band Classification Scenes (74 overlapping scenes classified independently; visual/manual selection resolves overlaps).
    - NI uses a single 43-band (36 spectral + 7 context) Classification Scene per year.
  - Classification outputs and data structure
    - 20m Classified Pixels: 2-band rasters; band 1 = most likely class, band 2 = confidence (0–100). Preserves fine details not merged into parcels.
    - Land Parcels (UKCEH Land Parcel Spatial Framework): fixed parcels ~0.5 ha MMU; attributes include gid, hist, mode, purity, conf, stdev, n. Note: gid values do not match LCM2015; use gid to compare across 2017–2019.
    - 25m Rasterised Land Parcels: 3-band raster; band 1 = modal class (mode); band 2 = parcel-averaged confidence; band 3 = purity.
    - 1km rasters (produced by aggregating 25m parcels):
      - 1km Percent Cover: 21-band, 8-bit raster (percent cover per class per 1km).
      - 1km Percent Aggregate Cover: 10-band, 8-bit raster (aggregate class cover per 1km).
      - 1km Dominant Cover: 1-band, 8-bit raster (dominant class per 1km).
      - 1km Dominant Aggregate Cover: 1-band, 8-bit raster (dominant aggregate class per 1km).
  - Seasonal and contextual inputs
    - Seasonal Composite Images: four seasons (winter, spring, summer, autumn) from Sentinel-2, TOA reflectance, 20m resolution; sometimes with gaps due to cloud.
    - Context Rasters (GB 20m; NI 20m): include height, aspect, slope, distance to buildings/roads/sea/freshwater, foreshore mask, tidal water; NI also includes urban mask and coast/freshwater/road distances.
  - Classification Scenes and tiling
    - GB: 100x100 km tiles, 74 overlapping scenes; each scene trained/classified independently; overlaps may produce slight result variations; manual precedence applied to select final results.
    - NI: single 43-band scene per year per country.
  - UKCEH Land Parcel Spatial Framework
    - Framework originated for LCM2007; minor updates for LCM2017–2019; parcels 0.5 ha MMU; designed to group 20m classified pixels into real-world units; facilitates time-series comparisons but gid changes limit direct cross-year parcel matching with LCM2015.
  - Bootstrap Training and validation
    - Bootstrap Training uses historic data (LCM2015 as a baseline) to train the RF classifier; aims to use majority signals to robustly classify current imagery.
    - Validation: UK-scale validation against 22,325 points from GB countryside survey 2019, National Forest Inventory, IACS, and bespoke LCM validation points.
    - Reported overall accuracy (approximate):
      - LCM2017: 78.6%
      - LCM2018: 79.6%
      - LCM2019: 79.4%
    - Validation notes: uses a common validation dataset across products; accuracy reflects automatic maps with some inevitable misclassification; Appendix 4 contains full validation tables.

- Class definitions and thematic notes
  - 21 UKCEH Land Cover Classes are aligned with UKCEH LCM2015 and are linked to UK BAP Broad Habitats where applicable.
  - Appendix guidance clarifies class relationships, potential spectral confusions, and context-driven improvements (e.g., Neutral Grassland detection aided by slope and distance-to-water context rasters).
  - Some detailed notes on specific classes (e.g., Bracken, upland peatland vegetation) discuss limitations of remote sensing for fine distinctions and the intent to refine training data as methods evolve.

- Spatial reference, extents, and data access
  - Coordinate systems
    - Great Britain: British National Grid (EPSG: 27700)
    - Northern Ireland: Irish Grid (TM 75, EPSG: 29903)
  - Pixel and parcel sizes
    - 20m Classified Pixels; 25m Rasterised Land Parcels; 1km rasters as aggregations
  - Extents
    - GB-wide coverage; NI coverage documented separately
  - Access and reuse
    - Outputs are designed for end-user self-serve: 20m classified pixels, land parcels with detailed per-parcel attributes, 25m rasterised parcels, and multi-scale 1km rasters
  - Practical considerations for users
    - GIDs do not match across years; cross-year parcel comparisons should use gid for LCM2017–2019 comparisons rather than LCM2015 crosswalks
    - Some data products (e.g., 1km aggregates) are large and multi-band; users may need processing tools to handle 21-band per-1km rasters

- Appendices and additional resources (highlights)
  - Appendix 1 and 2: Detailed notes on UKCEH Land Cover Classes and Biodiversity Action Plan Broad Habitats; guidance on detection plausibility and class-level caveats
  - Appendix 3: RGB color recipes for displaying each land cover class
  - Appendix 4: Full confusion matrices and validation metrics for 2017–2019 (per-class and total) and producer/user accuracies
  - Appendix 5: Full list of datasets per year and per data product (GB/NI)

- Future plans and use cases
  - Intention to release a new LCM annually; exploration of filling seasonal gaps with alternative optical sources and radar (Sentinel-1) to improve continuity
  - Ongoing evaluation of input data (e.g., land surface reflectance vs TOA) and potential expansion of the input feature set
  - Emphasis on providing robust data products for policy support, land management, and environmental monitoring, with a data structure designed to enable flexible, self-serve analysis and product iteration

- Practical tips for Data Support audience
  - Leverage 20m Classified Pixels for maximum detail and use Land Parcels for stable, management-oriented units; use 1km rasters for coarse-scale change detection and thematic summaries
  - When comparing across years, prefer gid-based parcel comparisons for 2017–2019, and be cautious with direct LCM2015-to-2017 comparisons due to gid changes
  - Consult Appendices for class definitions, validation context, and recommended color schemes to support visualization and interpretation in client-facing outputs