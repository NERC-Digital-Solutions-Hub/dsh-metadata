# Final Report for LCM2007 - the new UK land cover map

## Purpose and scope
- Presents the UK’s first continuous parcel-based land cover map (LCM2007) with UK-wide coverage across vector (parcels) and raster products (25 m and 1 km).
- Aims to support habitat monitoring, biodiversity assessment, landscape planning, and policy evaluation by providing standardized, multi-scale land cover data aligned with Broad Habitats (BAP) classifications.
- Enables comparisons with Countryside Survey (CS) data from 2007 and supports change analysis within a UK-wide framework.

## Dissimilar area estimates (UK CS 2007 vs LCM2007)
- Dissimilar area estimates occur for Arable and Horticulture, Improved Grassland, Neutral Grassland, Dwarf Shrub Heath, Bog, Montane Habitats, and coastal habitats (areas outside CS 95% confidence limits).
- Arable and Horticulture:
  - CS UK total: ~46,574 km2; DEFRA 2007: ~63,005 km2 for UK agriculture/land-use mix.
  - LCM2007: ~63,005 km2; CS upper limit ~51,276 km2.
  Contributing factors:
  - Differences in what CS vs LCM2007 classify as “Arable and Horticulture.”
  - Spectral confusion and inclusion of Boundary/Linear Features in LCM2007’s arable extent.
  - Temporal range of imagery; multi-year composites increase field changes (temporary grassland ↔ arable) over time.
  - Boundary features in CS mapped at field level vs LCM’s field/delimited parcels.
- Improved Grassland and Neutral Grassland:
  - LCM2007 shows ~10,000 km2 more Improved Grassland and ~10,000 km2 less Neutral Grassland than CS.
  - Likely due to how neutral grasslands are spectrally represented vs spectral signatures and soil data influences.
- Dwarf Shrub Heath and Bog:
  - LCM2007 totals ~32,090 km2 vs CS lower/upper limits ~31,931 km2 for combined Dwarf Shrub Heath and Bog.
- Fen, Marsh and Swamp:
  - CS 2007 UK ~4,392 km2; LCM2007 ~101 km2.
  - Fennel mosaics and small patches lead to major differences; many CS Fen areas map to Rough Grassland or Acid Grassland in LCM2007.
- Montane and coastal habitats:
  - Represented poorly in CS data; differences expected.
- Overall interpretation:
  - Differences reflect methodological and spatial-structure differences, spectral variability, and how each product handles small, mosaicked, or transitional habitats.

## UK Land Cover distribution and cross-country patterns (LCM2007)
- UK-level snapshot:
  - More than 50% of the UK is intensive land use (Arable and Horticulture + Improved Grassland) or Built-up Areas and Gardens (6%), with Woodlands ~12% (split between Broadleaved and Coniferous).
  - Remaining ~30% semi-natural (including Mountain, Heath, and Bog; some coastal classes).
- Country-level patterns:
  - England: highest proportion of intensive land use (~76%: ~40% Arable, ~27% Improved Grassland, ~9% Built-up).
  - Scotland: lowest intensive share (~36%), but has the largest Coniferous Woodland share; substantial semi-natural areas (e.g., Mountain, Heath, and Bog; semi-natural grassland).
  - Wales and Northern Ireland: intermediate patterns with regional variations in habitat extents and CS survey strategies.
- Comparison with LCM2000:
  - LCM2007 shows increases in Arable and Horticulture share (relative to LCM2000) and changes in woodland classifications, with ongoing questions about spatial framework effects on area estimates.

## Discussion and interpretation (4.5)
- Agreement between LCM2007 and CS varies widely across Broad Habitats.
- Grassland complexity:
  - Grassland classifications are problematic due to one-to-many relationships with Broad Habitat types; Broad Habitat Association (BHA) rules were developed to interpret correspondences, adding a third level of thematic accuracy.
- Arable area:
  - High correspondence with CS 1 km squares for the Arable category, but total UK Arable area in LCM2007 is larger than CS, driven by classification and boundary feature integration.
- Fen, Marsh and Swamp:
  - Large discrepancies explained by mosaic nature and patch size; CS patches below LCM2007’s minimum mapping unit frequently mapped as Rough Grassland or Acid Grassland in LCM2007.
- Change mapping challenges:
  - Differing spatial and thematic structures across LCM generations complicate change detection; aggregation or reorganization around a common spatial framework is recommended for robust change analysis.
- Practical implications:
  - Use Grassland aggregations for better CS correspondence.
  - Be mindful of KBEs and consult polygon metadata; some classes are more accurately represented than others due to spectral variability and data quality.

## Products, metadata, and access (Vector, 25 m raster, 1 km raster)
- Vector product:
  - Parcel-based land cover with rich metadata per polygon (area, source images, Broad Habitat, processing history, KBE history, ProbList, etc.).
- Raster products:
  - 25 m resolution: 23 LCM2007 classes.
  - 1 km resolution: two summaries per pixel — (A) percentage cover per class, (B) dominant class.
- UK coverage and data structure:
  - Nine geographic chunks to ensure seamless UK output; detailed provenance and processing history retained for traceability.
- Data access:
  - 1 km raster data via CEH Information Gateway.
  - Full vector and 25 m raster data available on request under license; licensing fees may apply.

## Knowledge-based enhancements (KBEs) and Broad Habitat Associations (BHA)
- KBEs improve separation of spectral confusion and refine habitat mapping by using contextual data (terrain, soils, proximity to urban areas, etc.).
- Potential for misclassification if misapplied; manual checks and polygon metadata review recommended.
- BHA rules help interpret one habitat in terms of CS correspondence and vice versa; rules are designed to improve cross-product compatibility but are not always reciprocal.

## Validation and quality assurance
- LCM2007 includes field validation and QA procedures; polygon-level metadata enables users to assess the provenance and confidence for specific locations.
- Validation results indicate variable producer’s and user’s accuracy by class; cautions are provided for class-specific results.

## Practical implications for analysts monitoring the environment
- Expect class-dependent accuracy variability; refer to class-specific accuracy when using habitat classes.
- Consider aggregating grassland classes to improve correspondence with field data.
- Use KBEs to refine analyses, while keeping track of processing history to avoid misinterpretation.
- Leverage the UK-wide, multi-scale framework for comparable, cross-year analyses and for integration with other data sources (e.g., climate, hydrology, biodiversity).

## Appendices and contextual resources
- Appendix 5: Broad Habitat Association rules (BHA) outlining class-by-class correspondence logic between LCM2007 and CS.
- Appendix 4: Bespoke validation approach emphasizing fit-for-purpose accuracy and parcel-level metadata for validation planning.
- Appendix: Glossary of terms clarifies habitat classifications, data formats, and mapping terminology.

## Data provenance and related links
- LCM2007 builds on international European data (Corine, LUCAS) and CEH’s Countryside Survey lineage, leveraging MasterMap and large-scale cartography for improved integration and applicability to policy monitoring.
- Data and reports provide a framework for national-scale habitat monitoring, landscape planning, biodiversity assessment, and ecosystem service analyses, with potential for cross-border and European policy alignment.