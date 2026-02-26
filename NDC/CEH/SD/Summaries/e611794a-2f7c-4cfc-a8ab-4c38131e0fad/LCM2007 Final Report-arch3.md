# Final Report for LCM2007 - the new UK land cover map

- Overview
  - CEH’s LCM2007 delivers a nationwide, parcel-based map of Broad Habitats for policy support, biodiversity monitoring, and ecosystem assessments.
  - Builds on earlier LCMs (1990, 2000) with a cartography-driven spatial framework linked to national datasets to improve spatial and thematic accuracy and enable change detection.

- Aim for monitoring frameworks
  - Provides UK-wide, auditable baseline data to inform multi-source environmental monitoring, policy evaluation, and decision-making.
  - Supports integration with policy-relevant indicators, ecosystem services, habitat connectivity, and catchment management.
  - Emphasises data provenance, traceability, and the ability to harmonise with other datasets for governance.

- Data sources and spatial framework
  - Spatial framework derived from detailed national cartography: Ordnance Survey MasterMap (OSMM) and LPS Large-scale Vector; NI framework from NI vector data.
  - MMU 0.5 ha; MFW 20 m; OSMM generalised to match MMU/MFW; segmentation aligned with agricultural boundaries and OS boundaries.
  - Ground reference data: over 9,000 points for training/validation; field data collected 2006–2008.
  - External datasets (cartography, DEMs, soils, urban areas, agricultural boundaries) underpin the spatial KBEs.

- Image processing, segmentation, and knowledge-based enhancements (KBEs)
  - Pre-processing: cloud masking, atmospheric/topographic correction, geo-registration; 6-band, 2-date composites created.
  - Segmentation: object-based framework from winter NIR, summer red, and summer MIR inputs; integrated with OS boundaries and agricultural outlines.
  - Classification: parcel-based supervised maximum likelihood classification into 21 single-date and 37 composite classes; iterative training/validation with ground data.
  - KBEs: seven automated rules applied post-classification to resolve spectral confusion and improve thematic resolution; incorporate contextual data (urban, coastal proximity, soils, terrain) to refine classes.
  - Impact of KBEs: modify around 20% of parcels; outputs recorded in vector attributes for traceability and user adjustments.

- Data products and metadata
  - Vector product: parcels with 10+ attributes detailing processing steps, including Construct, ProbList, KBE, and field codes; BH and BHSub classes stored; provenance tracked.
  - Raster products: 25 m resolution with 23 LCM2007 classes; 1 km raster products providing either percent cover or dominant class per cell.
  - Broad Habitats (BH) and Broad Habitat Associations (BHA) align with JNCC classifications; uncertainties documented.
  - Example areas and figures provided in the report illustrate application across landscapes.

- Access and licensing
  - 1 km raster data available via CEH Information Gateway.
  - Full vector and 25 m raster products available on request under licence; licensing fees may apply for some users/applications.

- Product scope and regional variation
  - Coverage across almost 10 million parcels ( GB ~8.6M; NI ~0.9M).
  - UK-wide distribution shows over 50% in intensive land use (Arable/Horticulture + Improved Grassland) or Built-up areas; timber and semi-natural areas constitute the remainder.
  - England shows highest proportion of intensive land use; Scotland has the largest share of semi-natural and montane habitats; regional differences in BH composition and land-use mix are notable.

- Comparison with Countryside Survey (CS) 2007
  - Two comparison approaches: CS 1 km squares vs LCM2007 BH; and CS national CS estimates vs LCM2007 BH extents.
  - Agreement varies by Broad Habitat; grassland classes are particularly challenging due to one-to-many relationships and field vs. spectral interpretation.
  - Arable and Horticulture tends to be overestimated by LCM2007 in UK-wide area estimates, influenced by spectral variability and inclusion of boundary features; temporary grass misclassification is a key driver.
  - Fen, Marsh and Swamp shows large UK-scale discrepancies (CS ~thousands of km2 vs LCM2007 ~hundreds) due to mosaic nature, small patch sizes, and spectral ambiguity; KBEs may offer routes to reassign some areas.
  - 1 km CS squares show higher correspondence for Arable and Horticulture, but broader habitat extents differ; BHA-level correspondences improve alignment (up to around 76–93% depending on context).
  - Overall, CS and LCM2007 are complementary; CS provides field-based nuances and small-scale features CS can capture that satellite imagery may miss; LCM2007 offers coast-to-coast, consistent UK-wide coverage and change-detection potential.

- Change mapping and limitations
  - Change detection across LCM1990, LCM2000, and LCM2007 is challenged by differences in spatial structure, class definitions, and spectral error (approx. 20%).
  - Robust real-change separation requires sophisticated methods; aggregating to consistent classes or focusing on stable classes could help.
  - The generalised spatial framework in LCM2007 provides a reusable structure to support future monitoring and change detection.

- Example areas
  - A series of example areas demonstrates LCM2007 performance in upland, calcareous, urban, arable, and fenland contexts, illustrating how different habitat mixtures are captured.

- Validation and uncertainty
  - Bespoke validation acknowledges no absolute truth in geography; aims to determine fitness for purpose relative to intended uses.
  - Parcel-level metadata enables users to assess which parcels are associated with which KBEs and their top spectral variants; this supports site-level validation against imagery in a Bayesian-like approach.
  - Validation highlights that some habitats (e.g., Bog, Montane) can be well captured, while others (e.g., Neutral/Improved Grassland) show more ambiguity.

- Broad Habitat Associations (BHAs)
  - BHAs provide rules for linking LCM2007 classes to Countryside Survey interpretations where direct correspondence is ambiguous (e.g., Bog ↔ Dwarf Shrub Heath/Acid Grassland; Montane ↔ upland grassland variants).
  - Rules are reciprocal where feasible and help rationalise cross-product correspondences for policy-relevant monitoring.

- European links and policy context
  - UK component contributes to Corine Land Cover 2006 (via vector-to-raster transformation) and aligns with pan-European monitoring initiatives.
  - LCM2007 builds on IMAGE2006 for European-wide earth observation efforts and supports cross-border environmental assessments.

- Implications for monitoring frameworks
  - Provides a robust, scalable UK-wide data platform suitable for multi-source integration in biodiversity, landscape planning, water and catchment management, and ecosystem service assessment.
  - Delivers a transparent, auditable processing chain (training data, segmentation, KBEs, validation) useful for governance and evaluation of policy impacts.
  - Public access to 1 km data enables broad analysis; full vector data can be licensed for higher-resolution or redistribution-restricted work.

- Conclusion for policy authors
  - LCM2007 offers a rigorous, data-rich baseline for habitat monitoring and policy evaluation, with a scalable spatial framework and traceable processing history.
  - While highly robust, some differences remain with field-based surveys (notably for semi-natural grasslands and upland habitats); careful use of BH vs. BH Associations is recommended when aligning with local monitoring programs.
  - The combination of national-scale cartographic structure with knowledge-based refinements enhances accuracy and enables proactive change planning, while metadata supports reproducibility and governance.