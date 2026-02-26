# Dataset documentation

## Overview
- Land Cover Map 2015 (LCM2015) is a parcel-based UK land cover map classifying satellite data into 21 Broad Habitat classes, built from Landsat-8 (30 m) with AWIFS (60 m) support.
- It updates the 2007 LCM and aligns with the JNCC Broad Habitat framework; designed for a broad user community with a per-polygon, per-plot data structure.
- Cautions: differences across LCM versions and between outputs mean LCM2015 is not recommended for current-change mapping without careful validation.

## What LCM2015 is for data leaders care about
- Provides a stable, archived data resource with rich metadata and uncertainty information to support governance, reporting, and data-driven decision making.
- Enables communication about land cover at multiple scales via multiple products (vector, 25 m raster, 1 km aggregates) and supports cross-dataset integration.

## Data products and structure
- Core products:
  - Vector data (GB and NI): polygons with 9 attributes including dominant class, pixel breakdown per class, uncertainty, and a unique geometry ID (gid).
  - 25 m raster: two-band product; band 1 is dominant class, band 2 is mean per-polygon probability.
  - 1 km raster products: dominant class and percentage cover per class (21 classes and 10 aggregate classes).
- Class structure:
  - 21 target LCM2015 classes based on UK Broad Habitats; several are further subdivided (e.g., Built-up Areas and Gardens into Urban and Suburban; Dwarf Shrub Heath into Heather and Heather grassland; Littoral Sediment into Saltmarsh and Littoral Sediment).
- Aggregates:
  - 1 km products include aggregated classes to simplify large-scale analyses.
- Spatial coverage and details:
  - GB and NI provided separately with different projections (Great Britain: British National Grid; Northern Ireland: TM75 Irish Grid).
  - Minimum mapping unit: >0.5 ha; polygons <0.5 ha and linear features <20 m dissolved into surrounding landscape.
- Uncertainty and probability:
  - Random Forest classifier provides per-pixel probability; reported as mean polygon probability (vector) and as band 2 in the 25 m raster.
- Data lineage and labeling:
  - Unique gid for each parcel; per-polygon pixel counts (Pix_dist) and dominant class (Modal_class) for display; composite image identifier tracks the data source year.

## Methodology highlights (beginning -> middle)
- Classification approach:
  - New: Random Forest classifier replaces previous maximum likelihood; handles multi-modal training data and simplifies training data preparation.
  - Ancillary data (e.g., slope, proximity to rivers, soil-related factors) are integrated as inputs rather than post-classification rules, enabling objective knowledge-based enhancements.
- Training data:
  - Start with a stable set of training areas classified consistently in 2000 and 2007; expanded for coastal areas and traditionally poorly mapped classes (e.g., Fen, Marsh and Swamp, semi-natural grasslands).
- Spatial framework:
  - Omit segmentation-based polygons used in LCM2007; move toward per-pixel classification with a simpler spatial framework to improve change detection potential.
- Output differences vs. LCM2007:
  - Montane class removed; rough grassland class removed; 25 m raster now two-band; per-polygon probability stored differently; sub-class spectral groupings removed; segmentation removed to reduce misalignment with final classifications.
- Woodland classification:
  - Mixed woodland treated by per-pixel classification with modal_class aggregation; pix_dist provides detailed breakdown for users needing finer interpretation.
- Data products and formats:
  - Vector and 25 m raster serve as core products; 1 km products provide broad-scale summaries; DOIs exist for all products to support reproducible usage.

## Data access, licensing, and citation (endpoints for governance)
- Data access:
  - 1 km raster products available via CEH Environmental Information Platform.
  - Full vector and 25 m raster products available on request under licence; licensing fees may apply.
- Projections and coordinates:
  - GB data in British National Grid; NI data in TM75 Irish Grid; explicit table values provided for coordinates and pixel dimensions.
- DOIs and citation:
  - All LCM2015 products have individual DOIs; citations should include the DOI in publications to support reproducibility.
  - Examples provided for GB vector, GB 25 m raster, GB 1 km products, and NI products (vector, 25 m, 1 km targets/aggregates).
- Usage notes:
  - LCM2015 is a stable, archived dataset intended for long-term analysis; users should refer to the accompanying documentation and appendices for class definitions and color mappings.

## Data quality, uncertainties, and caveats
- Change mapping caution:
  - Differences across time and methods mean that observed differences between LCM products reflect both real change and classification or framework changes; not all differences imply actual landscape change.
- Data quality and training:
  - The use of stable training areas plus enhanced ancillary data reduces some classification errors; uncertainties are quantified per polygon and per-pixel probabilities are available.
- Spatial considerations:
  - 0.5 ha MMU results in some exclusion of smaller features; coastal and near-shore areas may have limitations due to sensor resolution and mixed spectral signals.
- Metadata richness:
  - Extensive polygon-level metadata, including pixel distributions and probabilities, enhances traceability and supports quality control and data provenance.

## Practical takeaways for Data Leaders
- Governance and reproducibility:
  - Use DOIs to cite data; track data lineage from the composite images to final products; document processing steps for auditability.
- Data discovery and interoperability:
  - Access options across vector and raster formats with explicit class mappings and aggregation schemes facilitate integration with other datasets (e.g., meteorological or ecological models).
- Quality management:
  - Leverage per-polygon probability and pixel-level distributions to assess confidence; be mindful of caveats around change mapping and class definitions.
- Usage planning:
  - Choose product granularity based on task: vector for detailed analyses with metadata, 25 m for balanced detail and simplicity, 1 km for national-scale modeling and integrations.
- Citation and standards:
  - Follow the provided citation format and DOIs to support transparency and replicability in analytics and reporting.

References and further information
- CEH contact and access URLs provided for data products, documentation, and queries.
- Appendices contain detailed class definitions aligned with JNCC Broad Habitat classifications and standard color mappings for visualization.