# Final Report for LCM2007 - the new UK land cover map

- The LCM2007 project delivers a national, parcel-based land cover map for the UK with associated raster products and a framework designed for consistent future monitoring and change detection.
- Outputs include: 23 LCM2007 land cover classes, 10 Aggregates, continuous UK vector parcels, 25 m raster (23 classes), and 1 km rasters (23 classes plus 10 aggregates) suitable for national-scale analyses.
- Data products are designed to support biodiversity policy, habitat monitoring, landscape planning, catchment management, and integration with other datasets and national maps (e.g., Corine/LUCAS).

## Key findings and data structure

- 23 LCM2007 land cover classes linked to Broad Habitats; over 10 million land parcels across GB and NI combined.
- Image data: 91% of UK classified from Summer–Winter composites; 9% from single-date imagery; post-classification edits and KBEs applied.
- Vector product: parcel-based with extensive metadata per parcel, including processing steps, training data, and knowledge-based enhancements (KBEs).
- Raster products: 25 m resolution (23 classes) and 1 km rasters (percentages or dominant class per kernel), enabling flexible analyses at multiple scales.
- KBEs: seven automated rules applied after initial classification to improve thematic accuracy by incorporating context such as urban boundaries, terrain, soil, and coastal proximity; KBEs modify around 20% of parcels, with the original spectral classification accessible via ProbList for user control.

## Dissimilar area estimates: LCM2007 vs Countryside Survey (CS) 2007

- Dissimilarity appears for: Arable and Horticulture, Improved Grassland, Neutral Grassland, Dwarf Shrub Heath, Bog, Montane Habitats, and coastal habitats.
- Causes for differences:
  - Differences in what constitutes Arable and Horticulture (CS vs DEFRA definitions and LCM2007 scope, including boundary/linear features).
  - Spectral confusion due to diverse crop types and growth stages; spectral variability leads to misclassifications, especially in arable areas.
  - Boundary and linear features often below MMU and are treated differently across CS and LCM2007 (affects field size estimates).
  - Grassland classifications (Improved vs Neutral vs Neutral/Calcareous) have misalignment due to field-level signatures and soil context.
  - Fen, Marsh, and Swamp show large discrepancies due to mosaic nature and small patch sizes; many CS fen areas map as Rough Grassland or Acid Grassland in LCM2007.
- Temporal range of imagery and the need to aggregate across multiple years affect field-change interpretations (temporary grassland vs arable shifts).

## Discussion

- Agreement between LCM2007 and CS varies across Broad Habitats; grassland categories pose particular challenges due to the one-to-many relationship with Broad Habitats.
- Broad Habitat Association (BHA) rules were developed to better align grassland classes with CS observations, adding a third thematic level for accuracy assessment.
- LCM2007 shows high correspondence with CS 1 km squares for Arable and Horticulture in CS2007, but overall Broad Habitat extents tend to be higher in LCM2007 for Arable and Horticulture.
- Fen, Marsh, and Swamp estimates vary drastically between CS2007 and LCM2007; many CS fen areas correspond to Rough Grassland or Acid Grassland in LCM2007, suggesting potential for future KBEs or additional data to refine Fen mapping.

## UK Land Cover (national and country-level patterns)

- UK distribution: more than half of the UK is in intensive land use (Arable + Improved Grassland) or Built-up Areas and Gardens; woodlands cover ~12% (split between Broadleaved and Coniferous).
- England: highest intensive land use (around 76%); Scotland: lower intensive use but higher Coniferous Woodland; NI and Wales show intermediate patterns.
- There are notable country-level differences in Green/sem-natural areas and freshwater distribution; LCM2007 vs LCM2000 shows changes in Arable and Semi-natural Grassland proportions.
- The spatial framework differences between LCM2007 and prior maps contribute to observed disparities in aggregate classes; further analysis is required to fully interpret these differences.

## Applications and policy relevance

- Supports habitat monitoring, biodiversity policy, ecosystem service assessment, landscape planning, habitat connectivity analysis, and catchment management.
- Provides a consistent UK framework for policy evaluation and cross-country comparisons; facilitates long-term monitoring and change detection.
- European links: LCM2007 is used to derive UK components of Corine Land Cover 2006; acts as a bridge to pan-European environmental assessments.

## Data products and access

- Vector product: main product with 10 attributes documenting processing steps, ProbList, and KBE history.
- Raster products: 25 m (23 classes) and 1 km rasters (percentages or dominant class per 1 km cell).
- Access:
  - 1 km raster data via CEH Information Gateway (gateway.ceh.ac.uk).
  - Full vector and 25 m data available on request via CEH (licensing may apply).
- Practical note: KBEs are a refinement layer; users can inspect, adjust, or revert KBEs using ProbList and related metadata.

## Practical notes for GIS work

- Data are continuous vector parcels with rich metadata; 25 m raster and 1 km summaries provide flexible options for mapping and analysis.
- When comparing with field surveys or other datasets, account for resolution and spatial framework differences (MMU, boundaries, and parcel definitions).
- KBEs introduce a context-driven refinement layer; ProbList allows users to review or revert KBEs as needed.
- Change detection across LCM1990, LCM2000, and LCM2007 is complex due to differences in spatial structure and classification approaches; robust change analysis may require re-structuring to a common spatial framework.

## Example areas and visualization

- A set of example areas demonstrates LCM2007 performance across upland, calcareous grassland, urban, and fenland landscapes, illustrating how the vector and raster products depict diverse habitat types and landscape mosaics.

## Summary figures and references (high-level implications)

- LCM2007 provides 23 land cover classes, 17 Broad Habitats, and a large parcel dataset; >91% classified from composite imagery.
- Data products are designed for broad GIS use, with licensing options for full vector and 25 m data and open access to 1 km rasters.
- The report discusses QA results, cross-product comparisons with Countryside Survey, and avenues for future refinement via KBEs and integration with supplementary data sources.

## Access points and contacts

- CEH Information Gateway for 1 km rasters: gateway.ceh.ac.uk
- CEH data portal for full vector and 25 m data (license may apply): www.ceh.ac.uk/data
- For licensing and data requests: spacialdata@ceh.ac.uk