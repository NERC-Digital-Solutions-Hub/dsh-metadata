# The UKCEH Land Cover Maps for 2017, 2018 and 2019 v1.6

- Purpose and scope
  - User guide accompanying the release of three UKCEH Land Cover Maps: LCM2017, LCM2018 and LCM2019.
  - Maps present land cover across Great Britain (GB) and Northern Ireland (NI) using 21 UKCEH Land Cover Classes (based on Biodiversity Action Plan Broad Habitats) with automated production, validation, and plans for annual updates.
  - Emphasises how data were produced, validated, and how to apply them with understanding of limitations and future plans.

- Key outputs and data architecture
  - 21 UKCEH Land Cover Classes (aligned with LCM2015; close to BAP Broad Habitats concepts but not exact BAP definitions for remote sensing).
  - UKCEH Aggregate Classes (10 classes) for generalized summaries.
  - Complete dataset suite includes 42 datasets (GB and NI versions for each year): 
    - 20m Classified Pixels (new for 2017–2019): RF classification results with per-pixel class membership probability and a 0–100 confidence band.
    - Land Parcels: 20m pixel classifications summarised within the UKCEH Land Parcel Spatial Framework; extensive parcel-level attributes (_hist, _mode, _purity, _conf, _stdev, _n).
    - 25m Rasterised Land Parcels: 3-band rasters (mode, conf, purity) summarising parcels at 25m resolution.
    - 1km Dominant Cover and 1km Dominant Aggregate Cover: single-band and multi-band rasters summarising parcel results at 1km resolution.
    - 1km Percent Cover (21 bands) and 1km Percent Aggregate Cover (10 bands): percentage-area products; totals may deviate slightly from 100 due to rounding.
  - Coordinate systems: GB products in British National Grid (EPSG:27700); NI products in Irish National Grid (EPSG:29903).
  - Production scale: GB classification uses 100x100 km Classification Scenes; NI uses a single 43-band scene; 74 GB Classification Scenes in total for GB coverage.

- Production methodology
  - Bootstrap Training: automatic training data derived from historic UKCEH maps (not requiring field campaigns). Uses majority signal across historic maps to bootstrap training data for the RF classifier.
  - Random Forest classification: supervised learning trained on Bootstrap Training data; balanced sampling to ensure rare classes are learned adequately.
  - Sentinel-2 seasonal data: classification scenes are built from Sentinel-2 Seasonal Composite Images (TOA reflectance) by season (winter, spring, summer, autumn) with 20 m resolution, derived via Google Earth Engine (GEE).
  - Context Rasters: 20 m context layers (terrain, proximity to buildings/roads/coast, foreshore, tides, wood presence) combined with Seasonal Composite Images to form Classification Scenes and reduce spectral confusion.
  - Seasonal Composite Images: created from GEE with 9 Sentinel-2 bands (2, 3, 4, 5, 6, 7, 8, 11, 12); some seasons may have cloud gaps; classifier tolerant of missing data.
  - Classification Scenes: GB uses 100x100 km tiles; NI uses a single tile; each scene is trained/classified independently; overlaps are resolved by visual inspection to choose best results.
  - UKCEH Land Parcel Spatial Framework: fixed spatial framework (roughly 0.5 ha MMU) used to generalise 20 m pixels into parcels; framework re-ordered for performance but parcel IDs (gid) do not match LCM2015; changes enable faster processing and change-detection support.
  - Data lineage: 20m Classified Pixels feed all subsequent products; 25m, 1km products derived by summarising 20 m outputs within the Land Parcel Framework.

- Validation and accuracy
  - UK-wide validation against GB countryside survey 2019 data, National Forest Inventory data, IACS, and bespoke LCM validation points (22,325 points) intersected with Land Parcel datasets.
  - Reported overall accuracy (across the three years): 
    - LCM2017: 78.6%
    - LCM2018: 79.6%
    - LCM2019: 79.4%
  - Validation notes: the same validation points were used across products; accuracy is a robust indicator but not absolute truth. Some misclassifications reflect spectral and definition ambiguities; approximately 80% correspondence is considered strong for an automatic map series.
  - Appendix 5 provides detailed confusion matrices and producer/user accuracies by class for 2017–2019.

- Data interpretation and usage guidance
  - The 20m Classified Pixels dataset preserves landscape detail (e.g., narrow features) that are lost in parcel-aggregated products; useful for high-resolution analyses and change detection.
  - The Land Parcels dataset aggregates 20 m results into fixed parcels (MMU ~0.5 ha) to reduce noise and support time-series comparisons; parcel IDs differ from LCM2015, except gid can be used to relate corresponding parcels across 2017–2019.
  - 25m Rasterised Land Parcels and 1km products provide generalized, scalable outputs suitable for broader-scale analyses.
  - Thematic class interpretations are based on UKCEH Land Cover Classes and their relationship to BAP Broad Habitats; some habitat distinctions cannot be perfectly resolved from satellite data alone.
  - Spectral confusion persists among certain classes; context rasters and the multiband approach mitigate but do not eliminate ambiguity (e.g., saltwater vs freshwater near coasts; various grassland types).
  - Outputs include colour recipes (Appendix 3–4) and QGIS symbol files to support visualization; confusion matrices (Appendix 5) aid accuracy interpretation.

- Future plans and evolution
  - UKCEH intends to release a new LCM annually (as stated for 2020 onward); exploration of additional input data, potential gap-filling strategies, and incorporating broader data sources (e.g., Sentinel-1 SAR) to improve coverage in cloudy seasons.
  - Methodological evolution includes potential refinements to Bootstrap Training and possibly a refined Land Parcel Spatial Framework to accommodate higher-resolution data in the future.

- Appendices and supplementary notes (highlights)
  - Appendix 1–2: Definitions and mapping relationships between UKCEH Land Cover Classes, UK BAP Broad Habitats, and detailed notes on class derivations and detection considerations.
  - Appendix 3–4: Recommended colour schemes for displaying classes (including color-blind friendly options) and accompanying QGIS symbology files.
  - Appendix 5: Full confusion matrices for LCM2017, LCM2018, and LCM2019 (class-by-class, with user/producer accuracies).
  - Appendix 6: Full list of datasets per year and product naming conventions.

- Practical takeaways for analysts monitoring the environment
  - Use LCM20m Classified Pixels for high-resolution, change-detection analyses across 2017–2019; use Land Parcels for stable, parcel-based time-series comparisons; leverage 1km products for broad-scale summaries; combine with context rasters for improved classification in spectrally similar areas.
  - When comparing years, rely on gid-based parcel tracking (not raw parcel IDs from LCM2015) and prefer Bootstrap Training-based consistency across years.
  - Be mindful of around-100% rounding in percentage-cover outputs and coast-edge limitations; coastal and rare habitats may have higher uncertainty.
  - Consult Appendices for habitat definitions, visualisation guidelines, and validation context to better interpret thematic maps.