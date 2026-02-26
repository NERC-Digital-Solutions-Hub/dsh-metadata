Final Report for LCM2007 - the new UK land cover map

## Overview
- Presents a comparison between LCM2007 and Countryside Survey (CS) 2007, focusing on area estimates for Broad Habitats and how well LCM2007 aligns with CS at various thematic levels.
- Documents reasons for similarities and differences, including spatial structure, data sources, spectral/classification issues, and the Broad Habitat Association (BHA) framework.

## Key data and methods (context for Analysts)
- LCM2007 is based on a parcel/land-cover classification derived from national cartography and multi-temporal satellite data, enhanced by knowledge-based rules (KBEs) and Broad Habitat Association rules.
- Validation draws on 9,127 ground reference points; CS 2007 provides UK-wide estimates and 95% confidence limits used for comparison.
- Important sources of discrepancy discussed include MMU/space, spectral variability (especially for Arable and Horticulture), and how boundaries/linear features are treated.

## Very similar area estimates (LCM2007 vs CS 2007)
- Coniferous Woodland
- Freshwater
- Built-up Areas and Gardens
- Calcareous Grassland
- Rationale: strong agreement between LCM2007 and CS for these classes, reflecting stable spectral/landscape signatures or well-captured boundaries.

## Similar area estimates
- Broadleaved Woodland
- Acid Grassland
- Inland Rock
- These show substantial alignment when CS 95% limits are considered.

## Dissimilar area estimates
- Arable and Horticulture
- Improved Grassland
- Neutral Grassland
- Dwarf Shrub Heath
- Bog
- Montane Habitats
- Coastal habitats
- Key drivers of dissimilarity:
  - Arable and Horticulture: LCM2007 ~63,005 km2 vs CS upper limit ~51,276 km2; attributed to differences in classification scope, spectral confusion, and inclusion of boundary/linear features in LCM2007.
  - Boundary and linear features: CS maps many boundaries below LCM MMU; LCM2007 often incorporates them into field polygons, inflating arable/improved grassland areas.
  - Grassland varieties: Improved vs Neutral grassland differ depending on spectral signatures and soil data; Neutral/Improved misclassification linked to soil context and spectral variability.
  - Fen, Marsh and Swamp: CS 2007 shows much larger areas than LCM2007; mosaics and small patch sizes contributing to divergence; CS may map as Rough Grassland or Acid Grassland in places where LCM2007 detects Fen differently.
  - Montane Habitats: upland classes challenging to separate spectrally and via altitude-based KBEs; Montane mappings can substitute for other upland habitats.
  - Coastal and some upland habitats show regionally variable correspondence.

## UK-wide indicators and country variation (LCM2007 vs CS 2007)
- LCM2007 shows that over 50% of the UK is in intensive land use (Arable and Horticulture plus Improved Grassland) or Built-up Areas.
- Woodland accounts for about 12% UK-wide (roughly evenly split between Broadleaved and Coniferous).
- Scotland has the largest share of Montane/Hill-type habitats; England has the highest proportion of Arable and Built-up areas; Northern Ireland/Wales show distinct patterns driven by local land use.
- Comparison with LCM2000 indicates some shifts in class proportions (e.g., Arable and Semi-natural grassland), but interpretation is complicated by changes in spatial framework and temporal coverage.

## Change mapping and methodological considerations
- Change detection between LCM generations (1990, 2000, 2007) is challenging due to differences in spatial structure and classification schemes.
- Typical image classification error around 20% means robust separation of real change from observational error requires methodological advances.
- KBEs and contextual data help mitigate some uncertainties and improve thematic resolution, particularly for grassland and montane adjustments.

## KBEs and Broad Habitat Association (BHA)
- Seven automated KBEs applied to resolve spectral confusion and refine thematic resolution; KBEs affect about ~20% of parcels.
- KBAs leverage boundaries, soils, terrain, urban context, and altitude to guide reclassifications while preserving the ProbList (top spectral signatures) for traceability.
- BHA rules help reconcile spectral classes with CS Broad Habitat interpretations, especially for complex mosaics (e.g., Bog, Dwarf Shrub Heath, Montane Habitats, Fen, Marsh and Swamp).

## Product details and data access (analyst-focused)
- Vector product: parcel-level polygons with attributes including area, Broad Habitat, KBE history, and ProbList; includes detailed metadata per polygon.
- Raster products: 25 m (23 LCM2007 classes) and 1 km dominant/percent cover products; used for broad-scale analyses and modelling.
- Access:
  - 1 km raster data: CEH Information Gateway (open access).
  - 25 m vector and 25 m raster data: available under licence on request from CEH.
  - License terms may apply; contact spatialdata@ceh.ac.uk or CEH data portal.

## Validation, uncertainties, and interpretation guidance
- Ground reference validation (9,127 points) yields overall accuracy around 83%; per-class accuracies vary (e.g., Bog high producer but low user accuracy; grassland aggregations improve aggregated accuracies).
- Differences with CS reflect not only spectral and classification issues but also differences in spatial structure, MMU, and field vs satellite perspectives.
- For analysts, aggregation (e.g., grassland types) and using Broad Habitat Associations improves comparability with CS and supports policy-relevant interpretation.
- The Bespoke validation appendix advocates a flexible, probabilistic approach to accuracy (e.g., plausible/probable/possibly) using high-resolution imagery as a sanity check.

## Implications for decision-makers and researchers
- LCM2007 provides a consistent UK-wide land cover framework aligned with BAP Broad Habitats, enabling habitat assessment, connectivity analyses, and policy evaluation.
- The integration of high-resolution cartography with spectral classification yields a robust spatial framework that facilitates future monitoring and change detection.
- Analysts should use aggregated grassland classes and BHA guidance when comparing with CS or other datasets; be cautious about interpreting raw 1:1 class matches for fringe habitats (Fen, Montane, etc.).

## Practical guidance for analysts
- Use KBEs and BHA rules to interpret problematic classes and to harmonize with field-based CS outputs.
- When validating against CS, consider aggregation and country-specific landscape context to improve comparability.
- For change analyses, apply a combination of KBEs with contextual data and focus on robustly mapped, consistently classified classes or aggregated groups.

## Summary takeaway
- LCM2007 advances UK-wide land cover mapping by using a parcel-based framework derived from national cartography and enhanced with multi-temporal imagery and KBEs. While achieving high agreement with CS for several key habitats, notable discrepancies remain in arable, certain grasslands, fen/marsh, montane, and coastal habitats due to spectral classification limits, spatial structure differences, and boundary feature treatment. The UK-wide, multi-resolution data products and the Broad Habitat Association framework provide a versatile, traceable basis for habitat monitoring, policy support, and change detection, with careful interpretation required when comparing to field-based surveys.