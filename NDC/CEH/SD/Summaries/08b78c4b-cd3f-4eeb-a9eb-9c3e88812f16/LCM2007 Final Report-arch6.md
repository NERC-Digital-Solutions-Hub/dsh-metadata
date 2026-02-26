# Final Report for LCM2007 - the new UK land cover map

## Overview of the project
- The UK’s first continuous parcel-based land cover map (LCM2007), aligning land cover to Broad Habitats for biodiversity planning.
- Outputs include 23 land cover classes mapped to 17 Broad Habitats, with about 10 million land parcels across GB and NI.
- Uses multi-date satellite imagery combined with a cartographic spatial framework to deliver a change-aware national product.

## Data products and formats
- Vector product: parcel polygons with 10+ attributes documenting processing history, class, and provenance (e.g., Construct, ProbList, KBE history).
- Raster products:
  - 25 m resolution: 23 LCM2007 classes.
  - 1 km resolution: two formats per pixel:
    - Percent cover for each LCM2007 class.
    - Dominant LCM2007 class for each location.
- Metadata and provenance are extensive, enabling traceability and reproducibility.
- Access:
  - 1 km rasters via CEH Information Gateway.
  - Full vector and 25 m data on request under licence from CEH (licensing may apply).

## Data sources and spatial frameworks
- Satellite data: Landsat TM/ETM+, SPOT-4/5, IRS AWIFS/LISS-III; majority mapped from multi-date composites with cloud masking and atmospheric/topographic corrections.
- Additional spatial data: OS MasterMap GB, LPS NI, agricultural boundaries, urban areas, soils, digital elevation, and Scotland’s LCS88; coastal context data.
- Spatial frameworks:
  - Great Britain: cartography-based objects (generalised OSMM+ag boundaries) with MMU of 0.5 ha.
  - Northern Ireland: NI Large-scale Vector boundary framework, integrated with imagery.
- The framework provides reusable, change-aware objects suitable for nationwide mapping.

## Processing workflow
- Pre-processing: cloud/shadow masking, atmospheric correction (FLAASH/MODTRAN), georeferencing, topographic correction, multi-date composites.
- Image segmentation: segmentation of ~60 composite images into land parcels; NI uses additional single-date segments to boost coverage.
- Classification: parcel-based supervised maximum likelihood classification using ground reference points (9127 validation points for accuracy assessment); iterative training refinement and manual edits for rare/topographic issues.
- Knowledge-based enhancements (KBEs): seven automated rules using context and ancillary data (terrain, soils, urban proximity, etc.) to resolve spectral confusion and improve thematic resolution; applied sequentially to ~20% of parcels.
- Post-classification handling: hole-filling with Landsat ETM+ where needed; metadata includes details of all KBEs applied and options to revert KBEs if required.

## Quality assurance, validation, and key findings
- Ground reference validation: 9127 points; UK-wide overall accuracy of 83% for LCM2007 classes.
- Per-class accuracy varies; NB: class-specific producer and user accuracies provided; some classes show spectral ambiguity (e.g., bog, neutral grassland).
- Validation metadata and confusion matrices accompany outputs to aid interpretation and user validation.

## Countryside Survey (CS) comparison: similar and dissimilar area estimates
- Two CS–LCM2007 comparison approaches:
  - Area within CS 1 km squares vs LCM2007 areas (BH level).
  - CS National Broad Habitat estimates vs LCM2007 extents.
- Key patterns:
  - Similar area estimates: Broadleaved woodland, Acid Grassland, Inland Rock.
  - Dissimilar area estimates: Arable and Horticulture; Improved Grassland; Neutral Grassland; Dwarf Shrub Heath; Bog; Montane Habitats; coastal habitats; Fen, Marsh and Swamp.
- Contributing factors to differences:
  - Differences in classification definitions (e.g., Arable and Horticulture), spectral confusion, and inclusion of boundaries in LCM2007.
  - Boundary and linear features in CS often map differently due to LMU differences.
  - Grassland distinctions (Improved vs Neutral vs Calcareous/Acid) reflect how classes are represented spectrally and in field surveys.
  - Fen, Marsh and Swamp areas are complex mosaics; CS patches can be small and exceed LMU in LCM, leading to large discrepancies.
- Overall interpretation: CS and LCM2007 offer complementary views; robust change assessment requires careful harmonization of spatial and thematic frameworks.

## UK land cover distribution and comparative context
- LCM2007 provides >50% of the UK in intensive land use (Arable and Horticulture plus Improved Grassland) and Built-up Areas; remainder is semi-natural (woodland and semi-natural grasslands, etc.).
- Country-level variations: England has the highest intensive land-use share; Scotland has the largest Coniferous Woodland share and substantial Montane/rough habitat representation.
- Compared to LCM2000, LCM2007 shows changes in arable and semi-natural grassland proportions and slight shifts in woodland and urban areas, with ongoing analysis needed to interpret spatial framework effects.

## Change mapping and temporal context
- Change mapping is challenging due to evolving class schemes and different spatial structures across LCM generations (LCM1990, LCM2000, LCM2007).
- Reliable separation of real change from mapping error requires advanced methods; aggregation and focus on consistently mapped classes offer a practical path forward.

## Applications, use cases, and impact
- Provides a robust evidence base for habitat monitoring, biodiversity assessments, ecosystem services, landscape planning, and catchment management.
- Outputs support detailed local analyses (vector parcels with rich metadata) and broad-scale analyses (1 km rasters for national-scale modeling, e.g., climate, hydrology, or species distribution).
- Facilitates policy-related work, comparability across the UK, and integration with other data streams ( soils, terrain, urban, etc.).

## Practical considerations for data support and use
- Data access through CEH gateways; licensing may apply for full vector and 25 m products.
- Outputs are designed for interoperability with knowledge-based enhancements, terrain/soil context, and urban boundaries to improve reliability and reuse.
- Vector data offer rich attribute-level detail; 25 m rasters provide a balance between detail and processing practicality; 1 km rasters cater to national-scale analyses and integration with other datasets.

## Concluding perspective
- LCM2007 represents a significant advance in UK land cover mapping, delivering a reusable, change-aware national product by integrating cartographic spatial frameworks with multi-date satellite imagery and knowledge-based enhancements.
- The approach strengthens data interoperability for national biodiversity planning and provides a solid platform for future land cover monitoring and policy-relevant analyses across the UK.