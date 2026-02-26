# The UKCEH Land Cover Map for 2023

- Purpose and scope
  - User guide for UKCEH Land Cover Map 2023 (LCM2023), an annual UK land cover product.
  - Consists of seven datasets across Great Britain and Northern Ireland: three per region (10 m classified pixel data, land parcel datasets, and 25 m rasterised land parcels), plus a 1 km summary raster product covering both GB and NI.
  - Aims to support informed use, data production understanding, validation, and accuracy assessment; emphasizes data governance, metadata, and versioning for discoverability and reuse.
  - 21 UKCEH Land Cover Classes, related to Biodiversity Action Plan (BAP) Broad Habitats with careful cross-referencing; BAP terms are italicised when explicitly referenced.

- Data products and structure
  - 10 m Classified Pixel datasets (GB and NI)
    - Derived from Classification Scenes; classifier outputs the most likely UKCEH Land Cover Class as band 1, with a second band providing the associated probability/confidence.
    - Not generalised by the Land Parcel Spatial Framework to preserve fine detail (e.g., narrow features below MMU).
  - 25 m Rasterised Land Parcel datasets (GB and NI)
    - Rasterised version of Land Parcel data; three bands per parcel: dominant land cover (mode), confidence, and purity.
  - Land Parcel datasets (vector)
    - Attributes include gid, hist, mode, purity, conf, stdev, agg, n; MMU ~0.5 ha.
    - Parcels are derived from the UKCEH Land Parcel Spatial Framework; parcel identifiers may not match LCM2015 for direct comparison.
  - 1 km Summary Raster products (GB and NI)
    - Summary of 25 m data to provide dominant class, dominant aggregate class, and percentage cover per 1 km pixel.
  - Appendix differences and mapping
    - Relationships between UKCEH classes, UK BAP Broad Habitats, and aggregate classes are described; some habitats are split or merged to balance spectral detectability with historical mapping.

- Production methods and data standards
  - Bootstrap Training and Random Forest classification
    - Bootstrap Training uses historic LCM observations (LCM2020–LCM2022) filtered for >80% probability and consistent class across three years to train a Random Forest classifier.
    - Sampling with replacement ensures balanced class representations; a bespoke software stack (Weka, PostGIS, GDAL) is used.
  - Seasonal Composite Images
    - Four-season Sentinel-2 composites (Jan–Mar, Apr–Jun, Jul–Sep, Oct–Dec) at 10 m resolution; 10 bands used (including red edge and SWIR bands); occasional cloud gaps are managed by classifier tolerance.
  - Context Rasters
    - 10 m context rasters used to reduce spectral confusion (e.g., terrain, distance to buildings/roads, proximity to water, foreshore, binary masks for woodland and saltmarsh in GB; urban mask and distance layers in NI).
  - Classification Scenes
    - GB classified as 32 tile-based scenes; NI treated as a single 49-band scene (Sentinel-2 bands plus NI context rasters).
    - Some overlaps between tiles occur due to tiling boundaries.
  - UKCEH Land Parcel Spatial Framework
    - 0.5 ha MMU; parcels generalised from national cartography to form discrete units for change detection and noise reduction.
    - A re-ordered storage and new indices optimize processing; parcel identifiers may not align with earlier releases.
  - Method evolution and governance
    - Methods are evolving; annual production anticipates improvements and supports change detection; significant method changes may affect comparability across years.

- Validation and accuracy
  - Validation performed with 33,107 reference points across all 21 classes.
  - Overall accuracy reported at 83% for full thematic detail.
  - Validation data sources include countryside survey, National Forest Inventory, Rural Payments data, and bespoke validation points; accuracy metrics provided at class and producer’s/User’s accuracy levels (see appendix tables in the source).

- Known issues and caveats
  - Minor polygons missing from vector land parcel products; negligible impact on 1 km summary rasters; 10 m classified pixels remain unaffected.
  - Class confusion common between certain UK BAP Broad Habitats and UKCEH Land Cover Classes; detailed notes and glossary in Appendices 1–4 explain typical misclassifications (e.g., Heather vs Heather grassland, Bog, Fen, Marsh, Swamp, Saltmarsh, Saltwater vs Freshwater near coasts).
  - Annual methodological changes may cause observed differences year-to-year beyond real land-cover change.

- Access, provenance, and citation
  - Each LCM2023 dataset has a DOI and a formal citation; Table 5 lists DOIs and corresponding references for:
    - 10 m Classified Pixels (GB and NI)
    - 25 m Rasterised Land Parcels (GB and NI)
    - Land Parcels (vector, GB and NI)
    - 1 km Summary Rasters (GB and NI)
  - Users encouraged to cite Marston et al. (2023/2024) for production methods and to refer to the DOIs for dataset-specific citations.
  - Disclaimer notes that annual updates may introduce changes due to method evolution, affecting comparability beyond genuine land-cover change.

- Practical implications for data stewardship
  - Clear separation of data products by resolution and geometry (pixel, parcel, raster, vector) with explicit MMU and processing notes to guide data integration and lineage tracking.
  - Metadata and DOIs enable robust data governance, version control, and reproducibility.
  - Awareness of class-confusion patterns is essential for quality assurance, especially when integrating LCM2023 with historical maps or policy reporting that relies on BAP Broad Habitat classifications.
  - The yearly update cycle supports change-detection workflows but may require re-mapping or re-aggregation when comparing across years due to methodological updates.