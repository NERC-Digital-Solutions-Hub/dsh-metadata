# Final Report for LCM2007 - the new UK land cover map

- Compares LCM2007 with Countryside Survey (CS) 2007 to assess agreement in Broad Habitats and UK land cover extents.
- Identifies when LCM2007 and CS agree (or diverge) at national and country scales, and explores reasons for differences.
- Presents the Broad Habitat Association (BHA) framework to better interpret cross-walks between LCM2007 classes and CS Broad Habitats.
- Highlights data and methodological factors affecting comparisons, including spatial units, spectral confusion, and mapping thresholds.
- Notes the value of parcel-level metadata and knowledge-based enhancements (KBEs) for improving classification and for enabling user-driven validation.

## Very similar area estimates (CS 2007 within UK CS 95% limits)

- Very similar area estimates occur for:
  - Coniferous Woodland
  - Freshwater
  - Built-up Areas and Gardens
  - Calcareous Grassland
- This reflects strong agreement between CS 2007 field data and LCM2007 outputs for these classes (spatial and thematic alignment).

## Similar area estimates

- Similar area estimates (within CS 2007 UK 95% limits) occur for:
  - Broadleaved woodland
  - Acid Grassland
  - Inland Rock

## Dissimilar area estimates

- Dissimilar area estimates (beyond UK CS 95% limits) occur for:
  - Arable and Horticulture
  - Improved Grassland
  - Neutral Grassland
  - Dwarf Shrub Heath
  - Bog
  - Montane Habitats
  - Coastal habitats
- Main contributing factors:
  - Classification differences in Arable and Horticulture (e.g., spectral confusion, temporal range, and inclusion of boundaries/lines in LCM2007)
  - Discrepancies in grassland categories (Improved vs Neutral vs Calcareous/Acid) and how grassland is spectrally represented
  - Differences in how Fen, Marsh and Swamp are identified (complex mosaics and small patch sizes)
  - Spatial structure differences and MMU effects (Minimum Mapping Unit) impacting class extents
  - Boundary and linear features being treated differently across CS and LCM2007

- Specific points:
  - CS and DEFRA agricultural statistics show ARABLE and HORTICULTURE figures that can align with LCM2007 when temporary grass and uncropped land are interpreted differently.
  - Spectral variability in Arable and Horticulture leads to overestimation in some areas.
  - Boundary/linear features in CS are often below LCM MMU and thus mapped differently in LCM2007, influencing area estimates for Arable/Improved Grassland.

## 4.4 UK Land Cover

- UK-wide distribution: more than 50% of UK land is intensive (Arable + Improved Grassland) or Built-up Areas and Gardens; remainder semi-natural.
- Woodland: ~12% UK, split between Broadleaved and Coniferous.
- Regional variation:
  - England: highest intensive land use (~76%: 40% Arable and 27% Improved Grassland; 9% Built-up)
  - Northern Ireland and Wales: ~64% intensive land use
  - Scotland: ~36% intensive land use but highest Coniferous Woodland share
- Differences vs LCM2000:
  - LCM2007 shows higher Arable area (26% vs 23% in LCM2000) and higher semi-natural grassland (13% vs 17% in LCM2000 for Semi-natural Grassland in some contexts)
  - Coniferous woodland slightly increased; Urban area slightly lower
- Change mapping across LCM1990, LCM2000, and LCM2007 is complex; automated change detection remains challenging due to differing spatial and thematic structures.

## 4.5 Summary and discussion

- Agreement between LCM2007 and CS varies widely across Broad Habitats; grassland categories are particularly problematic due to cross-walking complexities.
- Broad Habitat Association (BHA) rules were developed to improve interpretability of correspondences, adding a third level of thematic accuracy beyond Broad Habitat and Aggregate class levels.
- LCM2007 aligns well with CS 1km-square arable and horticulture areas, but LCM2007 often reports larger Arable and Horticulture extents overall.
- Fen, Marsh and Swamp estimates differ by an order of magnitude; fen is a mosaic of types, leading to misclassification or reallocation to Rough Grassland/Acid Grassland in LCM2007.
- The appendix emphasizes bespoke validation and the utility of parcel-level metadata to assess the likelihood of accurate class attribution in a given location.
- Recommendations for analysts:
  - Consider both Producer’s and User’s accuracies; use aggregated grassland classes where appropriate.
  - Use the KBEs and BHA framework to interpret cross-walk results and to inform validation efforts.
  - Leverage parcel metadata and probability lists to inform site-specific validation and to quantify uncertainty.

## Bespoke validation (Appendix 4)

- Accuracy depends on use; no absolute truth for geography.
- LCM2007 provides parcel-level metadata, including knowledge-based enhancements (KBE) history and probabilities for the top five spectral variants.
- A practical validation approach: use high-resolution imagery to judge consistency with LCM2007 attributes, applying a two-part assessment (high-probability vs moderate-probability parcels) and using fuzzy categories (plausible, probably, possibly) to bound accuracy estimates.
- A Python-based validation toolkit accompanies the methodology.

## Broad Habitat Association (Appendix 5)

- Provides rationale for how LCM2007 Broad Habitats correspond to CS Broad Habitats (class-by-class rules).
- Key examples:
  - Bog: reciprocal correspondence with CS Dwarf Shrub Heath, Acid Grassland, and Montane Habitats, recognizing continuum and peat-depth considerations.
  - Dwarf Shrub Heath vs Acid Grassland: upland mosaics may shift between classes; cross-walk allows correspondence in different directions depending on context.
  - Montane Habitats: generally map upland montane areas; correspondence with CS Dwarf Shrub Heath, Acid Grassland, and Bog at the Broad Habitat adjacency level.
  - Built-up Areas and Gardens: CS maps urban parcels but with additional attributes; LCM2007 correspondence may map urban areas to grassland, woodland, or water in LCM depending on context.
  - Fen, Marsh and Swamp: mosaic nature leads to cross-walk with various CS classes; not reciprocal for all cases.
  - Rough Grassland: treated as mixed; is assigned to Neutral Grassland in some contexts but may include Improved Grassland and other grassland types; cross-walk uses a broader acceptance.
  - Water classes and tidal areas: LCM water classes correspond to CS water classes; tidal position affects correspondence with Littoral habitats.
- These rules are designed to improve interpretability and comparability between LCM2007 and CS outputs, acknowledging inherent differences in spatial structure and data sources.

Note: The summary captures core comparisons, interpretations, and methodological insights from the provided text chunks, focusing on data-driven analysis, cross-validation, and interpretive frameworks relevant to analysts seeking correlations and robust, reproducible conclusions.