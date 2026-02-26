# Final Report for LCM2007 - the new UK land cover map

- Purpose and scope
  - Presents the first continuous parcel-based UK land cover map (LCM2007) with 23 land cover classes mapped to Broad Habitats (BH).
  - Provides a robust, policy-relevant evidence base for habitat monitoring, biodiversity assessments, ecosystem services, landscape planning, and catchment management.
  - Delivers a governance-ready data framework with detailed metadata, traceability of processing steps, and knowledge-based enhancements to improve classification defensibility.

- Data sources and spatial frameworks
  - Imagery: multi-date composites from Landsat TM5, IRS LISS-3, SPOT-4/5 (plus backups), with summer/winter combinations to boost contrast.
  - External data: Ordnance Survey MasterMap (GB), OSNI/LPS (NI), agricultural boundaries, urban datasets, digital elevation (NEXTMap), soils data, and other cartographic layers.
  - Spatial frameworks: GB MasterMap generalised to support 0.5 ha MMU; Northern Ireland boundaries aligned with LPS; nine-chunk processing strategy to ensure coherent UK-wide boundaries and processing efficiency.

- Processing, segmentation, classification, and knowledge-based enhancements
  - Pre-processing: cloud/cloud-shadow masking, atmospheric correction, georeferencing, topographic correction; composite creation.
  - Segmentation and classification: parcel-based approach classifying 37 composites and single-date images into 23 LCM2007 classes using maximum likelihood, with ground references for refinement.
  - Knowledge-based enhancements (KBEs): seven automated rules applied to parcels using contextual data (urban boundaries, coastal proximity, terrain, soils, etc.) to improve accuracy and thematic resolution; documented per parcel; ~20% of parcels affected.
  - Data governance and provenance: vector attributes capture processing history, KBEs applied, and probability lists; KBEs and segmentation details embedded in outputs for traceability.

- Product specification and access
  - Outputs:
    - Vector product: land parcels with 10 processing attributes and KBEs.
    - 25 m raster: 23 LCM2007 classes.
    - 1 km raster: two summaries per location—(A) percentage cover per LCM2007 class, and (B) dominant class.
  - Access and licensing:
    - 1 km rasters via CEH Information Gateway.
    - Full vector and 25 m products available on request under CEH license (some applications may incur fees).
  - Metadata and transparency: comprehensive metadata documents processing steps; KBEs and segmentation details are embedded for audit and validation.

- Quality assurance and validation
  - Ground reference: 9,127 points from 2006–2008; overall accuracy around 83% for LCM2007 classes.
  - Class-level performance varies; forests and urban areas tend to be higher accuracy, while certain grasslands and montane/bog mosaics show greater confusion due to spectral ambiguity and patch mosaics.
  - Change detection caveats: substantial challenges in distinguishing real change due to shifts in class definitions, spatial structure, and pixel-level error rates (~20%).

- Comparison with Countryside Survey (CS) 2007
  - CS provides field-based national estimates; LCM2007 often shows different extents due to methodology, MMU differences, and spectral confusions.
  - Grasslands are a major source of discrepancy; Broad Habitat Association (BHA) rules were developed to improve cross-dataset correspondence at multiple thematic levels (BH, BH Sub-class, and 1 km aggregates).
  - LCM2007 closely matches CS for certain classes (e.g., Arable and Horticulture at 1 km scale) but often reports higher broad-habitat extents; Fen, Marsh and Swamp shows large discrepancies due to complexity and patch size.
  - Implications: cross-dataset comparisons require careful interpretation of class definitions, MMU, and context-driven adjustments; BHA rules help contextualize correspondences.

- UK-wide and country-level distributions
  - UK highlights: majority of land is intensive use (Arable and Horticulture plus Improved Grassland) or built-up areas; about 12% Broadleaved/Coniferous Woodland; remaining semi-natural.
  - Country variations: England highest intensive-use share; Scotland with more Coniferous Woodland and montane/semi-natural areas; Northern Ireland and Wales with distinct land-use patterns and mosaics.
  - Temporal and spatial framework changes complicate direct comparisons with earlier CEH maps; LCM2007’s spatial framework is designed to support consistent future monitoring.

- Applications for monitoring and policy
  - Provides a consistent, repeatable evidence base for habitat monitoring, biodiversity surveillance, ecosystem services assessments, landscape planning, and catchment management.
  - Enables cross-site and national-scale comparisons over time; supports policy dashboards via 1 km summaries and governance-ready metadata.
  - KBEs allow regional customization and rule-based refinements to align with policy needs while maintaining a transparent processing history.

- Limitations and cautions for users
  - Class-specific accuracy varies; spectral separability issues for certain grasslands and upland habitats; caution when interpreting changes across LCM editions.
  - Change detection across editions remains difficult due to evolving spatial and thematic frameworks; aggregated-change approaches or re-alignment to a common spatial structure are recommended.
  - Comparisons with field surveys (CS) require careful interpretation of MMU, class definitions, and context-driven mapping differences.

- Example areas and data products
  - Demonstrates application across upland, calcareous grassland, urban, arable, fenland, and coastal mosaics.
  - Outputs include example maps, vector/raster product details, and guidance for applying LCM2007 outputs to monitoring frameworks.

- Data sources for broader monitoring context
  - Links to European products (Corine, LUCAS) and other national inventories; emphasizes integration with soils, geology, climate data, and sub-surface information for comprehensive land information systems.

- Appendices and additional resources
  - Bespoke validation approach and broader validation framing.
  - Broad Habitat Association rules and rationale (BHAs) to improve cross-dataset correspondences.
  - Glossary of terms, production metadata, and details on data access and licensing.

- Overall takeaway for monitoring frameworks
  - LCM2007 delivers a major step forward in UK land cover mapping with coast-to-coast coverage, a robust spatial framework, rich metadata, and knowledge-based enhancements that support policy-relevant monitoring.
  - It provides a parcel-based, transparent, and governance-ready platform for habitat monitoring and cross-country policy evaluation, while acknowledging limitations in class-specific accuracy and change detection across editions.