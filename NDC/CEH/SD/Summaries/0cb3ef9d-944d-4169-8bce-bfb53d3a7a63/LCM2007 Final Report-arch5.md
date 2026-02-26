# Final Report for LCM2007 - the new UK land cover map

- Objective and scope
  - Delivers the first continuous parcel-based (vector) UK land cover dataset with a suite of raster products (25 m and 1 km) for UK, GB, England, Scotland, Wales, and Northern Ireland.
  - Aligns with Broad Habitats to support biodiversity, ecosystem services, landscape planning, policy, and monitoring; provides a robust baseline for change detection and policy analysis.

- Data governance, provenance, and spatial framework
  - Spatial framework derived from detailed national cartography (Ordnance Survey MasterMap and LPS Large-scale Vector) to ensure stable, reusable boundaries.
  - Vector product: 23 LCM2007 classes with 10 polygon-level attributes; comprehensive metadata, processing logs, and knowledge-based enhancements (KBE history).
  - MMU and feature width: minimum mapping unit 0.5 ha; minimum feature width 20 m.
  - Knowledge-based enhancements (KBEs) are applied post-classification with auditable logs; KBEs can be revisited or reversed by users via ProbList and KBE history.

- Data sources and acquisition
  - Satellite imagery: multi-date composites from Landsat TM/ETM+, SPOT-4/5, LISS-III, AWIFS; target year 2007 with some multi-year inputs to fill UK coverage gaps.
  - Ancillary data: OS MasterMap topography, LPS vector, agricultural boundaries, urban outlines, soils, digital elevation, and regional soil data; coastal and urban context data integrated to refine classifications.

- Production workflow
  - Pre-processing: cloud/mask, atmospheric and topographic corrections; image-to-image geo-registration accuracy aiming for high precision.
  - Segmentation and framework assembly: image segmentation integrated with cartographic boundaries to form a stable parcel-based framework.
  - Classification: parcel-based supervised maximum likelihood classification using 37 composites and 21 single-date images; training data from ground references; iterative refinement with manual edits and hole-filling.
  - KBEs: seven automated rules (e.g., urban context, coastal proximity, terrain, water, within/outside urban boundaries, soil) applied sequentially to improve thematic resolution; logs stored with the vector product; reversion possible.
  - Change mapping: cross-year mapping between LCM1990, LCM2000, and LCM2007 is complex due to differing class definitions and structures; reliable separation of real changes from error not fully established.
  - Validation: 9,127 ground reference points used; overall accuracy reported at 83% across 23 classes; class-level accuracies vary.

- Data products and metadata
  - Vector product: 23 land cover classes with 10 polygon attributes (Construct, ProbList, KBE, etc.); includes Broad Habitat sub-classes (BHSub) for debugging and user exploration.
  - Raster products: 25 m resolution with 23 classes; 1 km raster products providing percent cover and dominant class per cell.
  - Metadata and data lineage: extensive provenance information, including dataset origin, processing steps, spectral signatures, and KBE history; ProbList preserves top spectral variants for user validation.
  - Access and licensing: 1 km rasters available via the CEH Information Gateway; full vector and 25 m raster data on request under licence; fees may apply; contact CEH data services.

- Knowledge-based enhancements and algorithms
  - KBEs cover seven domains (urban context, coastal proximity, terrain, offshore, within/outside urban boundary, water, soil integration) to resolve spectral confusion and improve habitat-specific mapping.
  - KBEs applied in sequence to reclassify parcels toward more plausible land cover; posterior classifications stored while preserving original spectral class in ProbList to allow user-driven adjustments.
  - Soil and terrain data are particularly important for distinguishing grassland types and resolving ambiguous semi-natural classes.

- Validation, comparison with Countryside Survey (CS)
  - CS-based comparison shows variable agreement across Broad Habitats; grassland categories (and their BH associations) are especially challenging due to one-to-many mappings.
  - LCM2007 aligns well with CS area for certain classes (e.g., Arable and Horticulture at coarse scales) but shows discrepancies in others due to spectral variability, boundary delineation, and MMU differences.
  - Notable divergences include Arable and Horticulture (LCM2007 higher than CS estimates), and Fen, Marsh and Swamp (CS vs. LCM2007 differences driven by habitat mosaics and patch sizes below MMU).
  - KBEs help improve correspondence in several areas but cannot fully resolve all discrepancies caused by spatial structure and data differences.

- Practical implications for data stewards
  - Rich metadata and processing logs enable traceability, reproducibility, and auditable classification decisions; KBEs and ProbList support user-driven validation and adjustments.
  - Licensing considerations: some data are openly accessible; others require licences with potential fees; ensure compliance when sharing or reusing.
  - Use cases: high-level habitat mapping, landscape-level analyses, integration with CS outputs, and baseline data for policy-relevant assessments; 1 km rasters are suitable for nationwide modeling and comparisons with CS outputs.
  - Limitations: change detection across years remains challenging due to evolving spatial and thematic structures; spectral confusion persists in semi-natural upland areas; cross-dataset comparisons require careful interpretation and an understanding of boundary delineation differences.

- Access points and governance
  - Primary access: CEH Information Gateway for 1 km rasters; vector and 25 m rasters available by licence on request via CEH data portals.
  - Licensing and terms: expected to involve some fees depending on use-case; ensure adherence to data licensing terms.

- Significance and future opportunities
  - LCM2007 represents a major advance with a reusable spatial framework anchored to static national cartography, enabling consistent monitoring and future change detection.
  - The KBEs provide enhanced thematic resolution in difficult areas; ongoing work could further harmonize outputs with Countryside Survey, refine change-detection methodologies, and expand validation using additional data sources.
  - European integration: LCM2007 supports Corine Land Cover mapping through translation from vector outputs, contributing to pan-European environmental assessment.

- Key takeaways for data stewards
  - Comprehensive provenance and auditable processing history are embedded in the vector product, with KBEs logged and ProbList available for validation.
  - A robust licensing and access framework supports wide reuse, with clear pathways to obtain full vector data and 25 m rasters.
  - The project provides a solid, policy-relevant baseline for UK land cover, while highlighting methodological challenges and opportunities for improved interoperability and change detection in future updates.