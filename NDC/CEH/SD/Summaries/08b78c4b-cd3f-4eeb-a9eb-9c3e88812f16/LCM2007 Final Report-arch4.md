# Final Report for LCM2007 - the new UK land cover map

## Executive summary
- LCM2007 delivers the UK’s first coast-to-coast, parcel-based land cover map with a UK-wide vector product and raster derivatives at 25 m and 1 km resolution.
- Built on a generalised spatial framework derived from detailed national cartography (OS MasterMap, LPS vector) to enable consistent change detection and integration with other national datasets.
- 23 LCM2007 land cover classes are mapped and aggregated into 10 Broad Habitats; 1 km rasters provide both percentage cover and dominant class summaries.
- Knowledge-based enhancements (KBEs) improve thematic resolution, applied regionally; about 20% of parcels are affected.
- Validation against ground reference data yields an overall accuracy around 83%, with class-specific variability.
- Data access: 1 km rasters are openly available via the CEH Information Gateway; full vector and 25 m products are available on license or by request (fees may apply).

## Data sources and workflow
- Imagery and composites
  - Multi-temporal, multi-sensor imagery (Landsat-5 TM/ETM+, SPOT-4/5, LISS-3) forming 60 composites; 37 composites and 21 single-date images used for classification.
  - Pre-processing includes cloud masking, atmospheric and topographic corrections; segmentation links to the OSMM framework.
- Training and validation
  - Ground reference from CEH field surveys and Countryside Survey (CS) data; 9,127 ground reference polygons used for validation.
- Spatial framework
  - UK-wide framework built from OS MasterMap generalised cartography, refined with agricultural boundaries and image segments; NI framework adapted from LPS data.
  - MMU 0.5 ha (minimum mappable unit); MFW 20 m; segmentation converts to a UK-wide segment-based vector framework.
- Classification approach
  - Parcel-based supervised classification using maximum likelihood with iterative refinement; top five class probabilities recorded per parcel.
  - KBEs apply regionally adaptive contextual rules (urban context, coastal proximity, terrain, soils) to improve class distinction; sequential application; around 20% of parcels affected.

## Products and metadata
- Vector product
  - Parcels annotated with area, source images, Broad Habitat (BH), field codes, and detailed processing history (Construct, ProbList, KBE history).
  - Includes Broad Habitat sub-classes (BHSub) for additional guidance; careful validation recommended for sub-class use.
- Raster products
  - 25 m raster: 23 LCM2007 classes.
  - 1 km raster: two outputs per pixel — (A) percentage cover for each class, (B) dominant class.
- Aggregates and mapping
  - 23 LCM2007 classes mapped to 10 Broad Habitat aggregates; alignment with JNCC Broad Habitats.
- Access and metadata
  - 1 km rasters openly accessible via CEH Information Gateway; full vector and 25 m data available on request under license.
  - Rich metadata supports provenance and traceability of processing steps and KBEs.

## Quality assurance and validation
- Validation
  - Ground reference validation: 83% overall accuracy; class-specific accuracies vary (e.g., certain grassland classes present spectral challenges).
- Countryside Survey (CS) comparison
  - Agreement with CS varies by Broad Habitat; grasslands show notable discrepancies due to one-to-many relationships and methodological differences.
  - Fen, Marsh and Swamp exhibits large UK-level differences due to mosaic land-cover compositions and CS patch size reporting.
- Interpretation guidance
  - The CS-based estimates are extrapolated field observations; LCM2007 provides continuous, repeatable mapping with explicit provenance and KBEs, enabling cross-method reconciliation where needed.
- Practical validation notes
  - Differences in boundaries, the MMU, and temporal ranges of imagery influence arable vs. boundary classifications and grassland allocations.

## Key findings for data strategy (Data Leaders perspective)
- Proactive, system-wide data management
  - LCM2007 demonstrates a scalable national data product that integrates satellite imagery, advanced cartography, soils, DEM, urban boundaries, and KBEs to support cross-organisational data strategies.
- Data discoverability and governance
  - Open access at 1 km supports wide adoption; higher-resolution vector and 25 m data require licensing, underscoring governance and IP considerations.
- Data quality, provenance, and transparency
  - Rich, parcel-level metadata and a transparent KBEs history enable targeted quality assessment and validation, supporting co-ownership and collaborative validation with partners.
- User needs and co-ownership
  - KBEs are context-driven (urban, coastal, soil, terrain, etc.) and are designed to improve utility for policy, planning, and habitat monitoring; users can disable KBEs if unsuitable for specific analyses.
- Gaps and evolving needs
  - Spectral confusion in grasslands, upland mosaics, and boundary feature representation remain challenging; change attribution remains difficult due to methodological differences between map products.
- Change detection and temporal consistency
  - Cross-version comparisons require sophisticated, aggregated-change approaches; a common spatial framework enhances cross-year comparability but requires careful interpretation to distinguish real change from methodological effects.

## Practical considerations for Data Leaders
- Data system scope
  - A scalable national land-cover data product with a reusable spatial framework suitable for multi-partner ecosystems and cross-sector policy support.
- Data discovery and access
  - Leverage CEH Information Gateway for 1 km products; establish licensing pathways for vector and 25 m data to enable broader use while protecting IP.
- Data quality and governance
  - Maintain detailed metadata, provenance logs, and KBE history; acknowledge class-specific accuracy variability when applying results to policy or planning.
- Co-ownership and user engagement
  - Engage partners to validate KBEs and contextual rules; align data products with partner data ecosystems ( soils, demographics, urban planning, biodiversity, etc.).
- Gaps and continuous improvement
  - Invest in improving grassland class separation, upland mosaic interpretation, and validation datasets; pursue enhanced attribution of actual change vs. classification artifacts.

## Data access and European context
- LCM2007 supports European biodiversity reporting via Corine Land Cover transformation; European datasets (IMAGE2006, Corine) were instrumental in contextual European monitoring.
- The integrated spatial framework facilitates future monitoring and cross-border comparisons, aligning UK data with pan-European environmental assessment efforts.

## Concluding note
- LCM2007 marks a major advance in UK land cover mapping: a national, repeatable, policy-relevant dataset with robust provenance, extensive metadata, and a forward-looking, reusable spatial framework for monitoring, validation, and cross-sector data integration.