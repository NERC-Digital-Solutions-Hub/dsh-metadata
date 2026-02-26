# Mapping Quality Assurance Exercise

- Purpose and context
  - 2007 Countryside Survey produced high-quality habitat and landscape data aligned with national datasets in a geodatabase.
  - Shift to digital mapping (Surveyor software) to reduce interpretation errors and enable early data checks via an interactive wiki.
  - QA (Quality Assurance) compared field survey data (CS) with QA assessments to evaluate mapping accuracy across scales and habitat types.
  - Aimed to test mapping efficacy, data integration, and reliability of conclusions drawn from the mapped data.

- Extent of QA
  - QA covered 23 1-km squares, chosen to represent land classes and locations across Great Britain.
  - Some access refusals; analyses focused on common surveyed areas between CS and QA.

- Approach and data flow
  - QA teams used standard CS tablets; data uploaded to a single geodatabase; unsurveyed and refused areas excluded from analyses.
  - QA activities often conducted in conjunction with survey teams to minimize temporal changes.
  - Mapping QA included area, linear, and point features; QA and CS datasets were aligned for comparability.

- Analysis methods
  - Direct comparison of aggregate areas/lengths/points per square.
  - Raster comparison: convert polygons to 10x10 m raster cells, assign dominant Broad Habitat (BH), compare QA vs CS.
  - 100-point grid analysis: overlay 10x10 grid; assess concordance of BH between datasets.
  - Attribute-level comparisons: reference ID layers for matching areas/lines/points and their species attributes.
  - Surveyor efficiency metrics: use of visit-status layers, extent of visited areas, and species recording frequency.

- Key findings: general agreement with notable caveats
  - Broad Habitat presence and extent
    - In 81% of squares, both CS and QA recorded the same BH presence.
    - Mean differences in BH proportions typically under 1–3.5% across most BHs; some habitats showed higher variability (SD > 5% in several cases).
    - Common minor discrepancies for: Improved/Neutral Grassland, Broadleaf vs Coniferous woodland, upland mosaics, and urban vs grassland classifications.
    - Blanket Bog posed the strongest definitional challenges; revisions to the field key for 2007 influenced mismatches with Dwarf Shrub Heath in upland areas.
  - Raster and 100-point comparisons
    - Raster agreement averaged around 76% across squares; some squares as high as 98% (364, 488) and as low as 23% (773).
    - 100-point concordance varied by square: high (e.g., 364, 359) and notable low (e.g., 773, 261). Mis-matches often linked to mosaics, upland variability, and machair-like or transitional habitats.
    - Overall, most habitat-level agreements were good, but certain squares and habitat pairs revealed regional definitional and mapping challenges.
  - Species attributes in polygons
    - Of polygons matched by location, around 45% had at least one species in common between QA and CS.
    - Among matched polygons, 77% also had a matching BH, indicating species lists influence BH allocation.
    - Species concordance overall (~40%) was lower than habitat concordance, partly due to multiple species per polygon and dominance variation; Lolium perenne showed relatively higher agreement.
  - Linear features
    - Aggregate lengths by land-use theme showed small differences; overall high consistency between QA and CS.
    - Some ambiguity between similar feature types (e.g., belts of trees vs woody linear belts) but little evidence of systematic misclassification.
  - Points
    - Total points per square were broadly similar; veteran trees showed the largest discrepancy due to field instructions (limited to two trees per species) and interpretation differences.
    - Point habitat codes for matched features generally aligned; minor confusion between woodland codes could occur from historical coding practices.
  - Change recording
    - Introduction of digital change codes (Real change, Error Change, No change) allowed more precise updates of previous maps.
    - Overall agreement on change coding was strong across many habitat types and feature types, though some complexities remained, especially for habitat-based changes.
    - Blanket Bog and related upland habitats were areas where interpretation of change and habitat boundaries caused more disagreement.
  - Data quality and training
    - Greater consistency linked to the use of mandatory fields, in-field data checks, and better guidance.
    - Experience and training affected consistency, notably in complex upland habitats and where habitat definitions were evolving (e.g., Blanket Bog).

- Notable challenges and considerations
  - Habitat definitions and transitional mosaics (e.g., upland Blanket Bog vs Dwarf Shrub Heath) complicate direct matches.
  - Upland mosaics and across-square variability can produce mismatches when small-scale heterogeneity is present.
  - Machair and region-specific habitats may exhibit unique characteristics not fully aligned with standard BH categories.
  - Training and field handbook clarity influence consistency, especially for urban vs grassland classifications and coniferous vs broadleaved woodland definitions.
  - Species concordance is inherently more variable than habitat concordance due to multiple species per polygon and dominance effects.

- Conclusions and implications
  - The digital Surveyor-based mapping and integrated QA process substantially improved data quality and transparency, enabling robust cross-dataset comparisons.
  - Overall agreement between CS surveyors and QA assessments is strong across most BHs, habitats, and linear/point features, with some habitat-definitional and regional variability challenges.
  - Key improvements recommended: refine habitat definitions for ambiguous or transitional habitats (notably Blanket Bog), enhance training for upland mosaic mapping, and continue documenting data provenance with metadata.
  - The QA framework provides a scalable, data-driven approach to validate large national geospatial datasets and to support ongoing methodological refinement and comparability with other national datasets.