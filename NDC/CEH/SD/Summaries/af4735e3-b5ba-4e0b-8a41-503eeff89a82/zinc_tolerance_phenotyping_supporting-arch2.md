# Dataset: Zinc tolerance scores for Silene uniflora populations

## Aim and scope
- Document describes a dataset of zinc tolerance in Silene uniflora across 50 populations.
- Data collected to support environmental monitoring and assessment of plant tolerance to zinc exposure.

## Collection and experimental design
- Timeframe: March 2021 to September 2021.
- Material: cuttings from 50 wild populations of Silene uniflora.
- Propagation: cuttings grown in common conditions, then subjected to deep water culture for 4 weeks.
- Treatment: roots stained with activated charcoal, transferred to fresh Hoagland's solution with 1000 μM ZnSO4.
- Scoring: after 48 hours, root growth scored on a 0–2 scale:
  - 0 = no growth
  - 1 = visible growth
  - 2 = visible growth with new root growth >30% of original root length
- Population tolerance levels: estimated as the mean score per population.

## Recorded values and data structure
- For each population, the dataset records:
  - Population code/name (column 1) and corresponding geolocation in a connected dataset ("Site records for Silene uniflora").
  - Number of cuttings assessed (column 2).
  - Zinc tolerance score (mean) for the population (column 3).
  - Standard deviation of the zinc tolerance score (column 4).
- Dataset composition: 50 rows, each representing a single population.

## Quality control
- Scoring performed by a single author (Giles, L).
- Approximately 10% of scores were verified by the other two authors.

## Metadata and data integration
- Geographic positions of scored populations are provided in a connected dataset (Site records for Silene uniflora).
- Data are suitable for standardised reporting, mapping, and integration into environmental monitoring portals.

## Relevance for environmental monitoring and policy
- Provides a standardised measure of plant zinc tolerance across multiple populations.
- Facilitates cross-population comparisons and trend analysis when combined with other environmental datasets.
- Supports data-sharing and interoperability for broader monitoring initiatives.