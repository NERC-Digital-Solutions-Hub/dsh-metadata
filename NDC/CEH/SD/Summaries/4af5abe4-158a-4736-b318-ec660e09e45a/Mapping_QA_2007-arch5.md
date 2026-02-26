# Mapping Quality Assurance Exercise

- Purpose: Assess the quality and consistency of digital habitat mapping for Countryside Survey 2007, ensuring data are suitable for rapid analysis, integration with other national datasets, and long-term governance.

- Context and goals for Data Stewards:
  - Transition to field-based digital mapping (Surveyor software) to reduce in-field subjectivity and improve data clarity and attribute capture.
  - Early, ongoing data quality checks via an interactive wiki and QA teams to enforce protocols.
  - Produce data compatible with a geodatabase and suitable for cross-dataset analysis.

## Methods and Data Architecture

- Digital data capture and validation
  - Field surveyors used Surveyor software with mandatory fields and prompts; data uploaded to a wiki for prompt office-based checks.
  - QA teams conducted field QA visits to ensure protocol compliance.

- QA approaches (methods applied across data types)
  - 4.1 Direct comparison of aggregated areas/lengths/points per 1 km square (CS vs QA data).
  - 4.2 Raster data comparisons: convert polygons to 10 x 10 m rasters; compare dominant Broad Habitats.
  - 4.3 100-point grid analysis to evaluate concordance of Broad Habitats at a fixed resolution.
  - 4.4 Attribute-level comparisons for areas, lines, and points using reference ID layers.

- Surveyor efficiency and data capture
  - Use of visit status layers, recording of dominant species, and reduced refusals through digital workflows.
  - Average not-visited land was low in many squares; some landowners restricted access.

## QA Coverage and Scale

- Extent and sampling
  - QA mapped data covered 23 1 km squares; aimed to be representative across land classes and GB regions.
  - Access refusals and not-visited areas constrained some coverage but were accounted for via masking common surveyed areas.

- Data flow and integration
  - Datasets from CS surveyors and QA teams were aligned on common surveyed areas for robust comparisons.
  - Analyses employed both aggregate statistics and spatially explicit comparisons (rasters, grids, and polygons).

## Key Findings: Data Quality and Agreement

- Overall agreement between CS surveyors and QA teams
  - High level of concordance for many Broad Habitats; mean differences in proportions often under 3.5% across several habitat types.
  - Direct area/length comparisons showed many squares with strong alignment, though some variability existed.

- Raster-based comparisons (per square)
  - Overall raster agreement across squares averaged around 76%, with notable outliers (e.g., squares 261 and 773 showing lower concordance; squares like 364 and 488 showing very high concordance up to 98%).
  - Some squares exhibited habitat-specific disagreements, guiding attention to definitions and mapping practices.

- 100-point point-in-grid concordance
  - Most squares demonstrated good concordance, but a few squares showed significant mismatches (e.g., 773 at 19–23% concordance, 261 around 41%).

- Habitat-definition challenges and notable issues
  - Blanket Bog: substantial mis-matches with Dwarf Shrub Heath in some squares; ongoing debates about definitions and field interpretation.
  - Neutral vs Improved Grassland: overlap in species composition led to allocation differences; generally balanced between CS and QA.
  - Woodland definition: issues with broadleaf vs coniferous woodland allocations; mosaics in upland areas complicated precise matching.
  - Machair habitat on Scottish sand dunes introduced local anomalies; largely aligned with Neutral/Improved Grassland categories.
  - Upland mosaics: mosaicked habitat mapping introduced mismatches when disaggregated into component Broad Habitats.

- Species attributes (polygon-level)
  - 45% of QA polygons matched with at least one listed species in the corresponding CS polygon.
  - Species concordance across polygons tended to be lower than habitat concordance, reflecting high species diversity and dominance effects.
  - Common species (e.g., Lolium perenne) showed higher concordance than some others.

- Point and linear features
  - Point and linear feature habitat codes showed high consistency between CS and QA data; the change-codes for these features were generally well aligned.

- Change recording
  - Introduction of an explicit change field (Real change, Error change, No change) improved update capability but added complexity.
  - Overall, there was broad agreement on change coding across many habitat types and linear/point features, though some habitat categories showed more variability in coding.

## Habitat- and Data-Specific Insights

- Broad Habitats with notable discrepancies
  - Improved/Neutral Grassland and Broadleaf/Coniferous Woodland showed more frequent cross-allocation in some squares.
  - Urban areas occasionally misclassified as Improved Grassland, indicating field-collection guidance needs reinforcement.
  - Dwarf Shrub Heath and Blanket Bog mismatches were particularly evident in upland squares.

- Mosaic and continuum challenges
  -1: mosaics in upland or transitional zones created matching ambiguities when disaggregating into component Broad Habitats.
 2: differences in field interpretation vs. QA interpretation highlighted the need for clearer, harmonized keys and training.

## Implications for Data Governance and Stewardship

- Data standards and interoperability
  - Need for harmonized habitat definitions, especially for tricky cases like Blanket Bog, Neutral/Improved Grassland, and woodland types.
  - Clear guidelines for mosaicked landscapes and how to allocate areas to competing habitat categories.

- Metadata, provenance, and versioning
  - Maintain audit trails for habitat allocations, change codes, and species lists per polygon.
  - Document the mapping methodology, definitions used, and any revisions stemming from QA findings.

- Change management and data updates
  - Implement a robust workflow for applying QA-driven corrections to previous datasets (e.g., 1998 vs 2007 changes).
  - Ensure that “change” fields are consistently filled and interpreted across future surveys.

- Training and governance controls
  - Targeted training to address habitat-definition uncertainties (e.g., Blanket Bog, woodland types) and to reduce mosaic-induced mismatches.
  - Standardize field handbook interpretations and ensure Field Handbook and QA tools align with the published definitions.

## Recommendations and Next Steps

- Strengthen habitat definitions and mapping guidance
  - Revise and harmonize field keys for problematic habitats ( Blanket Bog, Neutral vs Improved Grassland, Woodland types, Machair).
  - Provide explicit handling rules for mosaics and transitional habitats to improve cross-squad consistency.

- Enhance training and QA procedures
  - Expand QA sampling in identified problematic squares (e.g., 261, 773) to reduce systematic mismatches.
  - Offer refresher training on recent field handbook changes and the interpretation of complex habitats.

- Improve change recording governance
  - Standardize interpretation of “change” across habitat types; ensure consistent use of Real vs Error vs No Change fields.
  - Integrate change updates into versioned datasets with clear provenance.

- Strengthen data integration and documentation
  - Ensure metadata clearly documents data collection methods, software versions, QA procedures, and square-level coverage.
  - Maintain an accessible log of habitat-definition decisions and their rationales for future re-use and comparison.

- Data quality benchmarks for future cycles
  - Establish target concordance thresholds (e.g., >75% raster/point concordance across squares; habitat-level agreement >70–80% for key habitats) to guide ongoing QA and harmonization efforts.

- Governance-ready outputs
  - Publish QA findings and reconciled definitions as part of data governance documentation to support discoverability, reproducibility, and reuse.

- Overall takeaway for Data Stewards
  - The 2007 Mapping Quality Assurance Exercise demonstrates strong overall data quality and usable alignment between surveyors and QA teams, with identifiable areas for definition refinement, training, and process enhancements to further improve data governance and interoperability across systems.