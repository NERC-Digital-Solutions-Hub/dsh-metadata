# Final Report for LCM2007 - the new UK land cover map

## Overview
- LCM2007 provides a parcel-based vector dataset (land parcels) with 23 LCM2007 classes mapped to 17 Broad Habitats (BHs), plus a 25 m raster and 1 km summary products.
- Outputs support habitat monitoring, biodiversity planning, landscape planning, and policy analysis; includes detailed processing provenance and knowledge-based enhancements (KBEs).
- Validation shows overall accuracy around 83% across the 23 LCM2007 classes; accuracy varies by class. Countryside Survey (CS) comparisons show variable agreement, with notable differences in grassland and fen/moist habitats.
- Change detection across map versions is complex due to evolving spatial and thematic frameworks; KBEs improve thematic resolution but can be disabled if needed.

## 4.3 Dissimilar area estimates
- Dissimilar area estimates (classes outside CS 95% confidence limits for the UK) occur for:
  - Arable and Horticulture
  - Improved Grassland
  - Neutral Grassland
  - Dwarf Shrub Heath
  - Bog
  - Montane Habitats
  - Coastal habitats
- Key factors driving differences:
  - Differences in what is classified as a given class between CS and LCM2007
  - Spectral confusion and high spectral variability within some classes (e.g., Arable and Horticulture)
  - Inclusion or treatment of Boundary and Linear Features by LCM2007 (often not present in CS maps)
  - Temporal differences requiring multi-year imagery, causing fields to flip between classes (temporary grass vs arable)
  - Differences in how certain habitats are allocated or split (e.g., Improved vs Neutral Grassland; Dwarf Shrub Heath vs Acid Grassland)
  - Fen, Marsh and Swamp are particularly challenging due to mosaics and small patch sizes; CS often records larger patches that LCM2007 may map to multiple classes
- Overall implication: dissimilar areas reflect both genuine land-cover change signals and methodological differences in data sources, temporal windows, and classification rules.

## 4.3 Discussion
- Agreement between LCM2007 and CS varies considerably across Broad Habitats.
- Grassland areas are especially problematic due to one-to-many relationships with BHs; Broad Habitat Association (BHA) rules were developed to improve interpretability.
- LCM2007 shows high correspondence with CS 1 km square estimates for Arable and Horticulture, but broad Habitat extents can be larger in LCM2007 than CS national estimates.
- Fen, Marsh and Swamp estimates differ by orders of magnitude; mosaics and small patch sizes contribute to this discrepancy.
- Future work could use additional data (e.g., KBEs) to better allocate mosaic habitats (e.g., Fen vs Rough Grassland) and refine cross-walks between CS and LCM2007.

## 4.4 UK Land Cover
- UK-wide distribution: more than 50% in intensive land use (Arable and Horticulture + Improved Grassland) or Built-up Areas and Gardens; about 12% in woodland; remaining areas are semi-natural (including coastal, semi-natural grassland, and montane habitats).
- Country-level patterns:
  - England: highest proportion of intensive land use (roughly 76%)
  - Scotland: large share of Coniferous Woodland; substantial semi-natural land in Mountain, Heath, and Bog
  - Northern Ireland and Wales: around 64% intensive land use
  - Scotland also has the largest extent of Coniferous Woodland and notable semi-natural grassland (and montane habitats)
- Comparison with LCM2000:
  - LCM2007 increased Arable area to about 26% and semi-natural grassland to about 13% (compared with 23% and 17% in LCM2000, respectively)
  - Coniferous woodland changes from 5.4% (LCM2000) to 6.1% (LCM2007)
  - Urban area coverage is slightly lower in LCM2007 (5.9%) than in LCM2000 (6.7%)
- Notes on CS comparison: LCM2007 estimates for some broad habitats fall outside CS 95% bounds; differences reflect methodological and spatial-structure differences, including CS’s field-based survey approach versus satellite-derived mapping.

## 4.5 Summary and discussion
- Two main comparisons with Countryside Survey (CS):
  - Comparison against CS mapped in 1 km squares shows varying agreement by Broad Habitat.
  - Comparison of CS national Broad Habitat estimates with LCM2007 estimates shows further differences; grassland remains a challenge due to BH-to-class mappings.
- Key takeaways:
  - LCM2007 aligns well with CS for certain classes (notably Arable and Horticulture in 1 km squares) but tends to estimate larger extents for some Broad Habitats overall.
  - Fen, Marsh and Swamp remain difficult due to mosaic nature and small patch sizes; potential improvements include additional KBEs to allocate certain grassland/fen patches more accurately.
  - The Broad Habitat Association framework improves interpretability and cross-walk with CS, but classification uncertainties persist, especially for grasslands.
- Implications for practice:
  - LCM2007 serves as a robust, coast-to-coast UK land-cover reference with substantial applicability to biodiversity planning, habitat monitoring, and environment-related policy, while acknowledging limitations in certain habitats and the complexities of change detection across historical maps.

## Practical implications for GIS specialists
- Data formats and access
  - 1 km raster data: available via the CEH Information Gateway (free in many cases).
  - Full vector and 25 m raster products: available on license from CEH.
  - Vector data includes rich metadata per parcel (spectral class, KBE history, processing provenance, etc.).
- Thematic resolution and KBEs
  - KBEs improve accuracy by using contextual rules but can be disabled to revert to the original spectral classifications.
  - The dataset supports downstream analyses such as habitat monitoring, connectivity analyses, and landscape planning.
- Change detection and temporal analysis
  - Cross-map change assessment is complex due to evolving spatial frameworks (LCM1990, LCM2000, LCM2007) and varying error rates.
  - Recommended approach: use aggregated or BH-level changes, or reorganize older CEH maps into a common spatial framework to enable more reliable change detection.
- Validation and QA
  - Ground reference validation used 9,127 points with overall accuracy around 83% (class-dependent). CS comparisons show variable correspondence; grasslands and fen/moist habitats require careful interpretation.
  - The parcel-level metadata enables users to assess the quality and plausibility of classifications at a local scale, potentially enabling field- or imagery-based validation.
- Outputs and formats
  - Vector (parcel-based polygons) with 23 LCM2007 classes, BH/Sub classifications, and extensive processing history (KBE history, ProbList, etc.).
  - 25 m raster (23 classes) and 1 km raster summaries (percent cover or dominant class).
  - Documentation and appendices provide detailed methodological context, KBEs, and crosswalk information for BH and CS alignment.

## Notes on access and usage
- The dataset is designed to support a wide range of applications, from national-scale modeling to local policy support, while providing a stable spatial framework for future monitoring and change detection.
- Users should refer to the accompanying methodological documentation, validation appendices, and Broad Habitat Association guidance when applying KBEs or performing cross-walk analyses with Countryside Survey data.