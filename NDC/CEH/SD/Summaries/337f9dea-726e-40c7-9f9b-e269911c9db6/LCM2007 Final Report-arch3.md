# Final Report for LCM2007 - the new UK land cover map

- Purpose and audience
  - Provides a standardized, auditable UK-wide land cover baseline to inform biodiversity monitoring, landscape planning, policy evaluation, and future decision-making.
  - Targeted at managers and policymakers designing and governing environmental monitoring programs.

- What LCM2007 is (outputs and scope)
  - Vector product: 23 LCM2007 classes with rich attribute metadata, including processing history and knowledge-based enhancements (KBEs).
  - Raster products: 25 m resolution with 23 classes; 1 km summary rasters offering either percentage cover or dominant class per cell.
  - Multi-scale utility: UK-wide, with country-level breakdowns (England, Scotland, Wales, Northern Ireland) and ties to Broad Habitats for policy context.
  - Knowledge-based enhancements (KBEs): seven automated rules applied post-classification to improve thematic accuracy using contextual data (terrain, soils, urban context, coastal proximity, etc.).
  - Metadata and provenance: ProbList (top five spectral class candidates), CorePixels, and KBE history enable independent validation and traceability.

- Spatial framework and data sources
  - Built on detailed national cartography (Ordnance Survey MasterMap and LPS in NI) and integrated with external datasets (DEM, soils, urban areas, boundaries).
  - Image data: multiple sensors (Landsat, SPOT, LISS-III, AWIFS) across several years to create multi-date composites; 73 images used for summer-winter composites; remaining areas from single-date imagery.
  - Segmentation and classification: parcel-based approach with segment-level attributes; integration of segmentation with cartographic boundaries to form a UK-wide framework.
  - Image preprocessing includes cloud masking, atmospheric and topographic corrections; minimum mapping unit is 0.5 ha; 9–25 m pixel scale depending on product.

- Methodology highlights
  - Classification: supervised maximum likelihood on segment/polygon constructs, followed by a sequence of KBEs to reduce misclassification (notably for Grassland and upland habitats).
  - KBEs: incorporate terrain, soils, urban context, coastal proximity, water features, and other contextual cues; while they modify classifications, original spectral classifications (ProbList) are preserved to permit inspection or reversion.
  - Validation: ground reference validation with 9,127 points; overall accuracy around 83%, with class-specific variations.
  - Comparisons with Countryside Survey (CS) 2007:
    - Substantial but variable agreement depending on habitat type and aggregation level.
    - Grasslands and certain mosaics show notable discrepancies due to spectral variability, MMU differences, and one-to-many habitat relationships.
    - Fen, Marsh and Swamp areas show large differences due to land-cover mosaics and small patch sizes.
  - Broad Habitat Association (BHA) rules were developed to better align one habitat’s spectral signal with CS classifications across multiple aggregation levels.

- Data access, licensing, and governance
  - 1 km rasters: publicly available via CEH Information Gateway.
  - Full vector and 25 m rasters: available on request under licence (fees may apply).
  - Emphasizes metadata, data provenance, and processing transparency to support reproducibility and governance.

- Practical implications for monitoring frameworks
  - Provides a robust, auditable UK-wide baseline for habitat monitoring and policy evaluation.
  - Supports long-term change detection through a consistent, parcel-based spatial structure that can be reused and integrated with other datasets (e.g., CS, KBEs).
  - KBEs demonstrate how contextual information can enhance thematic resolution and reduce misclassification, guiding future rule-development in monitoring programs.
  - Outputs are scalable (UK-wide, country-level, 1 km summaries) to support governance, reporting, and policy analysis.
  - Highlights the importance of high-quality metadata and robust data governance to maximize data utility and openness.

- Key findings relevant to monitoring design
  - Data quality and accessibility challenges can hinder use (data gaps, access timeliness, silos, public sharing requirements, poor metadata, and data transformation needs).
  Data governance and transparent provenance are essential for credible monitoring.
  Grassland classifications remain problematic due to their one-to-many relationships with Broad Habitats; BHA rules help, but nuanced validation remains important.
  Fen, Marsh and Swamp areas are especially challenging to map consistently, necessitating potential integration with additional data sources or bespoke KBEs.

- Recommendations for policy and practice
  - Use LCM2007 as a contextual UK-wide base map (Broad Habitat level) to underpin higher-resolution habitat mapping, connectivity analyses, and biodiversity policy evaluation (e.g., Natura targets, woodland expansion planning).
  - Leverage the multi-scale product range to accommodate different reporting and governance needs (nation-level reporting, local planning, national-scale modelling).
  - Employ KBEs to improve classification reliability in monitoring applications, while maintaining traceability via ProbList and KBE histories.
  - Prioritize metadata quality, transparent data provenance, and governance mechanisms to ensure data openness and reproducibility.
  - Consider reorganizing earlier CEH land cover maps into a common spatial structure to improve cross-product change detection and trend analysis.

- Enduring value and broader context
  - LCM2007 delivers the first continuous parcel-based UK land cover map with coast-to-coast coverage, enabling comprehensive monitoring, ecosystem service assessments, carbon accounting, flood modelling, and urban planning support.
  - The framework aligns with European land cover initiatives (e.g., Corine) and European data infrastructures, enhancing comparability and policy relevance across Europe.
  - The report emphasizes that combining LCM2007 with in-situ data (Countryside Survey fieldwork) and other data sources yields a richer evidence base for environmental policy and planning.