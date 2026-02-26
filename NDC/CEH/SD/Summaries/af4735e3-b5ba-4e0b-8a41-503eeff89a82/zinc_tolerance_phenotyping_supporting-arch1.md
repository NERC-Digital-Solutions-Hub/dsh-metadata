# Dataset: Zinc tolerance scores for Silene uniflora populations (ZnSO4 exposure)

## Overview
- Deep water culture experiments conducted from March 2021 to September 2021.
- 50 wild Silene uniflora populations were sampled; cuttings propagated under common conditions.
- Zn tolerance measured by root growth after exposure to 1000 μM ZnSO4 in Hoagland's solution.

## Experimental method and protocol
- Propagation: Cuttings from each population grown in diluted Hoagland's solution (pH 5.5) for 4 weeks.
- Treatment: Roots stained with activated charcoal, then transferred to fresh Hoagland's with 1000 μM ZnSO4.
- Scoring: After 48 hours, root growth scored as 0 (no growth), 1 (visible growth), or 2 (visible growth with new root length >30% of original).
- Population tolerance: Estimated as the mean root growth score per population.

## Data collected and measurements
- For each population, the dataset records:
  - Population code/name (column 1)
  - Number of cuttings assessed (column 2)
  - Zinc tolerance score (mean) per population (column 3)
  - Standard deviation of the zinc tolerance score (column 4)

## Data structure and linkage
- 50 rows total; each row corresponds to a single population.
- Populations named after local areas/landmarks; population codes provided.
- Full names and geolocations available in a connected dataset named “Site records for Silene uniflora.”

## Data quality and provenance
- Collected and scored by a single author (Giles, L); 10% of scores verified by the other two authors.
- The dataset provides a mean score per population and the associated variability (standard deviation).

## Considerations for analysis
- Outcome is derived from an ordinal 0–2 scale averaged at the population level; consider implications of using a mean for ordinal data.
- Sample size per population varies (number of cuttings per population recorded), which affects precision of the mean and SD.
- Single-lab data with partial cross-checking; potential measurement error or bias to consider.
- Data can be integrated with the connected site records dataset to explore geographic or environmental correlations with zinc tolerance.
- Temporal scope and standardized growth conditions support comparisons across populations, but local environmental histories are external to the dataset.