# Mapping Quality Assurance Exercise

- Purpose: Assess and improve the quality and interoperability of Countryside Survey (CS) 2007 habitat mapping by comparing field survey data (CS) with QA data collected using a digital workflow, ensuring compatibility with national spatial datasets and enabling rapid analysis within a geodatabase.

- Context for Data Stewards: Demonstrates governance of large, multi-source spatial datasets, highlighting data standards, metadata/ provenance, change recording, and update mechanisms essential for datasets intended to be discoverable and reusable.

## Goals and Aims for Data Quality and Governance

- Ensure digital mapping reduces interpretation errors and provides clear, auditable attribute data.
- Use mandatory data fields and prompts to improve consistency and metadata completeness.
- Enable early data checking via an interactive wiki and QA visits to verify protocol adherence.
- Maintain QA processes that allow comparison against previous datasets (e.g., 1998 data) and support data sharing with other national datasets.

## Data Collection, Standards, and Tools

- Field collection: Surveyors used Surveyor software with mandatory fields and prompts; aim to minimize handwriting issues and ensure visit status visibility.
- Data integration: Immediate upload to a wiki for data checking; QA teams conducted field visits to verify protocols.
- Data architecture: Output data uploaded into a single geodatabase for analysis; common survey areas masked for comparisons.
- Documentation and transparency: Protocols and QA approaches documented to support reproducibility and governance.

## QA Methodology and Scope

- Extent: QA covered 23 x 1 km squares, designed to be representative across land classes and GB regions; some areas were not surveyed due to access issues.
- Approaches to QA:
  - 4.1 Direct comparison of aggregated areas/lengths/points per square.
  - 4.2 Raster comparisons: convert polygons to 10 x 10 m cells, assign dominant Broad Habitat, and compare raster grids.
  - 4.3 100-point grid: 100 points per square to compare Broad Habitat concordance; highlights mis-matches.
  - 4.4 Attribute-level analyses: cross-check species attributes for matched polygons.
- Data handling: Excluded unsurveyed or refused areas; aligned CS and QA datasets to common surveyed extents.

## Key Findings: Habitat-Level Agreement and Differences

- Overall concordance: High agreement between CS surveyors and QA across many Broad Habitats; most differences are small in extent and magnitude.
- Table-based results show:
  - 6.1a/b: Mean differences between QA and CS usually under 3.5% for most Broad Habitats; some habitats show larger SDs indicating potential differential allocation.
  - Notable discrepancies in certain habitats (e.g., Neutral vs Improved Grassland, Broadleaf vs Coniferous woodland, Dwarf Shrub Heath vs Blanket Bog, and upland/mosaic areas).
- Habitat-specific issues:
  - Blanket Bog: Major definitional and mapping challenges; revised 2007 field handbook descriptions led to mis-matches where wet heath and blanket bog overlapped; training and consistent definitions are critical.
  - Upland mosaics: Small-scale variability led to mismatches when mosaicked habitats were disaggregated for analysis.
  - Machair species/habitat on Scottish dunes caused localized anomalies; highlighted need for location-specific definitions.
  - Urban and grassland allocations: Instances where urban areas were recorded as Improved Grassland; indicates need for clearer urban/land-cover guidelines.
- Raster and 100-point analyses show:
  - Raster-level agreement averages around 60–90% across squares, with some squares showing high concordance (e.g., 364, 488) and others lower (e.g., 261, 773).
  - 100-point concordance generally strong (typical ranges 50–90%), but notable exceptions (squares 773 and 261 with lower concordance).
- Species attributes within polygons:
  - 45% of QA polygons had at least one matching listed species with the corresponding CS polygon.
  - Of polygons with matching species, 77% also matched Broad Habitat (BH).
  - Common species concordance varied by habitat; Improved Grassland and woodlands tended to have higher species concordance; Bracken and upland mosaics showed lower BH concordance despite species matches.
  - A broader 40% concordance across listed species indicates that species lists are more variable than habitat codes, reflecting difficulty in species-level identification and the influence of dominant species on habitat assignment.

## Linear Features, Points, and Change Recording

- Linear features (7.x):
  - High consistency in land-use theme assignment between QA and CS for linears; very few cases where QA recorded a feature not present in CS data.
  - Some ambiguity between certain forestry and woody-linear categories (FO vs WNS/WUS), but overall strong alignment.
- Point features (8.x):
  - High consistency in habitat codes for matched points; some confusion around woodland/forest coding noted.
  - Change recording on points generally consistent with QA, reinforcing protocol adherence.
- Change recording (9.x):
  - Change codes introduced: Real Change, Error Change, No Change.
  - Some surveyors needed time to adapt; QA exercise helped clarify usage.
  - Across habitats and features, change coding largely aligned with QA, though habitat-level change assessment remained challenging.

## Data Governance Implications and Recommendations

- Definitions and standards:
  - Harmonize habitat classifications with clear, consensus definitions (e.g., Blanket Bog, Dwarf Shrub Heath, Urban grassland) to minimize cross-team misclassifications.
  - Address mosaics and transitional habitats by refining field allocation matrices and post-field backallocation rules.
- Training and handbooks:
  - Invest in targeted training for upland and rare habitats (e.g., Scottish machair, Blanket Bog) to reduce misclassification risk.
  - Update field handbooks to clarify Woodland classifications and urban grassland boundaries; ensure consistent interpretation across teams.
- Metadata and provenance:
  - Maintain comprehensive metadata for all datasets, including habitat definitions, versioning, collection dates, data sources, and preprocessing steps (e.g., rasterization thresholds).
  - Ensure change logs and change-codes are preserved with polygon-level provenance for traceability.
- Data interoperability and updates:
  - Preserve geodatabase compatibility with national datasets; document schema mappings and attribute codings for easy integration.
  - Implement transparent update workflows for updates and embargoes; ensure updates propagate across portals and catalogs.
- Quality assurance tooling:
  - Leverage wiki and digital QA processes to enable ongoing, auditable checks; consider automated validation scripts for consistency in mandatory fields and cross-wield metadata.
  - Improve handling of mosaics, large upland areas, and rare habitats in QA design to minimize bias and misclassification.
- Future work:
  - Refine definitions and guidance for challenging habitats (e.g., Blanket Bog vs Dwarf Shrub Heath) and for interpretable species-habitat relationships.
  - Expand polygon-level species concordance analyses to better understand how species lists influence habitat allocation.

## Overall Assessment

- The 2007 Mapping Quality Assurance Exercise demonstrates strong data quality and a robust governance framework for large, multi-source ecological datasets.
- Digital data collection, early QA checks, and standardized metadata fields substantially improve data reliability and discoverability.
- Remaining challenges center on habitat definition harmonization, upland mosaic handling, and localized habitat variations, all of which are addressable through targeted training, clearer definitions, and enhanced provenance documentation.
- The exercise provides a concrete basis for ongoing data stewardship, interoperability, and iterative refinement of data standards for future surveys.