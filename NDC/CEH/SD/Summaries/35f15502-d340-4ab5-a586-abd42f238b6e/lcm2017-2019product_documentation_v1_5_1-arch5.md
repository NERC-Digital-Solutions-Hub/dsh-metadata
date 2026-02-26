# The UKCEH Land Cover Maps for 2017, 2018 and 2019 v1.5.1 30/06/2020

- Purpose and scope
  - Introduces three new UKCEH Land Cover Maps: LCM2017, LCM2018, and LCM2019.
  - Each map contains 21 UKCEH Land Cover Classes (based on BAP Broad Habitats) aligned with previous maps (LCM2015/2007/2000) for consistency in change detection.
  - Produces land cover automatically using Bootstrap Training and a Random Forest classifier to enable near real-time, UK-wide mapping.
  - Plans to release a new LCM annually; provides a full UK-wide dataset suite across Great Britain and Northern Ireland (GB and NI versions).

- Production approach and data flow
  - Bootstrap Training: uses historic UKCEH LCM observations (primarily from LCM2015, bootstrap-sampled with high purity) as training data, enabling automatic, self-starting training without fresh field data.
  - Random Forest classification: balanced sampling from training data to yield the 20m Classified Pixels product; the classifier outputs probabilities per pixel for 21 classes.
  - Classification Scenes and context: uses Sentinel-2 Seasonal Composite Images (TOA reflectance at 20m) plus 20m Context Rasters (terrain, proximity to buildings/roads, coast, freshwater, etc.) to form Classification Scenes.
  - seasons and data sources: four seasons represented; processing relies on Google Earth Engine for Sentinel-2 data; in production, SR (surface reflectance) data were not fully available, so TOA was used.
  - Tiling and processing: Great Britain classified with overlapping 100x100 km tiles (100x100 km GB Classification Scenes, 74 scenes); Northern Ireland classified with a single 43-band scene per year.
  - Land Parcel Spatial Framework: maintains a GB NI land parcel system (gid, hist, mode, purity, conf, stdev, n) to summarise 20m pixels into parcel-level attributes; the framework supports 0.5 ha MMU and is designed for change-detection, while acknowledging gid values do not match LCM2015 parcels.

- Datasets and structure (three years, 42 datasets in total)
  - 20m Classified Pixels (new): RF classification results per 20m pixel; GB and NI versions; band 1 = most-likely class, band 2 = confidence (0–100).
  - Land Parcels: summary attributes derived from 20m pixels within the UKCEH Land Parcel Framework (gid, hist, mode, purity, conf, stdev, n).
  - 25m Rasterised Land Parcels: rasterized representation (3 bands: modal class, parcel-averaged confidence, parcel purity).
  - 1km Percent Cover: 21-band raster giving per-1km-square percentage cover for each class.
  - 1km Percent Aggregate Cover: 10-band raster giving per-1km-square cover by UKCEH Aggregate Classes.
  - 1km Dominant Cover: single-band raster of the dominant UKCEH Class per 1km grid.
  - 1km Dominant Aggregate Cover: single-band raster of the dominant UKCEH Aggregate Class per 1km grid.
  - Extents and coordinates: GB uses British National Grid (EPSG:27700); NI uses Irish Grid (TM75, EPSG:29903); 8-bit rasters with specified pixel sizes (20m, 25m, 1km).
  - Yearly duplication: the product suite is duplicated for each year (2017, 2018, 2019) resulting in 42 datasets (GB and NI per year).

- Context and ancillary inputs
  - Seasonal Composite Images: four-season TOA reflectance composites derived from Sentinel-2 (bands 2,3,4,5,6,7,8,11,12); gaps due to cloud handled by the RF classifier without manual gap filling; potential future use of alternative sources (e.g., Sentinel-1) for gap-filling.
  - Context Rasters: include height, aspect, slope, proximity masks (buildings, roads, sea, freshwater), foreshore and tidal water masks, and urban/woodland indicators; GB and NI differ in specific context layers used.
  - Land Parcel Spatial Framework: unchanged geometry from LCM2015, but with storage/reindex changes for faster processing; gid values do not match LCM2015, though cross-year comparisons can use gid within the same year’s datasets.

- Validation, quality, and limitations
  - Validation: UK-scale validation against GB countryside survey 2019 data, National Forest Inventory, IACS, and bespoke validation points (22,325 points).
  - Accuracy: LCM2017 78.6%; LCM2018 79.6%; LCM2019 79.4% overall accuracy against UKCEH Land Cover Classes.
  - Interpretive caveats: validation datasets differ in purpose and class mappings; approximately 80% correspondence is considered strong given automated production and evolving methods.
  - Class-level notes: some spectral confusion between upland peatlands, acid/neutral/grassy classes, and coastal vs inland features is acknowledged; Saltwater vs Freshwater often confused near tidal zones; some classes (e.g., Built-up vs Suburban) have varying accuracies; MMU constraints may affect small patches (as with 20m vs 25m products).
  - No manual corrections: the 2017–2019 run intentionally avoided manual spatial corrections to enable rapid annual updates; visual checks and formal validation were still performed.

- Accessibility, documentation, and governance considerations
  - Dataset descriptions and appendix content provide class definitions, relationships, and color mappings (Appendices 1–3, with detailed class notes and relationships to BAP Broad Habitats).
  - Appendix 5 lists the full dataset catalog, including GB/NI versions and year-specific products; notes on dataset naming conventions and availability.
  - GID-based parcel matching: users comparing 2017–2019 parcels to 2015 parcels should rely on gid within each year, noting gid changes across years due to land parcel framework reorganization.
  - Practical governance implications: the annual release cycle supports time-sensitive change detection and policy-relevant land cover analysis, while versioning and explicit notes on gid compatibility guide longitudinal studies.

- Implications for future work and plans
  - Anticipated next-generation LCM2020 (and beyond) to use bootstrap from 2017–2019 majority signal, with potential future integration of additional data sources (e.g., Sentinel-1 radar) and gap-filling strategies.
  - Ongoing refinement of training data, training strategies, and validation resources to improve per-class accuracy and reduce misclassification in challenging upland and coastal contexts.
  - Continued alignment with UKCEH Land Cover Classes and BAP Broad Habitats while acknowledging spectral limitations of remote sensing for some Broad Habitat distinctions.

- Practical takeaways for data stewards
  - Robust, automated production with transparent Bootstrap Training and RF methodology supports scalable, repeatable updates and governance.
  - Clear documentation of data structure, coordinate systems, and level of detail (20m, 25m, 1km products) aids data discovery, discovery, and integration into downstream workflows.
  - Validation results provide a transparent quality baseline, with caveats that enable informed interpretation and risk assessment for uses in policy, planning, and environmental monitoring.