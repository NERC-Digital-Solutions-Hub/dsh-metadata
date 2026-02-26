# Final Report for LCM2007 - the new UK land cover map

## Overview
- Introduces the first continuous parcel-based UK land cover map (LCM2007) with nationwide coverage and a consistent set of land cover classes.
- Provides a suite of products at multiple resolutions (vector, 25 m raster, and 1 km summaries) to support habitat monitoring, biodiversity policy, ecosystem services, landscape planning, and catchment management.
- Improves spatial and thematic accuracy by deriving the spatial framework from detailed national cartography (OS MasterMap and LPS Large-scale Vector) and applying multi-temporal imagery with knowledge-based enhancements.

## What it contains
- Class structure: 23 LCM2007 classes mapped; aggregated to 17 Broad Habitats; minimum mappable unit 0.5 ha; vector and 25 m raster products; 1 km summaries (percent cover and dominant class).
- Coverage and imagery: near-coast-to-coast UK mapping using 20–30 m sensors (Landsat, SPOT, AWIFS); 91% of the UK mapped with multi-date composites; ground reference data for validation.

## Data and processing framework
- Spatial framework: GB built from OS MasterMap polygons (with agricultural boundaries); NI from LPS data; image pre-processing (cloud masking, atmospheric/topographic correction) and parcel-based segmentation.
- Knowledge-based enhancements (KBE): seven automated rules (e.g., terrain, soil, urban boundaries) applied post-classification to resolve spectral confusion and improve thematic resolution; some KBEs can be disabled to revert to base spectral results.
- Metadata and governance: per-polygon attributes record processing steps, KBE results, and provenance; rich metadata supports reproducibility and governance.
- Outputs and formats:
  - Vector: parcels with 10 core attributes (processing history, KBE results, probabilities, etc.).
  - Raster: 25 m resolution with 23 classes; 1 km rasters with percentage and dominant class summaries.

## Quality assurance and validation
- Validation dataset: 9,127 ground reference points (2006–2008).
- Overall accuracy: 83%; class-level accuracy varies (e.g., higher for Bog, Arable, Horticulture, Urban; more uncertain for Neutral Grassland and Montane habitats).
- Use of producer’s and user’s accuracies to convey reliability; results emphasize the need to consider both metrics for policy-relevant decisions.

## Comparison with Countryside Survey (CS)
- Purpose: assess how LCM2007 areas compare with CS 2007 Broad Habitats and national estimates.
- Key findings:
  - Agreement varies by Broad Habitat; LCM2007 aligns well for some classes but diverges for others, especially grasslands and fen/marsh–swamp mosaics.
  - Broad Habitat Associations (BHAs) were developed to interpret cross-walks where direct class-to-class mapping is inappropriate (e.g., grassland–habitat continua).
  - LCM2007 shows high correspondence with CS 2007 for Arable and Horticulture in 1 km squares, but total Broad Habitat extents can be overestimated by LCM2007 relative to CS.
  - Fen, Marsh and Swamp estimates differ by an order of magnitude due to complex mosaics and small patch sizes; many Fen areas mapped as Rough grassland or Acid Grassland in LCM2007.
- Implications:
  - Differences arise from spatial structure, minimum mapping unit, and class definitions; when interpreting CS–LCM2007 comparisons, use BHAs and aggregated classes to improve comparability.
  - Highlights the value of integrating multiple data sources (CS field surveys and satellite-derived LCM) for robust policy monitoring.

## Change mapping and temporal context
- Change detection between LCM2007 and prior maps is complex due to differing spatial structures and class definitions across time.
- LCM2007’s cartographic framework supports improved change detection in future mappings, despite interpretive challenges when comparing with earlier products.

## Access, licensing, and data availability
- 1 km raster products: available via the CEH Information Gateway.
- Full vector and 25 m raster products: available on request under licence; licence fees may apply for some users/applications.
- The study provides a range of data products to suit diverse monitoring needs and scales.

## Practical implications for monitoring and policy
- Provides a robust, nationwide evidence base suitable for multi-tier habitat monitoring, informing biodiversity policy, ecosystem services assessments, landscape planning, and catchment management.
- The coherent UK-wide spatial framework enables country comparisons and evaluation of policy applications across England, Scotland, Wales, and Northern Ireland.
- When used alongside Countryside Survey data, LCM2007 can support national-scale habitat estimates and trend analyses, but requires careful interpretation of differences in class definitions, spatial resolution, and boundary delineation.
- KBEs and rich metadata support reproducibility, auditable governance, and transparent monitoring frameworks; the system is designed to be re-run with updated imagery and knowledge bases for ongoing policy evaluation.

## Figures, figures and key figures
- 23 land cover classes; 17 Broad Habitats; MMU 0.5 ha; 25 m raster; 1 km summaries.
- 91% UK coverage with composite imagery; overall accuracy 83%.
- BH-based associations and cross-walking provide context for interpreting cross-class correspondences with CS.

## Data user guidance and cautions
- Expect spatial/thematic differences when comparing LCM2007 with field surveys (CS) or later updates; use Broad Habitat Associations to interpret cross-walks.
- KBEs are powerful for refinement but should be validated in critical areas to avoid misclassification.
- The continuous UK coverage and the ability to re-run KBEs offer a flexible framework for ongoing monitoring and policy evaluation.

## Broader context and European links
- LCM2007 contributes to European-scale assessments by enabling integration with Corine Land Cover mappings; it also aligns with pan-European datasets (e.g., IMAGE2006) that informed data sourcing and processing at the European level.