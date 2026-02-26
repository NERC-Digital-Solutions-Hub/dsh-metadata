# Final Report for LCM2007 - the new UK land cover map

## Validation and comparison with Countryside Survey (CS)

- Very similar area estimates (within CS 95% confidence limits in every country) for:
  - Coniferous Woodland
  - Freshwater
  - Built-up Areas and Gardens
  - Calcareous Grassland
  - Calcareous Grassland highlighted as surprisingly similar; CS and LCM2007 correspondence methods differ, yet UK-wide totals align in places.

- Similar area estimates (within UK CS 95% limits) for:
  - Broadleaved woodland
  - Acid Grassland
  - Inland Rock

- Dissimilar area estimates (beyond CS 95% limits) for:
  - Arable and Horticulture
  - Improved Grassland
  - Neutral Grassland
  - Dwarf Shrub Heath
  - Bog
  - Montane Habitats
  - Coastal habitats
  - Differences attributed to definitions, spectral confusion, inclusion of boundaries, temporal differences in imagery, and CS’s patch- and survey-approach versus LCM2007’s parcel-based mapping.

- Key reasons for disparities between CS and LCM2007:
  - Classification definitions (e.g., Arable and Horticulture capturing boundaries and temporaries in LCM2007)
  - Spectral confusion and spectral variability within arable grassland
  - Different spatial representations (CS parcels vs LCM MMU and parcel approach)
  - Temporal sampling differences across years required for UK-wide coverage
  - CS patch sizes below LCM MMU affecting comparisons, especially for Fen, Marsh and Swamp

- Fen, Marsh and Swamp (CS vs LCM2007) shows large UK-level discrepancies due to mosaic nature and small patch sizes, with many Fen areas mapped as Rough Grassland or Acid Grassland by LCM2007.

## UK-wide land cover patterns (LCM2007 vs CS)

- UK-level distribution: over half of UK in intensive land use (Arable and Horticulture plus Improved Grassland) or Built-up Areas; woodlands about 12% (roughly split between Broadleaved and Coniferous); remainder in semi-natural, coastal, and montane classes.
- Country-level differences:
  - England: highest intensive land-use share (~76%)
  - Scotland: largest Coniferous Woodland share; substantial semi-natural and Montane habitats
  - NI and Wales: notable intensive land use but different habitat mixes
  - Wales and NI show differences in coastal/montane representations; CS and LCM2007 comparability varies by habitat type
- Relationship to LCM2000: LCM2007 shows higher Arable and Horticulture area (and changes in grassland classifications) compared with LCM2000; interpretation affected by spatial framework changes and the spectral/temporal dynamics of imagery.

## Change mapping and methodological challenges

- Change mapping across LCM1990, LCM2000, and LCM2007 is complex due to differing class schemes and spatial frameworks; robust separation of real change from classification/change-detection error remains difficult.
- LCM2007 provides a reusable, largely static spatial framework based on fixed cartographic boundaries, enabling more reliable future change detection when combined with spectral data and knowledge-based rules.

## Data products and access

- Data products:
  - Vector product: land parcels with 10 processing- and context-related attributes, including KBE history and ProbList
  - 25 m raster: 23 classes
  - 1 km rasters: two types
    - Percentage cover per 1 km pixel for each LCM2007 class
    - Dominant class per 1 km pixel
- Access:
  - 1 km rasters available via the CEH Information Gateway
  - Full vector and 25 m rasters available on request under licence (possible fees)
- Metadata and knowledge-based enhancements (KBEs) are integral to classification history and downstream usability.

## Knowledge-based enhancements (KBE) and validation framework

- KBEs help resolve spectral confusion (e.g., arable versus urban) and improve thematic distinctions among Broad Habitats, often affecting a substantial but controllable portion of parcels.
- Appendix 4 Bespoke validation outlines a fit-for-purpose approach, emphasizing parcel-level metadata, high-resolution imagery checks, and a probabilistic or fuzzy validation framework to gauge accuracy for specific study needs.
- Appendix 5 Broad Habitat Association (BHA) rules define cross-walks between CS and LCM2007 classes to improve interpretability and comparability in the context of grassland, upland mosaics, water, and boundary features.

## Example areas and practical usage

- A set of example areas demonstrates LCM2007’s performance across upland, calcareous grassland, urban, arable, fenland, and mixed landscapes.
- Practical implications for analysts:
  - LCM2007 provides a coastal-to-coastal UK-wide framework suitable for change detection, habitat connectivity analyses, ecosystem assessments, and policy support when combined with KBEs and auxiliary datasets.

## Data formats and architectural advantages

- Vector vs raster trade-offs:
  - Vector (parcels) offers rich attribute metadata (area, origin images, KBE history, ProbList, CorePixels, etc.) but larger file sizes and more complex processing
  - 25 m raster provides uniform land cover detail with simpler handling
  - 1 km rasters are ideal for UK-wide modeling and integration with climate, weather, and species distribution data
- The spatial framework is largely static and derived from generalised national cartography (OS MasterMap and LPS), enabling future re-use and consistent change detection.

## Broader context and European links

- LCM2007 contributes to pan-European land cover assessment (e.g., Corine Land Cover 2006) by providing the vector base for transformation into European classifications.
- LCM2007 leveraged IMAGE2006 data and SPOT/IRS imagery to build a cohesive UK-wide land cover product that aligns with European monitoring initiatives.

## Practical implications for analysts

- Use LCM2007 to establish a UK-wide baseline for Broad Habitat monitoring, landscape planning, biodiversity assessment, and ecosystem service analysis.
- Be mindful of cross-walk challenges with CS, particularly for grassland and fenland types; consider employing KBEs and the Broad Habitat Association framework to interpret results.
- For change detection, lean on the common spatial framework and KBEs to reduce misclassification-driven change signals; validate key areas with bespoke validation approaches as described.

## Limitations and avenues for refinement

- Grassland classifications remain complex due to one-to-many relationships with Broad Habitats; spectral variability and temporal image ranges can induce misclassifications, especially for temporary grass, neutral vs improved grassland, and calcareous vs acid grasslands.
- Fen, Marsh and Swamp remain especially challenging due to mosaics and small patch sizes relative to the MMU.
- Future work may enhance KBE rules, integrate additional data sets (soil, terrain, climate, hydrology) and refine cross-walking to CS for more consistent comparisons and change tracking.

## Overall significance

- LCM2007 marks a major advancement in UK land cover mapping by combining a nationally derived spatial framework with multi-temporal satellite imagery and knowledge-based refinements.
- It provides a high-utility, policy-relevant data resource with explicit limitations, enabling robust, reproducible analyses for biodiversity policy, landscape planning, and climate- and ecosystem-service-related assessments.