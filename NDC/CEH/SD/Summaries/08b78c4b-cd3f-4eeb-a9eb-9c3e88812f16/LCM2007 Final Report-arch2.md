# Final Report for LCM2007 - the new UK land cover map

## Overview
- Presents the Final Report for LCM2007, the first UK land cover map with a continuous vector framework derived from national cartography, mapping 23 land cover classes to 17 Broad Habitats.
- Aims to provide a consistent, auditable evidence base for habitat monitoring and landscape policy performance across the UK, with extensive metadata and QA processes.
- Outputs include a 25 m raster product, 1 km rasters, and a vector parcel dataset with detailed provenance and knowledge-based enhancements (KBEs).

## Dissimilar area estimates with Countryside Survey (CS) 2007
- Dissimilar area estimates (outside CS UK 95% confidence limits) occur for:
  - Arable and Horticulture
  - Improved Grassland
  - Neutral Grassland
  - Dwarf Shrub Heath
  - Bog
  - Montane Habitats
  - Coastal habitats
- Key observation: CS 2007 and LCM2007 show substantial differences in several broad habitats, with the largest area discrepancies found in arable/grassland categories and fen-related habitats.

## Main factors driving dissimilarities (4.3.2)
- Classification boundaries and definitions:
  - Differences in what CS and LCM2007 classify as Arable and Horticulture, including temporary or uncropped land being mapped within Arable and Horticulture by LCM2007.
- Spectral and temporal issues:
  - Spectral confusion due to the diverse spectral signatures of arable crops and their growth stages; temporal range of images can shift grassland/arable boundaries.
- Boundary and linear features:
  - CS maps boundary/linear features (e.g., field boundaries) not always mapped in LCM MMU; LCM often incorporates boundary elements into adjacent field polygons, inflating Arable/Grassland areas.
- Grassland classifications:
  - Differences between Improved Grassland and Neutral Grassland largely drive discrepancies; spectral similarity and soil data limitations complicate disambiguation.
- Montane, bog, fen, and coastal areas:
  - Montane and coastal habitats are underrepresented in some CS data; Fen, Marsh and Swamp are particularly challenging due to mosaics and small patch sizes, leading to large inter-product differences.
- Additional notes:
  - LCM2007’s handling of “Rough grassland” includes mixed contributions from various grassland types, affecting correspondence with CS categories.
  - The inclusion of aquatic and boundary features can shift area allocations between habitat classes.

## UK-wide land cover distribution (4.4)
- Overall UK composition (LCM2007):
  - More than 50% of the UK is either intensive agriculture (Arable & Horticulture + Improved Grassland) or built-up areas (Built-up Areas and Gardens).
  - About 12% Broadleaved/Coniferous Woodland; the remainder is semi-natural or natural (30% semi-natural; 1% Coastal; remaining categories vary by country).
- Country-level patterns:
  - England: highest intensive land use (about 76%: Arable 40%, Improved Grassland 27%, Built-up 9%).
  - Scotland: lowest intensive use (about 36%), with the largest proportion of Coniferous Woodland and substantial semi-natural habitats (e.g., Montane and mountain heath).
  - Northern Ireland and Wales show intermediate patterns, with regions of intensive land use and notable water/forest components.
- Comparisons to LCM2000:
  - LCM2007 records higher Arable extents (26%) and lower Semi-natural Grassland proportions (13%) than LCM2000, with modest changes in Woodland and Urban shares. The cause of changes relates to the new spatial framework and classification updates; further analysis is needed to fully attribute these shifts.

## Comparison with Countryside Survey (CS) 2007: key outcomes
- Grassland and arable correspondences show notable inconsistencies due to one-to-many relationships (grass appears in multiple Broad Habitats) and boundary treatment differences.
- CS 1 km square comparisons show a reasonable agreement for some broad habitats, but CS national estimates differ from LCM2007 totals, particularly for Arable/Horticulture and Fen/Marsh/Swamp, prompting discussion of potential re-allocation rules (KBEs) and improved cross-walks.
- Fen, Marsh and Swamp differences are especially large (CS vs LCM2007), largely explained by the mosaic nature of fen habitats and small patch sizes; many CS fen areas map as Rough Grassland or Acid Grassland in LCM2007.
- The report emphasizes that LCM2007 provides a robust, repeatable UK-wide framework, but users should account for CS-LCM differences in trend analyses and area estimates, particularly for grasslands and upland habitats.

## Example areas (5.1)
- A series of example areas demonstrates LCM2007’s performance across uplands, calcareous grasslands, urban areas, and arable/fenland mosaics.
- Illustrates the ability to map complex land cover mixes and to visualize transitions between habitat types in varied landscapes.

## Data products and access (5.2)
- Vector data: parcel-based polygons with attributes including area, source images, Broad Habitat, KBEs, and provenance.
- Raster data: 25 m raster (23 classes) and 1 km raster products (percentage cover and dominant class per cell).
- Licensing and access:
  - 1 km rasters available via CEH Information Gateway.
  - Full vector and 25 m raster products available on request under license from CEH.

## Change detection and methodological context (Chapter 6)
- LCM2007 provides a generalised spatial framework based on real-world land units (OS MasterMap and LPS Large-scale Vector), enabling consistent change detection over time.
- Changing comparisons across CEH maps (LCM1990, LCM2000, LCM2007) are complex due to differences in spatial structure and thematic detail; sophisticated, aggregated-class approaches or reorganization of earlier maps into a common spatial structure are recommended for robust change analysis.
- CS and LCM2007 are complementary: CS offers ground-truth context from field plots; LCM2007 offers coast-to-coast-wide coverage and consistent spatial units for national monitoring.

## Validation, KBEs, and Broad Habitat Association (Appendix 4 and 5)
- Bespoke validation acknowledges that “fit for purpose” is use-dependent; parcel-level metadata and KBEs enable users to assess and adapt classifications locally.
- Broad Habitat Association rules address cross-walk between LCM2007 classes and CS Broad Habitats, reflecting ecological continua (e.g., Bog ↔ Dwarf Shrub Heath, Acid Grassland, Montane Habitats) and non-reciprocal mappings where appropriate.
- KBEs (e.g., terrain, soils, urban proximity, coastal masks) are applied post-classification to improve thematic resolution, with explicit provenance kept for traceability.

## Access, licensing, and reuse
- 1 km raster data: CEH Information Gateway.
- Full vector and 25 m raster data: available on request from CEH under license; contact spatialdata@ceh.ac.uk.
- Licensing may apply; materials carry CEH/NERC copyrights.

## Relevance for environmental monitoring and policy
- LCM2007 provides a consistent, auditable UK-wide data source for habitat extent, landscape change, and policy evaluation.
- Supports biodiversity assessments, ecosystem services analysis, landscape planning, habitat connectivity, and catchment management.
- When used with Countryside Survey and other context data, LCM2007 informs cross-sector policy analysis and national monitoring programs, while acknowledging differences in classifications and spatial frameworks across datasets.