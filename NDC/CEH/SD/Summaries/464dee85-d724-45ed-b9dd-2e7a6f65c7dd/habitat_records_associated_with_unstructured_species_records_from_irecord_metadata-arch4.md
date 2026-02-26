# iRecord data with EUNIS habitat information

- Focuses on habitat data entered directly into iRecord and coded to the EUNIS habitat classification, aiming to explore potential uses of this data for habitat analysis.
- iRecord and Indicia collect biological records from structured schemes and unstructured (ad hoc) recording; this study uses the habitat data associated with unstructured records that are coded to EUNIS.

## Data filtration and verification

- Include only records from iRecord survey forms that use the EUNIS habitat classification to enable cross-source comparability.
- Verification by taxonomic experts: decisions rely mainly on species identification; location checks (e.g., grid reference vs. location name) are also possible.
- Status handling: Accepted, Pending, Plausible, Queried, Rejected. For this dataset, queried and plausible records are included; rejected records are removed.
- Rejections are occurrence-level (species ID). If a record within a sample is rejected, the sample may be removed unless another accepted record exists.
- Location inaccuracies and inland coastal records observed; these are not removed to avoid masking other errors.
- Records can be added at low spatial resolution; habitat usefulness is reduced below 1 km² resolution, so data included at 1 km² or larger.
- Dataset covers England, Isle of Man, Northern Ireland, Scotland, and Wales; habitat data submission is not required, so records without habitat information are excluded.

## Data structure and metadata

- Dataset contains fields such as: sample_id, sample_status, grid_reference, derived_1km_square, derived_10km_square, year_start/year_end, recorded_biotope, eunis_habitat_group, eunis_code_group, eunis_habitat, eunis_code, among others.
- Habitat data are drawn from a dropdown based on the EUNIS classification; some wording differences exist to suit UK context.
- Habitat data filtering excludes non-EUNIS or non-coded entries; descriptions may be ambiguous for nonstandard situations.

## Data coverage and geography

- Total dataset: 996,232 rows.
- Geographic reach: majority across England, Isle of Man, Northern Ireland, Scotland, and Wales; data density varies by 10 km square.
- Temporal distribution: data span from 1812 to 2024, with surges in recent decades; 2020s contain the largest share of records (about 642,696 records) and 1 km squares (≈58,864) and 10 km squares (≈2,851).
- Habitat group coverage: 11 habitat groups with varying data density; some groups (e.g., Regularly cultivated habitats) have many records and squares, others have fewer.

## Habitat groups and data richness

- Example disparities: "Regularly or recently cultivated agricultural, horticultural and domestic habitats" shows high data volume (over 222k records; ~33k squares); "Inland unvegetated or sparsely vegetated habitats" has fewer records but still notable square coverage.
- Co-occurrence: many 1 km squares contain multiple habitat groups; common co-occurrences include Hedgerows with Arable land; some rare combinations may indicate data errors (e.g., marine/coastal habitats recorded inland).

## Data quality, caveats, and cleaning

- Data quality issues: habitat data often lacks explicit guidance; some records may not align with expected habitat associations for the recorded taxa.
- Validation tests (e.g., with Odonata) show most habitat associations are reasonable, but taxonomy- or taxon-specific mapping would improve relevance.
- Coastal/marine inland misclassifications occur; the study chooses not to remove these inland coastal records to avoid masking other issues.
- Absence of habitat data does not imply absence of that habitat in a square.
- The UK-context wording adjustments help clarity but highlight the need for clearer guidance on habitat category meanings.

## Implications for data strategy and potential uses

- Enables mapping of habitat distribution at 1 km resolution and analysis of habitat co-occurrence across squares.
- Useful for cross-checking habitat-context with taxon data (e.g., Odonata) to assess consistency with known habitat associations.
- Highlights data governance needs: better metadata, user guidance on habitat terms, and standardized interpretation.
- Supports development of taxon-specific habitat forms to improve classification accuracy.

## Recommendations for Data Leaders

- Establish clearer guidance on interpreting and applying habitat terms, including nonstandard sites.
- Invest in taxon-specific habitat fields or forms to improve data quality and relevance for analyses.
- Implement lightweight, scalable data-cleaning rules to flag obvious misclassifications (e.g., inland records labeled as coastal) while preserving data for quality assessment.
- Emphasize metadata provenance, record/update tracking, and versioning to support data stewardship.
- Foster a community of practice to share best practices in collecting, validating, and using habitat data from iRecord and similar platforms.