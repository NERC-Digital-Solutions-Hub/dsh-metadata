# Final Report for LCM2007 - the new UK land cover map

- Overview of comparisons
  - The report compares LCM2007 with Countryside Survey (CS) 2007 to assess agreement in Broad Habitats and aggregated classes, using both 1 km CS squares and national CS estimates.
  - Differences between spectral-based LCM2007 and field-survey CS arise from class definitions, scale, spatial framework, and inherent classification errors.

- Very similar area estimates (CS upper/lower 95% limits)
  - Very similar for: Coniferous Woodland, Freshwater, Built-up Areas and Gardens, and Calcareous Grassland.
  - Calcareous Grassland similarity is notable given it was a class that performed poorly in the correspondence matrix; large mapped calcareous grassland areas (e.g., Salisbury Plain, South Downs) may drive alignment with CS totals.

- Similar area estimates (UK-wide 95% limits)
  - Similar for: Broadleaved woodland, Acid Grassland, and Inland Rock.

- Dissimilar area estimates (UK-wide 95% limits)
  - Dissimilar for: Arable and Horticulture, Improved Grassland, Neutral Grassland, Dwarf Shrub Heath, Bog, Montane Habitats, and coastal habitats.
  - Key drivers of discrepancies (examples):
    - Arable and Horticulture: CS and DEFRA agricultural totals differ; LCM2007 may include boundaries/linear features or temporal changes that CS excludes; spectral variability of arable crops causes misclassification.
    - Boundary and Linear Features: CS maps include boundaries that often fall below LCM MMU; LCM tends to lump these into adjacent land-cover parcels, inflating some categories.
    - Grasslands (Improved/Neutral): Differences in spectral signatures and field-identified species composition; neutral vs improved grassland distinctions are challenging spectrally and soil data provide limited resolution.
    - Fen, Marsh and Swamp: Highly mosaicked and small, CS tends to record mosaic patches differently; LCM2007 often maps as Rough Grassland or other types, leading to large UK-level differences in this category.
    - Montane, Inland Rock, coastal habitats: CS data are sparser or differently captured in upland/coastal zones, contributing to discrepancies.

- UK Land Cover distribution (LCM2007 vs CS)
  - UK distribution: over 50% of land in Arable and Horticulture plus Improved Grassland; ~12% in Broadleaved/Coniferous Woodland; remaining semi-natural (coastal, semi-natural grasslands, montane habitats).
  - Country patterns:
    - England shows highest intensive land use (about 40% Arable, 27% Improved Grassland, ~9% Built-up).
    - Scotland has more Coniferous Woodland and larger shares of semi-natural and montane habitats.
    - Ireland and Wales show different compositions, with notable upland and coastal patterns.
  - Comparison to LCM2000 indicated some shifts in proportions, but interpretation is complicated by spatial framework changes.

- Chapter 4.5: Summary and discussion
  - Agreement between LCM2007 and CS varies across Broad Habitats; grassland categories are particularly problematic due to one-to-many relationships between observed land cover and Broad Habitat groupings.
  - Broad Habitat Association (BHA) rules were developed to improve correspondence assessment, especially for grassland mosaics.
  - LCM2007 shows high correspondence with CS area for Arable and Horticulture in 1 km CS squares, but UK-wide Broad Habitat extents may be overestimated in some categories.
  - Fen, Marsh and Swamp differences are dramatic due to mosaic and small patch sizes; future work could use KBEs to reallocate some of these to Fen, Marsh and Swamp.

- 5.1 Example areas
  - A set of example areas demonstrates LCM2007’s performance across habitats (upland, calcareous grassland, urban, arable/fenland), highlighting boundary delineation, mosaic landscapes, and the mix of land-cover types within parcels.

- 5.2 Vector and raster products
  - LCM2007 provides both vector (parcels with attributes) and raster products at 25 m and 1 km resolution.
  - Vector: includes Parcel_ID, Broad Habitat (BH), Broad Habitat sub-class (BHSub), FieldCode, KBE history, ProbList (top five spectral class probabilities), CorePixels, and Construct history.
  - 25 m raster: 23 LCM2007 classes with metadata.
  - 1 km raster: (A) percentage cover per class, (B) dominant class per pixel.
  - KBEs (Knowledge-Based Enhancements) are recorded in the KBE field to trace processing steps and are meant to be used with caution; validation is advised for sub-class and probability fields.

- 6. Change detection and data integration
  - LCM2007 represents an advance in providing a continuous UK-wide spatial framework; however, comparing LCM2007 with earlier CEH maps (LCM1990, LCM2000) is complicated due to differing spatial structures and class schemes.
  - The chapter emphasizes the need for a common real-world spatial framework to enable robust change detection and comparability across time.

- Data access and usage
  - 1 km rasters are available via the CEH Information Gateway; full vector and 25 m rasters are available on request (licensing may apply).
  - KBEs and detailed metadata enable reproducibility and local tailoring; users are advised to consider grassland aggregation or BH-level analyses to optimize comparability with CS data.

- Knowledge-based enhancements and Broad Habitat Association (BHA)
  - KBEs use contextual data (terrain, soils, urban context, coastal proximity, etc.) to resolve spectral confusion and refine thematic resolution.
  - BHA rules address complex relationships between grassland and associated Broad Habitats, and relationships between land-cover classes and CS classifications. Rules are reciprocal where possible and designed to improve interpretability in cross-dataset comparisons.

- BESPOKE validation and quality assurance
  - Bespoke validation emphasises fit-for-purpose accuracy rather than absolute truth, using parcel-level metadata to evaluate the consistency of LCM2007 classifications with high-resolution imagery and field data.
  - A two-part validation approach (high-probability and moderate-probability parcels) supports a nuanced understanding of target-class accuracy.

- Practical implications for analysts
  - Expect variability in agreement across habitats; use BHA rules and KBEs to interpret mismatches.
  - When aligning LCM2007 with CS, consider aggregating grassland classes or evaluating at the BH or aggregate class level to improve correspondence.
  - Use the 1 km CS-based comparisons for broad-scale validation but rely on LCM2007’s UK-wide parcel framework for change detection and policy-relevant analyses.
  - For local analyses, leverage the parcel-level metadata and KBEs to assess the plausibility of classifications against high-resolution imagery.

- Access and citation
  - The report provides guidance on data access, licensing, and recommended citation: Final Report for LCM2007 - the new UK land cover map, Countryside Survey Technical Report No 11/07, CEH.