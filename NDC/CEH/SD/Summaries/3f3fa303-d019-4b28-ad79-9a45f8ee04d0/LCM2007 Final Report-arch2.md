# Final Report for LCM2007 - the new UK land cover map

- Overview
  - LCM2007 delivers a continuous parcel-based UK land cover map with broad habitat classifications, enabling cross-UK monitoring and potential change detection against Countryside Survey (CS) data.
  - Major focus in the excerpt: comparison with Countryside Survey 2007, dissimilar area estimates, UK-wide and country-level distro, validation issues, data products, and cross-walking between classifications for analysts.

## Dissimilar area estimates (CS vs LCM2007)

- Dissimilar areas arise for the following classes (UK scale, CS upper/lower 95% limits exceeded by LCM2007): Arable and Horticulture, Improved Grassland, Neutral Grassland, Dwarf Shrub Heath, Bog, Montane Habitats, and coastal habitats.
- Key drivers of differences
  - Classification differences: what counts as Arable and Horticulture may differ between CS and LCM2007; inclusion of Boundary and Linear Features in LCM2007 inflates some areas.
  - Spectral confusion: Arable and Horticulture is spectrally highly variable due to crops, growth stages, and multi-year imagery requirements, leading to misclassifications.
  - Boundary mapping: CS maps boundary/linear features that are often below LCM’s minimum mappable unit (MMU); LCM tends to group these into field polygons, increasing mapped area for Arable and Horticulture or Improved Grassland.
  - Grassland classification differences: Improved vs Neutral Grassland areas show substantial divergence; soils and land-use histories complicate spectral-to-phenology assignments.
  - Fen, Marsh and Swamp: CS and LCM2007 diverge by an order of magnitude due to mosaic nature, small patch sizes, and differing validation approaches; many CS Fen areas map as Rough Grassland or Acid Grassland in LCM2007.
- Additional notes
  - Temporary grass and uncropped land may be included in Arable and Horticulture in LCM2007, contributing to higher totals.
  - LCM imagery for full UK coverage requires multi-year inputs, influencing field-change signals (temporary grassland vs arable).

## Discussion

- Change mapping and comparability
  - Direct change detection between LCM2007 and CS is challenging due to structural differences (pixel vs segment vs parcel-based mapping) and classification error (~20%).
  - Aggregate-level or trajectory-based approaches may offer more reliable change signals than class-level comparisons.
  - A unified spatial framework based on real-world land-use units (as in LCM2007) is recommended to support consistent future monitoring.
- Grassland and BH (Broad Habitat) associations
  - Grasslands present a persistent challenge due to one-to-many relationships with Broad Habitats; Broad Habitat Association rules were developed to quantify correspondences beyond simple BH-to-class matches.
- CS comparison highlights
  - LCM2007 shows high correspondence with CS 1 km squares for Arable and Horticulture, but totals for Arable and Horticulture can be higher in UK-wide estimates.
  - Fen, Marsh and Swamp estimates show substantial differences; many Fen areas in CS are mapped as Rough Grassland or Acid Grassland in LCM2007.
- Practical implications for analysts
  - Expect regional variability in agreement; use BHAs and associated rules for more robust cross-walks.
  Using LCM2007 metadata and KBE history enables users to adjust analyses or re-run with alternative assumptions while retaining original spectral results.

## UK Land Cover distribution (4.4)

- UK-wide distribution
  - More than 50% of the UK is either intensive agriculture (Arable and Horticulture + Improved Grassland) or Built-up Areas and Gardens.
  - About 12% is Broadleaved and Coniferous Woodland combined; roughly 30% is semi-natural (including Mountain, heath and bog and semi-natural grassland).
  - Freshwater and coastal components vary by country due to geography (e.g., Lough Neagh in NI, upland Scotland).
- Country-level differences (England, Scotland, Wales, Northern Ireland)
  - England: highest intensive land-use share (around 76%).
  - Scotland and Northern Ireland/Wales have substantial semi-natural components and woodland types; Scotland has the largest Coniferous Woodland share and the greatest proportion of Mountain, heath and bog.
- Comparisons with LCM2000
  - LCM2007 increases Arable area and slightly reduces Semi-natural Grassland compared with LCM2000; minor shifts in woodland proportions noted.

## Summary and discussion (4.5)

- Agreement and variability
  - Agreement between LCM2007 and CS varies widely by Broad Habitat; grassland categories are particularly problematic due to one-to-many relationships and the need for BH Association rules.
  - LCM2007 aligns well with CS for Arable and Horticulture at the 1 km square level, but UK-wide totals for Arable and Horticulture exceed CS estimates.
- Fen, Marsh and Swamp
  - Large discrepancies attributed to complex mosaics and scale; CS tends to map Fen areas that are often captured as Rough Grassland or Acid Grassland in LCM2007.
- Implications for policy and monitoring
  - LCM2007 provides a consistent UK-wide framework to support habitat monitoring, biodiversity assessments, and landscape planning, especially when combined with other data.
  - The Broad Habitat Association rules and metadata enable flexible, transparent re-analysis while preserving spectral signatures.

## Example areas and data products (5.x)

- Example areas (Chapter 5)
  - A variety of habitats and landscapes (upland, calcareous grassland, urban, arable, fenland) illustrated to demonstrate LCM2007 performance across contexts.
- Vector and raster products (5.2)
  - Vector product: land parcels (polygons) with attributes such as area, sources, Broad Habitat (BH), processing history, KBE history, probabilistic signatures (ProbList), core pixels, etc.
  - BHSub and FieldCode provide sub-class information; CorePixels used for classification statistics.
  - Raster products: 25 m resolution (23 LCM2007 classes) and 1 km resolution (two summaries per pixel:
    - Percentage cover per class (for each LCM2007 class)
    - Dominant class per pixel
  - Access
    - 1 km rasters via CEH Information Gateway.
    - Full vector and 25 m rasters licensed on request from CEH (licensing may apply).

## Validation, bespoke validation, and quality assurance (Appendix 4)

- Validation philosophy
  - There is no absolute truth in geography; accuracy is about fitness for purpose.
  - LCM2007 provides parcel-level metadata, including KBE history and probability of top spectral variants, enabling targeted quality checks.
- Bespoke validation approach
  - Proposes an informal Bayesian-like approach using high-resolution imagery to assess whether LCM2007 attribution is consistent with observed imagery.
  - Suggests a two-part assessment: parcels with high vs. moderate probability for a target class; use fuzzy categories (plausible, probably, possibly) to bound accuracy.
  - A Python-based toolset has been developed to support this validation approach.

## Broad Habitat Association (Appendix 5)

- Purpose
  - Describes rationale and rules for cross-walking between LCM2007 classes and CS Broad Habitats (BHAs) to improve interpretability and comparability.
- Key cross-walk rules (highlights)
  - Bog: LCM Bog ↔ CS Dwarf Shrub Heath / Acid Grassland / Montane Habitats (and vice versa) with reciprocal compatibility at BH adjacency level.
  - Dwarf Shrub Heath vs Acid Grassland: upland mosaics may be ambiguous; rules acknowledge transitional zones.
  - Montane Habitats: LCM Montane can substitute for CS Dwarf Shrub Heath / Acid Grassland / Bog in BH-level comparisons; montane areas above threshold may not map to non-montane classes.
  - Built-up Areas and Gardens: CS urban parcels may include water, grassland, woodland within urban extents; LCM mapping may reflect more varied land covers; compatibility defined but not reciprocal in all cases.
  - Fen, Marsh and Swamp: complex mosaics; non-Fen components within a polygon mapped as CS Fen may still be considered acceptable.
  - Rough Grassland: treated as a mixture of Improved Grassland and various grassland types; acceptable correspondences are defined with multiple habitat classes.
  - Water classes: CS water classes correspond to LCM Water categories (Saltwater / Freshwater) with non-reciprocal aspects in some cases.
  - Tidal areas: Saltwater vs Littoral classifications are considered with reciprocal compatibility under tidal context.

## Data access, European context, and policy relevance (Chapter 6 and related)

- Change detection and policy relevance
  - LCM2007 provides a foundational framework for habitat monitoring, landscape planning, biodiversity accounting, carbon and hydrology-related analyses, and catchment management.
  - Cross-border and country comparisons are facilitated by a common spatial framework, enabling consistent policy evaluation.
- European links
  - UK component of Corine Land Cover 2006 derived from LCM2007 vector product through generalisation/thematic transformations.
  - LCM2007 aligns with European data initiatives (e.g., IMAGE2006), supporting pan-European environmental assessment.
- Access and use
  - 1 km rasters via CEH gateway; full vector and 25 m rasters via license requests to CEH.
  - The report emphasizes that licensing fees may apply and usage should reference the original data.
- Purpose and impact
  - LCM2007 represents a major advancement as the first continuous parcel-based UK land cover map, enabling more accurate change detection and cross-sector analyses.
  - The transition to a stable, reusable spatial framework is intended to improve efficiency for future national land cover mapping and monitoring.

Note: Throughout the document, the emphasis for analysts monitoring the environment is on using LCM2007 as a consistent, evidence-based baseline for habitat monitoring, policy evaluation, and cross-sector analyses, while recognizing and accounting for known limitations in grassland, fen, and boundary-feature mappings, and leveraging the provided metadata, KBEs, and BHAs to tailor analyses to specific needs.