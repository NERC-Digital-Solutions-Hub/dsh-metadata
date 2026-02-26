# The UKCEH Land Cover Maps for 2017, 2018 and 2019 v1.6

- Purpose and scope
  - Provides three new UKCEH Land Cover Maps (LCMs): LCM2017, LCM2018, and LCM2019, mapped to 21 UKCEH Land Cover Classes derived from Biodiversity Action Plan (BAP) Broad Habitats.
  - Automated production aims to deliver UK-wide maps annually, with ongoing validation and future plan updates.
  - Emphasises data provenance, production decisions, and guidance for appropriate application.

- Data content and structure
  - 21 UKCEH Land Cover Classes mapped across Great Britain (GB) and Northern Ireland (NI).
  - Product suite includes 42 datasets (GB and NI versions of each dataset) with multiple resolutions and formats:
    - 20m Classified Pixels (new for these products): per-pixel RF classification results with class and confidence (band 1 = class, band 2 = membership probability 0–100).
    - Land Parcels: attributes detailing per-parcel composition, including hist (pixel frequencies per class), mode (dominant class), purity, conf (mean class probability), stdev, and n (npix).
    - 25m Rasterised Land Parcels: 3-band rasters (mode, conf, purity) derived from Land Parcels.
    - 1km Datasets (GB and NI): 1km Percent Cover (21 bands), 1km Percent Aggregate Cover (10 bands), 1km Dominant Cover (1 band), 1km Dominant Aggregate Cover (1 band).
  - Dataset extents and grids
    - GB: British National Grid (EPSG:27700), 20m pixels; 21 classes; 2-band 20m outputs for Classified Pixels; 100x100 km tile strategy for classification scenes.
    - NI: Irish Grid (TM75, EPSG:29903), 20m classification outputs; single 43-band Classification Scene per year (smaller area).
  - Full dataset set totals 42 GB-level items; Appendix 6 lists the complete dataset breakdown.

- Production methodology and workflow
  - Bootstrap Training + Random Forest classifier
    - Bootstrap Training samples historic observations from UKCEH LCM2015, using parcels with purity ≥ 99% to train the RF.
    - Training yields the 20m Classified Pixels product; 10,000 samples per class drawn with replacement to balance learning.
    - Process is fully automatic; no manual corrections were applied for LCM2017–2019.
  - Sentinel-2 seasonal composites and contextual information
    - Seasonal Composite Images (TOA reflectance, 4 seasons) created from Sentinel-2 data in Google Earth Engine, resampled to 20m.
    - Seasonal data combined with 20m Context Rasters (spectral and contextual features) to produce Classification Scenes.
    - GB: 36-band Seasonal Composite Images over overlapping 100x100 km tiles; 74 overlapping Classification Scenes classified independently; overlaps may yield multiple results; visual inspection selects the best results.
    - NI: a single 43-band Classification Scene per year for the entire NI extent.
  - Context rasters
    - GB 20m context layers include height, aspect, slope, distances to buildings/roads/sea/freshwater, foreshore, tidal water, and woodland.
    - NI 20m context layers include height, aspect, slope, urban mask, and distance layers to coast, freshwater, roads.
  - UK Land Parcel Spatial Framework
    - Framework unchanged in geometry; gid identifiers are not the same as LCM2015 due to data storage reordering.
    - MMU ~0.5 hectares; parcels generalize national cartography to represent real-world land units; parcels typically dominated by a single land-cover type.
    - The framework enables time-series comparison; the 20m Classified Pixels can be summarized by user-defined parcel structures beyond the UKCEH framework.
  - Validation and quality assurance
    - UK-scale validation uses GB countryside survey data (2019), National Forest Inventory data, IACS, and bespoke validation points (22,325 locations).
    - Reported accuracy (relative to UKCEH LCM classes):
      - LCM2017: 78.6%
      - LCM2018: 79.6%
      - LCM2019: 79.4%
    - Values are indicative; a single validation dataset is reused across years, so comparability of currency varies; full correspondence tables are in Appendix 5.

- Data inputs and classification decisions
  - Sentinel-2 data
    - 4-season TOA reflectance, 20m resolution, using bands 2,3,4,5,6,7,8,11,12 (Seasonal Composite Images).
    - Ground truth training relies on Bootstrap Training; surface reflectance (SR) was not adopted because TOA performed similarly for current land-cover classes; potential for future inclusion of additional input sources.
  - Manual corrections
    - No manual corrections were performed for the three products presented; visual checks and formal validation were used to assess quality.
  - Classification approach
    - RF classification is supervised and relies on majority signal derived from historic maps; aims to detect real land-cover change over time with annual updates.

- Spatial scale, limitations, and interpretive notes
  - Scale and boundaries
    - 20m Classified Pixels provide detailed, topographic and landscape nuance (e.g., narrow features) but remain below some MMU tolerances; 25m and 1km products summarize across larger extents.
  - Cross-year comparisons
    - gid identifiers differ from LCM2015, so direct parcel-id comparisons across years require careful handling; parcel-based comparisons are possible using gid within LCM2017–LCM2019.
  - Class relationships and terminology
    - 21 UKCEH Land Cover Classes aligned with UK BAP Broad Habitats where possible; strict mappings are nuanced due to differences between field-detection-based BAP Broad Habitats and remote-sensing detectability.
  - Output use and interpretation
    - The dataset includes color recipes and projections; Appendix 3/4 provide display schemes, including color-blind friendly options (Appendix 4); confusion matrices (Appendix 5) illustrate per-class user and producer accuracies.

- Future plans and ongoing development
  - Aims to release a new LCM annually; planning to adjust bootstrap strategies for LCM2020 and LCM2021 to reflect multi-year majority signals (2017–2019; 2018–2020).
  - Ongoing evaluation of additional data sources (e.g., Sentinel-1 SAR) to fill seasonal gaps and improve classification in cloud-prone regions.
  - Continued refinement of training data and production software to enhance accuracy and usability.

- Notable appendices and references
  - Appendix 1–2: Details on UKCEH Land Cover Classes and their relationship to UK BAP Broad Habitats; nuanced definitions and detection considerations.
  - Appendix 3–4: Display colour recipes for UKCEH Land Cover Classes; colour-blind friendly versions.
  - Appendix 5: Confusion matrices for LCM2017, LCM2018, LCM2019 (class-level accuracies and producer/user accuracies).
  - Appendix 6: Full list of datasets for LCM2017, LCM2018, and LCM2019.