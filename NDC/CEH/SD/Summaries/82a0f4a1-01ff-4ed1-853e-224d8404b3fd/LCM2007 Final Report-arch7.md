# Final Report for LCM2007 - the new UK land cover map

- Overview of LCM2007
  - First continuous parcel-based UK land cover map with a suite of raster products (25 m and 1 km) and a detailed vector framework.
  - Uses a generalised national cartography spatial framework (OS MasterMap, NI LPS) combined with multi-date satellite imagery and knowledge-based enhancements (KBEs).
  - 23 LCM2007 land cover classes aligned with Broad Habitats; supports nationwide analyses, change detection, and policy-oriented tasks.

- Data architecture and products
  - Vector product: land parcels (polygons) with extensive attributes and a history of processing steps, including Broad Habitat (BH) and Broad Habitat sub-classes (BHSub), FieldCode, KBE history, ProbList, Construct, and core pixel information.
  - 25 m raster: 23 LCM2007 classes, georeferenced with corresponding metadata.
  - 1 km raster: two summary formats per location:
    - A. Percentage cover per class.
    - B. Dominant class per 1 km cell.
  - Aggregated products: UK-wide summaries for 1 km with broader class groupings.

- Data sources and spatial framework
  - Imagery: Landsat-5 TM, Landsat-7 ETM+, LISS-3, SPOT-4/5, AWIFS; composites combine multiple dates to improve class separation.
  - Ground truth and reference data: Countryside Survey 2007 (CS2007) field data; additional soil, elevation, climate, and agricultural boundaries as ancillary data.
  - Spatial frameworks:
    - Great Britain: OS MasterMap Topography generalized to 0.5 ha MMU; integration with agricultural boundaries and segmentation.
    - Northern Ireland: LPS Large-scale Vector polygons generalized and integrated with image segments.
  - Pre-processing and segmentation: cloud masking, atmospheric/topographic correction, geo-registration (RMSE < 0.3 px), segment-based approach using multi-band inputs; parcel and cartography-derived boundaries integrated.

- Classification and knowledge-based enhancements
  - Parcel-based supervised maximum likelihood classification applied to 37 composites and 21 single-date images into Broad Habitat classes.
  - Knowledge-based enhancements (KBEs): seven rule-based algorithms to resolve spectral confusions and improve thematic resolution (e.g., Grassland types, Montane/Bog distinctions, urban/coastal context).
  - KBEs applied sequentially; documentable in vector attributes; approximately 20% of parcels affected; traceable via ProbList and KBE history for reversion if needed.
  - Change mapping is complex due to differing historical maps and spatial structures; reliability limited by spectral error and epoch interpretation.

- Validation, accuracy, and interpretation
  - Validation using 9,127 ground-reference points; overall accuracy around 83% for LCM2007 classes.
  - Class-level accuracy varies; grassland and upland semi-natural types show greater uncertainty.
  - CS2007 comparison reveals varying agreement across Broad Habitats; grassland categories are particularly challenging due to one-to-many relationships between observed land cover and BHs.
  - Grassland aggregation (combining all grasslands) improves correspondence with CS2007 (e.g., up to ~87–90% in some cases).
  - Fen, Marsh and Swamp show large discrepancies due to complexity and small patch sizes; many Fen areas mapped as Rough Grassland or Acid Grassland in LCM2007.
  - Differences between CS and LCM2007 are partly due to MMU, boundary generalisation, data structures (parcel vs field polygons), and the use of multi-year imagery.

- 4.3.2 Dissimilar area estimates (summary)
  - Dissimilar outputs observed for Arable and Horticulture, Improved Grassland, Neutral Grassland, Dwarf Shrub Heath, Bog, Montane Habitats, and coastal habitats.
  - Causes include: differences in what is classified as Arable/Horticulture, spectral confusion, inclusion of boundaries/linear features in LCM2007, and how temporary grassland and uncropped land are treated.
  - Differences in arterial figures may reflect temporal range of imagery and how multi-year composites influence land-cover transitions.

- 4.4 UK Land Cover: high-level patterns
  - UK distribution: Arable and Horticulture plus Improved Grassland account for about 51%; built-up areas ~6%; woodlands ~12% (Broadleaved and Coniferous); semi-natural areas ~30% (including Mountain, Heath, Bog, semi-natural grassland).
  - Country-level variations: England shows highest intensive land use; Scotland has more Coniferous Woodland and semi-natural uplands; Northern Ireland and Wales show distinct patterns in grassland and boundary features.
  - Comparison with LCM2000 indicates shifts in arable and semi-natural grassland proportions, with some uncertainty linked to spatial framework changes.

- Practical implications for GIS workflows
  - LCM2007 offers a robust UK-wide, map-based data foundation suitable for habitat mapping, biodiversity assessments, ecosystem service analyses, and policy support.
  - Combination of a cartography-derived high-resolution spatial framework with satellite-derived classifications and KBEs enables consistent change detection and cross-year analyses.
  - Access options:
    - 1 km raster data via the CEH Information Gateway (fast overviews).
    - Full vector and 25 m raster data on request under licence (licensing may apply).
  - Documentation and metadata accompany products to support reproducibility and traceability.

- End-use and applications
  - Supports multi-tier habitat monitoring, biodiversity surveillance, landscape planning, ecosystem services assessment, and catchment management.
  - Suitable for integration with other data sources to inform environmental policy and planning decisions.

- Key takeaways for GIS stakeholders
  - LCM2007 advances UK land cover mapping by fusing a real-world cartographic spatial framework with multi-date imagery and KBEs.
  - Product suite (vector, 25 m, and 1 km summaries) supports flexible, multi-scale GIS workflows and cross-dataset comparisons.
  - Overall accuracy is solid, but several habitat classes (notably upland semi-natural grasslands, fen-related types, and some coastal/montane classes) show higher classification uncertainty; KBEs and cross-dataset validation are valuable for interpretation.
  - Grassland aggregation improves cross-dataset correspondence with field surveys, a practical consideration when aligning LCM2007 with Countryside Survey or similar datasets.
  - The UK-wide 1 km products are useful for quick overviews and modelling, while vector and 25 m raster data support detailed, site-specific GIS analyses.