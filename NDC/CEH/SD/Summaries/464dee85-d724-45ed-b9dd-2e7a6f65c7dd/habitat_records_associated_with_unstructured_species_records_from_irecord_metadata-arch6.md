# iRecord data with EUNIS habitat information

## Overview
- Focuses on habitat data entered directly into iRecord using the EUNIS habitat classification system.
- Data originate from multiple sources, including structured monitoring schemes and unstructured (ad hoc) recording.
- Aims to explore potential uses of habitat data and enable cross-source comparisons, mapping, and analyses at UK-wide levels (England, Isle of Man, Northern Ireland, Scotland, Wales).

## Data filtration and verification
- Only iRecord survey forms using EUNIS habitat classification are included for cross-source comparability.
- Habitat data are verified by taxonomic experts; verification decisions primarily concern species ID, with checks on location accuracy. Habitat verification itself is not performed.
- Status handling:
  - Records can be Accepted, Pending, Plausible, Rejected, or Queried.
  - Rejected records are removed; Pending and Plausible records are retained; Queried/awaiting verification kept as appropriate.
  - If a sample contains any rejected record, the sample may be removed unless another record within the sample is accepted.
- Habitat data are not the basis for rejection decisions; location verification is prioritized.

## Data cleaning decisions
- Notable inconsistencies (e.g., coastal/marine records inland) are acknowledged; inland “Coast” records are not removed to avoid masking other errors.
- Records with very low spatial resolution or high sensitivity may be blurred; habitat usefulness is reduced below 1 km square.
- Dataset includes only records with habitat information and with geographic coverage across England, Isle of Man, Northern Ireland, Scotland, and Wales; records lacking habitat data are excluded.
- Records without habitat information do not imply absence of habitat in a square.

## Dataset structure and contents
- Key columns include:
  - sample_id, sample_status (verifier decisions on occurrences within the sample)
  - grid_reference (capture resolution)
  - derived_1km_square, derived_10km_square
  - year_start, year_end
  - recorded_biotope, eunis_habitat_group, eunis_code_group
  - eunis_habitat, eunis_code
- Size and scope:
  - 996,232 rows in total.
  - Spatial coverage spans most of the UK with varying data density by 10 km and 1 km squares.
  - Temporal coverage shows increasing data density over time, with substantial data from the 2010s and 2020s.

## Data coverage and time distribution
- Habitat group data spans 11 groups with varying data richness.
- Example coverage:
  - Regularly or recently cultivated agricultural, horticultural and domestic habitats: recorded in 33,118 1 km squares; average ~10.9 recordings per square.
  - Inland unvegetated or sparsely vegetated habitats: 4,829 total records; average ~2.22 recordings per square.
- Tables summarize per-habitat-group records and square coverage (1 km and 10 km squares), highlighting uneven data distribution influenced by habitat area and recording frequency.
- Many squares host multiple habitat groups; co-occurrence analyses show common pairings (e.g., Hedgerows with Arable land) and some rare combinations, indicating potential for square-level habitat profiling.

## Habitat groups and co-occurrence
- Co-occurrence analyses reveal frequent combinations of habitat groups within the same 1 km squares.
- Some combinations are infrequent and may indicate data artifacts or boundary ambiguities.
- Co-occurrence findings enable potential reconstruction of general habitat profiles for individual squares by combining multiple records.

## Data quality and interpretation
- Errors exist, particularly because habitat data are not consistently validated at the habitat level.
- Location accuracy is checked, but many records remain as Pending or Queried without full habitat verification.
- Habitat categories derive from EUNIS (UK-adapted wording), but meanings of some descriptors can be ambiguous; guidance for nonstandard situations (e.g., brownfield sites) is limited.
- Taxon-specific checks (e.g., Odonata) generally align habitat associations but may miss finer-scale habitat nuances; taxon-specific recording forms would improve fidelity.
- Inland “Coast” records are often user errors; very few coastal-inland mislabels are corrected due to scale and manual validation limits.
- Absence of a habitat record does not imply absence of that habitat in a square.

## Practical implications for use
- Useful for coarse, square-level habitat mapping and exploratory analyses, especially when combining multiple habitat groups to characterize a square.
- Suitable for building dashboards and self-serve analyses that show habitat distribution and co-occurrence patterns across the UK, with clear notes on data quality and potential misclassifications.
- When high precision is required, consider taxon-specific forms or additional validation; be mindful of partial records (Pending/Queried) and the absence of habitat data in some squares.
- Users should treat inland coastal mislabels as potential errors and interpret coastal classifications with caution.