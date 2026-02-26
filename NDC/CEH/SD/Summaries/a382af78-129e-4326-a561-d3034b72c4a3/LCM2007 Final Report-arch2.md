# Final Report for LCM2007 - the new UK Land Cover Map

- Purpose and scope
  - Presents the UK’s first continuous parcel-based land cover map (LCM2007), derived from multi-temporal satellite imagery and aligned to national cartography.
  - Maps 23 land cover classes that aggregate to Broad Habitats (17 in total), focusing on land cover rather than land use.
  - Covers the entire UK (GB and Northern Ireland) with a common methodology; data structured for change detection, habitat monitoring, and policy support.

- Dissimilar area estimates (4.3.2)
  - Dissimilar results (beyond Countryside Survey 95% confidence limits) occur for:
    - Arable and Horticulture
    - Improved Grassland
    - Neutral Grassland
    - Dwarf Shrub Heath
    - Bog
    - Montane Habitats
    - Coastal habitats
  - Key causes for Arable and Horticulture discrepancies:
    - Differences in what is classified as Arable/Horticulture
    - Spectral confusion and inclusion of boundary/linear features in LCM2007
    - Temporal mismatch: LCM images span several years, increasing field changes (e.g., temporary grass to arable)
  - Grassland discrepancies (Improved vs Neutral):
    - Spectral similarity and soil data limitations hinder reliable separation; spectral/soil signals may misassign Neutral vs Improved grassland
  - Dwarf Shrub Heath and Bog:
    - Allocation between adjacent habitats; spectral signatures and厚montane classifications complicate separation
  - Fen, Marsh and Swamp:
    - Large discrepancies; CS tends to map as Rough Grassland or Acid Grassland in many cases; Fen areas are mosaic and often below LCM’s minimum mapping unit (MMU), leading to underrepresentation in LCM2007
  - General observation:
    - CS patch size and spatial structure influence how CS areas appear in LCM, highlighting scale effects and the difficulty of direct one-to-one comparisons.

- Discussion (4.3.3)
  - CS estimates are derived by scaling field observations; sensitivity to how land classes are defined and scaled is under investigation.
  - When LCM2000 areas are re-scaled to CS schemes, results resemble CS estimates more closely than direct LCM2000 comparisons, indicating methodological alignment matters.
  - Patch-size effects and the MMU influence how mosaic landscapes are represented; understanding patch-size distributions could improve comparisons between LCM and CS.

- UK Land Cover distribution and country variation (4.4)
  - UK-wide: over half of land is either Arable/Horticulture or Improved Grassland; woodland accounts for about 12% (Broadleaved and Coniferous, split). Semi-natural areas and water features fill the remainder.
  - Country patterns:
    - England: most intensive land use (about 64–76% when combining major intensive classes)
    - Scotland: lowest intensive land use, large semi-natural areas (Montane habitats, semi-natural grasslands)
    - Wales and Northern Ireland show intermediate patterns with regional variations in grasslands and woodlands
  - Comparison with LCM2000 indicates shifts in arable and grassland proportions and small changes in woodland and urban areas; the spatial framework change makes direct interpretation complex.

- Summary and discussion (4.5)
  - Agreement between LCM2007 and CS varies by Broad Habitat; grassland categories are especially challenging due to one-to-many relationships with Broad Habitats.
  - Broad Habitat Association (BHA) rules were developed to improve correspondence across mapping schemes, adding a third thematic accuracy level.
  - LCM2007 shows high correspondence with CS 2007 for the 1 km Arable/Horticulture area, but broad habitat extents can diverge due to classification/structure differences.
  - Fen, Marsh and Swamp estimates differ by an order of magnitude; many Fen areas in CS map as Rough Grassland or Acid Grassland in LCM2007. KBEs (Knowledge-Based Enhancements) could help reallocate certain grassland areas to Fen, Marsh and Swamp in future work.
  - Overall, LCM2007 and CS are complementary, with potential for integrated use alongside other data sources to strengthen environmental indicators and monitoring.

- Example areas (5.1)
  - A set of geographic exemplars (upland, calcareous areas, urban, and fenland) illustrate LCM2007’s performance across habitat types and landscape contexts.

- Data products and formats (5.2)
  - Vector product: land parcels with extensive metadata, including area, source images, Broad Habitat (BH), Broad Habitat Sub-class (BHSub), FieldCode, KBE history, ProbList, CorePixels, and construction history.
  - Raster products:
    - 25 m raster with 23 LCM2007 classes
    - 1 km raster summaries (two options per location):
      - Percentage cover by each class
      - Dominant class per pixel
  - Minimum mapping unit (MMU) = 0.5 ha; Minimum feature width (MFW) = 20 m
  - Access:
    - 1 km raster data via the CEH Information Gateway
    - Full vector and 25 m raster data licensed on request from CEH (fees may apply)

- Change mapping, interpretation and change management
  - LCM2007 enables multi-tier habitat monitoring and landscape planning but, due to methodological differences with CS and earlier LCMs, robust change detection requires careful handling of error sources and boundaries.
  - Aggregated class trajectories and focusing on consistently mapped classes can help mitigate interpretation challenges in change detection.

- QA, validation, and accuracy
  - Validation against ground references (9127 points in related sections) yielded high-level accuracy, with class-level variation; overall validation results indicate strong but uneven performance across habitat types.
  - Producer’s vs User’s accuracy per class documented, highlighting that certain habitats (e.g., specific grassland and montane classes) are more challenging than others (e.g., bogs, coniferous woodland).

- Data sources, context and European links
  - LCM2007 builds on Landsat, SPOT and IRS sensors; integrates national cartography (OS MasterMap, LPS Vector), soils and terrain data; linked to Countryside Survey and biodiversity/broad habitat frameworks.
  - European alignment:
    - UK component of Corine Land Cover 2006 (via generalisation and transformation of LCM2007 vector data)
    - Connection to IMAGE2006 for pan-European consistency and cross-border comparability

- Practical implications and applications for analysts
  - Provides a coast-to-coast UK dataset suitable for biodiversity assessments, habitat connectivity studies, ecosystem service analyses, and land management planning.
  - Serves as a consistent national frame of reference for cross-country comparisons and policy evaluation (e.g., Natura targets, woodland expansion planning).
  - Encourages integrated use with in situ surveys, higher-resolution habitat mapping, LiDAR data, and climate/soil datasets to generate robust environmental indicators.

- Accessibility and usage notes
  - The 1 km raster is publicly accessible via CEH Gateway; full vector and 25 m raster require licensing and an application.
  Important: change detection and interpretation should account for the MMU, boundary differences, and the distinct spatial structures of LCM2007 versus CS and earlier CEH maps.