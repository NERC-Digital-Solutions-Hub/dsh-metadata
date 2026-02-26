# Final Report for LCM2007 - the new UK land cover map

- A UK-wide, parcel-based land cover map (LCM2007) built from generalised national cartography and multi-temporal imagery, designed for robust change detection and cross-border consistency.
- Outputs include a 23-class 25 m raster, a vector parcel product with full provenance, and 1 km raster products (percentage and dominant class), plus extensive metadata and QA.

## Key aims and scope for GIS work
- Provide map-based evidence to support biodiversity, policy, planning, and landscape analysis.
- Enable repeatable, auditable workflows with rich metadata and a transparent processing chain.
- Support cross-year change detection and UK-wide consistency through a stable spatial framework.

## Spatial framework and data sources
- Spatial framework: land parcels derived from generalised national cartography (OS MasterMap/Gazetted boundaries), optimized for change detection and cross-year comparisons.
- Resolution and units:
  - 25 m raster: 23 LCM2007 classes.
  - 1 km raster: dominant class and percent cover per 1 km cell (aggregates included).
  - Vector: polygons with 10+ processing-stage attributes for full provenance.
- MMU and boundary logic:
  - Minimum mapping unit (MMU) ~0.5 ha; MFW ~20 m.
  - Boundary details linked to field/parcel-level metadata; boundary features can influence class extents (e.g., Arable/Horticulture areas include boundary/linear features in LCM2007).
- Data sources include Landsat, SPOT, IRS imagery, and ancillary layers (topography, soils, urban extent, etc.).

## Processing workflow and Knowledge-Based Enhancements (KBE)
- Image processing: cloud masking, atmospheric and topographic correction, multi-date composites, segmentation aligned with real-world objects.
- Classification: parcel-based supervised maximum likelihood across 37 composites and multiple single-date images, mapped to 23 LCM2007 classes.
- KBEs: regionally adaptive, context-based rules using terrain, soils, urban proximity, and coastal context to resolve spectral confusion and improve thematic resolution. Applied to ~20% of parcels.
- Post-classification edits: targeted manual edits for rare classes or topographic quirks; hole-filling used selectively.
- Outcome: improved discrimination among spectrally similar classes, with explicit attention to grassland sub-types and habitat associations.

## Products, metadata, and QA
- Vector product: parcel-based polygons with 10 processing-stage attributes (including KBE history and provenance).
- 25 m raster: 23 LCM2007 classes.
- 1 km raster: two summaries per pixel (percentage cover and dominant class) for all 23 classes plus 10 aggregates.
- Metadata and QA: detailed provenance per parcel; validation data collected; overall accuracy ~83% with class-dependent variations; user’s and producer’s accuracies reported to guide interpretation.

## Dissimilar area estimates (4.3)
- Dissimilar areas identified between LCM2007 and Countryside Survey (CS) 2007 for:
  - Arable and Horticulture
  - Improved Grassland
  - Neutral Grassland
  - Dwarf Shrub Heath
  - Bog
  - Montane Habitats
  - Coastal habitats
- Main drivers of discrepancy:
  - Differences in what is classified as each habitat (scope and definitions).
  - Spectral confusion due to crops, growth stages, and multi-year imagery required for full UK coverage.
  - Boundary/linear features handling causing field boundaries to be integrated differently in LCM2007 vs CS.
  - Grassland classifications (Neutral vs Improved) and soils context; spectral signatures vs field observations.
  - Fen, Marsh and Swamp areas are especially variable and often mapped differently due to small patch sizes and mosaic composition.
- Consequences: challenges in separating real change from mapping and methodological differences; suggests cautious interpretation for change detection.

## UK-wide and country-level patterns (4.4)
- UK distribution: over 50% of land in intensive use (Arable + Improved Grassland) or Built-up Areas; woodland ~12%; other semi-natural and natural habitats compose the remainder.
- England shows the highest intensive land use; Scotland has the largest share of Coniferous Woodland and the most semi-natural grassland and montane habitats.
- Comparisons with LCM2000 show shifts in arable and semi-natural grassland proportions; linkage to spatial framework changes remains to be fully assessed.

## Countryside Survey (CS) comparisons and implications
- Overall agreement with CS varies by Broad Habitat; grassland categories are particularly challenging due to one-to-many relationships with Broad Habitats.
- Grassland issue mitigated with Broad Habitat Association (BHA) rules to improve cross-dataset correspondences at BH, BHSub, and Aggregate levels.
- LCM2007 aligns well with CS 2007 for Arable and Horticulture at the 1 km square level but shows higher CS-derived area for Arable/Horticulture than in CS estimates.
- Fen, Marsh and Swamp estimates differ by orders of magnitude due to mosaic composition and patch size; many CS Fen areas map as Rough Grassland or other grassland types in LCM2007.
- Use guidance: consider grassland aggregation or BHA cross-walking to improve cross-dataset compatibility; CS and LCM2007 are broadly aligned in major habitat groups but differ in detail and scale.

## Change mapping and interpretation guidance
- Change detection is complex due to differing baselines (LCM1990, LCM2000, LCM2007) and their distinct spatial/thematic structures.
- Best practice involves:
  - Aggregating to stable classes or use of BHAssociation rules to reduce misinterpretation.
  - Focusing on trajectories rather than single-class changes where possible.
  - Reorganising earlier CEH maps into a common spatial structure to support robust change detection.

## Practical guidance for GIS practitioners
- Data access:
  - 1 km raster datasets: CEH Information Gateway.
  - Full vector and 25 m raster products: licensing on request from CEH.
- Use of metadata: exploit parcel-level KBE history and ProbList to assess per-parcel confidence; validate with high-resolution imagery where needed.
- Boundary considerations: anticipate boundary/linear feature integration within polygons and plan analyses accordingly.
- Grassland caution: when combining with CS or other datasets, consider aggregating grassland classes or applying BHA rules for better cross-dataset consistency.
- MMU and accuracy: work within the 0.5 ha MMU constraints; interpret smaller parcels with caution due to potential below-MMU representations in CS.

## Example areas and data formats (5.x)
- Examples illustrate uplands, calcareous grasslands, urban areas, fenland, etc., across the UK using both vector and raster representations.
- Vector provides rich attribute data per parcel; raster offers standard gridded products for modelling and large-area analyses.
- A comparative visualization of 1 km percentage and dominant-class rasters demonstrates suitability for broad-scale UK modelling and integration with ancillary data (e.g., climate, hydrology).

## Access, licensing, and further information
- CEH Information Gateway: 1 km rasters.
- Full vector and 25 m rasters available on request; licensing may apply.
- For consultation, contact spatialdata@ceh.ac.uk or visit CEH data pages.

## Context, heritage, and broader significance
- LCM2007 builds on LCM1990/2000 with a cartography-derived spatial framework, enabling long-term change detection and cross-country comparability.
- It complements field-based Countryside Survey by providing coast-to-coast UK coverage and enabling integration with European datasets (e.g., Corine) and pan-European monitoring efforts.

Note: This summary distills the key GIS-relevant points, focusing on data products, processing, validation, comparisons with CS, change-mapping considerations, and practical usage guidance for GIS professionals.