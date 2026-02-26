# Final Report for LCM2007 - the new UK land cover map

- Provides the UK’s Land Cover Map 2007 (LCM2007), a parcel-based (vector) land cover dataset with derived 25 m raster and 1 km raster products, covering GB and Northern Ireland.
- Built from generalised national cartography (OS MasterMap and LPS Large-scale Vector) and multi-temporal satellite imagery; aims to support habitat monitoring, biodiversity policy, ecosystem services, and landscape planning.
- Core outputs: 23 LCM2007 classes (aggregate to 10 Broad Habitats), 25 m raster, and 1 km summaries (percent cover or dominant class). Minimum mapping unit is 0.5 ha. Full vector includes 10 polygon-level processing attributes and a KBEs/history log.
- Accessibility: 1 km rasters via CEH Information Gateway; full vector and 25 m raster data available on license/request (licensing may apply).

## Data architecture, framework and processing workflow

- Spatial framework and generalisation:
  - UK-wide parcel-based framework derived from detailed cartography; MMU 0.5 ha; generalisation/merging to create UK-wide parcels while retaining salient land-cover units.
  - Integration of image segments with cartography to delineate spectral regions and improve classification.
- Image processing and segmentation:
  - Pre-processing: sensor selection, cloud/shadow masking, atmospheric and topographic correction (DEM), geo-registration.
  - Segmentation: 60 composite images built from multiple sensors/bands to generate a segment-based vector framework; NI uses single-date segments to supplement composites.
- Classification:
  - Parcel-based supervised maximum likelihood classification across 37 composites and 21 single-date images.
  - Training data from ground reference points; iterative refinement of spectral classes; manual edits and hole-filling where needed.
  - Output: vector product with 10 processing-related attributes; 25 m raster with 23 classes; 1 km rasters for each class and aggregates.
- Data provenance and traceability:
  - Comprehensive metadata and processing history, enabling reproducibility and QA.

## Knowledge-based enhancements (KBEs)

- Purpose: resolve spectral confusion and increase thematic resolution by applying contextual and ancillary data after classification.
- Impact: modified ~20% of parcels to improve realism; applied in a defined sequence to converge on plausible classifications.
- Contextual inputs included:
  - Urban context and proximity; coastal vs inland; terrain (altitude, slope) to assign montane vs coastal classes.
  - Water classifications (coastal vs inland; rivers, lakes, estuaries).
  - Within/outside urban boundary rules to correct urban misclassifications.
  - Soil data to help distinguish grassland subtypes and certain habitats.
- Transparency: KBEs are recorded in each parcel’s ProbList and KBE history, allowing users to see and, if needed, revert KBEs.

## Metadata, lineage and quality assurance

- Parcel-level metadata:
  - 10 polygon attributes documenting construction, source images, Broad Habitat, and processing steps; KBE history; ProbList and CorePixels.
  - Broad Habitat sub-classes (BHSub) included for traceability, though not all are equally validated; ProbList provides top spectral-class probabilities.
- QA and validation:
  - Ground reference validation with 9,127 points; overall accuracy around 83%, with variation by class.
  - Producer’s vs User’s accuracy discussed; spectral/confusion issues acknowledged, especially for grassland and certain natural classes.
  - KBEs improve some classes but can reduce accuracy for others that rely heavily on spectral data alone.
- Change mapping and interpretation:
  - Change detection across LCM2007 and earlier CEH maps is complex due to differing spatial structures and class definitions; aggregated class approaches and BHAs help mitigate misinterpretation.

## Comparison with Countryside Survey (CS) 2007

- CS provides 1 km-square national estimates; LCM2007 offers UK-wide pixel/parcel data.
- Findings include:
  - Moderate alignment for Broad Habitat associations; substantial differences for certain grassland and fen-related classes due to definitional/structural differences.
  - When grasslands are collapsed to a single Grassland category, correspondence improves, highlighting spectral ambiguity and class-mapping challenges.
  - Montane and coastal habitats show variable correspondence due to CS’s upland mapping limitations and habitat mosaic patterns.
- Implications for data steward governance: LCM2007 and CS complement each other; careful handling of class semantics and aggregation is essential when comparing datasets.

## Data products and access

- Products:
  - Vector: 23 LCM2007 classes with 10 polygon-level attributes.
  - 25 m raster: 23 LCM2007 classes.
  - 1 km raster: per-class percentages and dominant class per 1 km cell; also available as aggregated BHs.
- Access and licensing:
  - 1 km rasters via CEH Information Gateway.
  - Full vector and 25 m rasters available on license (online application; fees may apply).
- Documentation and traceability: extensive metadata and KBEs documentation to enable auditability, reproducibility, and governance.

## Implications for Data Stewards (governance and stewardship focus)

- Robust governance and provenance:
  - Standardised UK-wide spatial framework with explicit data sources (cartography, soils, DEMs, agriculture, urban boundaries) and a transparent KBEs history.
  - Parcel-level metadata supports reproducibility, audit trails, and quality assurance across institutions.
- Data quality and provenance:
  - Documented overall accuracy and class-level variability; QA procedures and ground reference validation underpin data integrity.
  - Knowledge-based enhancements provide a reproducible, traceable mechanism to improve classifications.
- Metadata, lineage and accessibility:
  - Rich attribute schema (10 polygon attributes and BHSub), enabling data lineage tracking and reuse decisions.
  - Clear access routes (CEH gateway for 1 km; licensed vector/25 m products) and licensing considerations for different user groups.
- Interoperability and reuse:
  - UK-wide, integration-ready with GB/NI datasets; explicit considerations required when comparing with other habitat datasets due to differences in class semantics and spatial structure.
  - KBEs and ProbList offer a transparent means for external users to assess classification confidence and to perform independent validation.
- Change monitoring and policy relevance:
  - LCM2007 provides a stable baseline for habitat monitoring but change assessment must account for model semantics, class definitions, and spatial structure.
  - Useful as a contextual base for higher-resolution habitat mapping and for biodiversity policy support, habitat networks, and catchment planning.
- Practical guidance for data users:
  - Prioritize aggregated Broad Habitat or suitable BHAs when comparing with CS due to one-to-many grassland relationships.
  - Use the parcel-level KBE history to understand and validate classifications in specific locations.
  - Consider temporal variability and multi-year image requirements that can influence class assignment (e.g., temporary grass vs arable transitions).

## Summary takeaway for Data Stewards

- LCM2007 delivers a robust, governance-friendly UK land cover map with a transparent processing chain, provenance, and documentation, suitable for governance, monitoring, and policy-support use.
- It balances spectral classification with knowledge-based enhancements to improve thematic accuracy while acknowledging class-level uncertainties and comparability challenges with other datasets.
- Access is clear and license-based for non-public data, with comprehensive metadata enabling reproducibility, traceability, and responsible reuse.