# Final Report for LCM2007 - the new UK land cover map

## Overview and Aims
- Presents LCM2007 as the UK-wide, parcel-based land cover map designed to support policy-relevant monitoring, habitat assessment, and landscape planning.
- Provides a consistent framework for stock estimates, change detection, and policy evaluation across the UK, GB, England, Scotland, Wales, and Northern Ireland.
- Aims to enable environmental monitoring and inform decision-making in biodiversity, ecosystem services, catchment management, and related sectors.

## Data, Products and Spatial Framework
- Products:
  - Vector (land parcels) with detailed attributes, provenance, and knowledge-based enhancements (KBEs).
  - 25 m raster with 23 LCM2007 classes.
  - 1 km raster summaries (percentage cover and dominant class per grid cell).
- Spatial framework:
  - UK-wide integration with national cartography; GB and NI datasets ensure consistent cross-border comparisons.
  - Minimum mapped unit (MMU) of 0.5 ha; KBEs attached to parcels for traceability.
- Accessibility:
  - 1 km rasters openly accessible via the CEH Information Gateway.
  - Full vector and 25 m rasters available on request (licensing may apply).

## Processing, KBEs and Uncertainty
- Processing workflow:
  - Multi-temporal image data (Landsat, SPOT, LISS-III/AWIFS) with pre-processing, segmentation, and parcel-level classification.
  - Knowledge-Based Enhancements applied post-classification to improve thematic resolution and align with Broad Habitats.
- Accuracy:
  - Overall producer’s/user’s accuracy demonstrated; reported overall accuracy for LCM2007 is 83% (class-level varies by habitat).
- KBEs:
  - Seven sequential KBEs address spectral confusion and context (e.g., terrain, urban proximity, soils, coastal/urban context).
  - Approximately 20% of parcels are reclassified or refined due to KBEs.
- Quality assurance:
  - Detailed metadata and processing provenance maintained for reproducibility and governance.

## Similarity and Dissimilarity with Countryside Survey (CS) 2007
- Similar area estimates (within CS 95% confidence limits UK-wide) for:
  - Broadleaved woodland
  - Acid Grassland
  - Inland Rock
- Dissimilar area estimates (beyond CS 95% confidence limits) for:
  - Arable and Horticulture
  - Improved Grassland
  - Neutral Grassland
  - Dwarf Shrub Heath
  - Bog
  - Montane Habitats
  - Coastal habitats
- Key drivers of differences:
  - Differences in class definitions and what is captured under each category.
  - Spectral confusion and the wide spectral variability of Arable and Horticulture, which can lead to overestimation and misallocation of boundary/linear features.
  - Boundary and linear features mapped differently; Countryside Survey includes boundaries that may be below LCM’s MMU, causing field-boundary–field mappings in CS to inflate certain class areas in LCM.
  - Grassland-related discrepancies (Improved vs Neutral vs Calcareous/Acid) due to spectral similarity and field-interpretation differences.
  - Fen, Marsh and Swamp shows order-of-magnitude differences due to mosaic nature and small patch sizes; CS tends to record more fragmented habitats than LCM2007 could consistently map.
- Implications:
  - LCM2007 aligns well with CS for policy-relevant extents in major habitats but exhibits notable differences in mosaic and spectrally ambiguous classes.
  - Broad Habitat Associations (BHAs) help mitigate some mismatches by providing a higher-level correspondence framework.

## Change Mapping and Monitoring Implications
- Change detection challenges:
  - Differences in spatial structure and class definitions across LCM1990, LCM2000, and LCM2007 complicate robust change mapping.
  - Typical classification error rates (~20%) can obscure real habitat changes when comparing maps with different architectures.
- Approaches for policy monitoring:
  - Consider aggregation across different class schemes, or focus on consistently mapped classes and habitat associations.
  - Use trajectory-based analyses to identify plausible changes while discounting implausible shifts caused by mapping or data differences.
  - Reorganize earlier CEH maps into a common spatial structure based on real-world land-use units to enhance comparability over time.

## Applications for Monitoring Frameworks and Policy
- LCM2007 provides a repeatable, policy-relevant evidence base for:
  - Biodiversity monitoring, habitat connectivity, and landscape-scale planning.
  - Ecosystem services assessments, resource management, and climate-related analyses.
  - Catchment management, water resources planning, and biodiversity reporting (e.g., Natura targets).
- Supports multi-tiered monitoring approaches:
  - Class-level, Aggregate-class level, and Broad Habitat Association levels.
  - Facilitates integration with field data (CS) for validation and scenario analysis.
- Framework alignment:
  - The continuous-vector framework and extensive metadata enable rigorous monitoring, governance, and future methodological refinements as data and methods evolve.

## Data Governance, Metadata, and Transparency
- Metadata and provenance:
  - Comprehensive metadata tracks inputs, processing steps, and KBEs for each parcel, enabling auditability and reproducibility.
  - KBEs and processing histories support governance and transparency in data-derived decisions.
- Data sharing and access:
  - Public sharing of underlying datasets can be a barrier; LCM2007 addresses this with clear data linkages and licensing terms.
  - Access to 1 km rasters is open; full vector and 25 m rasters are accessible on request (licensing may apply).

## Key Challenges and Limitations
- Data gaps and access:
  - Gaps and variable data accessibility hinder timely updates and rapid monitoring.
- Silos and governance:
  - Organizational barriers impede data sharing and integrated monitoring efforts.
- Metadata and data harmonization:
  - While metadata is extensive, some datasets require transformation to enable cross-product comparisons.
- Change detection:
  - No universally adopted UK-wide method exists to robustly separate real habitat change from mapping/processing differences; ongoing methodological development is needed.
- Fen, Marsh and Swamp:
  - Highly mosaic and small-area features challenge consistent mapping across time; CS vs LCM differences remain substantial for these habitats.

## Conclusion
- LCM2007 represents a major advance in UK land cover mapping, delivering a policy-relevant, transparent, and repeatable framework for monitoring Broad Habitats and landscapes.
- A robust integration of national cartography, satellite imagery, segmentation, KBEs, and metadata provides a strong platform for habitat monitoring, policy evaluation, and evidence-informed decision-making.
- Comparisons with Countryside Survey highlight valuable synergies and notable mismatches, particularly in mosaic and spectrally ambiguous classes; BHAs help contextualize these differences.
- The combination of a continuous spatial framework and rich metadata supports rigorous monitoring, validation, governance, and future refinements as data and methods evolve.