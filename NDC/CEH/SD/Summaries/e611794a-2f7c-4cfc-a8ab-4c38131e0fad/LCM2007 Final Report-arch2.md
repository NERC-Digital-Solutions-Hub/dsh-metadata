# Final Report for LCM2007 - the new UK land cover map

- Aims
  - Provide a consistent, data-driven view of UK land cover aligned to Broad Habitats for biodiversity action planning and policy monitoring.
  - Deliver a continuous UK-wide parcel-based spatial framework to support habitat monitoring, landscape planning, ecosystem services, and change detection.

- What LCM2007 is
  - UK-wide land cover map with 23 land cover classes (mapping land cover, not land use) and 17 Broad Habitats.
  - Outputs: vector parcel-based product, a 25 m raster (23 classes), and 1 km rasters (percentage cover and dominant class).
  - Spatial framework built from Ordnance Survey MasterMap and LPS Large-scale Vector; NI adapted with NI boundaries; parcel-based classification.

- Data sources and framework
  - Primary imagery: Landsat-TM5, IRS-LISS3, SPOT-4/5 (20–30 m); AWIFS as backup (60 m).
  - Multi-date composites (summer-winter) cover ~91% of UK; remaining from single-date imagery.
  - Segmentation and KBEs (knowledge-based enhancements) applied to refine parcel delineation and improve thematic resolution.
  - Additional data: digital elevation/Soils; urban boundaries; coastline context; agricultural boundaries; ground references; NI-specific datasets.

- Production: methods and workflow
  - Pre-processing: cloud masking, atmospheric/topographic corrections, geo-registration (target <0.3 px RMSE), compositing.
  - Segmentation: 60 composites segmented and linked to cadastral boundaries; NI segmentation with single-date data where needed.
  - Classification: parcel-based supervised maximum likelihood using 37 composite + 21 single-date images; training from ground references; iterative KBE refinement.
  - KBEs: seven automated algorithms (contextual data such as terrain, soils, proximity to coast, urban context, water, etc.) to reclassify parcels and resolve spectral ambiguities; users can disable KBEs.
  - Validation: ground reference data from 2006–2008; 9,127 points; overall accuracy ~83% across LCM2007 classes; cross-checks with Countryside Survey (CS) data and year-to-year consistency.

- Product range and outputs
  - Vector dataset: 10 attributes documenting processing steps (Construct, ProbList, KBE results, etc.).
  - Raster data:
    - 25 m resolution: 23 LCM2007 classes.
    - 1 km resolution: two products per location – (a) percentage cover per class, (b) dominant class.
  - Coverage: UK-wide with GB and NI maintained as two databases for compatibility.

- Access and usage
  - 1 km rasters: CEH Information Gateway.
  - Full vector and 25 m rasters: license-on-request from CEH (data@ceh.ac.uk); some applications may incur fees.

- Change mapping considerations
  - Change detection is complex due to:
    - Different class definitions across LCM1990, LCM2000, and LCM2007.
    - Varied spatial structures and typical per-image classification errors (~20%).
    - Lack of robust, consistent methods to separate real change from artefacts.
  - Recommendations: focus on aggregated class changes, or use a common spatial framework to align older maps to current structures; consider reclassifying into common units for robust change assessment.

- Comparison with Countryside Survey (CS) 2007
  - Broad Habitat correspondence with CS 2007 for 1 km squares various by habitat type; grassland types particularly challenging.
  - Grassland: spectral variability and one-to-many mapping to Broad Habitats drive discrepancies; Broad Habitat Association rules were developed to improve cross-class correspondences.
  - Major patterns:
    - LCM2007 aligns well with CS for some broad extents (e.g., Conifer/Broadleaved Woodland extents similar in several respects).
    - Arable and Horticulture areas in LCM2007 are often higher than CS 2007 estimates, partly due to classification differences, inclusion of boundary/linear features, and temporal composition effects.
    - Fen, Marsh, and Swamp shows large discrepancies (CS 2007 vs LCM2007) due to the mosaic nature of fen and small patch sizes; many CS fen areas map to Rough Grassland or Acid Grassland in LCM2007.
  - Implications: LCM2007 is broadly consistent with CS for major habitats and UK-wide scales but differences reflect methodological choices, MMU, and remote-sensing limitations in complex mosaics.

- UK land cover distribution (summary)
  - UK-wide: >50% in intensive land use (Arable + Improved Grassland) or Built-up Areas; ~12% Broadleaved and Coniferous Woodland combined; remainder semi-natural (including Mountain, Heath, Bog, semi-natural grasslands).
  - Country variation: England highest share of intensive land use; Scotland highest proportion of Coniferous Woodland and largest semi-natural mountain/peat areas; Northern Ireland and Wales show intermediate patterns.

- Validation, accuracy, and caveats
  - Overall accuracy around 83% across classes; class-level accuracy varies (grasslands and mosaics particularly variable).
  - Validation includes CS comparison and cross-year consistency checks; Fen, Marsh, Swamp areas are especially tricky to map spectrally due to mosaic character.
  - The dataset provides parcel-level metadata (KBE history and top-5 class probabilities) enabling users to assess and validate classifications locally.

- Key figures and highlights
  - LCM2007 delivers a UK-wide, parcel-based land cover map aligned to Broad Habitats with enhanced spatial and thematic resolution relative to earlier maps.
  - Outputs support habitat monitoring, policy assessment, landscape planning, and cross-border comparisons.
  - Data accessibility via CEH platforms enables integration into environmental monitoring workflows.

- Conclusions
  - LCM2007 provides a robust, continuous UK-wide land cover map with a reusable spatial framework for monitoring and policy evaluation.
  - The integration of multi-date imagery, a parcel-based structure, and knowledge-based enhancements improves spatial and thematic fidelity, but known challenges remain for grassland mosaics, fen, upland features, and small coastal elements.
  - The product supports multi-tier habitat monitoring, policy evaluation, and change detection, with metadata-rich outputs to track processing history.
  - Access to datasets through CEH platforms facilitates uptake by researchers and policymakers, supporting evidence-based environmental management.

- Appendices and context (for analysts)
  - Broad Habitat Association (BHA): rules linking LCM2007 classes to CS Broad Habitats; addresses cross-mapping for complex mosaics (e.g., Bog, Dwarf Shrub Heath, Montane).
  - Bespoke validation approaches emphasize using parcel-level metadata and a Bayesian-like, fuzzy validation approach to gauge plausibility of classifications at target classes.
  - The report positions LCM2007 as part of a broader, Europe-oriented framework (e.g., support for CORINE linkage) and as a foundation for future change detection within a common spatial framework.