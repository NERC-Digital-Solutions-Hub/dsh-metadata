# Final Report for LCM2007 - the new UK land cover map

## Executive snapshot for Data Leaders
- LCM2007 delivers UK-wide, parcel-based land cover mapping with 23 Broad Habitat classes, plus 1 km and 25 m raster products, designed to support policy, biodiversity monitoring, and landscape planning.
- A unified spatial framework is built from detailed national cartography (OS MasterMap and LPS) to enable cross-border reuse, change detection, and long-term monitoring.
- The dataset combines automated spectral classification with Knowledge-Based Enhancements (KBEs) that use context such as urban boundaries, soils, terrain, and coastal features to improve thematic resolution; KBEs are fully documented and reversible.
- Ground-truth validation shows overall Producer/User accuracy around 83% (class-dependent); similarities and differences with Countryside Survey (CS) vary by Broad Habitat, with grassland and fen areas presenting interpretation challenges.
- Access is via the CEH Information Gateway for 1 km rasters; full vector and 25 m products are licensed on request (licensing may apply).

## What LCM2007 is and what it contains
- A continuous parcel-based map for the UK with 23 LCM2007 classes mapped to 17 Broad Habitats; minimum mappable unit ~0.5 ha.
- Products:
  - Vector: land parcels with 10 processing attributes, ProbList (top five class probabilities), KBE history, and Construct metadata.
  - 25 m raster: 23 land cover classes.
  - 1 km raster: UK-wide 1 km cells with either percentage cover per class or a dominant class.
- Data governance and provenance are embedded, with detailed metadata at the polygon level and options to disable KBEs for reproducibility.

## Data sources, structure, and processing approaches
- Spectral classification: parcel-based supervised maximum likelihood using multi-temporal imagery.
- Knowledge-Based Enhancements (KBEs): seven automated post-classification rules using urban boundaries, soils, topography, and coastal context to reduce spectral confusion (about 20% of parcels affected).
- Spatial framework: derived from OS MasterMap, LPS for GB and NI boundaries; generalised boundaries configured for stable cross-time use.
- Validation: ~9,127 ground-reference points (2006–2008); overall accuracy ~83% (class-dependent).
- Complexities addressed: grassland and fen classifications often show discrepancies with CS due to different definitions, patch sizes, and data structures.

## Knowledge-based enhancements and data governance
- KBEs rely on external datasets (urban, soils, coastal outlines, terrain) sourced from government and research bodies.
- Documentation and provenance of KBEs are explicit; users can disable KBEs to reproduce results.
- The KBEs improve thematic resolution and enable re-interpretation if needed, while preserving the original spectral classification (ProbList) for reversibility.

## Change assessment and comparability with Countryside Survey
- The comparison between LCM2007 and CS shows variable agreement across Broad Habitats.
- Grassland types are particularly challenging due to multiple Broad Habitat mappings for the same spectral signals; Broad Habitat Association (BHA) rules were developed to improve cross-product comparability.
- LCM2007 aligns well with CS 1 km squares for Arable and Horticulture but tends to estimate a larger Arable and Horticulture area at the Broad Habitat level.
- Fen, Marsh and Swamp estimates differ by an order of magnitude due to the mosaic nature and small patch sizes; KBEs could help reallocate some areas to Fen, Marsh and Swamp in future work.
- Difference in spatial structure and MMU (minimum mapping unit) between LCM2007 and CS complicates direct change detection; future work may re-organise earlier CEH maps into a common spatial framework to support robust trend analysis.

## UK-wide and country-level findings
- UK distribution: over 50% of the country in intensive land use (Arable/Horticulture plus Improved Grassland) with 12% in woodlands; semi-natural and coastal/montane habitats fill the remainder.
- England shows the highest share of intensive land use; Scotland has the largest proportion of Coniferous Woodland and a substantial semi-natural/ Montane component; country differences reflect landscape and CS sampling characteristics.
- Comparison with LCM2000 indicates some shifts in percentages for Arable and semi-natural grasslands, with ongoing interpretation required to attribute changes to mapping framework versus real land-cover change.

## Applications, impact, and how Data Leaders can use LCM2007
- Provides a robust, policy-relevant evidence base for habitat monitoring, biodiversity assessment, ecosystem services, and landscape planning.
- Serves as a consistent UK frame of reference for cross-border analysis and country-level policy evaluation (e.g., Natura targets, woodland expansion planning).
- Supports habitat connectivity and network analyses when used with higher-resolution data and other data layers ( soils, urban context, hydrology, etc.).
- Demonstrates a scalable data governance model: centralized UK-wide spatial framework, documented processing history, and explicit provenance for external data dependencies.

## End-to-end data strategy and governance considerations for Data Leaders
- Centralized, reusable spatial framework: A single, consistent structure across GB and NI enables long-term monitoring and easier cross-border data integration.
- Data quality and standards: Class-dependent accuracy; spectral-based classifications complemented by KBEs; need for caution in change detection and for future harmonisation of grassland and fen classifications.
- Provenance, reproducibility, and governance: Transparent KBE history; ability to disable KBEs; comprehensive polygon-level metadata supports reproducibility and auditable analyses.
- Accessibility and licensing: Public 1 km rasters via CEH gateway; full vector/25 m products require licensing; license terms and costs should be planned in data strategies.
- Data integration and networks: Demonstrates successful integration of national cartography, agricultural boundaries, soils, urban boundaries, and DEMs to improve spatial and thematic accuracy; supports cross-sector collaboration and co-ownership of data assets.
- Change detection future-proofing: Recognize that comparing LCM2007 with earlier CEH maps is technically challenging; a common spatial framework and aggregated class approaches may enhance trend analyses.

## Takeaways for data-driven policy and practice
- LCM2007 marks a major advance in UK land-cover mapping with transparent processing, robust spatial structure, and rich metadata that support a wide range of policy applications.
- While KBEs improve classification, cross-study comparability remains nuanced; continued refinement via BH Association rules and potential reallocation of complex mosaics (e.g., Fen, Marsh and Swamp) could enhance consistency.
- For data leaders, the LCM2007 approach offers a practical blueprint for building enduring, governance-enabled, cross-border land-cover data assets that support both current policy needs and future monitoring challenges.