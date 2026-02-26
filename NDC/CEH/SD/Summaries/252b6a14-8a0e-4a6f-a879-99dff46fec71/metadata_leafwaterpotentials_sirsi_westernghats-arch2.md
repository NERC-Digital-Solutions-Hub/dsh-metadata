# Western Ghats Leaf Water Potential measurements - seasonal cycle

## Overview
- Time-series of pre-dawn and mid-day leaf water potentials for 10 flora species (trees and plants).
- Spanning September 2020 to May 2021; measurements every three months.
- Data, when combined with hydraulic conductance vulnerability curves from the same project, indicate a tree’s safe operating space under dry and high vapour pressure deficit conditions.

## Site and collection methods
- Location: near Sirsi, Western Ghats, India (latitude 14.49 N, longitude 74.75 E; altitude 538 m).
- Measurement method: Scholander pressure chamber (Model 1505D). Detached leaves measured; pressure at which liquid exudes from the leaf petiole is observed and interpreted as leaf water potential (negative of that pressure).
- Sampling times: Predawn (4–6 am) and Mid-day (12:30–3 pm).
- Data scope: 10 species including trees and plants.

## Data structure and variables
- Data format: CSV with variables organized in columns.
- Key variables:
  - species: species name
  - id: initial of species
  - replicate_treeID: Tree ID
  - Time_in_day: PreDawn or MidDay
  - leaf_water_potential_MPa: Leaf water potential (MPa)
  - number_of_leaves_measured: Count of leaves measured
  - Month: Abbreviated month of sampling
  - Year: Year (YYYY)
  - Notes: Additional notes
- Units: leaf_water_potential_MPa expressed in MPa.
- Data completeness: Blank cells indicate missing data; replicate numbers missing for November sampling.

## Quality control
- Leaf potentials were measured multiple times and data were quality-checked by the team.
- Noted gap: replicate number missing for November sampling.

## Relevance for monitoring and analysis
- Provides standardized, time-bounded measurements of plant water status across multiple species, enabling environmental health monitoring and trend analysis.
- Facilitates integration with drought vulnerability curves to assess forest resilience under increasing dry spells and high vapour pressure deficit.

## Data management and access considerations
- Datasets are stored and uploaded to appropriate portals, supporting data sharing and reuse.
- Potential to increase value by linking with additional datasets (e.g., hydraulic conductance) and by ensuring underlying data are accessible to analysts for cross-dataset analyses and policy-oriented assessments.