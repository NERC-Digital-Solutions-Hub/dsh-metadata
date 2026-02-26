# Final Report for LCM2007 - the new UK land cover map

## Overview
- LCM2007 provides coast-to-coast UK land cover mapped as parcels within a parcel-based vector framework, aligned with Broad Habitats, and supported by Countryside Survey (CS) 2007 comparisons.
- Key aim: enable policy-relevant habitat monitoring and change detection, with validated comparisons to field survey data and national estimates.

## Comparison with Countryside Survey 2007
- Two main comparative analyses:
  - Comparison against CS 2007 field-squares and Broad Habitats (BH) and Broad Habitat Associations (BHA).
  - Comparison of CS 2007 national estimates with LCM2007 by UK-wide totals.
- Very similar area estimates (CS 95% bounds overlap for all countries) observed for:
  - Coniferous Woodland
  - Freshwater
  - Built-up Areas and Gardens
  - Calcareous Grassland
- Similar area estimates (within UK 95% bounds) observed for:
  - Broadleaved woodland
  - Acid Grassland
  - Inland Rock
- Dissimilar area estimates (outside UK 95% bounds) observed for:
  - Arable and Horticulture
  - Improved Grassland
  - Neutral Grassland
  - Dwarf Shrub Heath
  - Bog
  - Montane Habitats
  - Coastal habitats
  - Fen, Marsh and Swamp
- Causes of differences discussed:
  - Differences in what CS and LCM2007 classify as in Arable/Horticulture and grassland categories
  - Spectral confusion and the need to aggregate multiple crops and growth stages
  - MMU-related differences and how boundaries/linear features are treated
  - Spatial structure differences and how patch size affects classification and comparison
  - Underrepresentation of certain habitat mosaics (e.g., Fen) in spectral data and the role of ground-based validation

## Notable numerical findings
- Overall accuracy: 83% (based on 9,127 ground reference points).
- BH correspondence (CS vs LCM2007): 62% UK-wide.
- BHA correspondence (CS vs LCM2007): 76% UK-wide.
- Grassland resolution improvements observed when consolidating grassland classes (roughly 87–90% correspondence in some CS–LCM2007 comparisons).
- Fen, Marsh and Swamp estimates show large UK-scale discrepancies (CS ~4,392 km² vs LCM2007 ~101 km²) due to the mosaic nature of fen and small patch sizes; many CS fen areas are mapped as Rough Grassland or Acid Grassland by LCM2007.
- Arable and Horticulture area estimates differ markedly (CS ~46,574 km² vs LCM2007 ~63,005 km²); contributing factors include classification boundaries, spectral variability of crops, and inclusion of boundaries/linear features in LCM2007’s arable/horticulture class.

## UK Land Cover distribution (LCM2007 vs CS 2007)
- UK-wide: more than 50% of land in intensive use (Arable and Horticulture plus Improved Grassland) and Built-up Areas and Gardens (~6%); woodlands ~12%; remainder semi-natural (coastal, semi-natural grassland, mountain, etc.).
- Country variation:
  - England: highest intensive land use (~76% total: 40% Arable/Horticulture, 27% Improved Grassland, 9% Built-up Areas and Gardens).
  - Scotland: largest Coniferous Woodland share; lower overall intensive land use (~36%); higher semi-natural areas (e.g., 36% Mountain, heath and bog).
  - Northern Ireland and Wales: intermediate levels of intensive land use (~64%).
- Comparison with LCM2000 shows some shifts in Arable and Grassland proportions; spatial framework changes contribute to differences, with exact interpretation needing further analysis.

## Discussion and implications
- LCM2007 represents a major step forward in UK land cover mapping by using national cartography-based spatial frameworks, multi-date imagery, and knowledge-based enhancements to create a coherent UK-wide parcel-based dataset aligned with Broad Habitats.
- Strengths:
  - Strong spatial integration with MasterMap/Large-scale Vector frameworks improves delineation, change detection potential, and cross-product compatibility.
  - Ground-truth validation and CS comparisons provide robust quality assurance context.
- Limitations:
  - Certain habitat classes (notably various grasslands, bog, montane and fen-related classes, and coastal mosaics) show variability in accuracy due to spectral limitations and real-world land-use mosaics.
  - Differences between CS field parcels and LCM2007 parcel geometry affect direct comparisons, especially for small or transitional habitats.
- Conclusions:
  - LCM2007 offers a robust UK-wide land cover resource with strong policy-relevant potential (biodiversity assessment, habitat connectivity, landscape planning, and change monitoring).
  - Discrepancies with CS highlight the need for integrated datasets and continued development of knowledge-based enhancements (KBEs) and improved handling of mosaics and transitional habitats.

## Data products and access
- 1 km raster data available via the CEH Information Gateway.
- Full vector and 25 m raster products available on request under licence from CEH; licensing terms may apply.
- The parcel-level metadata (KBE history, probability lists) enables user-driven validation and uncertainty assessment.

## Overall takeaway for data-driven analysis
- The LCM2007 dataset provides a high-resolution, parcel-based template aligned with national frameworks, enabling robust spatial analyses, change detection, and cross-country comparisons.
- When used with CS data and additional datasets (habitat associations, spectral nuances, and ground-truthing), it supports nuanced interpretation of habitat extent and change, while acknowledging areas where spectral or structural differences may lead to disagreements with field-based surveys.