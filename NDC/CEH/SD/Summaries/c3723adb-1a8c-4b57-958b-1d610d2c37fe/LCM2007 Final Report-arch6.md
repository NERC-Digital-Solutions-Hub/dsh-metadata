# Final Report for LCM2007 - the new UK land cover map

## 4.3.2 Similar area estimates
- Similar area estimates are defined as classes falling within the Countryside Survey (CS) upper and lower 95% confidence limits for the UK.
- Similar areas occur for: Broadleaved woodland, Acid Grassland, and Inland Rock.

## 4.3.2 Dissimilar area estimates
- Dissimilar area estimates are those falling beyond the CS 95% confidence limits for the UK.
- Dissimilar areas occur for: Arable and Horticulture, Improved Grassland, Neutral Grassland, Dwarf Shrub Heath, Bog, Montane Habitats, and coastal habitats.
- Key explanations for differences in Arable and Horticulture:
  - The CS and DEFRA 2007 figures differ in what is classified as Arable and Horticulture.
  - Spectral confusion and inclusion of Boundary and Linear Features in LCM2007’s Arable and Horticulture category.
  - LCM2007 requires imagery from several years; temporal range affects fields changing between temporary grassland and arable between dates, biasing spectral signatures toward arable when variability is high.
- Boundary and Linear Features:
  - CS maps many boundaries/linear features below the MMU; LCM2007 incorporates these into field polygons, increasing field sizes and shifting areas into Arable/Horticulture or Improved Grassland.
- Improved Grassland and Neutral Grassland:
  - LCM2007 reports about 10,000 km2 more Improved Grassland and 10,000 km2 less Neutral Grassland than CS; differences arise from how Neutral vs Improved grassland signatures appear spectrally and limited soil data utility for distinguishing them.
- Dwarf Shrub Heath and Bog:
  - Differences mainly due to how areas are allocated between habitats; Montane and coastal habitats are less well represented in CS.
- Fen, Marsh and Swamp:
  - Fen is a mosaic of land cover types; mapping differences arise because Fen areas in CS often map as Rough Grassland or Acid Grassland in LCM2007.
- Overall, CS patch size, spatial structure and methodological differences contribute substantially to observed dissimilarities.

## 4.3.3 Discussion
- CS estimates are derived by scaling CS 2007 field data (ITE Land Classes); sensitivity to how ITE classes are defined is under investigation.
- Prior CEH mappings (LCM2000) scaled to CS squares yielded results more similar to CS estimates than when using LCM2000 mapped areas.
- When comparing LCM2007 to CS 2007, grassland categories present notable challenges due to the one-to-many relationship between grass cover and Broad Habitats; Broad Habitat Association (BHA) rules were developed to improve correspondences.
- Fen, Marsh and Swamp estimates vary by an order of magnitude between CS and LCM2007 due to complexity and small patch sizes; this area may benefit from further KBEs to allocate parts of these mosaics more accurately.

## 4.4 UK Land Cover
- Summary: UK land cover shows more than 50% intensive land use (Arable and Horticulture plus Improved Grassland; together ~51%), with the remainder mainly semi-natural; woodlands cover about 12% (Broadleaved and Coniferous woodlands split evenly).
- Regional variation:
  - England: highest intensive land use (about 76%).
  - Northern Ireland and Wales: around 64% intensive.
  - Scotland: lowest intensive use (about 36%), but with the largest share of Coniferous Woodland.
- Scotland has substantial semi-natural areas (36% Mountain, Heath and Bog; 20% semi-natural grassland).
- England, Scotland, Wales differ in CS mapping practices and habitat composition, affecting comparability.
- LCM2007 builds on LCM2000 but shows shifts in Arable and semi-natural grassland proportions; changes relative to the older maps may reflect both real landscape change and differences in spatial frameworks and error characteristics.

## 4.4 UK Land Cover (Table 4.8/4.9 and related discussion)
- Broad Habitat-level comparisons show areas mapped by LCM2007 within CS 2007 bounds or outside them (with color coding on whether LCM2007 falls inside CS 95% limits).
- The UK-wide comparison indicates broad differences in several habitat classes, influenced by spectral interpretation, boundary mapping, and class definitions.

## 4.5 Summary and discussion
- The two CS–LCM comparisons reveal different perspectives: CS square-level comparisons and national Broad Habitat extent comparisons.
- Agreement between LCM2007 and CS varies widely by Broad Habitat; grassland remains problematic due to the one-to-many relationship with Broad Habitats.
- LCM2007 shows high correspondence with CS for the Arable and Horticulture area in 1 km CS squares, but overall Broad Habitat extents show larger Arable and Horticulture estimates by LCM2007.
- Fen, Marsh and Swamp estimates differ drastically between CS 2007 and LCM2007 due to mosaic complexity and patch size; future work could use additional datasets to create KBEs that reallocate some of these grassland/dark mosaics to Fen, Marsh and Swamp.

## 5.1 Example areas
- A series of example areas demonstrates LCM2007 performance across upland, calcareous, urban, and arable/fenland landscapes, including montane regions (Grampians), calcareous grasslands (Salisbury Plain), suburban London, and fen/riverine landscapes in East Anglia.

## 5.2 Vector and raster products
- Vector product:
  - Polygons with extensive metadata attached (area, source images, Broad Habitat, processing history, KBE history, ProbList, etc.).
  - Broad Habitat sub-classes (BHSub) provide additional detail but are not all validated with the same certainty as the main LCM2007 class.
- Raster products:
  - 25 m raster: 23 LCM2007 classes.
  - 1 km raster: two formats—percentage cover per class and dominant class per cell.
- Access and licensing:
  - 1 km rasters available via the CEH Information Gateway.
  - Full vector and 25 m rasters available on request under licence; fees may apply.

- Data formats and practical notes:
  - Vector data offer detailed attribution but larger file sizes; 25 m rasters provide similar thematic detail without polygon metadata.
  - The 1 km rasters are suitable for UK-wide modelling when combined with auxiliary data (e.g., meteorology, species distributions).

## Appendix 4: Bespoke validation
- There is no absolute truth in geography; the “quality” of a land cover product depends on its use and fit-for-purpose validity.
- LCM2007 provides parcel-level metadata: for each parcel, the history of KBEs applied and the top five spectral variants with probabilities prior to KBEs.
- A practical validation approach uses high-resolution imagery (e.g., Google Earth) to assess consistency with LCM2007 at a parcel level, applying a Bayesian-inspired, fuzzy confidence framework (plausible, probably, possibly).
- A Python-based tool supports this bespoke validation methodology, enabling location-specific accuracy appraisal for target classes.

## Appendix 5: Broad Habitat Association (BHA)
- Purpose: to justify the Broad Habitat Association rules used to improve thematic correspondences between LCM2007 and CS.
- Key rules and issues by habitat:
  - Bog: ecological continuum with Dwarf Shrub Heath, Acid Grassland, Montane Habitats; LCM2007 Class Bog is acceptable correspondence with CS classes Bog, Dwarf Shrub Heath, Acid Grassland.
  - Dwarf Shrub Heath: upland mosaics with Acid Grassland; LCM2007 Dwarf Shrub Heath can correspond with CS Acid Grassland and vice versa.
  - Montane Habitats: upland montane areas sometimes misclassified; Montane Habitats correspond to CS Dwarf Shrub Heath, Acid Grassland, and Bog at BH adjacency level; montane polygons above threshold not recorded as non-montane classes.
  - Built Up Areas and Gardens: urban areas may contain multiple cover types; correspondence accepted if CS label matches grassland, woodland, or water in LCM2007.
  - Fen, Marsh and Swamp: mosaic mosaics; non-reciprocal correspondences allowed when LCM2007 parcels include CS Fen, Marsh and Swamp components within mixed polygons.
  - Rough Grassland: often a mix of Improved Grassland and various grassland types; treated as containing contributions from multiple Grassland Broad Habitats; correspondence accepted with Improved Grassland, Acid Grassland, Neutral Grassland, Calcareous Grassland, or Fen, Marsh and Swamp.
  - Water classes and tidal areas: Water classes map to CS water classes; Saline and Freshwater definitions not always reciprocal due to tidal influences and coastal contexts.
- These rules aim to improve cross-product interpretability and provide a structured basis for comparing CS and LCM2007 outputs.

Note: This summary highlights the key points and conclusions from the provided excerpts, focusing on the comparison between LCM2007 and Countryside Survey results, the data products and access, validation approaches, and the Broad Habitat Association framework used to reconcile differences between datasets.