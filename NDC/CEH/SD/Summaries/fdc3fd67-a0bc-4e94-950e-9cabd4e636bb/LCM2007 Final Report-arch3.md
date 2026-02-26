# Final Report for LCM2007 - the new UK land cover map

## Overview and purpose
- Presents the first continuous parcel-based (polygon) UK land cover map (LCM2007) and derived raster products (25 m and 1 km) to support habitat monitoring and policy evaluation.
- Built to provide a policy-relevant, policy-ready evidence base for biodiversity assessments, ecosystem services, landscape planning, connectivity analyses, and catchment management.
- Aims to enable cross-country comparisons, trend detection, and integration with other data sources for environmental monitoring and planning.

## Data framework and inputs
- Spatial framework: parcel-based product derived from detailed national cartography (Ordnance Survey MasterMap and Large-scale Vector) for coherent integration with other national datasets.
- Spectral data: multi-temporal satellite imagery (Landsat TM/ETM+, SPOT, AWIFS, LISS-III) used to delineate spectrally homogeneous regions and enable change detection.
- Ancillary data: includes digital elevation, soils, urban boundaries, agricultural boundaries, and other contextual layers to support knowledge-based enhancements.
- Minimum mapping units: maintains a 0.5 ha MMU with multi-scale outputs (vector parcels, 25 m raster, 1 km summaries).

## Classification approach and enhancements
- Core method: parcel-based supervised classification (maximum likelihood) with 37 composite and 21 single-date images, mapped to 23 LCM2007 classes aligned to Broad Habitats (BH).
- Knowledge-based enhancements (KBEs): seven sequential rules/processes (terrain, soil, urban/coastal rules, etc.) applied post-classification to resolve spectral confusion and improve habitat specificity; resulted in reclassification of ~20% of parcels.
- Metadata and transparency: vector product includes extensive metadata, processing lineage, and KBE history for each parcel; probability distributions of top spectral variants are recorded for validation.

## Outputs and accessibility
- Outputs:
  - Vector: land parcels with attributes (area, source images, Broad Habitat, KBE history, etc.).
  - 25 m raster: 23 LCM2007 classes.
  - 1 km raster: percentage cover per class and dominant class per 1 km cell.
- Access and licensing:
  - 1 km raster data available via the CEH Information Gateway.
  - Full vector and 25 m raster products available on request under license; fees may apply.
  - Documentation and usage guidance accompany datasets.

## Validation, accuracy, and comparison with Countryside Survey (CS)
- Overall accuracy: approximately 83% when validated against ground reference data (field surveys and CS polygons); class-level accuracy varies.
- CS comparison findings (GB-wide and country-level):
  - Similar area estimates for some classes (e.g., Broadleaved woodland, certain grasses) defined by CS 2007 confidence limits.
  - Dissimilar area estimates for several habitats (Arable and Horticulture; Improved and Neutral Grasslands; Montane Habitats; Fen, Marsh and Swamp; coastal habitats) due to methodological differences, spectral confusion, temporal image requirements, and differences in spatial structure (parcel-based LCM vs field-based CS).
  - Key sources of discrepancy:
    - Differences in what CS and LCM2007 classify as “Arable and Horticulture,” including boundary features and temporary grass/uncropped land.
    - Spectral variability of arable land causing misclassification or overestimation.
    - Boundary and linear feature mapping differences due to MMU and parcel-based schema.
    - Grassland sub-types (Improved vs Neutral vs Calcareous/ Acid) and spectral ambiguity.
    - Fen, Marsh and Swamp: complex mosaics and small size leading to large differences; many CS “Fen” areas mapped as Rough Grassland or Acid Grassland in LCM2007.
- Summary conclusions from CS comparisons:
  - Grassland categories are particularly challenging; Broad Habitat Association (BHA) rules provide a third level of thematic accuracy to aid interpretation.
  - LCM2007 aligns well with CS for some classes in 1 km CS squares, but broad habitat extents often differ due to methodological structure and class definitions.
  - The comparison highlights the value of integrating multiple data sources and validation approaches to interpret habitat correspondences and trend analyses.

## Regional patterns and UK-wide context
- UK distribution: More than half of land cover is intensive use (Arable + Improved Grassland) or Built-up areas; woodland (~12%) split between Broadleaved and Coniferous; semi-natural and mountainous areas constitute the remainder.
- Country variations: England shows highest intensive land use; Scotland has substantial Coniferous Woodland and large semi-natural mountain/heath areas; NI and Wales show distinct mixes influenced by agriculture and urbanization patterns.
- Historic vs current maps: LCM2007 builds on LCM2000 with updated spatial framework and improved classification continuity to support change detection and policy evaluation.

## Implications for monitoring frameworks
- Data governance and openness:
  - Public sharing of underlying data can be a barrier; licensing and data governance influence openness and reuse.
  - Rich metadata and provenance are essential for monitoring integrity, reproducibility, and cross-country comparisons.
- Data integration and silos:
  - Success relies on integrating cartography, remote sensing, soils, elevation, and urban datasets across agencies; cross-domain collaboration is critical to reduce silos.
- Change detection challenges:
  - Differences in spatial structure (parcel-based vs CS field-based) and class definitions complicate direct change detection across time; stable spatial frameworks facilitate future monitoring but require harmonization across maps.
- Validation and "fit for purpose":
  - Bespoke validation emphasizes assessing usefulness for specific monitoring goals; parcel-level metadata enables targeted quality assessment using high-resolution imagery.
  - An informal Bayesian approach is suggested for evaluating consistency between imagery and LCM2007 attribution, enabling range estimates of accuracy per class.
- Policy-relevant capabilities:
  - Multi-scale outputs (vector parcels, 25 m, 1 km) enable both fine-scale habitat analyses and landscape-level reporting.
  - Broad Habitat and Broad Habitat Association (BHA) frameworks support policy needs for biodiversity surveillance, habitat connectivity, and Natura-target reporting.
  - Serves as a contextual base map for higher-resolution habitat mapping and network analyses, aiding woodland expansion planning, catchment assessments, and landscape planning.

## Relevance for policy and monitoring practice
- LCM2007 provides a robust, data-rich national basis for habitat monitoring, biodiversity assessments, ecosystem service evaluations, and landscape planning.
- The integration of KBEs and the BH/BHA framework enhances thematic resolution and interpretability for policy use.
- Provides a consistent UK-wide reference frame supporting country comparisons, biogeographical analyses, and cross-sector monitoring (climate, water, urban, agriculture, governance).

## Practical considerations for monitoring framework authors
- Emphasize use of the parcel-based spatial framework to improve comparability and change-detection potential over time.
- Leverage KBEs to reduce spectral confusion and improve habitat-specific accuracy, while documenting reclassifications for transparency.
- Rely on rich metadata and provenance to enable reproducibility and cross-site auditing.
- Incorporate both aggregated (1 km) and high-resolution (25 m and vector) products to satisfy diverse monitoring needs (macro-scale trend analysis and local policy decision-making).
- Plan for data access governance and licensing early to maximize data reuse while safeguarding quality and provenance.
- Use CS-like validation as a complementary benchmark, but interpret differences through a habitat-association lens (BHA) to better align cross-method results.

## Takeaways and conclusions
- LCM2007 advances national land cover mapping by delivering a parcel-based UK framework integrated with rich spectral and contextual data, enhanced by knowledge-based rules.
- The product suite supports policy-driven monitoring across scales, with clear pathways for data access, governance, and ongoing improvement.
- Comparisons with Countryside Survey reveal both strengths and areas needing careful interpretation, especially for grasslands and fen/bog mosaics, underscoring the value of multi-source validation and transparent association rules for monitoring design.
- To maximise monitoring utility, authors of monitoring frameworks should embrace the LCM2007 approach to spatial structure, metadata-rich outputs, and KBEs, while maintaining rigorous data governance and cross-agency collaboration.