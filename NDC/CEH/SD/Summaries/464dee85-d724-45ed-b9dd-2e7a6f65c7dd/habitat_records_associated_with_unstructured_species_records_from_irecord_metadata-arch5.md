# iRecord data with EUNIS habitat information

- A study on habitat data entered into iRecord using the EUNIS classification system, with focus on how habitat data can be used and interpreted alongside other records. Habitat data for unstructured records have not been widely analyzed previously; this work concentrates on habitat data linked to iRecord entries.

## Data scope and purpose

- iRecord and the Indicia software collect biological records from structured monitoring and unstructured recording; habitat data are used in structured schemes and are analyzed to explore potential uses of habitat information from iRecord.
- The analysis aims to enable cross-comparison with other data sources, ensure habitat data are usable, and understand how habitat information can support ecological insights.

## Data filtration, verification, and provenance

- Only data entries that use the EUNIS habitat classification are included to enable cross-comparison.
- Habitat data are verified by taxonomic experts; verification decisions are primarily based on species identification but can include location checks (grid reference consistency, reasonable location).
- Verification statuses:
  - Accept, Pending, Plausible, Queried, Rejected are possible.
  - For this dataset: records with queried or plausible statuses are included; rejected records are excluded; pending records are included.
- Verifiers do not confirm habitat information; they assess species identity and location accuracy.
- Record-level handling of rejections:
  - Rejections apply at the occurrence level (species identification).
  - If a sample contains a rejected record and no other accepted record, the sample may be removed unless other accepted records exist within the sample.
  - Alterations to a sample after rejection can move it back toPending status.

## Data structure, fields, and filtering decisions

- Data fields included (examples):
  - sample_id: unique identifier for recording event.
  - sample_status: verifier decisions for occurrences within the sample.
  - grid_reference: location at capture resolution (varies by country).
  - derived_1km_square and derived_10km_square: spatial aggregation for analysis.
  - year_start and year_end: temporal range of the recording event.
  - recorded_biotope and eunis_habitat_group / eunis_code_group: habitat category text and group codes.
  - eunis_habitat and eunis_code: detailed habitat descriptions and codes.
- Habitat data included only when habitat information is provided; records without habitat information are excluded.
- For habitat work, records at less than 1 km resolution are excluded due to reduced usefulness.

## Data quality, limitations, and validation

- Notable data quality issues:
  - Inland records labeled as coastal/marine; stemming from user data entry rather than true habitat.
  - Some records with potential location or habitat misclassification; complete cleaning of all errors is not performed due to dataset size.
  - Absence of a habitat record does not imply absence of habitat in a square.
- Habitats are selected from the EUNIS system (UK context has clarified wording); some categories may be ambiguous for nonstandard situations (e.g., brownfield sites, boundary cases).
- Species-taxa checks (e.g., Odonata) show most habitat associations align with known taxa-habitat relationships, but some records are inconsistent; taxon-specific forms could improve accuracy.
- Coastal/marine inland anomalies are common enough that removing them would mask other errors; thus they are retained for transparency and to reflect broader data realities.

## Data coverage, scope, and growth

- Geographic coverage: England, Isle of Man, Northern Ireland, Scotland, Wales.
- Temporal coverage: records span from 1812 to 2024 in the dataset, with data density increasing in recent decades.
- Overall dataset size: 996,232 rows.
- Temporal distribution by decade:
  - Before 1970: 2,075 records; 545 1km squares; 211 10km squares.
  - 1970s: 3,379 records; 884 1km squares; 277 10km squares.
  - 1980s: 2,463 records; 985 1km squares; 379 10km squares.
  - 1990s: 3,872 records; 1,299 1km squares; 520 10km squares.
  - 2000s: 15,666 records; 3,969 1km squares; 1,184 10km squares.
  - 2010s: 326,081 records; 45,274 1km squares; 2,736 10km squares.
  - 2020s: 642,696 records; 58,864 1km squares; 2,851 10km squares.
- Habitat groups:
  - 11 habitat groups with varying data density.
  - Example: Regularly or recently cultivated agricultural, horticultural and domestic habitats has 222,253 records across 33,118 1km squares (2368 10km squares in total for the group).
  - Inland unvegetated or sparsely vegetated habitats has 3,012 records, 4,829 squares (2,174 1km squares; 1,011 10km squares).
- Habitat co-occurrence:
  - Many 1km squares contain records from multiple habitat groups; frequent co-occurrences (e.g., hedgerows with arable land) suggest possible holistic square-level habitat interpretation.
  - Some rare combinations (e.g., marine/coastal with inland habitats) may indicate errors; inland coastal occurrences are less common and typically user-entry issues.
- Data quality checks via mapping:
  - Inland “Coast” records largely reflect misclassification; still retained to preserve data completeness and acknowledge potential errors elsewhere.

## Implications for data stewardship and use

- Potential uses:
  - Cross-source comparisons and habitat-based analyses at 1km and 10km scales.
  - Understanding habitat distribution and co-occurrence patterns across UK nations.
  - Informing habitat-related ecological studies when integrated with taxon data.
- Cautions for data stewards:
  - Be aware of nonstandard or ambiguous habitat classifications and boundary cases.
  - Acknowledge possible location and habitat misclassifications, especially for records with Pending or Queried statuses.
  - Recognize that the absence of a habitat record does not mean absence of habitat in a square.
  - Habitual data governance should consider taxon-specific habitat mappings or forms to enhance accuracy.
- Governance considerations:
  - Maintain clear provenance and status tracking for records (including sample-level decisions and rejections).
  - Document coordinate systems and geographic transformations (country-specific grid references and derived square fields).
  - Implement ongoing quality checks and potential targeted cleaning (e.g., coastal-inland misclassifications) without discarding valuable historical data.
  - Ensure updates and new habitat entries are aligned with the EUNIS framework and clearly communicated to data users.