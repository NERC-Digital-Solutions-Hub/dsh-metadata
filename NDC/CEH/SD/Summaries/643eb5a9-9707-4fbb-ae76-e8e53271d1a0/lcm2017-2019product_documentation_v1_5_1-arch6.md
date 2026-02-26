# The UKCEH Land Cover Maps for 2017, 2018 and 2019 v1.5.1

- Purpose and overview
  - Release of three UKCEH Land Cover Maps: LCM2017, LCM2018, and LCM2019.
  - Maps cover 21 UKCEH Land Cover Classes (based on Biodiversity Action Plan Broad Habitats) with a methodology designed for rapid, automated production.
  - Aims to enable UK-wide land cover mapping with annual updates, while ensuring users understand data production, validation, and limitations.
  - No manual corrections were applied in these releases; visual checks and formal validation were performed, giving confidence comparable to LCM2015.

- Data structure and datasets (42 total datasets across years and regions)
  - 20m Classified Pixels: new RF-classified per-pixel results from Sentinel-2 seasonal composites with class label and per-pixel confidence (0–100) in band 2.
  - Land Parcels: parcel-level attributes derived by intersecting 20m classified pixels with the UKCEH Land Parcel Spatial Framework; key fields include gid, hist, mode, purity, conf, stdev, n.
  - 25m Rasterised Land Parcels: three-band rasters (mode, conf, purity) summarising parcel data at 25m resolution.
  - 1km rasters (per year): 
    - 1km Percent Cover (21 bands)
    - 1km Percent Aggregate Cover (10 bands)
    - 1km Dominant Cover (1 band)
    - 1km Dominant Aggregate Cover (1 band)
  - 4-season Seasonal Composite Images: Sentinel-2 TOA reflectance (seasonal medians) at 20m, combined with 20m Context Rasters for classification.
  - Context Rasters (20m): GB and NI context layers to reduce spectral confusion (e.g., terrain, proximity to buildings, roads, coast, water, and urban/foreshore masks).
  - Classification Scenes: GB uses 100x100 km overlapping tiles (74 scenes per year); NI uses a single tile per year; scenes are trained/classified independently with manual precedence to resolve overlaps.
  - UK Land Parcel Spatial Framework: fixed parcel structure (MMU ~0.5 ha); gid identifiers may differ from LCM2015; framework designed for faster processing and stable parcel geometry.

- Production approach and data lineage
  - Bootstrap Training: automatic, self-starting training using historic LCM2015 data; selects high-purity parcels (≥99%) to bootstrap classifier; new maps bootstrap from majority signals over time.
  - Random Forest classification: training via balanced sampling (10,000 samples per class) using pixel data from Classification Scenes; produced the 20m Classified Pixels product.
  - Software stack: bespoke RF pipeline integrating WEKA, PostGIS, and GDAL (all open source).
  - Spatial and temporal linkage: historic maps seed training for new maps; aim to use majority signals for successive updates (LCM2020, LCM2021).

- Validation and quality
  - Validation dataset: GB countryside survey 2019 data, National Forest Inventory data, IACS data, and bespoke validation points (22,325 total).
  - Reported overall accuracy at UK scale (21-class): 
    - LCM2017: 78.6%
    - LCM2018: 79.6%
    - LCM2019: 79.4%
  - Validation points were harmonised to UKCEH classes; results are indicative rather than absolute truth, with some subjectivity in class mappings.

- Class definitions and mapping
  - 21 UKCEH Land Cover Classes mapped from BAP Broad Habitats; Appendix 1 and Appendix 2 provide notes on class definitions and interpretation.
  - Relationship table (Table 1) describes mapping between UKCEH Land Cover Classes and UK BAP Broad Habitats, including notes on special cases (e.g., Saltwater vs Freshwater, Urban vs Suburban).
  - Generalised aggregates: UKCEH Aggregate Classes available for higher-level analyses.

- Data specifics, formats, and extents
  - Coordinate systems: GB products use British National Grid (EPSG:27700); NI products use Irish Grid (TM75, EPSG:29903).
  - Extents: GB and NI with separate classification scenes and datasets per year.
  - Pixel and band structure:
    - 20m Classified Pixels: 2 bands (dominant class, probability 0–100).
    - 25m Rasterised Land Parcels: 3 bands (mode, conf, purity).
    - 1km rasters: 21-band Percent Cover; 10-band Percent Aggregate Cover; 1-band Dominant Cover; 1-band Dominant Aggregate Cover.
  - MMU and parcel framework: Land Parcels have a ~0.5 ha minimum unit; parcels are designed to correspond to real-world units (fields, parks, etc.) and to support temporal change detection.

- Outputs, visualization, and usage guidance
  - Appendix 3 provides recommended RGB color mappings for displaying each UKCEH Land Cover Class.
  - Outputs enable self-serve analysis at multiple scales: detailed 20m pixels for fine features; parcel-level summaries; and 1km grids for broad-scale assessments.
  - Users should be aware of potential spectral confusion between classes; context rasters and seasonal information are used to mitigate misclassifications.

- Notable changes since previous releases
  - Automatic production with no manual corrections (contrast with earlier maps which included manual edits).
  - Introduction of the 20m Classified Pixels dataset to preserve fine landscape features; subsequent products (Land Parcels and 25m rasters) derive from these.
  - Reorganization of the UKCEH Land Parcel Spatial Framework and adjusted gid identifiers; parcel identifiers from LCM2015 do not directly map to LCM2017–2019.
  - Bootstrap Training methodology refined to leverage historical maps and majority signals; ongoing evolution anticipated for future years.

- Appendices and references (for data support and technical validation)
  - Appendix 1: Notes on UKCEH Land Cover Classes (class-level considerations and potential confusions).
  - Appendix 2: Biodiversity Action Plan (BAP) Broad Habitats – detailed definitions.
  - Appendix 3: Recommended RGB color recipes for display.
  - Appendix 4: Full validation details (confusion matrices, user and producer accuracies by class, and notes on interpretation).
  - Appendix 5: Full dataset list by year and product.
  - References: foundational works on RF, bootstrap training, and related mapping methodologies.