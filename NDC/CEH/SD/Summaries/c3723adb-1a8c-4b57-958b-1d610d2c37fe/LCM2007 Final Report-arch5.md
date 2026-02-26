# Final Report for LCM2007 - the new UK land cover map

## Overview for Data Stewards
- LCM2007 provides UK-wide, governance-ready land cover data with detailed provenance and knowledge-based enhancements (KBEs).
- Outputs include a vector parcel product (23 LCM2007 classes with 10 processing/provenance attributes), a 25 m raster, and 1 km raster products.
- Aims to support habitat monitoring, biodiversity policy, landscape planning, ecosystem services, and related governance tasks.
- Significant emphasis on metadata, traceability, and interoperability; accessible via CEH portals with licensing for full data.

## Data products and metadata
- Vector product: 23 LCM2007 classes; 10 attributes documenting processing steps, provenance, and KBEs; includes FieldCode and Broad Habitat sub-classes (BHSub) for additional context.
- Raster products: 25 m (23 classes) and 1 km (two summaries: percent cover per class and dominant class per pixel).
- Provenance and documentation: comprehensive metadata on segmentation, training data, KBEs, and processing history; KBEs are stored in vector attributes to allow reversion if needed.
- Accessibility and licensing:
  - 1 km raster: via CEH Information Gateway (gateway.ceh.ac.uk).
  - Full vector and 25 m raster: available on request under licence from CEH; fees may apply.

## Spatial framework and processing pipeline
- Spatial framework built from detailed national cartography (Ordnance Survey MasterMap and LPS Large-scale Vector); aims for stable, reusable boundaries.
- Minimum mappable unit (MMU) set to 0.5 ha (MMU constraints applied to ensure robust parcels).
- Nine UK processing chunks merged into a seamless UK vector product; extensive provenance recorded with each parcel.
- Processing workflow highlights:
  - Multi-date image composites (summer+winter) with cloud masking, atmospheric/topographic corrections.
  - Parcel-based supervised classification (maximum likelihood) using ground reference data.
  - Knowledge-based enhancements (KBEs): seven automated rule-based algorithms addressing context (urban, coastal, soils, terrain, etc.); KBEs applied sequentially and recorded in attributes; ~20% of parcels affected by KBEs.
  - Integration steps: generalisation of OS MasterMap to MMU constraints; inclusion of agricultural boundaries; segmentation-cartography integration to refine spectral regions.

## Data quality, validation, and limitations
- Overall accuracy around 83%; class-level accuracies vary; validation uses 9,127 ground-reference polygons and cross-checks with Countryside Survey (CS) data.
- Key validation insights for Data Stewards:
  - Grassland distinctions are challenging due to one-to-many relationships with Broad Habitats; motivates Broad Habitat Association (BHA) rules for improved interpretability.
  - Fen, Marsh and Swamp areas show large discrepancies with CS due to complex mosaics and small patch sizes; CS tends to map such areas differently depending on patch size and methodology.
  - Arable and Horticulture areas show notable differences with CS due to temporal variability, spectral confusion, and inclusion of boundary features in LCM2007, plus multi-year imagery effects.
  - Water and urban classes show context-dependent differences; KBEs help resolve ambiguities but users should interpret at appropriate thematic levels (e.g., BH or BHA) when comparing to field data.
- Comparability with Countryside Survey (CS):
  - High-level correspondences in some broad habitats, but overall agreement varies by class and country.
  - Grassland classes particularly problematic; use Broad Habitat Associations to improve cross-walks.
- Change mapping considerations:
  - Temporal changes are hard to disentangle from classification differences due to differing spatial frameworks between LCM2007 and earlier CEH maps (LCM1990, LCM2000).

## Change, temporal considerations, and cross-data context
- LCM2007 provides coast-to-coast UK land cover coverage and enables change detection, but cross-map change interpretation requires careful methodological alignment due to differences in spatial structure and class definitions across map versions.
- When monitoring change, consider aggregating to BH/BHA levels or harmonizing grassland classes to reduce misinterpretation.

## Access, licensing, and data management
- Access options:
  - 1 km raster: CEH Information Gateway.
  - Full vector and 25 m raster: CEH licensing on request; fees may apply.
- Documentation and auditability:
  - Detailed processing provenance, segmentation inputs, and KBEs recorded per parcel enable reproducibility and audit trials.
  - KBEs are user-controllable (can be disabled for custom workflows).

## Practical guidance for Data Stewards
- Leverage KBEs and provenance to justify classifications and to trace changes or updates.
- Use Broad Habitat and Broad Habitat Association (BHA) frameworks to improve cross-dataset comparisons, especially for grassland and mosaic habitats.
- Align comparisons with field data (e.g., CS) at compatible thematic levels and spatial scales; be mindful of MMU and spatial framework differences.
- Maintain a versioned data governance approach:
  - Track updates to KBEs, classifications, and spatial frameworks.
  - Document data sources, processing steps, and any reclassification events.
- Integrate LCM2007 with other data layers (e.g., soils, elevation, urban boundaries) to support policy-relevant analyses and auditing.
- Plan for ongoing updates and reprocessing to maintain alignment with evolving habitat classifications and national mapping frameworks.

## Challenges and recommendations
- Challenges:
  - Incomplete user needs and expectations for grassland and mosaic habitats.
  - Complex cross-map comparisons due to evolving spatial frameworks.
  - Balancing high-resolution detail with governance-level usability.
- Recommendations for governance:
  - Continue documenting KBEs and processing histories for transparency.
  - Provide guidance on harmonizing grassland categories or using BH/BHA for cross-dataset alignment.
  - When communicating changes, emphasize provenance, uncertainty ranges, and the distinctions between map versions.
  - Promote data interoperability by maintaining a stable spatial framework and robust metadata.

## European and policy context
- UK component for Corine Land Cover 2006; European-level data integration supported via LCM2007 vector product.
- LCM2007 supports policy-relevant applications across biodiversity, ecosystem services, groundwater and climate-related analyses, and urban planning, with potential benefits for Natura and other reporting frameworks.

## Appendix highlights for governance
- Appendix 1: Broad Habitat Definitions (to inform cross-walks and BH/BHA analyses).
- Appendix 4: Bespoke validation approach (emphasizes fit-for-purpose accuracy assessment and a flexible, probabilistic validation mindset).
- Appendix 5: Broad Habitat Association (BHA) rules (guidance for class correspondences between LCM2007 and CS).
- Documentation of data formats (vector and raster) and metadata structures to support data governance, auditability, and reuse.