# iRecord data with EUNIS habitat information

- iRecord and Indicia are used to collect biological records from structured schemes and unstructured recording. This summary focuses on habitat data entered directly into iRecord to explore potential uses.
- Data are filtered to include only records that use the EUNIS habitat classification system, enabling cross-source comparability.

## Data filtration and verification

- Habitat entries come in various formats; only EUNIS-based formats are retained for consistency.
- Records are verified by taxonomic experts:
  - Verification decisions primarily rely on species identification.
  - Verifiers can check location accuracy (grid reference vs. location name).
  - Possible outcomes: query the recorder for more info; mark as plausible; or reject the record.
- Included: queried and plausible records; excluded: rejected records. Pending records are included (not yet reviewed by a verifier).
- Habitat verification is not performed by verifiers.
- Rejections are recorded at the occurrence level (species). Sample-level status captures any rejected occurrences within that sample.
- If a record within a sample is rejected for location, the entire sample is removed unless another record in the sample is accepted, to avoid conflating location vs. species errors.
- Some inconsistencies (e.g., coastal/marine records inland) exist; inland coastal records are not removed to avoid masking other errors.
- Records at low spatial resolution or blurred for sensitivity are allowed; habitat analyses focus on 1 km² resolution or greater.
- Dataset includes England, Isle of Man, Northern Ireland, Scotland, and Wales. Records without habitat information are excluded.

## Dataset structure and fields

- Core columns include:
  - sample_id: unique identifier for recording event
  - sample_status: verifier decisions (Accepted, Pending, Plausible, Rejected, Queried)
  - grid_reference: capture location (OSGB in most regions; Irish grid in NI)
  - derived_1km_square and derived_10km_square: spatial aggregation units
  - year_start/year_end: recording year range (earliest/latest)
  - recorded_biotope and eunis_habitat_group/eunis_code_group: habitat naming and codes
  - eunis_habitat: specific habitat wording; eunis_code: coded habitat
- The dataset contains 996,232 rows (records), with habitat data linked to 11 habitat groups.

## Data coverage and temporal scope

- Spatial coverage spans major UK nations and Isle of Man; most data concentrated in recent years.
- temporal distribution shows increasing data density over time, with substantial growth in 2010s and 2020s.
- Table data indicate:
  - Pre-1970: few records and small spatial coverage
  - 1970s–1990s: gradual growth
  - 2000s: notable increase in records and 1 km squares
  - 2010s–2020s: large expansion, especially 2020s with a majority of records
- 11 habitat groups exist, each with varying data density influenced by habitat extent and recording frequency.

## Habitat groups and data patterns

- Examples of groups and relative data:
  - Regularly or recently cultivated agricultural, horticultural and domestic habitats: most records (large totals) and wide 1 km square coverage
  - Grasslands, woodland, inland waters, and coastal/marine categories also present but with differing square coverage and record counts
- Co-occurrence analysis:
  - Many 1 km squares contain multiple habitat groups, indicating mixed habitats within squares.
  - Some rare co-occurrences (e.g., marine/coastal with inland habitats) may reflect data errors.
  - Common co-occurrences (e.g., Hedgerows with Arable land) suggest potential to derive broader habitat profiles per square.
- Co-occurrence mapping shows the potential to combine records to infer general habitat context per square.

## Data quality, limitations, and considerations

- Acknowledges data errors typical of unstructured biological datasets:
  - Habitat data is not validated for accuracy as thoroughly as location data; location checks are performed, but habitat accuracy is not guaranteed.
  - Some inland records labeled as coastal/marine likely reflect user error.
- Habitat descriptions come from a UK-adapted version of EUNIS; some terms may be ambiguous without guidance.
- Taxon-specific habitat mapping could improve accuracy (e.g., Odonata habitat types); the current dataset uses general habitat categories.
- Absence of a habitat record in a square does not imply absence of that habitat; it may simply be unrecorded.
- Inland coastal errors are not systematically removed due to scale and data volume, so visible anomalies may remain.
- Records without habitat information are excluded, but overall data volume remains large enough to support broad habitat analyses and cross-square comparisons.

## Implications for analysts

- The dataset enables exploration of habitat distributions across the UK and over time, with sufficient spatial granularity (1 km²) for regional analyses.
- Useful for identifying patterns, correlations, and potential habitat associations across taxa, with caveats about habitat data quality and potential misclassifications.
- The combination of sample-level and occurrence-level status requires careful data cleaning and interpretation, especially when aggregating across records within a sample.
- Potential to map and analyze habitat co-occurrence to infer dominant habitat contexts per 1 km square, while remaining mindful of possible data entry errors in coastal/marine classifications.
- When using for predictive or decision-support purposes, consider validating habitat classifications with taxon-specific forms or supplementary datasets to reduce misclassification risk.