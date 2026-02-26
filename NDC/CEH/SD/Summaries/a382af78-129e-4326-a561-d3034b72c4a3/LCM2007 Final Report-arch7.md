# Final Report for LCM2007 - the new UK land cover map

- Purpose and scope
  - Delivers a continuous parcel-based UK land cover map (LCM2007) built from multi-temporal satellite imagery, aligned with Broad Habitats under the UK Biodiversity Action Plan.
  - Provides high-resolution vector parcels (with rich metadata) plus raster products (25 m and 1 km) to support nationwide analyses, policy, and monitoring.
  - Maps 23 LCM2007 classes to 17 Broad Habitats, with 0.5 ha minimum mapping unit (MMU) and robust provenance through processing history.

- Data sources and spatial framework
  - Spatial framework derived from detailed national cartography (Ordnance Survey MasterMap and LPS Large-scale Vector), generalised to support MMU/MFW constraints.
  - Image segmentation complements cartography, creating spectral regions not captured by maps alone; segmentation results are merged with cartographic parcels to enhance spatial coherence.
  - Northern Ireland incorporated segmentation to supplement limited cartography.
  - Minimum Feature Width (MFW) 20 m; MMU 0.5 ha; aim to balance detail with manageability across the UK.

- Image processing, segmentation, and classification workflow
  - Pre-processing: cloud/shadow masking, atmospheric correction (FLAASH), precise geo-registration (RMSE < 0.3 px), topographic correction using Minnaert model.
  - Image segmentation: all 60 composites segmented; three-band inputs (winter NIR, summer red, MIR) used to build a segment-based framework; segments merged with parcel boundaries for robust delineation.
  - Classification: parcel-based supervised maximum likelihood classifier applied to 37 composites and 21 single-date images; training areas from ground references and OS maps; provides a top-5 class probability list per parcel.
  - Knowledge-based enhancements (KBEs): seven automated rules (terrain, soils, urban/terrestrial delineation, water handling, etc.) applied post-classification; KBEs affect roughly 20% of parcels to improve thematic plausibility and offer alternative classifications in vector attributes.

- Grassland, habitat association, and accuracy considerations
  - Grassland mapping exhibits one-to-many relationships with Broad Habitats; Broad Habitat Association (BHA) rules added to improve interpretability and accuracy across grassland types.
  - Montane and coastal habitats rely on altitude/terrain context and spectral signals; some misclassifications persist in transitional zones.
  - KBEs and soil/altitude data help distinguish rough grassland vs. improved neutral/calcareous/acid grasslands and related Broad Habitats; some residual ambiguity remains.

- Product range and metadata
  - Vector product: parcel-based land cover with approximately 10 attributes documenting processing steps (Construct, ProbList, KBE history, etc.), including Broad Habitat sub-classes (BHSub) and FieldCode notes.
  - Raster products: 25 m resolution with 23 LCM2007 classes; 1 km resolution with two summary formats:
    - Percentage cover per 1 km pixel for each LCM2007 class.
    - Dominant LCM2007 class per 1 km pixel.
  - Aggregates: UK-wide data include 10 Aggregate classes (for simplified analyses) and 1 km rasters for quick landscape overviews.
  - Quality traceability: rich metadata enables reconstruction of classifications and provenance; target for reproducibility and audit trails.

- Validation, accuracy, and crosswalk with Countryside Survey (CS)
  - Ground-truth validation: 9,127 ground-reference polygons; overall LCM2007 accuracy around 83%, with class-specific producer and user accuracies varying (e.g., arable-related classes typically challenging due to spectral variability).
  - Countryside Survey (CS) comparison (CS 2007 and 1 km squares):
    - LCM2007 shows high correspondence with CS for some classes at the 1 km square level (notably Arable and Horticulture) but higher overall CS-based extents for several Broad Habitats than LCM2007.
    - Grassland classifications show notable mismatches; aggregating grasslands to a single class improves correspondence (up to ~87% in some comparisons).
    - Fen, Marsh and Swamp exhibits order-of-magnitude differences due to spectral complexity, small patch sizes, and mosaic nature; many CS mappings of Fen are recorded as Rough Grassland or Acid Grassland in LCM2007.
  - Implications: CS and CS 1 km estimates are scaled differently and reflect distinct methodologies; direct one-to-one class correspondences are imperfect, underscoring the need for habitat association rules and potential re-aggregation for certain analyses.

- Change mapping and limitations
  - Change detection is complex due to differences in class definitions across LCM1990–LCM2000–LCM2007 and evolving spatial structures.
  - Pixel-level misclassification errors (~20%) complicate attributing real change; robust change detection may require aggregating classes, focusing on consistently mapped classes, or using trajectory-based statistical methods.
  - The generalised UK spatial framework from LCM2007 provides a reusable baseline for future monitoring and change assessment.

- Access, licensing, and data availability
  - 1 km raster data available via the CEH Information Gateway.
  - Full vector product and 25 m raster product available on request under license; licensing and fees may apply.
  - Contact CEH data team or use the online portals to request access.

- Practical implications for GIS specialists
  - Provides a coherent UK-wide vector framework plus high-resolution raster products suitable for cross-border analyses, national monitoring, and policy support.
  - Knowledge-based enhancements enable contextual refinement when integrating terrain, soils, urban data, and other layers.
  - The nine-chunk production approach supports scalable UK coverage with consistent results across boundaries, benefiting habitat monitoring, landscape planning, ecosystem service assessments, and policy evaluation.
  - Users should account for class-level accuracy variability and potential CS-LCM misalignments when integrating with field surveys or legacy datasets.

- Appendix and validation concepts (highlights)
  - Bespoke validation emphasizes user-centered accuracy assessments; parcel-level metadata allows users to validate classifications with local imagery (informal Bayesian-style plausibility checks).
  - Broad Habitat Association (BHA) rules provide structured crosswalks between LCM2007 classes and Countryside Survey Broad Habitats to improve interpretability and cross-dataset comparability.

- Key outputs for GIS workflows
  - 23 LCM2007 classes mapped to Broad Habitats (0.5 ha MMU; 25 m raster).
  - Continuous UK vector land parcels with 10 provenance attributes and KBE history.
  - 1 km rasters offering both percentage cover and dominant class per cell, plus aggregated 10-class summaries.
  - Rich metadata and traceability to support reproducibility and auditing.
  - Access through CEH gateways with licensing options for full data products.