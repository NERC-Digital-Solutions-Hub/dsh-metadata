# Final Report for LCM2007 - the new UK land cover map

## Purpose and audience
- Presents the Land Cover Map 2007 (LCM2007), a national-scale, parcel-based land cover dataset for the UK designed to monitor habitat extent, landscape change, and support policy evaluation.
- Aims to provide an evidence base for biodiversity, ecosystem services, land-use planning, catchment management, and policy evaluation at multiple scales.

## Data framework and products
- Outputs include:
  - Vector product: land parcels with 23 LCM2007 classes mapped to Broad Habitats, plus 10 Aggregate classes.
  - Raster products: 25 m resolution (23 classes) and 1 km resolution (percentage cover and dominant class per square).
- Spatial framework:
  - Based on national cartography (Ordnance Survey MasterMap and LPS Large-scale Vector) for coherent UK-wide mapping and easier data integration.
  - Generalised spatial structure designed for reuse in future monitoring and change detection.
- Metadata and accessibility:
  - Parcel-level metadata captures processing steps and knowledge-based enhancements (KBEs) history.
  - 1 km rasters publicly accessible via CEH Information Gateway; full vector and 25 m data on request (licences may apply).

## Methods and knowledge-based enhancements
- Processing workflow:
  - Multi-date imagery (summer and winter) from Landsat, SPOT, and IRS sensors; image segmentation and maximum-likelihood classification.
  - Post-classification KBEs to reduce spectral confusion and boost thematic resolution, especially in complex contexts (urban, terrain, soils, coastal areas).
- KBEs are applied in a defined sequence; the original spectral classification remains accessible for re-derivation or user validation.
- Classification output:
  - 23 LCM2007 classes linked to Broad Habitats; 0.5 ha minimum mapping unit; 25 m raster and 1 km summary products.
- Data provenance and reproducibility emphasized to support monitoring across generations.

## Validation, comparison, and interpretation
- Validation:
  - Ground-reference validation with 9,127 points; overall class accuracy around 83%; accuracy varies by class (e.g., high producer’s accuracy but variable user’s accuracy for some habitats like Bog).
- Countryside Survey (CS) comparisons:
  - UK-wide and country-level comparisons show varying agreement by Broad Habitat.
  - High correspondence for some classes (e.g., Arable and Horticulture when compared to 1 km CS squares) but notable discrepancies for others (notably Fen, Marsh and Swamp; various grasslands).
  - Issues contributing to dissimilarities include differences in classification schemes, spectral variability (especially for arable), inclusion of boundaries, and MMU-related effects.
- Explanatory narrative:
  - Grassland classes are particularly problematic due to one-to-many relationships with Broad Habitats; leads to Broad Habitat Association rules to improve cross-wataset comparability.
  - Fen, Marsh and Swamp areas are complex mosaics; many CS-recorded Fens are mapped as Rough Grassland or Acid Grassland by LCM2007.
  - Montane, coastal, and boundary features have additional complexities in CS vs LCM mappings.

## Policy relevance and monitoring implications
- Provides a robust, hierarchical framework for monitoring habitat extent, connectivity, and landscape change across the UK.
- Supports policy areas including biodiversity status, ecosystem services, landscape planning, habitat networks, Natura targets, and river catchment assessments.
- Enables multi-scale analysis: high-resolution vector/raster data for national policy, plus 1 km summaries suitable for broader reporting and integration with other datasets.

## Practical considerations for monitoring frameworks
- Data governance and metadata:
  - Emphasises traceability of data processing steps; underlying data can be shared under governance/licensing frameworks.
  - KBEs rely on external data (urban boundaries, soils, terrain, coastal data) that require ongoing maintenance to stay current.
- Data gaps and barriers:
  - Data gaps, access constraints, data silos, variable metadata quality, and the need for data transformation are acknowledged barriers to policy use.
- Temporal and spatial change detection:
  - Change detection across LCM generations is challenging due to differing spatial structures and temporal coverage; recommended approaches include aggregating classes, focusing on consistently mapped classes, and trajectory analyses.
  Encourages reorganising earlier CEH maps into a common spatial structure to enable more robust change assessment.

## Outputs, access, and usage
- Main outputs:
  - UK-wide continuous vector product (parcels with attributes), 25 m raster, and 1 km summary products across 23 LCM2007 classes and 10 aggregates.
- Access channels:
  - 1 km rasters via CEH Information Gateway.
  - Full vector and 25 m data on licence from CEH (fees may apply).
- Documentation and user guidance:
  - Includes detailed metadata, knowledge-based enhancement history, and class mappings to Broad Habitats for policy alignment.

## Context within the monitoring landscape
- LCM2007 represents a major step in UK land cover mapping, delivering coast-to-coast coverage aligned with Broad Habitats and supported by a reusable spatial framework and KBEs.
- Enables integration with European datasets (e.g., CORINE) and complements Countryside Survey field data, providing a scalable, policy-relevant evidence base for current and future decision-making.
- While offering significant policy and monitoring value, the report cautions about temporal change interpretation and class-level accuracy limits for certain habitat types.