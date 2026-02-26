# Final Report for LCM2007 - the new UK land cover map

## Overview of the dataset and purpose
- First continuous parcel-based UK land cover map (LCM2007) with vector parcels linked to a 25 m raster and 1 km aggregate products.
- Vector product maps 23 land cover classes aligned to 17 Broad Habitats (BH); supports GB and NI with ~8.6 million GB parcels and ~0.9 million NI parcels.
- Outputs designed for habitat monitoring, biodiversity policy, ecosystem services, landscape planning, and catchment management; provides a foundation for future UK-wide land surface mapping and monitoring.
- Data governance: rich metadata per parcel, including processing history, KBE (Knowledge-Based Enhancements) details, and probability lists for top spectral variants; data access via CEH Information Gateway with potential licensing for full-resolution data.

## Data sources and spatial framework
- Primary imagery and inputs
  - Satellite sensors: Landsat-TM5, IRS-LISS3, SPOT-4/SPOT-5 (20–30 m), AWIFS (60 m as backup).
  - 91% of UK classified from multi-date composites; remainder from single-date imagery with manual filling in parts.
  - Multi-date composites enhance spectral contrast; image segmentation creates parcels that are fused with OS MasterMap (GB) and NI boundaries.
- Complementary data
  - Ground reference points (CEH 2006–2008) for training/validation; Countryside Survey Broad Habitats (CS 2007) for validation.
  - External datasets: GB OS MasterMap topography, NI LPS boundaries, agricultural boundaries, urban areas, soils, digital elevation (NEXTMap Britain), etc.
- Spatial framework
  - GB: Generalised OS MasterMap polygons generalised to ~0.5 ha MMU with minimum feature width 20 m.
  - NI: Separate LPS polygon framework integrated with segmentation; agricultural boundaries included where beneficial.
  - UK-wide segmentation framework assembled from nine geographic chunks for continuous coverage.

## Image processing, segmentation, and classification
- Pre-processing and segmentation
  - Cloud/shadow masking; atmospheric correction (FLAASH); geo-registration; topographic correction; creation of multi-date composites.
  - Segmentation of 60 composite images using a three-band approach (winter NIR, summer red, summer MIR) to form image segments; segments merged with cartographic bases and boundaries to form parcel-based vector framework.
- Classification workflow
  - Parcel-based supervised maximum likelihood classification using 37 composites and 21 single-date images for Broad Habitat classes.
  - Training data from ground references; iterative refinement with additional training areas as needed.
  - Knowledge-Based Enhancements (KBE): seven automated algorithms (terrain, soil, urban context, coastal proximity, water, etc.) reassessing parcel context and spectral results.
  - Post-classification edits: occasional manual edits and hole-filling for rare or gap areas; KBEs often improve class plausibility and resolution.
  - Output structure: vector product with 23 LCM2007 classes and 10 processing attributes; 25 m raster with 23 classes; 1 km rasters with class percentages and dominant classes.
- Metadata and traceability
  - Each parcel records processing steps, KBE history, ProbList (top spectral variants with probabilities), CorePixels, and Construct history to support reproducibility and rollback if needed.

## LCM2007 classes, aggregation, and interpretation
- 23 LCM2007 land cover classes mapped to Broad Habitats (BH) with interpretive nuances for grasses and mosaics.
- Some classes map directly to BHs; others (notably various grasslands) require KBEs and soil context for accurate BH mapping.
- Aggregate classes (10) summarize the 23-class scheme for 1 km rasters and high-level analyses.

## Product specification and accessibility
- Products
  - Vector: 23 land cover classes; 10 attributes documenting processing history (e.g., Construct, ProbList, KBE).
  - Raster: 25 m resolution with 23 classes.
  - 1 km rasters: class percentages and dominant class per pixel.
- Access and licensing
  - 1 km rasters via CEH Information Gateway.
  - Full vector and 25 m rasters available on request from CEH; licensing fees may apply.
- Practical data formats
  - Vector data include parcel-level metadata, sub-classes (BHSub), field codes, and a recommended display class (INTCODE).
  - 25 m and 1 km rasters support broad-scale analyses and cross-domain data integration.

## Validation, accuracy, and comparisons
- QA and validation
  - Ground truth: 9,127 points; overall accuracy ~83% across LCM2007 classes.
  - Class-specific accuracies vary; higher for major classes (e.g., Coniferous Woodland, Arable/Horticulture, Urban) and lower for upland semi-natural and mosaic habitats (e.g., Neutral/Calcareous Grassland, Montane, Bog).
- Countryside Survey (CS) 2007 comparisons
  - Very similar area estimates for some Broad Habitats (e.g., Broadleaved woodland, Acid Grassland, Inland Rock) but notable dissimilarities for Arable and Horticulture, Improved/Neutral Grassland, Dwarf Shrub Heath, Bog, Montane, and Fen/Marsh/Swamp.
  - Explanations include spectral variability of Arable/Horticulture, inclusion of boundaries in LCM2007 classifications, and differences in mapping approaches for grasslands and fen mosaics.
  - The Broad Habitat Association (BHA) framework was developed to better align LCM2007 with CS habitat associations, acknowledging one-to-many relationships and mosaics.
- Change mapping and longitudinal use
  - CEH change mapping is complex due to evolving class structures and spatial frameworks; cross-map comparisons require caution.
  - LCM2007 provides a robust platform for change detection, but users should account for spectral error and structural differences when comparing with earlier maps (LCM1990/LCM2000).

## UK-wide results and regional patterns
- UK landscape composition (Broad Habitats)
  - Over half the UK is intensive land use (Arable and Horticulture plus Improved Grassland) or Built-up areas.
  - Woodlands cover around 12% (split between Broadleaved and Coniferous); semi-natural areas dominate upland areas.
  - Country-level differences reflect regional habitat mixes (e.g., Scotland with more coniferous woodland and upland habitats; England with higher intensive land use; NI and Wales with varied distributions).
- Comparison with LCM2000
  - LCM2007 shows shifts in arable and semi-natural grassland proportions and minor changes in coniferous woodland and urban areas, with differences linked to the revised spatial framework.

## Practical considerations for data leaders
- Governance, metadata, and traceability
  - Parcel-level metadata enables auditability and bespoke quality checks; full processing history and KBE trail support reproducibility and governance.
- Data standards and integration
  - BH framework (JNCC) provides consistency; however, grassland sub-class distinctions and field-survey definitions differ, requiring careful interpretation and possible custom validation.
- Data discovery and collaboration
  - CEH gateway provides data discovery; full-resolution data licensing supports cross-domain integration with OS MasterMap, soils data, topography, and other national datasets.
- Data limitations and risk management
  - Spectral confusion for grasslands, upland habitats, and fen mosaics; boundary features often below MMU require careful interpretation; change detection requires careful reconciliation of spatial and thematic differences.
- Data applications and use cases
  - Habitat monitoring, biodiversity surveillance, landscape planning, ecosystem services assessment, catchment management, and policy development (including Natura and Corine harmonization).
- Recommendations for responsible use
  - Leverage Broad Habitat Association rules to improve correspondence with field surveys.
  - Use aggregated BH or 1 km class outputs for robust national-level analyses; apply caution when interpreting small or mosaic features.
  - Combine LCM2007 with CS field data and other data sources (soil, climate, topography) to strengthen interpretation and Change Analysis.

## Additional context and appendices (highlights)
- Broad Habitat Association (BHA) Appendix
  - Details rationale and rules linking LCM2007 classes to CS Broad Habitats, including edge cases for Bog, Dwarf Shrub Heath, Montane Habitats, Built-up Areas, Fen/Marsh/Swamp, and Rough Grassland.
- Validation methodology
  - Bespoke validation approach emphasizing fit-for-purpose accuracy and the use of parcel-level metadata to refine assessments.
- Data formats and access notes
  - Vector versus 25 m raster trade-offs; 1 km rasters suitable for national-scale modeling; licensing details and contact points for access.