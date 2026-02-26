# Final Report for LCM2007 - the new UK land cover map

- Overview
  - Delivers the first continuous parcel-based land cover map for the UK with 23 land cover classes mapped to 17 Broad Habitats (BH) and associated metadata.
  - Provides multiple data products: vector parcels with attributes, 25 m raster, and 1 km summary products (percent and dominant class).
  - Supports policy-relevant applications such as biodiversity assessment, habitat monitoring, ecosystem service assessment, landscape planning, and catchment management.
  - Built on a common spatial framework derived from detailed national cartography (OS MasterMap, LPS) to enable integration with other national datasets.

- Data assets and products (for data leaders)
  - Vector product: parcel-based polygons with 10 processing attributes (e.g., Construct, ProbList, KBE history) and BH/BHSub classifications; includes field codes and core metadata for traceability.
  - 25 m raster: 23 LCM2007 classes aligned with BH framework.
  - 1 km raster: UK-wide summaries in two formats per class (percent cover and dominant class per 1 km cell).
  - Key scale coverage: GB and Northern Ireland, with 8.6 million GB parcels and 0.9 million NI parcels.
  - Accessibility: 1 km raster data via CEH Information Gateway; full vector and 25 m raster on request (licensing may apply).

- Data sources, processing, and spatial framework
  - Primary data: multi-date satellite imagery (e.g., Landsat, SPOT, LISS-III) with cloud masking, atmospheric and topographic corrections; segmentation and parcel construction anchored to OS MasterMap and LPS.
  - Ground references and external datasets support training/validation and KBEs (e.g., soil, terrain, urban context; Countryside Survey references).
  - Spatial framework harmonises with GB NI boundaries, enabling cross-border analyses while acknowledging boundary generalisation differences.

- Classification approach and knowledge-based enhancements (KBEs)
  - Parcel-based supervised maximum likelihood classification using multiple composites; target accuracy refined iteratively.
  - Knowledge-based enhancements (KBEs): seven automated algorithms leveraging contextual data (urban/coastal context, terrain, soils, water, etc.); about 20% of parcels reclassified or adjusted to improve thematic resolution and reduce spectral confusion.
  - Critical role of terrain and soil data for discriminating grassland types; some KBEs can be disabled to preserve spectral classification when needed.
  - KBEs support mapping to BH/BHA where possible and provide an audit trail via KBE history in the vector attributes.

- Classification accuracy and validation
  - Ground reference validation: 9,127 polygons; overall accuracy around 83%.
  - Class-specific performance varies; examples include higher accuracy for certain habitats and lower for spectrally similar or mosaic classes.
  - Countryside Survey (CS) 2007 comparisons show variable agreement across broad habitats; grassland classes are challenging due to one-to-many relationships with BHs and differences in spatial representation between products.
  - Notable discrepancies: Arable and Horticulture often overestimated in LCM2007 relative to CS; boundary/linear features and temporal compositing influence classifications; Fen, Marsh and Swamp shows large differences due to mosaic and small patch sizes.

- Change mapping, limitations, and methodological notes
  - Change detection across LCM epochs is complex due to differing class definitions, spatial frameworks, and typical classification errors (~20% for standard classifications).
  - Reliable change detection at broad habitat level requires methodological alignment; a common spatial structure and reorganization of older maps into real-world units is recommended for future change analysis.

- Access, licensing, and usage implications
  - 1 km raster data openly accessible via CEH Gateway.
  - Full vector and 25 m raster products available on request; licensing may apply.
  - Meta- and provenance-rich data support reproducibility, auditability, and reuse across agencies and studies.

- Implications for Data Leaders (governance, reuse, and systems)
  - Rich parcel-level metadata enables auditability and traceability of classifications and KBEs, facilitating quality assurance and user-specific validation.
  - Structured data assets support reproducible analyses, cross-border comparisons, and integration with other national datasets.
  - Open, discoverable data pathways (with controlled access) align with data reuse principles and policy needs.
  - The shared spatial framework enhances future monitoring and change detection, but requires careful handling of boundary generalisation when aggregating across borders.

- Gaps, challenges, and recommendations
  - Grassland and upland habitats remain challenging due to spectral similarity and ecological continua; continued development of KBEs and integration of additional data layers could improve VH/BH allocations.
  - Fen, Marsh and Swamp area estimates vary drastically between CS and LCM2007; consideration of additional datasets or refined rules for allocation to specific grassland or fen types is warranted.
  - Boundary and linear features are not fully captured at satellite resolution; interpretation with auxiliary data remains important for accuracy.
  - Future work should emphasize a common spatial framework across CEH maps to enable straightforward change detection and national-scale monitoring.

- Key figures and statistics (select)
  - 23 land cover classes, 17 Broad Habitats; vector parcels: ~8.6 million GB and ~0.9 million NI.
  - Major UK land covers: Arable/Horticulture and Grasslands dominate; woodland types and built-up areas comprise the remainder.
  - UK-wide validation accuracy around 83%; country-level agreement with CS varies by habitat type.
  - Access pathways: CEH Gateway for 1 km; licensing for vector/25 m data.

- Summary takeaway for Data Leaders
  - LCM2007 delivers a robust, auditable, multi-resolution UK land cover framework that can underpin policy, planning, and environmental monitoring.
  - The combination of spectral classification with knowledge-based enhancements yields richer thematic detail and better alignment with BH/BHA classifications, while preserving an auditable change history.
  - Strong governance, metadata depth, and clear licensing pathways support reuse across agencies; ongoing work should address known gaps in grassland, fen, and boundary features, and continue to harmonise spatial structures for effective change detection.