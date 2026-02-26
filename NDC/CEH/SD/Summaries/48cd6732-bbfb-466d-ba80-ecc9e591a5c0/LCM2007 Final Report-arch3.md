Final Report for LCM2007 - the new UK land cover map

- Purpose and scope
  - Introduces the UK Land Cover Map 2007 (LCM2007) as a continuous, parcel-based land cover product to inform biodiversity assessments, habitat monitoring, landscape planning, and policy evaluation.
  - Builds on previous LCM iterations and provides a policy-relevant, auditable evidence base for habitat monitoring and decision-making across the UK.

- Data sources and spatial framework
  - Multi-sensor imagery: Landsat TM5, IRS LISS3, SPOT-4/5 (20–30 m) with AWIFS as backup; combined into 34 multi-date composites from over 70 images.
  - Spatial framework: Great Britain uses OS MasterMap topography; Northern Ireland uses LPS LV polygons; integration creates a continuous UK-wide vector framework with MMU of 0.5 ha and minimum feature width of 20 m.
  - Pre-processing: cloud/shadow masking, atmospheric and terrain corrections, geo-registration (target RMSE < 0.3 px), and generation of 6-band composites; image segmentation to create homogeneous parcels and integration with cartographic boundaries.
  - Change mapping considerations: acknowledged difficulties in separating real land-cover change from misclassification due to differing spatial structures across LCM editions and spectral confusion.

- Classification approach and knowledge-based enhancements
  - Parcel-based supervised maximum likelihood classification using 37 composites and 23 land-cover classes mapped to 17 Broad Habitats.
  - Training data derived from ground references; iterative refinement to meet target accuracy.
  - Knowledge-based enhancements (KBEs): seven automated rules applied post-classification to reduce spectral confusion by incorporating context (urban, coastal proximity, terrain, soil, etc.).
  - KBEs affect about 20% of parcels and enable post-hoc adjustments (e.g., reclassifying urban-adjacent areas to more realistic habitat types).
  - Thematic resolution improvements: KBEs assist when optical data alone cannot reliably distinguish certain Broad Habitats (e.g., various grasslands distinguished by soil and context).

- Data products and metadata
  - Core products:
    - Vector parcel dataset with 10-stage attributes (including Construct, ProbList, and KBE attributes) and Broad Habitat classifications.
    - Raster products at 25 m resolution with 23 LCM2007 classes.
    - 1 km raster products providing either the percentage cover or the dominant class per 1 km square (for both 23 classes and 10 aggregates).
  - Coverage and access:
    - 23 land-cover classes (not land-use) with 0.5 ha MMU; UK-wide vector with GB and NI in separate databases.
    - Rich metadata documenting processing steps; 1 km data via CEH Information Gateway; full vector and 25 m data available on request (licence may apply).

- Validation and performance
  - Validation: ground reference points collected 2006–2008 (9127 points used for final validation); overall accuracy around 83% across classes; class-level accuracy varies.
  - Producer’s vs User’s accuracy reported for individual classes (e.g., Bog shows high Producer’s accuracy but lower User’s accuracy).
  - Comparison with Countryside Survey (CS) 2007:
    - GB-wide correspondence ~62% at Broad Habitat (BH) level; ~76% at Broad Habitat Association (BHA) level; ~67–76% depending on country and level.
    - Consolidating grassland classes improves correspondence (up to ~87–90% at BH/BHA levels).
    - Major divergence in grassland (Neutral/Improved), conifer/broadleaf woodland distinctions, upland mosaics (Bog, Montane, Acid/Calcareous Grasslands), and Fen, Marsh and Swamp due to spectral and structural differences.

- Change mapping and monitoring implications
  - LCM2007 provides a robust, repeatable spatial framework for habitat monitoring, biodiversity assessments, ecosystem services analysis, and landscape planning.
  - Change detection is challenged by differing spatial structures across editions and by classification error dominating apparent changes; separation of real change from error requires methodological development.
  - Reconciliation strategies include focusing on aggregated classes, using consistently mapped classes, or reorganising earlier CEH maps into a common spatial structure based on real-world land-use units.

- Policy relevance, monitoring utility, and applications
  - Supports multi-tier habitat monitoring, biodiversity reporting, ecosystem services analysis, catchment management, and landscape planning.
  - Serves as a consistent UK-wide baseline for policy evaluation and cross-country comparisons; enables assessment of habitat networks and connectivity for biodiversity targets (e.g., Natura contexts).
  - European linkage: UK component contributing to Corine Land Cover (CLC) via vector-derived generalisation and transformation; aligns with pan-European monitoring efforts (e.g., IMAGE datasets).

- Data governance, access, and future directions
  - Data governance includes metadata traceability, QA, and the KBE processing history to support user validation and transparency.
  - Access channels: CEH Information Gateway for 1 km rasters; full vector and 25 m data under licence; fees may apply.
  - Future monitoring implications: the standardized spatial framework supports efficient updates and consistent change detection; suggests integrating additional data sources and refining KBEs to reduce uncertainties in problematic classes (e.g., certain grasslands and upland mosaics).

- Key takeaways for monitoring framework authors
  - A national, policy-relevant land cover product can be built from multi-sensor, multi-date imagery and a robust knowledge-base, anchored to a consistent spatial framework.
  - Detailed metadata and the ability to trace classifications through KBEs enhance transparency and support governance.
  - High overall accuracy does not eliminate class-level uncertainties; explicit reporting and guidance are essential for decision-making.
  - Aligning spatial structure across time and with other land-cover frameworks (e.g., CS, Corine) improves interpretability of change and policy-relevant analyses.