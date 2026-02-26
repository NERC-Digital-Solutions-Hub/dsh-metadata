# iRecord data with EUNIS habitat information

- Overview
  - iRecord and the Indicia platform collect biological records from multiple sources, including both structured monitoring schemes and unstructured, ad hoc recording.
  - This study focuses on habitat data entered directly into iRecord to explore potential uses and value of this information.

- Data filtration and verification
  - Only iRecord survey forms using the EUNIS habitat classification system were included to enable cross-comparison.
  - Verification is conducted by taxonomic experts; decisions consider species ID and location accuracy. Status options include Accepted, Pending, Plausible, Rejected, and Queried.
  - Included: queried and plausible records; excluded: rejected records. Pending records are included.
  - Habitat information is not confirmed by verifiers (verification targets species and location, not habitat).
  - Sample handling: rejections are at the occurrence level (species). If a sample contains any rejection, the sample is removed unless another record in the sample is accepted; sample_status lists samples with at least one rejection.
  - Inland coastal records and other inconsistencies were observed; no removal of inland coastal records to avoid masking other errors.
  - Spatial resolution: records below 1 km2 are excluded; data included at 1 km2 or greater.
  - Geography: England, Isle of Man, Northern Ireland, Scotland, and Wales included. Habitat data are not required for submission, so records without habitat information were excluded.

- Dataset structure and contents
  - Columns include: sample_id, sample_status, grid_reference (OSGB or Irish grid), derived_1km_square, derived_10km_square, year_start, year_end, recorded_biotope, eunis_habitat_group, eunis_code_group, eunis_habitat, among others.
  - Data coverage: 996,232 rows across the UK and related regions; broad geographic reach with variability by 10 km square.
  - Temporal coverage shows greater data density in recent years, with usable records dating back to the 1800s–1900s, but substantial growth from the 1970s onward. Table 1 summarizes records and squares by decade, with a marked increase in the 2000s, 2010s, and 2020s.
  - Habitat group taxonomy: 11 habitat groups with varying data density. Example counts:
    - Regularly or recently cultivated agricultural, horticultural and domestic habitats: many records (224,253 records; 33,118 1 km squares; average ~10.9 records per square).
    - Inland unvegetated or sparsely vegetated habitats: fewer records (3,012 records; 4,829 squares; average ~2.22 records per square).
  - Co-occurrence: many 1 km squares record multiple habitat groups; notable co-occurrences (e.g., Hedgerows with Arable land and market gardens). Some rare combinations (shown in visualization) flagged as potential anomalies.

- Data quality and interpretation
  - Known data quality issues: habitat data lack explicit interpretation guidance, and some forms use nonstandard or ambiguous wording (e.g., “brownfield” situations); taxonomy-focused verification does not guarantee habitat accuracy.
  - The study tested habitat associations against known taxon-habitat preferences (e.g., Odonata) and found general alignment, but some mismatches exist due to form limitations; taxon-specific forms would improve suitability.
  - Spatial anomalies: inland records labeled as “Coast” typically result from user errors; majority of inland “Coast” records appear erroneous, but removing them entirely could hide other errors.
  - No removal of inland coastal errors due to scale of data and the difficulty of consistent cleaning across all habitat categories.
  - Absence of habitat records does not imply absence of habitat within a square.

- Implications for monitoring and analysis
  - Demonstrates potential for cross-dataset analyses by standardizing habitat data with EUNIS and leveraging 1 km and 10 km square grids for spatial analysis.
  - Highlights both opportunities (habitat co-occurrence insights, broad coverage) and challenges (data quality, ambiguous habitat descriptors, need for taxon-specific habitat mapping).
  - Emphasizes the importance of transparent data status (Accepted, Pending, Plausible, Queried) and access to underlying data for reuse and scrutiny.

- Key takeaways
  - The iRecord habitat dataset offers extensive spatial and temporal coverage across the UK with EUNIS-based habitat classifications, totaling nearly 1 million records.
  - While valuable for monitoring and policy performance assessment, data quality issues—particularly habitat interpretation, inland/coastal misclassifications, and incomplete habitat fields—necessitate careful filtering and context-aware analysis.
  - Integrating taxon-specific forms and enabling broader data access can enhance usefulness for environmental monitoring and decision-making.