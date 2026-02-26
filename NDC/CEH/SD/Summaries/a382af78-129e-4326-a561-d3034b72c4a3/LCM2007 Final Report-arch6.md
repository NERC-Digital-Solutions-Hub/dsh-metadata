# Final Report for LCM2007 - the new UK land cover map

- Overview of the section
  - Presents a detailed comparison between LCM2007 outputs and Countryside Survey (CS) 2007 results, focusing on similarity and dissimilarity in area estimates, and discussing reasons for differences.
  - Explores change-mapping considerations and implications for policy-relevant interpretation.
  - Provides UK-wide and country-level summaries of broad habitat extents and their agreement with CS.

## 4.3 Similar area estimates and 4.3.2 Dissimilar area estimates

- Similar area estimates (within CS 95% confidence limits for the UK)
  - Broadleaved woodland
  - Acid Grassland
  - Inland Rock

- Dissimilar area estimates (beyond CS 95% confidence limits for the UK)
  - Arable and Horticulture
  - Improved Grassland
  - Neutral Grassland
  - Dwarf Shrub Heath
  - Bog
  - Montane Habitats
  - Coastal habitats

- Examples and interpretation
  - Arable and Horticulture: CS UK estimate ~46,574 km2; DEFRA 2007 ~46,090 km2; CS upper limit ~51,276 km2. LCM2007 estimates ~63,005 km2, suggesting inclusion of boundary/linear features and seasonal/temporal dynamics in LCM2007, as well as spectral variability and method differences.
  - Differences in classification boundaries and what counts as Arable/Horticulture between CS and LCM2007 contribute to overestimation by LCM2007 in some areas.
  - Boundary and Linear Features: CS maps more boundaries; LCM2007 often incorporates these into field polygons, inflating Arable/Improved Grassland areas.
  - Improved Grassland vs Neutral Grassland: LCM2007 tends to estimate more Improved Grassland and less Neutral Grassland than CS. Discrepancies relate to spectral signatures and limited use of soil data to distinguish grassland types.
  - Dwarf Shrub Heath, Bog: Differences largely due to reallocation between these habitats; CS and LCM2007 show similar combined extents but differ in allocation to individual classes.
  - Montane Habitats: CS underrepresents montane zones; LCM2007 relies on altitude and spectral detection plus KBEs, causing mismatches in upland areas.
  - Fen, Marsh and Swamp: CS UK estimate differs by an order of magnitude from LCM2007; mosaics and small patches and spectral ambiguity frequently cause misclassification (often mapped as Rough Grassland or Acid Grassland by LCM2007).

## 4.3.3 Discussion

- Methodological differences drive discrepancies
  - CS uses field surveys and scaling to national estimates; LCM2007 uses satellite imagery and a generalised spatial framework with KBEs.
  - Differences in MMU/MFU and polygon structure affect how habitats are delineated and classified.
- Scaling and data processing considerations
  - CS scaling procedures can influence UK totals; prior work shows scaling CS to UK estimates can align more closely with satellite-derived results.
  - The series of LCM maps (1990, 2000, 2007) differ conceptually and spatially; integrating them requires careful handling of class definitions and spatial structure.
- Patch size and spatial structure
  - Patch size distribution in CS parcels below LCM2007 MMU can significantly affect habitat area estimates, particularly for Fens and small habitat fragments.
- KBEs and habitat associations
  - Broad Habitat Association rules and KBEs help explain some correspondences, especially for complex mosaics (e.g., Fen/Grassland transitions, Montane adjustments).
- Change detection implications
  - Given the complex spatial and thematic differences, robust real-change detection is challenging; aggregation by habitat groups and trajectory-focused methods are suggested approaches.

## 4.4 UK Land Cover

- UK-wide distribution highlights
  - More than 50% of the UK is in intensive land use (Arable and Horticulture plus Improved Grassland) or Built-up Areas and Gardens (about 6%), with the remainder semi-natural.
  - Woodlands account for about 12% (roughly split between Broadleaved and Coniferous).
  - The remaining ~30% comprises Coastal, Semi-natural Grassland, Mountain, Heath and Bog.
- Country-level differences
  - England: highest intensive land-use proportion (about 76%: ~40% Arable and ~27% Improved Grassland; 9% Built-up).
  - Scotland: lowest intensive land-use share (about 36%), but highest Coniferous Woodland proportion.
  - Northern Ireland and Wales: intermediate levels, with notable wooded and grassland components.
- Comparison with LCM2000
  - LCM2007 increases Arable area to about 26% (vs 23% in LCM2000) and Semi-natural Grassland to about 13% (vs 17% in LCM2000); Coniferous Woodland slightly increases from 5.4% to 6.1%.
  - The spatial framework changes introduce interpretive challenges in direct rowspan comparisons with LCM2000.
- CS 2007 vs LCM2007 comparisons (highlights)
  - LCM2007 generally aligns with CS2007 in some broad habitat extents, but varies across habitats due to definitions, spatial structure, and MMU differences.
  - Fen, Marsh and Swamp shows particularly large discrepancies, reflecting the complexity of mosaics and how each dataset handles small, patchy features.
- Note on data presentation
  - The document presents extensive table-based comparisons (CS 2007 vs LCM2007) across Broad Habitats and 95% limits, illustrating where LCM2007 falls within or outside CS confidence intervals at national and country levels.

## 4.5 Summary and discussion

- Key conclusions from the comparison
  - Agreement between LCM2007 and CS varies widely across Broad Habitats.
  - Grassland classifications are particularly challenging due to one-to-many relationships between observed land cover and habitat categories; Broad Habitat Association rules were developed to improve interpretability.
  - LCM2007 shows strong correspondence with CS 1 km-square data for Arable and Horticulture, but total extent estimates for Arable and Horticulture can be higher in LCM2007 due to boundary features and multi-year imagery.
  - Fen, Marsh and Swamp exhibits substantial discrepancy, driven by mosaic nature and small patch sizes; some CS mappings of Fen are allocated to Rough Grassland or other grassland types in LCM2007.
- Implications for data use and interpretation
  - Users should consider class definitions, spatial structure differences, and potential spectral confusions when comparing LCM2007 with CS or other data sources.
  - KBEs and Broad Habitat Association rules can improve cross-dataset correspondences and support policy-relevant analyses.
  - For change detection, changes should be interpreted cautiously; aggregating to more robust, consistently mapped classes or focusing on change trajectories may yield more reliable insights.
- Overall relevance to data support
  - Demonstrates real-world cross-dataset validation and the importance of explicit class correspondences and context-based rules in enabling data to inform policy and planning.
  - Highlights how end-to-end data products (from satellite imagery to KBEs and validated extents) can be used to support environmental monitoring, while acknowledging limitations and the need for careful interpretation.