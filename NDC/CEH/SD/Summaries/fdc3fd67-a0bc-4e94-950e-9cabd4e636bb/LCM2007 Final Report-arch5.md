# Final Report for LCM2007 - the new UK land cover map

- Overview of comparisons
  - LCM2007 (UK-wide land cover map) is compared with Countryside Survey (CS) 2007 estimates to assess agreement and differences.
  - Similar area estimates occur for Broadleaved woodland, Acid Grassland, and Inland Rock (within CS 95% confidence limits).

- 4.3.2 Similar area estimates
  - Similar results fall within CS 95% confidence limits for:
    - Broadleaved woodland
    - Acid Grassland
    - Inland Rock

- 4.3.2 Dissimilar area estimates
  - Dissimilar results fall beyond CS 95% confidence limits for:
    - Arable and Horticulture
    - Improved Grassland
    - Neutral Grassland
    - Dwarf Shrub Heath
    - Bog
    - Montane Habitats
    - Coastal habitats

- 4.3.3 Key factors driving dissimilarities (illustrative examples)
  - Arable and Horticulture
    - CS UK area: 46,574 km2; DEFRA 2007: 46,090 km2; CS upper limit: 51,276 km2; LCM2007: 63,005 km2.
    - Differences due to: how each method defines Arable and Horticulture; spectral confusion; inclusion of Boundary and Linear Features in LCM2007.
    - DEFRA 2007 agricultural breakdown (arable, horticulture, temporary grass, uncropped land) partly aligns with LCM2007’s larger arable category; temporary grass and uncropped land may be absorbed into Arable/Horticulture in LCM2007.
    - Spectral variability of arable crops leads to misclassification risk and potential overestimation in some regions.
  - Boundary and Linear Features
    - CS maps boundaries/fields; LCM2007 often incorporates boundaries into fields due to MMU constraints, increasing field sizes and shifting areas among Arable/Horticulture vs Improved Grassland.
  - Improved Grassland vs Neutral Grassland
    - LCM2007 shows ~10,000 km2 more Improved Grassland and ~10,000 km2 less Neutral Grassland than CS.
    - Spectral similarity and field boundary decisions contribute to misassignment between these broad grassland types.
  - Dwarf Shrub Heath and Bog
    - Differences largely due to allocation between these habitats; spatial structure and boundary delineation influence whether a polygon is classified as Dwarf Shrub Heath, Bog, or Montane.
  - Montane and Coastal Habitats
    - CS representation is limited in upland/coastal areas; discrepancies with LCM2007 are expected due to CS’s under-sampling in these zones.
  - Fen, Marsh and Swamp
    - CS 2007 estimates differ by an order of magnitude from LCM2007; Fen areas are mosaic and often mapped as Rough Grassland or Acid Grassland by LCM2007; CS CS suggests Fen is a challenging category for spectral classification.
  - General notes
    - Patch size and spatial structure differences between CS parcels and LCM2007 polygons affect change interpretation.
    - LCM2007’s 0.5 ha MMU and thematic grouping influence area allocations, especially for small Fen parcels.

- 4.4 UK Land Cover
  - UK distribution highlights
    - More than 50% of the UK is intensive land use (Arable and Horticulture plus Improved Grassland) or Built-up areas (around 6%).
    - Woodlands cover about 12% (split roughly evenly between Broadleaved and Coniferous).
    - The remainder is semi-natural (coastal, semi-natural grassland, mountain, heath, bog).
  - Country-by-country variation
    - England: highest intensive land use (~76%: 40% Arable, 27% Improved Grassland, 9% Built-up).
    - Northern Ireland and Wales: ~64% intensive land use.
    - Scotland: ~36% intensive land use, with the largest share of Coniferous Woodland and substantial semi-natural mountain/heath areas.
  - Comparison with LCM2000
    - LCM2007 slightly increases Arable (26% vs 23% in LCM2000) and semi-natural grassland (13% vs 17% in LCM2000), with minor changes in coniferous woodland and urban fractions.
  - Aggregated class notes
    - CS 2007 and LCM2007 estimates differ depending on spatial scale (UK vs country level) and aggregation method; sensitivity analyses in progress for ITE Land Classes.

- 4.5 Summary and discussion
  - Agreement between LCM2007 and Countryside Survey varies by Broad Habitat type; grassland categories are particularly challenging due to one-to-many relationships with Broad Habitats.
  - LCM2007 shows high correspondence with CS 2007 area for Arable and Horticulture at 1 km square scale, but overall Broad Habitat extents are larger in LCM2007.
  - Fen, Marsh and Swamp shows large discrepancies due to complex mosaics and small patch sizes; future work could use KBEs to reallocate some grassland areas to Fen, Marsh and Swamp.
  - Grassland classification remains problematic; Broad Habitat Association rules provide a framework to assess correspondences across multiple thematic levels (BH, Aggregate, and BHA).
  - Practical implications for data governance
    - Users should consider differences in spatial structure, MMU, and class definitions when integrating LCM2007 with CS data.
    - Document provenance, classification history, and crosswalks between LCM2007 and CS for robust change detection.
    Licensing and access
    - 1 km raster data available via CEH Information Gateway; full vector and 25 m rasters available on request with potential fees.
  - The study highlights that LCM2007 provides a coast-to-coast UK-wide baseline for habitat monitoring and policy-support, but careful interpretation is required when comparing to field-survey based datasets like Countryside Survey.

- Data governance implications for Data Stewards
  - Ensure clear documentation of spatial frameworks (MMU, MFW), class definitions, and knowledge-based enhancements used in LCM2007.
  - Track and report differences between LCM2007 and CS outcomes, including how boundary features, temporal image ranges, and spectral variability affect classifications.
  - Maintain data provenance and update pathways for future changes, using Broad Habitat Association rules to interpret cross-dataset correspondences.
  - Manage licensing terms and access provisions, with explicit notes on which products (1 km rasters, 25 m vector, etc.) are publicly available vs. restricted.