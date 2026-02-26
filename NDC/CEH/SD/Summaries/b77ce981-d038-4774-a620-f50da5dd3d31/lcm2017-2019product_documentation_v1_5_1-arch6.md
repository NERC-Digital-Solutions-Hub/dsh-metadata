# The UKCEH Land Cover Maps for 2017, 2018 and 2019 v1.5.1

- Purpose and scope
  - Release of three UKCEH Land Cover Maps: LCM2017, LCM2018, and LCM2019.
  - Maps use 21 UKCEH Land Cover Classes based on BAP Broad Habitats; produced automatically using Bootstrap Training with a Random Forest classifier.
  - Aim to provide rapid, nationwide land cover products with supporting data structures that enable users to explore and analyse land cover change.

- Data products and structure
  - 20m Classified Pixels: new 20m pixel-level RF classification with two bands per pixel (dominant class and confidence 0–100); preserves fine details for complex landscapes.
  - Land Parcels: vector-based framework (gid) with parcel-level attributes derived from 20m pixels; revised attributes compared to LCM2015; includes hist, mode, purity, conf, stdev, n.
  - 25m Rasterised Land Parcels: three-band raster (mode, conf, purity) summarising parcel information.
  - 1km rasters: four products summarising parcel data at 1km scale
    - 1km Percent Cover (21-band)
    - 1km Percent Aggregate Cover (10-band)
    - 1km Dominant Cover (1-band)
    - 1km Dominant Aggregate Cover (1-band)
  - Geographic coverage and coordinates
    - Great Britain (GB) and Northern Ireland (NI)
    - GB: British National Grid (EPSG: 27700); NI: Irish Grid (EPSG: 29903)
  - Total dataset composition
    - For each year (2017–2019) and each territory, products exist to yield 42 datasets overall.

- Data sources, inputs, and methods
  - Seasonal imagery
    - Sentinel-2 Seasonal Composite Images (TOA reflectance; four seasons) used as the spectral basis.
    - Seasonal data derived from nine Sentinel-2 bands (Table 6) with some seasons having gaps due to cloud; classifier tolerates partial data.
    - Google Earth Engine provides data; SR (surface reflectance) was considered but TOA used after testing.
  - Contextual information
    - 20m Context Rasters to reduce spectral confusion (e.g., height, aspect, slope, distances to buildings/roads/sea/freshwater, foreshore, tidal water, woodland).
  - Classification Scenes and tiling
    - GB: 100x100 km classification tiles; 74 overlapping GB scenes classified independently and then combined.
    - NI: single 43-band scene per year (36 spectral + 7 context layers).
  - UKCEH Land Parcel Spatial Framework
    - Modified framework with unchanged parcel geometries from LCM2015, but with re-ordered storage and new indices; gid values do not match LCM2015 for cross-year parcel comparisons (use gid for year-to-year matching, not for cross-year parcel comparison).
    - MMU of ~0.5 ha; parcels represent discrete real-world units (fields, parks, urban areas, etc.).
  - Bootstrap Training
    - Fully automatic training using LCM2015 as the bootstrap source; selects high-purity parcels (≥99%) to generate spectral training observations.
    - RF classifier trained with balanced sampling (10,000 samples per class, with replacement) to ensure rare classes are well represented.
    - Bootstrap Training is a self-starting process intended to update maps with short refresh intervals; future plans include 3-year majority bootstraps for 2021 and beyond.
  - Classification
    - Random Forest classification using the Bootstrap Training data to produce the 20m Classified Pixels product.
    - No manual corrections were applied in this release due to the automated workflow; visual checks and formal validation performed.

- Validation and quality
  - Validation approach
    - UK-scale validation against multiple data sources: GB countryside survey (2019), open National Forest Inventory, IACS, and bespoke validation points (22,325 points).
  - Reported accuracy
    - LCM2017: 78.6% overall accuracy
    - LCM2018: 79.6% overall accuracy
    - LCM2019: 79.4% overall accuracy
  - Validation notes
    - Validation points span sources with differing class definitions; some conversion/interpretation required to match UKCEH classes.
    - Validation points are not absolute truth; still, ~80% correspondence is considered robust for an automatically derived 21-class product.
  - Appendix 4 (noting data specifics)
    - Confusion matrices and producer’s/user’s accuracy metrics by class are provided in Appendices, illustrating per-class performance and overall reliability.

- Data continuity, compatibility, and caveats
  - Class definitions and nomenclature
    - 21 UKCEH Land Cover Classes based on BAP Broad Habitats; not identical to current live BAP habitat descriptions but aligned for comparability with past maps.
  - Parcel identifiers
    - gid values for LCM2017–2019 parcels do not correspond to LCM2015; for cross-map year comparisons, use spatial overlap rather than identical gid values.
  - Data limitations and interpretation
    - Some upland and peatland classes (e.g., Bog, Heather variants) show inter-class confusion due to spectral similarities and limitations of satellite detection for certain habitats.
    - Saltwater vs Freshwater distinctions rely on coastal context; some tidal rivers may exhibit confusion.
    - Seasonal gaps possible in future releases; ongoing exploration of additional data sources (e.g., Sentinel-1 SAR) to fill gaps.

- Appendix highlights and usage guidance
  - RGB color mapping recommendations for display (Appendix 3) to aid visualization and interpretation.
  - Classification rationale and notes on technical aspects of each class and its detection considerations (Appendices 1 and 2).
  - Appendix 5 provides a complete listing of the datasets for LCM2017, LCM2018, and LCM2019 (dataset names, extents, and storage details).

- Practical implications for data users and data support
  - Self-serve data products across GB and NI enable broad data use for policy, planning, and environmental assessment.
  - Multiple data resolutions (20m, 25m, 1km) support both fine-grained analysis and regional trend assessments.
  - Bootstrap Training ensures an automatic, scalable workflow suitable for yearly updates, with a clear pathway for future enhancements and expansion of input data types.
  - Validation provides a transparent indication of map reliability, with continual plans to improve training data and accuracy through updated bootstrap datasets.