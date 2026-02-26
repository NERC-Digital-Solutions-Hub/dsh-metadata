# iRecord data with EUNIS habitat information

## Overview
- iRecord and Indicia collect biological records from multiple sources, including structured monitoring schemes and unstructured ad hoc recording.
- This study focuses on habitat data entered directly into iRecord to explore potential GIS uses.
- Habitat data are linked to the EUNIS classification system and are suitable for map-based analyses and spatial exploration.

## Data filtration and quality control
- Only iRecord survey forms using the EUNIS habitat classification were included to enable cross-source comparisons.
- Habitat verifications are performed by taxonomic experts, primarily for species identifications; verifiers can also check location accuracy.
- Dataset decisions: include queried and plausible records; remove rejected records. Pending records are included.
- Rejections are at the occurrence level (species identification). If a record within a sample is rejected, the sample may be removed unless another accepted record remains.
- Verifiers do not confirm habitat data.
- Records with coastal/marine entries appearing inland are acknowledged as errors; inland records for coastal categories are not removed to avoid masking other issues.
- Habitat data quality caveats:
  - Habitat categories come from a dropdown (based on EUNIS) but lack formal guidance on precise meanings, leading to interpretive variation.
  - Some nonstandard situations (e.g., brownfields) and boundary cases are challenging to classify.
  - Some checks show that most habitat associations align with taxon expectations (e.g., Odonata with water body type), but some mismatches occur.
  - Coastal records misclassified inland are common enough that manual cleaning across all categories is not feasible; hence coastal/marine errors are not exhaustively removed.

## Data structure and content
- Spatial resolution: records included at 1 km² or larger; low-resolution and sensitive records may be blurred.
- Geographic coverage: England, the Isle of Man, Northern Ireland, Scotland, and Wales.
- Key fields included:
  - sample_id: unique recording-event identifier.
  - sample_status: verifier decisions for the sample (Accepted, Pending, Plausible, Rejected, Queried).
  - grid_reference: capture-resolution location (OSGB in Great Britain, Irish grid in Northern Ireland).
  - derived_1km_square: 1 km grid reference.
  - derived_10km_square: 10 km grid reference.
  - year_start / year_end: earliest/latest year of the recording event.
  - recorded_biotope: habitat wording as selected by the recorder (often UK-adapted).
  - eunis_habitat_group / eunis_code_group: EUNIS habitat group and code.
  - eunis_habitat / eunis_code: specific habitat descriptions and codes.
- Data coverage snapshot:
  - Full dataset: 996,232 rows.
  - Temporal pattern: expanding strongly in recent decades, with substantial data in the 2010s and 2020s.
  - Spatial pattern: widespread across the included UK regions, with variation in the number of records per 10 km square.
- Data completeness notes:
  - Absence of a habitat record does not imply absence of habitat in the square.
  - Records without habitat information were excluded from the dataset.

## Habitat groups and data distribution
- 11 habitat groups defined by EUNIS, with varying data density per group.
- Examples of group-level emphasis:
  - Regularly or recently cultivated agricultural, horticultural and domestic habitats: highest data density (over 222,000 records in the group; substantial square-level coverage).
  - Woodland, forest and other wooded land: substantial data (tens of thousands of records within the group’s squares).
- Group-level metrics include both total records within a group and the number of 1 km squares in which the habitat is recorded, illustrating spatial coverage and data density.
- Some habitat co-occurrence patterns observed:
  - Many 1 km squares contain multiple habitat groups.
  - Frequent co-occurrence examples include Hedgerows with Arable land and other common habitat pairings.
  - Some infrequent co-occurrences (e.g., marine/coastal with inland habitats) may indicate data errors or edge cases.
- Practical GIS insight: co-occurrence information can help infer the overall habitat character of a square when records within a square reference multiple habitat groups.

## Data quality considerations for GIS use
- Habitat categorization relies on user-selected descriptors from a fixed list; interpretation variability can affect mapping accuracy.
- Some records show misclassification (notably inland records labeled as coastal/marine); such anomalies are common and not exhaustively cleaned.
- No universal guidance on boundary or mixed-habitat classification; consider using multi-habitat representations per square where appropriate.
- Taxon-specific habitat mapping would improve accuracy for certain groups (e.g., pond type for Odonata), suggesting potential enhancements with taxon-specific recording forms.

## Practical GIS applications and cautions
- Suitable for mapping habitat distributions and exploring spatial patterns across the UK plus Isle of Man.
- Use derived_1km_square for high-resolution habitat mapping; grid_reference and sample_id help aggregate records spatially and by sampling event.
- Temporal analysis is feasible using year_start/year_end to assess data availability and habitat dynamics across decades.
- QA opportunities:
  - Identify inland records labeled as coastal/marine to flag potential errors for review.
  - Compare habitat mapping outcomes against known taxa-habitat associations to spot outliers.
- When building datasets or visualizations, be mindful of data density biases toward recent years and more-recorded habitats, and of the possibility that some squares contain multiple habitat groups.

## Summary of utility for GIS specialists
- Provides a large, UK-wide, EUNIS-classified habitat dataset derived from iRecord, suitable for map-based habitat visualization and habitat pattern analysis at 1 km and 10 km scales.
- Rich metadata supports spatial queries, temporal analyses, and habitat-group-level summaries.
- Data quality caveats and potential misclassifications should be accounted for in analyses, with opportunities for targeted QA or taxon-specific enhancements to improve suitability for precise habitat mapping.