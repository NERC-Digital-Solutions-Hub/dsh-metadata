# Final Report for LCM2007 - the new UK land cover map

## Overview
- UK-wide, first continuous parcel-based land cover map (LCM2007) produced by CEH as part of Countryside Survey 2007.
- Vector (parcel-based) plus 25 m raster and 1 km products, aligned with Broad Habitats for UK biodiversity reporting. Supports habitat monitoring, policy, biodiversity, ecosystem services, landscape planning, and catchment management.
- Data governance, provenance, and extensive metadata enable reproducibility and future updates.

## Data governance, provenance and access
- Licensing and access: 1 km rasters via CEH Information Gateway; full vector and 25 m rasters on request under licence; potential fees apply. Managed by CEH Data Licensing/IPR team.
- Metadata and traceability: Vector polygons carry 10 polygon-level processing attributes (e.g., Construct, ProbList) and a rich provenance trail; training data and knowledge-based enhancements (KBEs) are recorded.
- Reproducibility and updates: UK-wide assembly via nine processing chunks with defined priority; explicit documentation of pre-processing, segmentation, classification, and KBEs to support audits and future updates.
- Interoperability: Class definitions designed to align with Broad Habitat concepts; supports mappings to aggregated classes and habitat associations for comparability with field surveys.
- Validation and user guidance: Bespoke validation framework and guidance provided to help users assess uncertainties by class and region; ongoing data versioning and change detection considerations.

## Data sources and spatial framework
- Spatial framework: Britain uses OS MasterMap topography; Northern Ireland uses LPS Large-scale Vector; agricultural boundaries and urban extents integrated to refine land parcel delineation.
- External and ancillary inputs: Digital Elevation (NEXTMap), soils data, coastal/urban boundaries, and various boundary datasets to support contextual rules.
- Satellite imagery and sensors: Landsat-5 TM/ETM+, SPOT-4/5, LISS-III; AWIFS as backup. Six-band summer–winter composites crafted to maximize spectral contrast.
- Resolution and MMU: 20–30 m imagery; minimum mappable unit (MMU) approximately 0.5 ha; features must meet size/width thresholds (minimum feature width about 20 m).

## Processing workflow and methodologies
- Pre-processing: Cloud/cloud-shadow masking; atmospheric correction (e.g., FLAASH/MODTRAN); geometric and topographic corrections.
- Segmentation and framework integration: Segment-based UK-wide framework created by integrating OS MasterMap parcels and agricultural boundaries; 60 composite images (and some singles) used for segmentation.
- Classification: Parcel-based supervised maximum likelihood classification using 37 composites and 21 single-date images; 23 LCM2007 classes mapped to Broad Habitats; training areas from ground/reference data; iterative manual edits as needed.
- Knowledge-based Enhancements (KBEs): Seven sequential rules using terrain, soils, proximity to coast/urban contexts, and other contextual data to refine or reclassify classes; KBEs affect ~20% of parcels; original spectral signatures kept accessible via ProbList for revert/inspection.
- Quality control steps: Hole-filling and manual edits in limited areas; UK-wide assembly in nine chunks with boundary prioritisation to maximise edge accuracy.
- Documentation: Detailed processing history retained in vector attributes (KBE history, image(s) used, etc.).

## Data products
- Vector product: 23 LCM2007 classes with 10 polygon-level processing attributes (e.g., Construct, ProbList, KBE).
- Raster products: 25 m resolution raster (23 classes) and 1 km raster products (percent cover and dominant class per 1 km pixel).
- Complementary documentation: Extensive metadata and usage notes; access to 1 km rasters via gateway and vector/25 m products on request.

## Quality assurance and validation
- Validation dataset: 9,127 field/reference points used; overall accuracy ~83% with class-specific variation in producer’s and user’s accuracies.
- Comparison with Countryside Survey (CS) 2007: Varied agreement by Broad Habitat; grassland classes especially challenging due to one-to-many relationships with BHAs and differences in spatial structure and MMU.
- Key challenges and explanations:
  - Arable and Horticulture: CS vs LCM2007 differences due to class definitions, spectral variability, and inclusion of boundary/linear features; temporal range of imagery affecting grass/seasonal classifications.
  - Grassland categories: Differences between Improved/Neutral/Calcareous/Acid grasslands often reflect spectral ambiguity and soil influences.
  - Fen, Marsh and Swamp: Complex mosaics; CS often records small patches not easily mapped by LCM2007; reliance on KBEs and context rules discussed.
- UK-wide and country-level patterns: England, Scotland, Wales, and Northern Ireland show varying correspondences; BHAs and aggregation help reconcile some mismatches, but upland/mosaic regions remain challenging.

## Findings and implications for data stewardship
- LCM2007 provides a robust, policy-relevant UK land cover dataset with explicit structure, metadata, and audit trails enabling reproducibility and future monitoring.
- KBEs improve thematic/spatial accuracy where spectral data are insufficient but introduce class-specific uncertainties; users should perform local validation and consider region-specific uncertainties.
- Data licensing, provenance, and versioning are essential; clear governance around access, updates, and guidance on uncertainties by class/region is needed.
- Interoperability and comparability are enhanced by alignment with Broad Habitats and by providing mappings to aggregated BHAs for cross-study consistency.

## Practical relevance for Data Stewards
- Licensing and terms: Ensure licensing terms are current and clearly communicated; maintain primary license contacts.
- Provenance and metadata: Preserve complete preprocessing, segmentation, classification, and KBE histories; document any suppression or modification of KBEs.
- Reproducible workflows: Maintain chunking strategy, image priority rules, and processing steps to support audits, updates, and harmonisation with future UK land cover mappings.
- Interoperability: Provide clear class mappings to Broad Habitat concepts and BHAs; enable end-users to translate to aggregated classes for comparability with field data.
- Validation and uncertainty guidance: Support validation programs and provide class- and region-specific uncertainty guidance; encourage bespoke local validation by end users.
- Change detection and versioning: Plan for updates and change-detection protocols; maintain versioned data products with clear release notes.

## Additional context on comparison and change
- Change detection across CEH land cover maps (LCM1990, LCM2000, LCM2007) requires sophisticated, non-trivial methods due to differences in spatial structure and thematic classification; LCM2007’s generalized spatial framework is designed to facilitate future consistent monitoring and comparison through a common real-world unit-based structure.