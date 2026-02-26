# Final Report for LCM2007 - the new UK land cover map

- Aimed at providing a robust, policy-relevant view of UK land cover using a parcel-based vector product and derived raster products at 25m and 1km resolutions.
- Built to enable cross-dataset monitoring, habitat extent tracking, and change detection across the UK, GB and NI, with integration potential to Countryside Survey (CS) and broader biodiversity/planning workflows.

## What LCM2007 is and what it provides

- Parcel-based map of land cover derived from generalised national cartography (OS MasterMap and LPS Vector) plus multi-date satellite imagery; outputs include:
  - Vector product (parcels with attributes: area, Broad Habitat, KBEs, ProbList, etc.).
  - 25m raster product (23 LCM2007 classes).
  - 1km raster products (percent cover and dominant class for each 1km cell; both 23 classes and 10 aggregate classes).
- Class structure ties to Broad Habitats for UK Biodiversity Action Plan (BH/ BHSub classifications).
- Knowledge-based enhancements (KBEs) applied post-classification to improve thematic resolution, with original spectral classifications retained (ProbList) for user control.
- Outputs designed to support habitat monitoring, connectivity analyses, ecosystem services context, and policy evaluation.

## Key findings relevant to monitoring and policy analysis

- Dissimilar area estimates (LCM2007 vs Countryside Survey 2007 CS):
  - Classes with dissimilar UK-wide area estimates beyond CS 95% confidence limits: Arable and Horticulture, Improved Grassland, Neutral Grassland, Dwarf Shrub Heath, Bog, Montane Habitats, and coastal habitats; Fen, Marsh and Swamp also show large discrepancies.
  - Causes identified:
    - Definitions and boundaries differences (how “Arable and Horticulture” is delineated, including boundaries and linear features in LCM2007).
    - Spectral confusion due to diverse crop types, growth stages, and spectral variability (over- or misclassification risk).
    - Differences in spatial representation (CS maps boundaries vs LCM MMU, and how features below MMU are treated).
    - Temporal mismatch: LCM2007 uses multi-year imagery, inflating arable/temporary grass allocations in some areas due to seasonal field changes.
    - Grassland classifications: cross-cutting issues between Improved, Neutral, Calcareous, Acid, and Fen/Swamp categories; use of Broad Habitat Association rules to interpret relationships.
  - Specific examples highlight spectral and boundary issues driving over- or under-estimates forArable, Improved Grassland, Neutral Grassland, Fen/Marsh/Swamp, Montane, and coastal habitats.
- Change mapping and comparability:
  - Change detection is challenging due to differing spatial structures across LCM1990, LCM2000 and LCM2007 and parcel-level error (~20%); reliably separating real change from classification error is non-trivial.
  - Recommendation to re-align earlier CEH maps to a common real-world spatial framework (as in LCM2007) to improve change detection.
- Grassland and related habitats:
  - Grassland categories are particularly problematic due to one-to-many mappings to BHs; Broad Habitat Association rules were developed to improve interpretability and comparability with CS.
  - Appendix 5 (Broad Habitat Association) details reciprocal rules to align LCM2007 and CS classifications for several habitats (Bog, Dwarf Shrub Heath, Montane, Fen/Marsh/Swamp, Rough Grassland, Water classes, etc.).
- UK-wide and country-level patterns (4.4 UK Land Cover):
  - Over 50% of the UK classified as intensive land use (Arable/Horticulture + Improved Grassland) or Built-up Areas; remainder semi-natural with ~12% woodland; distribution varies by country (England highest intensity; Scotland higher Proportion of Coniferous Woodland and Montane/Heath components).
  - Comparisons to LCM2000 show notable shifts in Arable, Semi-natural Grassland, Coniferous woodland, and Urban fractions; spatial framework changes complicate direct interpretation of temporal trends.
- Implications for analysts:
  - LCM2007 provides a robust baseline for habitat extent, fragmentation, and landscape-scale ecological monitoring, with strong utility for policy evaluation (biodiversity, ecosystem services, catchment planning).
  - Be mindful of class-specific accuracy variation and known misclassifications (e.g., grasslands, fen, bog; coastal and montane areas).
  - Use 1km products to align with CS reporting where needed, and consider aggregating to BHAs or higher-level aggregates to improve comparability.

## Data quality, validation, and interpretation guidance

- Validation and accuracy:
  - Independent validation (CS reference points) indicates overall accuracy around 83% for LCM2007; class-level accuracy varies (e.g., Bog high producer accuracy; Neutral Grassland typically lower due to spectral/field-definition differences).
- Validation philosophy for analysts:
  - The Bespoke validation Appendix emphasizes “fit for purpose” rather than absolute truth; use parcel-level metadata (KBE, ProbList) to assess plausibility and consistency with imagery.
  - Suggested semi-quantitative validation approach: use high-resolution imagery (e.g., Google Earth) to judge plausibility of target classes, especially where ProbList indicates uncertainty.
- Outputs and metadata:
  - Vector: per-parcel attributes include area, Broad Habitat, BHSub (descriptive), FieldCode, KBE history, ProbList, CorePixels, etc.
  - KBEs provide traceability of post-classification corrections and context-based refinements.
  - 25m and 1km rasters derived from the vector, enabling different scales of analysis.

## Change detection and temporal considerations for monitoring

- Three-way map evolution (LCM1990, LCM2000, LCM2007) introduces structural differences; direct pixel-for-pixel or parcel-for-parcel change comparisons require careful methodological alignment.
- Recommendations for analysts:
  - When assessing trends, prefer aggregated classes or BHAs and/or re-project/transform older maps into the LCM2007 spatial framework for consistency.
  - Use the 1km raster products to support nationwide monitoring and cross-dataset comparisons (e.g., with CS data), while acknowledging differences in spatial detail and class definitions.
  - Consider the Broad Habitat Association rules to interpret cross-wacet changes between LCM and CS, especially for grasslands, fen, bog, and montane habitats.

## Outputs, access, and licensing

- Data products available:
  - 1km raster data (UK-wide) via CEH Information Gateway.
  - Full vector and 25m raster data available on request under licence from CEH (fees may apply).
- Practical use:
  - Vector data provides rich metadata and KBE/ProbLists for advanced validation and hypothesis testing.
  - 25m raster offers detailed land cover mapping with a direct analogue to the 23 LCM2007 classes.
  - 1km rasters facilitate broad-scale modeling and integration with other national datasets.

## Chapter 6: Discussion highlights

- LCM2007 delivers the first continuous parcel-based UK land cover map with a harmonised spatial framework derived from master cartography, enabling better inter-product compatibility and change-detection potential.
- Change detection between historic CEH maps requires rethinking to a common spatial structure; LCM2007’s framework is designed to support such harmonization for future monitoring.
- The LCM2007 map complements Countryside Survey by providing coast-to-coast coverage and consistent spatial units, while CS provides in-situ detail and habitat quality indicators not captured by satellite imagery.
- European links: data underpin Corine and LUCAS, contributing to pan-European land cover assessments and policy contexts.

## Practical guidance for environmental analysts

- Use LCM2007 as a baseline for UK-wide habitat extent, fragmentation, and landscape-change monitoring, with clear attention to class-specific accuracy and cross-dataset comparability.
- For trend analysis, align older LCM products to the LCM2007 spatial framework or translate CS outputs through Broad Habitat Association rules to improve interpretability.
- Leverage KBEs and ProbList metadata to assess classification confidence and to guide mask/validation decisions in areas with spectral ambiguity (e.g., grasslands, fen/bog transitions, coastal zones).
- When communicating results, report at multiple scales (parcel-level for precision, 1km for policy-relevant summaries, and BH-level aggregates for cross-country comparisons).

## Access and usage notes

- CEH Information Gateway hosts the 1km raster data; full vector and 25m raster data are available on request (licensing may apply).
- For detailed methodological guidance and validation procedures, consult Appendices on Bespoke validation and Broad Habitat Association rules, which provide structured approaches to comparing LCM2007 with CS and other datasets.