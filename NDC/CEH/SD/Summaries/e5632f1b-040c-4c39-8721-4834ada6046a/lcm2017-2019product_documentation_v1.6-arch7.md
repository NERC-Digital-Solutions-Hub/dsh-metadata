# The UKCEH Land Cover Maps for 2017, 2018 and 2019 v1.6

- Overview
  - Release of three UKCEH Land Cover Maps (LCMs): LCM2017, LCM2018 and LCM2019.
  - Maps cover 21 UKCEH Land Cover Classes (based on Biodiversity Action Plan Broad Habitats) and match earlier LCM2015 classifications.
  - Production is fully automatic (Bootstrap Training + Random Forest); aims for annual UK-wide maps with rapid production and consistent updates.

- What the guidance covers
  - How the data were produced and validated.
  - Production decisions, data structure, and future plans.
  - Practical guidance to help users apply UKCEH LCM data appropriately.

- Key data products (dataset suite)
  - 20m Classified Pixels (GB and NI)
    - New for these releases; RF classification results from 20m Sentinel-2 Seasonal Composite Images.
    - Band 1 = predicted land cover class; Band 2 = class membership probability (0–100) for confidence.
    - Preserves fine detail (not generalized by Land Parcels framework).
  - Land Parcels
    - Attributes describing land parcel composition from the 20m classified pixels via the UKCEH Land Parcel Spatial Framework.
    - Attributes include _hist (pixel distribution), _mode (dominant class), _conf (mean per-pixel membership probability), _purity (parcel-level purity), and more.
    - Note: gid values differ from LCM2015; framework unchanged in geometry but reorganized for speed.
  - 25m Rasterised Land Parcels
    - Rasterized version of Land Parcels (25m pixels) with three bands: _mode, _conf, _purity.
    - Provides a simplified, parcel-averaged representation.
  - 1km Percent Cover (21 bands)
    - 1km grid, area-weighted, reporting percentage cover for each of 21 classes per 1km cell.
  - 1km Percent Aggregate Cover (10 bands)
    - 1km grid; percentage cover per 1km cell for 10 UKCEH Aggregate Classes.
  - 1km Dominant Cover (1 band)
    - 1km grid; dominant UKCEH Land Cover Class per cell.
  - 1km Dominant Aggregate Cover (1 band)
    - 1km grid; dominant UKCEH Aggregate Class per cell.
  - Dataset extents and coordinate systems
    - Great Britain: British National Grid (EPSG:27700)
    - Northern Ireland: Irish Grid (EPSG:29903)
    - GB products use 20m, 25m, and 1km grids; NI products include 20m, 25m, and 1km variants with year-specific adaptations.

- How the data were produced
  - Sentinel-2 Seasonal Composite Images
    - Four-season (winter, spring, summer, autumn) median TOA reflectance per season, using nine Sentinel-2 bands (2,3,4,5,6,7,8,11,12).
    - Some seasonal gaps due to cloud; classifier tolerates partial spectral information.
    - Future work may fill gaps with alternative sources (e.g., Sentinel-1 SAR).
  - Context Rasters
    - 20m context rasters used to reduce spectral confusion (e.g., terrain, proximity to buildings/roads, coast, freshwater, urban, etc.).
    - GB: 10 context rasters (height, aspect, slope, distance to buildings/roads/sea/freshwater, foreshore, tidal waters, woodland mask).
    - NI: 7 context rasters (height, aspect, slope, urban mask, distance to coast, distance to freshwater, distance to road).
  - Classification Scene and Tile Structure
    - Great Britain: 100x100 km tiles; each tile yields a 46-band Classification Scene (36 spectral bands + 10 context bands).
    - Northern Ireland: single 43-band Classification Scene per year (36 spectral + 7 context).
    - 74 overlapping GB Classification Scenes classified; overlaps resolved by visual inspection to pick the best results.
  - Bootstrap Training
    - Fully automatic training using Bootstrap Training: training data derived from historic LCMs (primarily LCM2015) to bootstrap new maps.
    - Sampling ensures balanced class representation for RF training (10,000 samples per bag, with replacement).
    - Aim: leverage a long coast-to-coast record to train robust classifiers without new field data.
  - Random Forest Classification
    - RF classifier trained on Bootstrap Training data; produces the 20m Classified Pixel product.
    - Production software combines Weka with PostGIS and GDAL; open-source tools.
  - Data Validation
    - UK-scale validation against multiple sources: GB Countryside Survey 2019 data, National Forest Inventory data, IACS, and bespoke validation points.
    - Overall accuracies approximately: LCM2017 78.6%, LCM2018 79.6%, LCM2019 79.4%.
    - Validation points derive from diverse sources and were converted to UKCEH classes; results reflect best available indicators, not exact truth.
  - Relationship to UK BAP Broad Habitats
    - 21 UKCEH Land Cover Classes align with BAP Broad Habitats (some nuanced adjustments for remote-sensing detection).
    - Tables and appendices describe mappings and detection considerations (Appendix 1–2).

- UKCEH Land Parcel Spatial Framework
  - Fixed framework originally developed for LCM2007 and refined for LCM2015; reused with minor changes.
  - Parcel geometry remains the same, but storage and indexing changed for faster processing.
  - Minimum parcel size ~0.5 ha; designed to capture discrete land units (fields, parks, urban areas, woodlands, etc.).
  - The framework is an option for summarizing 20m pixels; future iterations may adopt finer boundaries as higher-resolution data become more common.
  - Parcel identifiers (gid) do not match LCM2015; comparisons between 2017–2019 and 2015 require overlap-based methods.

- Data quality, limitations, and notes
  - 20m Classified Pixels retain detailed landscape features; 25m and 1km products generalize details.
  - Some persistent inter-class confusion is noted (e.g., upland vegetation, Bracken vs Acid Grassland, Saltwater vs Freshwater near coasts); context rasters help but complete separation remains challenging.
  - Saltmarsh and coastal classes are strongly influenced by coastal context rasters; occasional commission errors can occur near complex coasts.
  - No manual corrections were performed for LCM2017–2019; classification is automatic but screening and validation were performed.
  - The maps are intended for change detection and trend analysis; annual maps enable detecting land cover change over time.

- User guidance and visualization
  - Appendix 3 and Appendix 4 provide recommended color schemes and color-blind-friendly schemes for displaying the 21 UKCEH Land Cover Classes (with explicit RGB values).
  - A QGIS symbol file is provided alongside the data to apply the recommended palette.

- Appendices at a glance
  - Appendix 1–2: Detailed definitions and relationships between UKCEH Land Cover Classes and UK BAP Broad Habitats; notes on detection considerations.
  - Appendix 3–4: Color recipes for displaying the 21 classes (standard and color-blind friendly).
  - Appendix 5: Confusion matrices for LCM2017, LCM2018 and LCM2019 (site-level details for each class; includes user’s and producer’s accuracies).
  - Appendix 6: Full list of datasets per year and product type (GB and NI), including dataset names, scales, and extents.

- Practical takeaways for GIS specialists
  - Choose the dataset that matches your scale and needs: 20m Classified Pixels for high-detail mapping; 1km or 25m Land Parcels for generalized, parcel-based analyses; 1km Percent/ Dominant products for wide-area summaries.
  - When comparing years, use gid-based matching within the Land Parcel Spatial Framework (note gid changes between 2015 and 2017–2019).
  - For change detection, rely on Bootstrap Training–based RF results and validate with available ancillary data; expect ~80% correspondence at national scale with validation data.
  - If you need repeatable, automated workflows, leverage the RF-based production approach and the accompanying dataset descriptions and attribute schemas.
  - Use the provided color palettes for consistent visualization; refer to the color-blind friendly options if needed.