# The UKCEH Land Cover Map for 2020

- Purpose and scope
  - User guide for LCM2020, the UKCEH land cover map for 2020.
  - Product consists of six datasets for GB and Northern Ireland plus 1 km summary rasters (total seven items described in Table 2/Appendix 6).
  - Goal: help users make informed decisions by describing data production, validation, and data accuracy; enable users to explore land cover data across time and space.

- UKCEH Land Cover Classes and relationships
  - 21 UKCEH Land Cover Classes derived from Biodiversity Action Plan (BAP) Broad Habitats; not identical to BAP Broad Habitats.
  - Appendices map UKCEH Classes to UK BAP Broad Habitats with notes on where mappings diverge.
  - Provides guidance on colour schemes and crosswalks for displaying classes (Appendix 3, 4).

- Data products and data formats
  - 10 m Classified Pixel datasets (GB and Northern Ireland)
    - Outputs: two-band raster per location; band 1 = most likely UKCEH Land Cover Class; band 2 = probability/confidence for that class.
    - Not generalized with the UKCEH Land Parcel Spatial Framework to preserve fine-scale details; intended for specialist users aware of this caveat.
  - Land Parcel Spatial Framework and Land Parcel Product
    - Parcellation: parcels derived from generalised national cartography; MMU ~0.5 ha.
    - Land Parcel Product attributes (Table 3): per parcel identifiers (gid), hist, mode, purity, conf, stdev, agg, n.
  - 25 m Rasterised Land Parcel datasets
    - 3-band rasters per parcel: dominant land cover mode; mean confidence (conf); parcel purity (purity).
  - 1 km raster products
    - Summaries derived from 25 m rasters: dominant class per 1 km pixel (1-band) and percentage cover per class (21 bands) plus aggregate classes (10 bands).
    - Integer-valued percentages; coastal areas may sum to less than 100 due to mapping extents and MMU.
  - Seasonal Composite Images and Classification Scenes
    - Seasonal Composite Images from Sentinel-2 (winter, spring, summer, autumn) using 9 spectral bands (2,3,4,5,6,7,8,11,12); some seasons may have null data due to cloud.
    - Context Rasters (10 for GB, 7 for NI) used to reduce spectral confusion (terrain, proximity to features, etc.).
    - Classification Scenes: GB uses 100x100 km tiles (36-band Seasonal Composite Images + 10 Context Layers → 46-band Scenes); NI uses a single 43-band Scene per year.
  - The UKCEH Land Parcel Spatial Framework
    - Used to aggregate 10 m pixels into parcels; changes in internal identifiers mean LCM2020 gid may not match LCM2015 parcel ids; spatial overlap comparisons are possible but parcel-id comparisons are not straightforward.
  - Coordinate systems and extents
    - GB: British National Grid (EPSG 27700)
    - NI: TM75 Irish Grid (EPSG 29903)
    - Datasets cover GB and NI with specific extents and pixel resolutions defined per product.

- Data production approach and validation
  - Bootstrap Training
    - Fully automatic training process using historic LCM observations as training data for current imagery; avoids new field data collection.
    - Training set for LCM2020 drawn from LCM2017, 2018, 2019, filtered to parcels with >99% purity across years.
    - Training object counts: GB ~941,027; Northern Ireland ~214,833.
  - Random Forest classification
    - 10,000 samples per class drawn per training set; sampling with replacement to balance class counts.
    - Produces the 10 m Classified Pixel product; robust to class imbalances.
  - Validation and accuracy
    - Validation dataset: 34,715 points derived from GB countryside survey data, National Forest Inventory data, IACS data, and bespoke validation points.
    - Overall accuracy: 79.2% (at full thematic detail; Appendix 5 reports detailed confusion matrices and class-level accuracies).
  - Automation and change detection
    - Annual production enables distinguishing real land cover change from random errors.
    - Historical maps provide training data for Bootstrap Training; changes are expected to persist over time, whereas random errors flicker in time.
  - Data quality notes
    - No manual region-wide corrections are performed; errors are treated as random and allow detection of genuine change over time.
    - The 10 m pixel dataset preserves fine features; validation is against the Land Parcel dataset, not the 10 m pixel set itself.
  - Update philosophy
    - Methods are evolving; if substantial accuracy improvements arise, re-application across the full catalog may occur to maximise temporal consistency and change detection potential.

- Practical considerations for data use
  - Outputs are designed to enable self-service exploration (dashboards, pivot tables, charts) and to facilitate guidance on how to use the products.
  - Outputs may require domain understanding:
    - The 10 m Classified Pixels provide rich detail but come with classification uncertainty; users should consider the second band (confidence) when interpreting results.
    - The Land Parcel Product’s _hist, _mode, _conf, _purity, and _agg fields give per-parcel composition and reliability information for change detection and longitudinal studies.
  - Comparability with earlier LCMs
    - Parcel identifiers (gid) do not align between LCM2015 and LCM2020; spatial overlap may be used for comparisons, but direct gid-based comparisons are not straightforward.
  - Acknowledged limitations and opportunities
    - Some spectral classes (e.g., some grasslands, bogs, upland vegetation) may exhibit confusion; context rasters and additional training data help mitigate this.
    - Saltwater vs Freshwater distinctions can be challenging in coastal/tidal zones; coastal context layers help manage this.

- Appendices and supporting material (highlights)
  - Appendix 1–2: Detailed notes on UKCEH Land Cover Classes and their relationship to BAP Broad Habitats, including nuances and potential misclassifications.
  - Appendix 3–4: Colour recipes for displaying UKCEH Land Cover Classes (including color-blind friendly versions).
  - Appendix 5: Correspondence matrices (confusion matrices) for UKCEH LCM2020, providing class-level accuracy and user/producer accuracies.
  - Appendix 6: Full list of datasets for UKCEH LCM2020 (dataset names and scope for GB and NI).
  - Glossary definitions for Bootstrap Training, Context Raster, Classification Scene, Seasonal Composite Image, and Land Parcel Spatial Framework.

- References and lineage
  - Key methodological references include Breiman (Random Forests) and related LCM methodological reports (LCM2007/2015), plus Jackson (BAP Broad Habitats) and Morton et al. for the Land Parcel Spatial Framework.
  - Describes evolution toward annual automated mapping and potential re-application if accuracy improvements warrant it.

- Summary takeaways for data users
  - LCM2020 provides a rich, annually updated set of land cover products for GB and NI at multiple resolutions (10 m pixels, 25 m parcels, and 1 km summaries) built with Bootstrap Training and Random Forest classification.
  - The data enable detailed change detection and cross-temporal analyses, supported by per-pixel confidence measures and per-parcel composition metrics, but require careful interpretation due to potential classification uncertainty and gid discontinuities with earlier maps.
  - Users should leverage context rasters and seasonal composites to reduce spectral confusion and employ the 1 km and parcel-level outputs for scalable analyses, while respecting the MMU and validation-based accuracy constraints.