# Final Report for LCM2007 - the new UK land cover map

- CEH-led project delivering the first continuous parcel-based UK land cover map (LCM2007) aligned with Broad Habitats, using multi-source imagery and knowledge-based enhancements.
- Provides UK-wide baseline for habitat monitoring, biodiversity planning, ecosystem services assessment, and policy evaluation; supports change detection and policy appraisal across sectors.

## Data products and access

- Products
  - Vector: land parcels with rich metadata, processing history, Broad Habitat (BH) and Broad Habitat sub-classes, and knowledge-based enhancements (KBEs).
  - 25 m raster: 23 LCM2007 classes covering Great Britain and Northern Ireland.
  - 1 km rasters: two formats per 1 km cell — (A) percentage cover for each class, and (B) dominant class.
- Accessibility and licensing
  - 1 km rasters available via the CEH Information Gateway.
  - Full vector and 25 m rasters available on request under licence; fees may apply.
- Spatial framework
  - MMU: 0.5 ha minimum feature; robust parcel-based structure derived from OS MasterMap and Large Scale Vector data to aid integration with other national datasets.
- Documentation
  - Extensive metadata and provenance; KBEs are auditable and can be reverted if needed by users.

## Classification approach and knowledge-based enhancements (KBEs)

- Method
  - Parcel-based supervised maximum likelihood classification across multiple image composites (winter/summer and mid-IR).
  - Iterative refinement of classes and training polygons; manual edits and hole-filling as required.
- KBEs
  - Seven automated KBEs use contextual data (terrain, soils, urban influence, proximity to coast, etc.) to reassign parcels to more plausible classes.
  - KBEs affect ~20% of parcels, notably improving grassland and specific habitat distinctions (e.g., acid/neutral/calcareous grasslands using soils and altitude data).
  - Probabilistic spectral classifications retained in attributes, allowing users to revert KBEs if desired.
- Image processing
  - Pre-processing includes cloud/shadow masking, atmospheric/topographic corrections; segmentation merges multi-date data to delineate homogeneous segments.
  - Integration with OSMM cartography and agricultural boundaries to improve robustness.

## Validation and accuracy

- Overall accuracy
  - Approximately 83% across LCM2007 classes, based on 9,127 ground reference points.
- Class-level patterns
  - Higher accuracy for coniferous woodland and bog in some contexts; Neutral and Calcareous Grasslands, Neutral Grassland, and some fen/marsh types show more spectral confusion.
  - Grassland classes are particularly challenging due to spectral similarity and field-based habitat ambiguity.
- Interpretive guidance
  - Accuracy is class-specific; consider both Producer’s and User’s accuracies when assessing reliability.
  - KBEs and external data can reduce some misclassification but may introduce errors in other classes; KBEs are auditable and adjustable by users.

## Comparison with Countryside Survey (CS) 2007

- CS vs LCM2007
  - LCM2007 generally shows high correspondence for some categories but notable differences for others, driven by spatial structure, MMU, and habitat delineation.
  - Grassland and fen remnants show the largest discrepancies; the 1 km CS-based estimates align more closely with LCM2007 for some broad habitats, but disparities persist for aggregate vs. detailed classes.
- Specific observations
  - Arable and Horticulture area estimates differ due to classification scope, spectral variability, and inclusion of boundaries in LCM2007.
  - Fen/Marsh/Swamp exhibits large UK-scale differences due to mosaic nature and small patch sizes; may reflect mapping differences rather than pure change.
  - When grasslands are collapsed to a single class, correspondences with CS improve, illustrating the impact of thematic resolution on cross-dataset comparisons.
- Implications for monitoring
  - CS provides ground-truth context; LCM2007 offers coast-to-coast coverage and repeatability for national monitoring.
  - The two datasets are complementary; integrating field surveys with LCM2007 improves interpretation and policy-relevance.

## Practical implications for monitoring and policy

- Strategic value
  - Provides a consistent UK-wide evidence base for habitat monitoring, biodiversity planning, landscape planning, and ecosystem-services assessment.
  - Enables habitat network/connectivity analyses and supports Natura targets, woodland expansion planning, and catchment management.
- Governance and stewardship
  - Emphasizes data provenance, rich metadata, and transparent data handling, aligning with data governance needs for monitoring frameworks.
  - KBEs demonstrate how contextual data can increase thematic resolution while preserving traceability to spectral signals.
- Policy integration
  - Serves as a UK-wide frame of reference for country comparisons, and supports assessment of “naturalness” in river catchments as part of conservation objectives.

## Challenges and considerations for users

- Change mapping
  - Detecting real land-cover change is complex due to differences in class structure, sensor streams, and typical change magnitudes (~20% error in some cases).
  - Requires careful methodological handling to separate true changes from processing artefacts; aggregated class analyses can aid interpretation.
- Spectral confusion and habitat interpretation
  - Grassland classifications are particularly susceptible to spectral variability and field-based habitat differences; BH and BH Association rules help but are not perfect.
  - Some semi-natural habitats (Fen, Montane) show limited spectral separability, affecting accuracy.
- Spatial framework harmonisation
  - Differences in boundary data (e.g., NI specifics) and the reliance on OS MasterMap/LPS frameworks influence classification outcomes.
- Data use and comparability
  - When using LCM2007 for policy monitoring, consider aggregating grasslands or aligning with Countryside Survey approaches to improve comparability.
  - For fine-grained habitat trend assessment, supplement with higher-resolution or field data where possible.

## Change detection and cross-dataset reconciliation

- The report discusses the methodological difficulties in reconciling changes across LCM versions (LCM1990, LCM2000, LCM2007) due to differing spatial and thematic structures.
- Recommends approaches such as focusing on aggregated classes, prioritizing consistently mapped categories, and using trajectory-based statistics to reduce artefacts from data source changes.
- Advocates reorganising older CEH maps into a common spatial framework based on real-world land-use units to enable more robust change detection.

## European links and future directions

- Corine Land Cover (CLC) integration: UK component of Corine is derived from LCM2007 vector products, promoting pan-European environmental assessment.
- IMAGE2006 and European data synergy: LCM2007 benefited from pan-European data streams, supporting harmonised monitoring across Europe.
- Emphasis on integrating land-use information with subsurface (soil, geology) and climate data to improve monitoring insights and policy relevance.

## Key takeaways for authors of Monitoring Frameworks

- Use LCM2007 as a robust UK-wide baseline for habitat monitoring, change detection, and policy evaluation, while accounting for class-specific accuracies.
- Leverage the parcel-level metadata and KBEs to audit classifications and to adapt to local policy needs; ensure users validate KBEs against their context.
- When comparing with field surveys, be mindful of spatial and thematic differences; use aggregated classes or Broad Habitat associations to improve comparability.
- Combine LCM2007 data with other data sources (soil, climate, hydrology, LiDAR) to enhance interpretation for governance and decision-making.
- Plan for change detection by adopting common spatial structures and trajectory analyses to distinguish real changes from artefacts due to data sources or processing.
- Consider licensing, data governance, and open-data strategies to facilitate transparent monitoring and public accountability.