# Final Report for LCM2007 - the new UK land cover map

- Purpose and scope
  - Provides a consistent, UK-wide land cover picture aligned to Broad Habitats to support biodiversity policy, ecosystem services, landscape planning, and catchment management.
  - Maps land cover (not land use) against Biodiversity Action Plan Broad Habitats for temporal monitoring and policy evaluation.

- Key outputs and data products
  - 23 LCM2007 land cover classes mapped to 17 Broad Habitats; MMU of 0.5 ha.
  - 25 m raster: detailed land cover classes.
  - 1 km raster: two formats per class — (a) percentage cover per 1 km pixel, (b) dominant class per 1 km pixel.
  - Spatial framework: continuous UK vector of land parcels derived from OS MasterMap/LPS boundaries with integrated agricultural boundaries and image segments.
  - Rich metadata for processing steps, KBEs, and change history to support traceability and reproducibility.

- Data sources and production methodology
  - Multi-sensor imagery: >70 images compiled into 34 summer–winter composites; majority mapped from composites; small portion from single-date imagery; a small fraction manually filled.
  - Additional spatial data: ground reference points (CEH 2006–2008), Countryside Survey 2007 for external validation, national cartography, soils, DEM, urban boundaries, etc.
  - Spatial framework and segmentation: uses OS MasterMap as base; combines image segmentation with land parcels to create a robust, reusable framework.
  - Pre-processing and segmentation: cloud/mask, atmospheric/topographic corrections; segmentation using winter NIR + summer red + summer MIR bands; parcels merged with OSMM.
  - Classification and KBEs: parcel-based supervised maximum likelihood classification with iterative refinement; KBEs applied to resolve spectral confusion and raise thematic resolution (about 20% of parcels revised).
  - Validation: ground reference points (9127 points) yield overall accuracy around 83%; class-level accuracy varies (e.g., Bog/Arable/Horticulture strong in some areas; Neutral/Calcareous Grassland and Montane habitats more challenging).

- Change mapping and monitoring
  - Change detection is complex due to differing class definitions and spatial structures across LCM1990, LCM2000, and LCM2007; typical pixel-level errors around 20% complicate interpretation of real habitat change.
  - Emphasizes the need for aggregated class analysis or trajectory-based methods to infer genuine change.

- Dissimilar area estimates (CS 2007 vs LCM2007)
  - Dissimilarity observed for Arable and Horticulture, Improved Grassland, Neutral Grassland, Dwarf Shrub Heath, Bog, Montane Habitats, and coastal habitats.
  - Main drivers:
    - Boundary and linear features: LCM often aggregates boundaries into field polygons, increasing apparent field sizes vs Countryside Survey.
    - Spectral confusion and classification differences, especially for Arable and Horticulture due to wide crop spectral variability and multi-year image requirements.
    - Grassland distinctions: differences between Improved, Neutral, Calcareous, and Acid Grassland; Rough Grassland inclusion and classification challenges.
    - Fen, Marsh and Swamp: CS often maps as multiple habitats; LCM tends to map as Rough Grassland or other classes; mosaic nature complicates direct mapping.
  - A notable point: temporary grass and uncropped land can be included in Arable and Horticulture in LCM2007, contributing to higher totals.

- Comparison with Countryside Survey 2007
  - Overall correspondences:
    - Broad Habitat (BH) correspondence around 62%.
    - Broad Habitat Association (BHA) correspondence around 76%.
    Higher correspondence (87–90%) when grasslands are aggregated into a single grassland class.
  - England, Scotland, Wales, Northern Ireland show country-level variations due to habitat definitions, boundaries, and sampling frames.
  - Grassland is a major source of mismatch; aggregating grassland improves correspondence substantially.
  - Fen, Marsh and Swamp shows large discrepancies (CS UK estimate vs LCM2007) due to mix of land cover types and small patch sizes; CS patches often below LCM MMU.

- UK land cover overview and temporal context
  - LCM2007 indicates more than 50% of the UK is in intensive land use (Arable and Horticulture plus Improved Grassland) or Built-up Areas and Gardens; forestry, semi-natural areas, and water bodies comprise the remainder.
  - Country-level patterns: England shows the highest proportion of intensive land use; Scotland has the largest area of Coniferous Woodland and the most extensive montane/semi-natural habitats.
  - LCM2000 vs LCM2007 comparisons reveal shifts in arable and grassland extents, with some differences in woodland and urban percentages; interpretation remains complex due to spatial framework changes.

- Access, licensing, and data availability
  - 1 km raster data: CEH Information Gateway (gateway.ceh.ac.uk).
  - Full vector product and 25 m raster product: available on request under licence from CEH (spatialdata@ceh.ac.uk); licence fees may apply.
  - Emphasis on enabling access to underlying data and data provenance for transparency and reuse.

- Implications for analysts monitoring the environment
  - LCM2007 provides a robust, policy-relevant UK-wide land cover dataset aligned to Broad Habitats, with comprehensive metadata and a reproducible production chain.
  - Supports standardized, repeatable habitat monitoring and policy evaluation, while recognizing limitations in change detection and class-level accuracy.
  - KBEs and a detailed spatial framework enhance spatial and thematic accuracy, though certain habitat distinctions (e.g., multiple grassland types, upland mosaics) remain challenging.
  - The parcel-based metadata and probability-based class variants enable users to assess data quality locally and apply bespoke validation as needed.
  - Encourages integration with in-situ surveys (e.g., Countryside Survey) and other data (e.g., climate, soils, hydrology) to support multi-source environmental monitoring and policy assessment.