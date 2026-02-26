# The UKCEH Land Cover Map for 2023

- Purpose and scope
  - User guide for the UKCEH Land Cover Map 2023 (LCM2023), describing data production, validation and accuracy to help informed decisions.
  - LCM2023 comprises seven datasets: three for Great Britain and Northern Ireland each (10 m classified pixel dataset, land parcels, and 25 m pixel rasterised land parcels) plus a 1 km summary raster across GB and NI.
  - 21 UKCEH Land Cover Classes derived from Biodiversity Action Plan (BAP) Broad Habitats, linked to historical classifications for consistency and comparability.
  - Formal validation reports an overall accuracy of 83% at full thematic detail.

- Data products and structure
  - 10 m Classified Pixel datasets (GB and NI)
    - Created from multiple Classification Scenes; each pixel carries: 
      - Band 1: most likely UKCEH Land Cover Class (integer)
      - Band 2: associated class membership probability (confidence)
    - Keeps full 10 m detail (not generalised by Land Parcel Framework) to preserve fine features; validation was performed against the 25 m parcel dataset.
  - Land Parcel datasets
    - Result from intersecting 10 m classified pixels with the UKCEH Land Parcel Spatial Framework.
    - Land parcels are ~0.5 ha minimum (Minimum Mapping Unit); designed to represent discrete real-world units (e.g., fields, parks, urban blocks).
  - 25 m Rasterised Land Parcel datasets (GB and NI)
    - Rasterised from the Land Parcel datasets; three attributes per parcel: dominant land cover (mode), confidence (conf), and purity (purity).
  - 1 km summary rasters (GB and NI)
    - Summaries of 25 m rasters to provide dominant class, percentage cover per class (21 classes) and per-aggregate class (10), with minor rounding effects.
  - Seasonal Composite Images
    - Sentinel-2 based, resampled to 10 m; four seasonal medians (Jan–Mar, Apr–Jun, Jul–Sep, Oct–Dec) across 10 bands.
    - Used to create Classification Scenes; handles occasional cloud gaps (partial data acceptable to classifier).
  - Context Rasters
    - 10 m rasters to reduce spectral confusion (e.g., terrain, proximity to buildings/roads, foreshore, water bodies, etc.).
    - GB and NI have tailored sets of context layers.
  - Classification Scenes and tiling
    - GB: 32 Classification Scenes (tiles, ~100 x 100 km) for full GB coverage; NI: a single 49-band Classification Scene.
    - Scenes are trained and classified independently to manage regional phenology and data volume.
  - UK Land Parcel Spatial Framework
    - Framework used to generalise national cartography; parcels designed to be consistent across maps and time for change detection.
    - Some identifiers (gid) do not match LCM2015 for cross-map comparisons; MMU remains ~0.5 ha.

- Production approach and methodologies
  - Bootstrap Training
    - Automatic generation of training observations from historic maps (LCM2020–LCM2022) with >80% probability and consistent class across three years.
    - Enables training data without new field collection; supports temporal consistency.
  - Random Forest classification
    - Balanced training via sampling with replacement; 10,000 samples per class per bag.
    - Open-source tools: Weka, PostGIS, GDAL; bespoke UKCEH software integrates these components.
  - Data sources and timing
    - Classification scenes built from Sentinel-2 Seasonal Composite Images plus Context Rasters to improve spectral separation.
    - Annual map production aims to maximise temporal consistency and enable change detection.
  - Validation and accuracy
    - Validation against 33,107 reference points across all 21 classes; overall accuracy 83%.
    - Validation data compiled from GB countryside survey data, National Forest Inventory, Rural Payments Agency data, and bespoke validation points.

- Known issues and caveats
  - Some polygons missing from vector Land Parcel products; resulting gaps appear in 25 m rasterised parcels but have negligible impact on 1 km summaries.
  - 10 m classified pixels maintain all detail and are not affected by the parcel-geometry gaps.
  - Classification methodology changes year to year; differences can reflect both real change and method evolution.

- Data access, citation and references
  - Each LCM2023 dataset has a DOI; citations provided (Marston et al. 2023; 2024a–g for specific products).
  - Products include: 10 m Classified Pixels (GB; NI), 25 m Rasterised Land Parcels (GB; NI), Land Parcels (GB; NI), 1 km Summary Rasters (GB; NI).
  - Disclaimer: annual updates may produce changes due to both real land-cover change and methodological updates.

- Additional context for analysts
  - The UKCEH Land Cover Classes are anchored to BAP Broad Habitats, with some nuanced mappings noted in Appendices; direct one-to-one mapping is common but not exact in all cases.
  - The multi-scale data (10 m pixels, 25 m parcels, and 1 km summaries) supports both fine-resolution analyses and large-area change detection.
  - The bootstrap-based training approach and annual release schedule enhance the ability to discern genuine land-cover change from methodological artefacts over time.