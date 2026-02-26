# Zinc tolerance in Silene uniflora populations

- The dataset documents zinc tolerance (root growth score) for 50 Silene uniflora populations, collected and tested in deep water culture experiments from March 2021 to September 2021.
- Cuttings were propagated under common conditions, then exposed to 1000 μM ZnSO4 in Hoagland's solution (pH 5.5) for 48 hours; root growth was scored as 0 (no growth), 1 (visible growth), or 2 (visible growth with new root growth >30% of original length).
- Population tolerance levels are estimated as the mean root growth score per population.

## Data collection and methods

- Collection/generation methods:
  - Deep water culture experiments conducted 03/2021–09/2021.
  - 50 populations represented by cuttings grown under uniform conditions.
  - Zn exposure and scoring as described above.
- Nature and units of recorded values:
  - For each population: mean zinc tolerance score, standard deviation, and number of cuttings scored.
  - Geographic positions of scored populations are documented in a connected dataset (Site records for Silene uniflora).
- Quality control:
  - Scoring performed by a single author; 10% of scores verified by two additional authors.

## Data structure and content

- Structure:
  - 50 rows, each representing a population.
  - Columns:
    1) Population name (local area name/landmark) and population code
    2) Number of cuttings assessed
    3) Zinc tolerance score (population mean)
    4) Standard deviation of the zinc tolerance score
- Linkages:
  - Full names and geolocations available in the connected dataset Site records for Silene uniflora.

## Data quality, provenance, and governance considerations

- Provenance:
  - Experimental design and scoring are documented; single-author scoring with partial cross-check (10%) provides some QA but may affect reproducibility if scaled.
- Reusability and interoperability:
  - Data expressed on a 0–2 scale; mean and SD per population; explicit link to geolocated site data via the connected Site records dataset.
  - Clear population coding supports integration with other datasets, but careful metadata is needed to maintain consistency across datasets.
- Sharing and updates:
  - The dataset appears designed for discovery and reuse; ensure metadata includes collection window, methods, scoring rubric, and QA details.
  - If Site records are updated, maintain stable linking and versioning to preserve provenance.

## Practical recommendations for Data Stewards

- Document metadata comprehensively:
  - Define scoring rubric and scale interpretation; specify number of cuttings per population and any variations.
  - Record collection dates, growth conditions, and exact Zn exposure protocol.
- Strengthen QA and reproducibility:
  - Consider expanding cross-validation of scores beyond 10% for future datasets; publish inter-rater reliability if applicable.
- Ensure data linkage and accessibility:
  - Maintain explicit links to Site records for geolocation data; keep identifiers stable across versions.
- Plan for updates and versioning:
  - Use DOIs or persistent identifiers; track changes to population codes or linked site records; provide a data availability statement.