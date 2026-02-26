# Final Report for LCM2007 - the new UK land cover map

## Overview
- First continuous parcel-based UK land cover map (LCM2007) supporting biodiversity monitoring, policy, planning, and ecosystem services assessment.
- Outputs: vector parcel product (land parcels with rich metadata), 25 m raster, and 1 km raster summaries; 23 LCM2007 classes mapped to Broad Habitats (BH).
- Minimum mapping unit: 0.5 ha; high-level provenance with traceable processing and knowledge-based enhancements (KBEs).
- Overall data quality: strong governance and reproducible workflows; some class-level uncertainties and regional variability.
- Access model: open 1 km raster; licensed vector and 25 m raster on request; fees may apply.

## Data assets and structure
- Vector product
  - Land parcels with attributes: area, source images, Broad Habitat (BH), BHSub, FieldCode, KBE history, ProbList, CorePixels, Construct.
  - Broad Habitat sub-classes provide additional but user-validated detail.
- Raster products
  - 25 m resolution: 23 LCM2007 classes.
  - 1 km resolution: either percentage cover per class or dominant class per pixel.
- Spatial framework
  - Based on generalised Ordnance Survey MasterMap (GB) and LPS Large-scale Vector (NI); parcels serve as the basic unit for spectral classification.
  - Segmentation and boundary data integrated with cartography for spatial coherence and change detection.

## Processing and methodology
- Image processing pipeline
  - Pre-processing: cloud masking, atmospheric/topographic correction, geo-registration; 6-band 2-date summer–winter composites.
  - Segmentation: 3-band segmentation (winter NIR; summer red and MIR) merged with cartographic parcels.
  - Classification: parcel-based supervised maximum likelihood using 37 composites and 21 single-date images; iterative training.
  - Hole-filling: manual corrections for small gaps.
- Knowledge-Based Enhancements (KBEs)
  - Seven automatic KBEs applied in sequence to reduce spectral confusion and improve thematic resolution.
  - KBEs rely on terrain, soils, coastal proximity, urban context, and other ancillary data.
  - KBEs influenced about 20% of parcels; designed to reduce misclassifications but may introduce some false positives.
  - Original spectral signatures retained in ProbList to allow reversion if needed.
- Thematic resolution and grassland
  - Grassland types refined via KBEs plus soil and altitude context; notes on alignment challenges between field Broad Habitat definitions and spectral signatures.

## Validation, accuracy and comparability
- Ground truth and validation
  - 9,127 ground reference points; overall accuracy about 83%; class-level accuracies vary by habitat type.
- Countryside Survey (CS) comparisons
  - UK-wide: ~62% correspondence at Broad Habitat (BH) level; ~76% at Broad Habitat Association (BHA) level.
  - Grassland: aggregation of grassland types significantly improves correspondence (87–90% when aggregated).
  - Regional differences reflect upland mosaics, boundary definitions, and methodological differences.
- Change mapping caveats
  - Differences across 1990, 2000, 2007 maps in class structure and spatial details complicate change detection.
  - Fen, Marsh and Swamp (FMS) estimates vary dramatically due to mosaic nature and small patch sizes; many FMS areas in CS map to Rough or Acid Grassland in LCM2007.
- 4.5 Summary context
  - CS and LCM2007 provide complementary perspectives (field vs. satellite); differences arise from definitions, scale, and data structures.
  - LCM2007 aligns with Broad Habitats for policy-relevant analyses but requires careful interpretation for grassland and fen-related classes.

## Data access, licensing, and products
- Access paths
  - 1 km raster: CEH Information Gateway.
  - Full vector and 25 m raster: available on request under licence; online application; fees may apply.
- Data products
  - 23 LCM2007 classes (vector and 25 m raster).
  - 1 km raster products: percentage cover and dominant class summaries for the 23 classes and 10 aggregated classes.
- Metadata and provenance
  - Rich per-parcel metadata documenting processing steps, KBE history, and ProbList; supports auditability and re-use.

## Applications and impact
- Strategic uses
  - Habitat monitoring, biodiversity planning, landscape-scale policy support, ecosystem services assessment, and catchment management.
- Cross-sector relevance
  - Biodiversity assessments, climate and carbon accounting, urban planning, water/resource management, and integration with other environmental datasets.
- European and policy connections
  - UK component supports Corine Land Cover mapping; aligns with European monitoring and policy-relevant frameworks.

## Data governance, challenges, and recommendations
- Key challenges for Data Leaders
  - Understanding user needs across diverse audiences; fragmented data sources; data gaps and granularity issues.
  - Data verification and quality: spectral confusion, limited metadata, and lack of standardized data models across sectors.
  - Coordination in the sector and risk of duplicated effort; need for stronger communities of practice.
- Recommendations
  - Maintain a holistic view of the data system; foster co-ownership of data products; prioritize based on data availability, gaps, and user needs.
  - Emphasize governance, metadata, discoverability, and update cycles; support iterative product improvement with user feedback.
  - Leverage KBEs and ancillary datasets carefully; document processing lineage to support reproducibility and future reclassification if needed.
  - Use cross-product validation (e.g., CS comparisons) to understand biases and uncertainties; plan for change-detection challenges across time.

## Key takeaways for Data Leaders
- LCM2007 provides a comprehensive, governance-backed UK land cover dataset aligned with Broad Habitats, with strong provenance, multi-resolution outputs, and an auditable processing chain.
- The data framework combines national cartography with image-derived segmentation, enhanced by knowledge-based rules to improve thematic resolution.
- Access is staged: open 1 km raster for broad use; licensed vector and 25 m data for more detailed analyses, balancing openness with licensing considerations.
- The dataset supports long-term monitoring and policy analyses but presents ongoing challenges in spectral confusion, grassland/fen classification, and cross-time change detection.
- Provenance, metadata richness, and cross-validation (e.g., Countryside Survey) illustrate a robust model for data stewardship and evidence-based policy support, while highlighting areas for methodological refinement and sector collaboration.