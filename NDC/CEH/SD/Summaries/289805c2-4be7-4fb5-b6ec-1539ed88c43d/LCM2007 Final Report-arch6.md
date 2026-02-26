# Final Report for LCM2007 - the new UK land cover map

- Overview
  - First continuous parcel-based UK land cover map (LCM2007) aligned with Broad Habitats (BH) and Broad Habitat Associations (BHA).
  - Provides coast-to-coast UK coverage with a transparent processing chain and rich metadata.
  - Aims to support habitat monitoring, biodiversity assessments, ecosystem services, landscape planning, and policy evaluation.

- Data sources and spatial framework
  - Satellite data: Landsat-5 TM/ETM+, SPOT-4/5, Landsat-7 ETM+ (for hole filling); sensors include LISS-III and AWIFS.
  - Composites: 34 multi-date composites (summer+winter), 37 composites, 21 single-date images; target year 2007.
  - Ground truth and ancillary data: CEH field references, Countryside Survey (CS) Broad Habitat data, OS MasterMap topography (GB), LPS (NI), soils, DEM ( NEXTMap Britain/NI), urban boundaries, and coastal data.
  - Spatial framework: Great Britain built on OS MasterMap with agricultural boundaries; Northern Ireland on LPS with similar integration; resulting UK-wide vector framework comprises >100 million real-world polygon objects after generalisation.
  - Segmentation and generalisation: image segments merged with cartographic boundaries; MMU 0.5 ha (minimum feature width 20 m); smaller segments dissolved into the surrounding most-similar polygon.

- Product specification and outputs
  - Classification: 23 LCM2007 land cover classes mapped to 17 BH (Broad Habitats); product is land cover (not land use) with a MMU of 0.5 ha.
  - Data products:
    - Vector: 10 polygon-level processing attributes plus full metadata; includes KBE history and ProbList for top class probabilities.
    - Raster: 25 m resolution with 23 classes.
    - 1 km rasters: two formats per pixel (percentage cover per class and dominant class).
  - Access and licensing:
    - 1 km rasters available via the CEH Information Gateway.
    - Full vector and 25 m rasters available on request under licence; fees may apply.

- Image processing, segmentation and classification workflow
  - Pre-processing: cloud/mask, atmospheric correction (FLAASH/MODTRAN), georeferencing (RMSE < 0.3 px), and topographic correction.
  - Segmentation and integration: segmentation using winter NIR, summer red, and summer MIR bands; integrated with OSMM generalised boundaries and agricultural boundaries.
  - Classification: parcel-based supervised maximum likelihood classification on 37 composites and 21 single-date images; training from ground references; iterative reclassification to target accuracy; ProbList captures top five class probabilities.
  - Manual edits and hole-filling: targeted edits for rare/winter cases; Landsat-7 ETM+ used for limited hole-filling.
  - Knowledge-based enhancements (KBEs): seven automated KBEs applied sequentially to reclassify parcels based on context (urban, terrain, soils, coastal proximity, etc.); improved thematic resolution and reduced spectral confusion; auditable trail of KBEs with some option to disable KBEs to reveal underlying spectral results.
  - KBEs details: core contextual data include urban, coastal, terrain, and soil information; soil data derived from NSRI Soilscapes and regional datasets; altitude/terrain corrections used for Montane Habitat classification.

- Change mapping and scientific use
  - Change mapping across LCM1990, LCM2000, and LCM2007 is complex due to differing spatial structures and class definitions; practical change detection remains challenging.
  - LCM2007 supports habitat monitoring and policy evaluation rather than precise change detection alone.
  - Emphasis on using aggregated/BH and BHA-level comparisons to improve interpretation across maps with differing conventions.

- Validation and accuracy
  - Field validation: 9,127 ground reference points; overall LCM2007 accuracy about 83%, with class-level accuracy varying by habitat type.
  - Lawn of performance: high user/producer accuracies for some classes (e.g., Bog, Arable, Coniferous Woodland); lower accuracies for Neutral Grassland, Calcareous Grassland, Montane Habitats due to spectral confusion and data limitations.
  - Countryside Survey (CS) 2007 comparison:
    - 591 CS squares evaluated.
    - Initial agreements: ~62% at BH level, ~67% at Aggregate level, ~76% at BH Association (BHA) level.
    - Grassland aggregation (combining grassland types) improved correspondence to ~87–90% in some cases.
    - Scotland showed lower BH-level correspondence but higher BHA-level correspondence due to habitat distribution and resolution differences.
  - 4.3.2 Similar and dissimilar area estimates (UK-wide):
    - Similar: Broadleaved woodland, Acid Grassland, Inland Rock.
    - Dissimilar: Arable and Horticulture, Improved Grassland, Neutral Grassland, Dwarf Shrub Heath, Bog, Montane Habitats, coastal habitats.
    - Key drivers of discrepancies include: differences in class definitions and boundaries, spectral confusion especially for Arable and Horticulture, inclusion of Boundary/Linear Features by LCM, MMU differences, and temporal variation across multi-year image sets.
  - Fen, Marsh and Swamp: CS vs LCM2007 show large disparity due to mosaic nature and small patch sizes; much CS-delineated Fen may map as Rough Grassland or Acid Grassland in LCM2007.

- Knowledge-based association and reconciliation (Broad Habitat Association)
  - Broad Habitat Association (BHA) rules developed to improve correspondence between LCM2007 and CS at BH, BH level, and higher levels.
  - Reciprocal and non-reciprocal mapping rules address edge cases such as Bog–Dwarf Shrub Heath–Acid Grassland continuums, Montane vs. other upland habitats, and coastal/water interactions.
  - Rules account for measurement differences (e.g., CS vs LCM MMU) and spectral ambiguities, guiding more robust cross-product comparisons.

- Practical usage, data governance and ecosystem applications
  - LCM2007 provides a robust UK-wide land cover framework with detailed metadata and a transparent lineage (KBE history, ProbList, etc.).
  - The 25 m and 1 km rasters, along with vector parcels, support a broad range of applications in biodiversity, habitat monitoring, landscape planning, ecosystem service assessment, carbon accounting, and policy evaluation when integrated with other datasets.
  - Licensing and access facilitate use in habitat monitoring and policy analysis; spatial data can be combined with climate, hydrology, soil, and biodiversity datasets for multi-disciplinary studies.

- Summary and implications
  - LCM2007 delivers a high-quality, continuous, UK-wide land cover product with robust spatial and thematic accuracy, supported by a transparent processing chain and rich metadata.
  - The integration of cartographic spatial frameworks, image segmentation, KBEs, and multi-source data enhances both spatial and thematic accuracy, enabling self-service use and policy-relevant analyses.
  - While overall accuracy is strong (83%), certain habitat classes—especially various grassland types, fen/marsh, bog, and montane habitats—remain challenging due to spectral variability and data limitations.
  - The product suite (vector, 25 m raster, 1 km summaries) supports a wide range of environmental policy and planning applications, with pathways for future improvements via additional data sources and refined KBEs.