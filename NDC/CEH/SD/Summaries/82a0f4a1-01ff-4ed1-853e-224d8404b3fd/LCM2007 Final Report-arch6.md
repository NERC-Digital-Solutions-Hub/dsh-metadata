# Final Report for LCM2007 - the new UK land cover map

## Overview
- Comparison between LCM2007 (UK land cover map) and Countryside Survey 2007 (CS 2007) reveals variable agreement across Broad Habitats.
- Grassland-related classes are especially problematic due to one-to-many relationships between observed land cover and Broad Habitat categories.
- LCM2007 provides coast-to-coast UK coverage with a parcel-based vector framework and derived raster products, enabling national-scale habitat monitoring and change detection, but differences with CS arise from methodology, spatial structure, and classification rules.

## 4.3.2 Similar area estimates
- Similar area estimates (within CS 2007 UK 95% confidence limits) occur for:
  - Broadleaved woodland
  - Acid Grassland
  - Inland Rock

## 4.3.2 Dissimilar area estimates
- Dissimilar area estimates (beyond CS 95% limits) occur for:
  - Arable and Horticulture
  - Improved Grassland
  - Neutral Grassland
  - Dwarf Shrub Heath
  - Bog
  - Montane Habitats
  - Coastal habitats

## Key drivers of differences
- Classification definitions and temporal range
  - CS and LCM2007 use different definitions and spatial structures; CS is based on field surveys across 591 1km squares with extrapolation, while LCM2007 uses a parcel-based vector framework tied to generalised cartography.
- Spectral vs. field-based distinctions
  - Grassland types exhibit high spectral similarity, leading to misassignment between Improved, Neutral, Calcareous, and Acid Grasslands.
- Boundary and linear features
  - CS maps many boundaries and linear features below the LCM MMU; LCM2007 tends to dissolve/merge these into adjacent fields, increasing apparent field size and altering Arable/Improved Grassland extents.
- Arable and Horticulture classification
  - LCM2007’s Arable and Horticulture area is larger than CS 2007 upper limit, partly due to inclusion of boundaries/linear features and spectral variability across multi-year image composites.
  - Spectral variability of crops and varying growth stages across years complicate robust classification.
- Boundary effects and MMU
  - MMU (0.5 ha) effects and how boundaries are treated lead to systematic differences in several classes, especially Arable, Horticulture, and Grassland categories.
- Special cases (Fen, Marsh and Swamp)
  - Fen is a mosaic of land cover; many Fen areas in CS 2007 map to Rough Grassland or Acid Grassland in LCM2007, causing large inter-product discrepancies.
- Montane and coastal representations
  - CS under-represents Montane and coastal habitats; LCM2007’s montane delineation (based partly on altitude and KBEs) can differ from CS, contributing to discrepancies in these classes.

## 4.4 UK Land Cover (summary context)
- LCM2007 indicates more than 50% of the UK is in intensive land use (Arable and Horticulture plus Improved Grassland) or Built-up Areas.
- Scotland shows a larger share of Coniferous Woodland and upland semi-natural habitats; England shows high intensification in arable and urban areas; Wales and Northern Ireland show different distributions reflecting regional land-use patterns.
- Compared with LCM2000, LCM2007 emphasizes changes in Arable and Horticulture, semi-natural grasslands, Coniferous Woodland, and urban areas, though interpretation is complicated by differing spatial structures.

## 4.5 Summary and discussion
- LCM2007 delivers the first continuous parcel-based UK land cover map, with vector (parcel) data and derived 25 m and 1 km raster products.
- Improvements and ongoing challenges
  - Strengths: integration with detailed national cartography (OS MasterMap, LPS), coherent spatial framework, potential for robust change detection, wide applicability to policy and planning.
  - Challenges: substantial differences with CS for several habitats (notably grasslands and fen), spectral confusion, MMU limitations, and the complexity of comparing across products with different spatial structures.
- Change detection
  - Complex due to differing spatial structures; robust change detection requires re-organising earlier CEH maps into a common spatial framework based on real-world land-use units.
  The recommended path is to use aggregated classes, focus on consistently mapped classes, or apply trajectory-based statistical approaches.
- Data usage and access
  - 1 km rasters publicly available via the CEH Information Gateway.
  - Full vector and 25 m rasters available under licence on request from CEH.
  - Outputs support habitat monitoring, biodiversity policy, landscape planning, ecosystem services analysis, and catchment management.

## Practical implications for Data Support
- When using LCM2007 data, be mindful of:
  - Differences in spatial structure and temporal ranges vs Countryside Survey data.
  - The MMU and the treatment of Boundaries and Linear Features, which can inflate or deflate certain class extents.
  - The known spectral confusion among grassland types and mosaic habitats (Fen, Marsh and Swamp).
- For end-users and decision-makers:
  - Use LCM2007 as a UK-wide, coast-to-coast baseline for Broad Habitats, with explicit caveats on grassland and fen classifications.
  - Combine LCM2007 with CS and other data sources (soil, topography, urban boundaries) for enhanced interpretation and validation.
  - Leverage the parcel-level metadata and knowledge-based enhancements to assess classification plausibility in local contexts (e.g., high-probability vs. moderate-probability classifications).
- Data integration guidance:
  - Consider recoding or aggregating classes to better align with CS categories when comparing outputs.
  - Use the 1 km raster products for broad-scale modelling and multi-dataset analyses; use 25 m rasters or vector data for finer-scale habitat mapping and change detection, with attention to MMU-related limitations.

## Access pointers
- CEH Information Gateway for 1 km rasters.
- CEH data access portal for full vector and 25 m raster products (licensing and fees may apply).
- The LCM2007 outputs are intended to support policy-relevant environmental analyses, including biodiversity assessment, habitat connectivity, and ecosystem services evaluation.