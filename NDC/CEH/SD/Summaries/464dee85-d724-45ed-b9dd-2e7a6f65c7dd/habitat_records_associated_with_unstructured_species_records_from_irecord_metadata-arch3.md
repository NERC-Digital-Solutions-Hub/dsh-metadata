# iRecord data with EUNIS habitat information

- A study of habitat data collected through iRecord using the EUNIS classification, focusing on habitat information entered via iRecord survey forms (1 km resolution or higher) and excluding unanalysed habitat data from structured schemes.

## Purpose and scope
- Examine how habitat data from unstructured iRecord submissions can be used for cross-source analyses and policy monitoring.
- Assess data quality, structure, coverage, and potential uses for informing environmental health monitoring.

## Data filtration and verification
- Only iRecord survey-form habitat entries aligned with EUNIS classifications were included.
- Habitat data entered by iRecord users is verified by taxonomic experts, mainly based on species identification; location checks may occur.
- Verification statuses: Accepted, Pending, Plausible, Queried, Rejected. Rejected records are removed; queried/plausible records are retained; pending records may not have been reviewed.
- Habitat verifications are not performed; decisions focus on species identification and location consistency.
- If a record within a sample is rejected (e.g., for location), the entire sample is removed unless another record in the sample is accepted.
- Records with coastal/marine habitat misclassifications inland are retained to avoid masking other errors; coastal records are not removed due to data volume and to preserve overall error signals.

## Data structure and content
- Dataset includes detailed fields for each recording event (sample_id), spatial references (grid_reference, derived_1km_square, derived_10km_square), and temporal data (year_start, year_end).
- habitat information fields:
  - recorded_biotope: user-selected habitat wording (aligned to EUNIS with UK clarifications)
  - eunis_habitat_group and eunis_code_group: group and specific codes from EUNIS
  - eunis_habitat: broader habitat descriptors
- Spatial resolution: records included at 1 km square resolution or greater; records without habitat data are excluded.
- The dataset contains 996,232 rows across the UK nations, with a mix of coastal, inland, and marine records and incomplete habitat fields.

## Data coverage and habitat groups
- Coverage spans England, the Isle of Man, Northern Ireland, Scotland, and Wales, with data density varying by 10 km squares and by year.
- Time distribution shows more recent data are more abundant (notable growth in 2010s and 2020s); earlier data exist back to the 1800s in places, with peak activity post-1970.
- There are 11 habitat groups with varying data density; some groups are heavily represented (e.g., Regularly or recently cultivated agricultural, horticultural and domestic habitats) while others have sparser data (e.g., Inland unvegetated or sparsely vegetated habitats).
- Co-occurrence analysis reveals many 1 km squares contain multiple habitat groups; some common co-occurrences (e.g., Hedgerows with Arable land) are frequent, while rare combinations (including coastal/marine with inland habitats) may indicate errors.

## Data quality and interpretation
- Data quality issues include: variable guidance on habitat meanings, nonstandard/non-UK-specific terminology, and challenges interpreting boundary cases (e.g., brownfields).
- Taxon-specific habitat mapping would improve categorization (e.g., pond types for Odonata); current dataset uses broader, non-taxon-specific habitat fields.
- Validation checks show inland records labeled as COAST, usually due to user error; many coastal/marine misclassifications cannot be cleanly separated from genuine errors without manual review.
- Absence of a habitat record in a square does not imply absence of habitat in the square; non-recording is not evidence of absence.
- The approach does not remove all erroneous data but documents errors and preserves data to avoid obscuring issues; cleaning decisions are limited by dataset scale.

## Implications for monitoring frameworks
- Demonstrates the value and limitations of integrating unstructured, user-submitted habitat data into environmental health monitoring.
- Highlights the need for:
  - Clear metadata and guidance on habitat classification to reduce interpretation variance.
  - Robust data governance, provenance tracking, and transparency about verification statuses and data transformations.
  - Strategies for handling unverified or pending records and for communicating uncertainty.
  - Mechanisms to address data silos and to combine heterogeneous data sources while preserving data quality signals.
  - Consideration of spatial resolution and co-occurrence analyses to infer general habitat patterns at square levels.
- Suggests that taxon-specific recording forms could improve habitat assignment accuracy for targeted monitoring programs.

## Limitations and opportunities for improvement
- Incomplete habitat fields (not required for submission) limit interpretability; more complete metadata would enhance usefulness.
- Enhancement opportunities include taxon-specific habitat mapping, improved guidance on ambiguous habitat terms, and automated quality checks to reduce inland/coast misclassifications.
- Co-occurrence insights offer a pathway to derive general habitat characterizations per square, albeit with caution due to potential data quality issues.