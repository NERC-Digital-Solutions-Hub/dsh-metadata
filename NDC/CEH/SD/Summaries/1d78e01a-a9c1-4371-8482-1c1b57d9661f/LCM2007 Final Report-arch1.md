# Final Report for LCM2007 - the new UK land cover map

- This section summarizes the comparisons between LCM2007 and the Countryside Survey (CS) 2007, focusing on area estimates across Broad Habitats (BH) and their Broad Habitat Associations (BHAs), and discusses reasons for similarities and differences.

## Very Similar area estimates (CS 2007 vs LCM2007)
- Very similar area estimates occur for:
  - Coniferous Woodland
  - Freshwater
  - Built-up Areas and Gardens
  - Calcareous Grassland

- Note: The strong agreement for Coniferous Woodland aligns with correspondence analyses. Calcareous Grassland similarity is somewhat surprising given its variability, but large mapped extents (e.g., Salisbury Plain, South Downs) help align totals with CS.

## Similar area estimates
- Similar results occur for:
  - Broadleaved woodland
  - Acid Grassland
  - Inland Rock

## Dissimilar area estimates
- Dissimilar results occur for:
  - Arable and Horticulture
  - Improved Grassland
  - Neutral Grassland
  - Dwarf Shrub Heath
  - Bog
  - Montane Habitats
  - Coastal habitats
  - Fen, Marsh and Swamp (noted separately below)

- Key explanatory themes:
  - Differences in what CS and LCM2007 classify as “Arable and Horticulture” (including temporary grass and uncropped land in LCM2007).
  - Spectral confusion and multi-year temporal variability in arable crops driving overestimation in some areas.
  - How boundaries and linear features are treated: CS maps boundaries/lines that may be below LCM MMU, while LCM often folds these into adjacent fields, affecting habitat categorization.
  - Grassland classifications: mismatch between grassland types (Improved, Neutral, Calcareous, Acid) due to spectral variability and soil context.
  - Dwarf Shrub Heath, Montane Habitats, and Bog allocations often reflect transitions along ecological continua or montane thresholds, complicating one-to-one mappings.
  - Fen, Marsh and Swamp: CS identifies small, mosaic components; LCM often records as Rough Grassland or other BHs, leading to large UK differences; CS patches below MMU also influence comparisons.

## Drivers of discrepancies (further detail)
- Class definition differences and spatial structure: LCM2007’s parcel/vector approach vs CS’s field-based or square-based framework.
- Spectral variability and temporal range: arable/grassland spectral signatures vary with crop type, growth stage, and year-to-year conditions.
- Boundary and feature delineation: formal boundaries in CS vs MMU-based aggregation in LCM2007.
- Habitat mosaics and transitional habitats: Fen, Marsh and Swamp, Montane, Bog, and coastal habitats show larger discrepancies due to mosaics and limited ground-truth for some BHAs.
- Ground-truth data limitations: CS 2007 provides field observations at discrete squares; LCM2007 provides coast-to-coast coverage but may miss narrow features (hedgerows, streams) that CS captures more finely.
- Temporal mismatch: need multiple-year imagery to map some land uses; seasonal differences can bias arable/grassland classifications.

## 4.4 UK Land Cover (national and country-level patterns)
- UK-wide distribution:
  - More than 50% of the UK land is intensive use (Arable and Horticulture plus Improved Grassland) or Built-up Areas and Gardens.
  - Approximately 12% is woodland (Broadleaved and Coniferous combined).
  - About 30% semi-natural (including Mountain, Heath, Bog, etc.).
- Country-level variation:
  - England shows the highest proportion of intensive land use (roughly 40% Arable and Horticulture, 27% Improved Grassland, 9% Built-up Areas and Gardens).
  - Scotland has the largest share of Coniferous Woodland and the greatest extent of semi-natural habitats (e.g., Mountain, Heath, Bog; 36% Mountain/heath and 20% semi-natural grassland).
  - Northern Ireland and Wales show intermediate patterns of intensive use.
- Comparison with LCM2000:
  - LCM2007 increases Arable and reduces semi-natural grassland compared with LCM2000 (e.g., Arable around 26% vs 23% in 2000; semi-natural grassland around 13% vs 17% in 2000).
  - Some shifts in Coniferous Woodland and Urban areas are noted; interpretation of these changes is complex due to framework differences.
- UK-wide summaries (Broad Habitats) indicate broad-scale differences in certain BH classes when compared with CS 2007 confidence limits (CS 95% limits used to judge whether LCM2007 is within expected bounds).

## 4.3.3 Discussion (interpretive context)
- Agreement between LCM2007 and CS varies widely by Broad Habitat, reflecting differences in data sources and structures.
- Grasslands are especially problematic due to one-to-many correspondences between observed land cover and BH classes; this motivated the development of Broad Habitat Associations (BHAs) to improve interpretability.
- LCM2007 aligns well with CS 1km square-area estimates for Arable and Horticulture, but its national total for Arable and Horticulture tends to be higher, partly due to the treatment of boundaries, spectral variability, and the need to integrate multi-year imagery.
- Fen, Marsh and Swamp estimates differ dramatically between CS 2007 and LCM2007, largely due to the mosaic nature of Fen and the small patch sizes that complicate detection; this area may benefit from KBEs to reclassify some Fogams into Fen, Marsh and Swamp in future work.
- Overall, LCM2007 provides a coast-to-coast, parcel-based view that complements CS field surveys, offering a valuable evidence base for habitat monitoring and policy, albeit with acknowledged uncertainties in certain habitat classes.

## 4.5 Summary and discussion (high-level takeaways)
- Two complementary comparisons (BH-based CS squares vs LCM2007 and UK-wide CS 2007 estimates vs LCM2007) reveal different facets of agreement and discrepancy.
- Grassland remains the most challenging category due to the one-to-many relationship with Broad Habitats; BH Associations help contextualize correspondences beyond single-class matches.
- LCM2007 shows strong correspondence with CS for Arable and Horticulture at the 1 km square level, but UK-scale totals can diverge due to classification and boundary differences.
- Fen, Marsh and Swamp illustrates large divergence due to mosaic and patch-size issues; future work could leverage KBEs to reallocate areas more accurately.
- LCM2007 is positioned as a robust, reusable foundation for habitat monitoring, landscape planning, and biodiversity assessments, especially when used in conjunction with other data sources.

Appendix notes (high-level)
- The report emphasizes the value of parcel-level metadata and Knowledge-Based Enhancements (KBEs) for improving thematic resolution and enabling user-driven validation, acknowledging that no single dataset is a perfect truth and that “fit for purpose” should guide accuracy assessment.