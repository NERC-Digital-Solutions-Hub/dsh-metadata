# Final Report for LCM2007 - the new UK land cover map

- The project delivers the first continuous parcel-based (polygon) UK land cover map (LCM2007) built from a generalised national cartographic spatial framework (OS MasterMap and LPS Large-scale Vector) and enhanced with multi-temporal satellite imagery, plus a suite of knowledge-based enhancements.
- Outputs include a full UK vector product, a 25 m raster product, and 1 km aggregated products, mapped to 23 LCM2007 classes that align with 17 Broad Habitats; minimum mapping unit is 0.5 ha; minimum feature width about 20 m.
- The work aims to support biodiversity monitoring, habitat planning, ecosystem services, and policy development, while improving cross-year comparability and enabling change detection through a common spatial framework.

## Data sources and spatial framework

- Spatial framework
  - Based on detailed national cartography (Ordnance Survey MasterMap and Agricultural Large-scale Vector), generalised to meet the 0.5 ha MMU and integrated with image-derived segmentation.
  - Final UK framework merges cartographic parcels with image-segment data and agricultural boundaries to improve parcel density and classification accuracy.
  - Two UK-wide vector databases (GB and NI) ensure continuous coverage; nine processing chunks manage data volume and spatial overlap; a defined priority order ensures seamless UK-wide products.
- Inputs and scale
  - Demographic and boundary context: OSMM topography, agricultural boundaries, urban boundaries, soils, DEMs (e.g., NEXTMap Britain), and other boundary/context layers.
  - Data scale: vector parcels with 10 attributes (including processing history); 25 m raster with 23 classes; 1 km raster products (percent cover and dominant class).
- Minimum mapping unit
  - 0.5 ha (MFT 20 m) as the lower limit for map accuracy and consistency.

## Image processing, segmentation, and classification

- Pre-processing
  - Cloud and cloud-shadow masking; atmospheric correction; geometric correction achieving RMSE < 0.3 pixel; topographic correction using appropriate models; multi-date 6-band composites created to maximise spectral information.
- Segmentation and integration
  - Image segmentation applied to multiple composite images; spectral segments are integrated with OSMM parcels and agricultural boundaries to create a parcel-based spectral framework; Northern Ireland uses additional single-date segments as needed.
- Classification
  - Parcel-based supervised maximum likelihood classification using training data from ground references; 37 composites and 21 single-date images feed into 23 LCM2007 classes (mapped to 17 Broad Habitats).
  - Output includes ProbList (top five class probabilities per parcel) and final classification; manual edits applied only in rare cases.
- Edits and enhancements
  - Hole-filling and manual corrections (e.g., Landsat ETM+ data) in selected areas.
  - Knowledge-based enhancements (KBEs) applied post-classification to resolve spectral confusion and improve thematic resolution using contextual data (urban, coastal, terrain, soils, etc.).
  - Grassland and habitat-specific refinements include altitude-based adjustments for Montane Habitats and refined handling of various grassland types.

## Knowledge-based enhancements (KBEs)

- Purpose
  - Resolve spectral confusion and align classifications with Broad Habitats; incorporate contextual determinants not captured by spectral data alone.
- Data inputs and methods
  - Seven automated KBEs using urban boundaries, coastal outlines, terrain metrics (altitude, slope, aspect), soils, and other ancillary layers.
  - KBEs applied in a sequence, with iterative refinement and logging for traceability; approximately 20% of parcels are affected.
  - Outputs can be reverted if needed; knowledge-based rules refine parcels to more plausible land cover classes.
- Examples and limitations
  - Terrain- and soil-driven reclassifications (e.g., Montane adjustments), urban/coastal proximity adjustments, and enhanced discrimination among grassland types.
  - Potential for misclassification (false positives); region-specific suppression and validation recommended.

## Data products and access

- Data products
  - Vector product: full UK vector dataset with 10 attributes documenting processing stages (Construct, ProbList, KBE, etc.), including Broad Habitat sub-classes and FieldCodes; ProbList provides top spectral-class probabilities; KBE history retained for auditability.
  - Raster products: 25 m raster (23 LCM2007 classes); 1 km rasters with either percentage cover per class or dominant class per pixel.
- Access and licensing
  - 1 km rasters available via the CEH Information Gateway.
  - Full vector and 25 m raster data available under licence on request from CEH; licensing fees may apply for some users/applications.
- Data provenance and metadata
  - Detailed parcel-level metadata supports traceability of classification and KBEs, enabling user-driven validation against imagery and other data sources.

## Validation and comparability

- Ground-truth validation
  - 9,127 ground reference polygons collected 2006–2008; overall LCM2007 accuracy around 83%; class-specific accuracy varies (e.g., Bog ~93% Producer; Improved Grassland ~83% User; 89% Producer).
- Countryside Survey (CS) comparisons
  - CS 2007 comparison across GB-wide areas shows 62% correspondence at Broad Habitat level; 76% at Broad Habitat Association (BHA) level.
  - Grassland classifications show notable discrepancies; consolidating grasslands into a single class improves correspondence (e.g., 62% to 87–90% in some cases).
  - Fen, Marsh and Swamp (CS vs LCM2007) diverge dramatically due to the mosaic nature of Fen and small parcel sizes; many CS Fen areas map to Rough Grassland or Acid Grassland in LCM2007.
- Change mapping and interpretation
  - Comparisons between LCM2007 and CS are complicated by differing class definitions, spatial structures, and reference frameworks.
  - KBEs and altitudinal corrections affect change detection; direct one-to-one comparisons across versions (LCM1990/2000/2007) require sophisticated approaches.
- Summary takeaway
  - There is variable agreement across Broad Habitats; grasslands pose challenges due to one-to-many mappings; a common, habitat-referenced framework (Broad Habitat Associations) enhances comparability.

## Change mapping and comparability (chapter highlights)

- Change detection is hampered by spectral/classification differences and spatial structure changes across LCM generations.
- Aggregated/class-level analyses can provide more robust insights than direct cross-class change comparisons.
- Reorganising earlier CEH maps into a common spatial framework based on real-world land use units will facilitate more reliable change assessment.

## Practical implications for data support and usage

- The parcel-based spatial framework improves reusability, cross-year comparability, and potential for change detection, provided users apply consistent class interpretations.
- KBEs add discrimination power but require careful interpretation; users should treat certain sub-classes with caution and validate with ancillary data.
- The available multi-resolution products (vector, 25 m, 1 km) support diverse user needs:
  - Vector: detailed audit trail and per-parcel provenance for analysis and validation.
  - 25 m: finer detail without extensive metadata, suitable for some applications.
  - 1 km: suitable for UK-wide modeling and integration with other environmental datasets.
- Change detection and habitat-network analyses are feasible but require harmonisation with other data sources and careful handling of class definitions.

## Practical implications for data support and licensing (recap)

- Access routes:
  - 1 km rasters via CEH Gateway.
  - Vector and 25 m rasters licensed via CEH; licensing fees may apply.
- End-use considerations
  - Outputs are suitable for biodiversity policy, habitat monitoring, and landscape planning, with an auditable processing history.
  - Users should validate Broad Habitat-level outputs in their region of interest and consider using KBEs as guidance rather than definitive classifications in isolation.

## End note

- LCM2007 represents a significant advancement in UK land-cover mapping by integrating a robust, generalised spatial framework with multi-temporal satellite imagery and knowledge-based enhancements.
- The product provides scalable, auditable data suitable for policy-relevant analyses across a range of environmental and planning domains, while acknowledging ongoing challenges in grassland, fen, and change-detection comparability.