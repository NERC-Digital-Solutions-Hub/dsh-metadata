# Western Ghats Leaf Water Potential measurements - seasonal cycle

- Data scope: Time-series of pre-dawn and mid-day leaf water potentials for 10 plant species, spanning September 2020 to May 2021 with measurements every three months.
- Location: Sirsi, Western Ghats, India (14.49 N, 74.75 E; altitude 538 m).
- Measurement method: Scholander pressure chamber; leaf inserted upside down, pressure at which liquid exudes observed to determine leaf water potential (predawn 4–6 am; mid-day 12:30–3 pm).
- Relevance: When combined with hydraulic conductance vulnerability curves from the same project, indicates a tree’s safe operating space under dry and high vapor pressure deficit (VPD) conditions.

## Data structure and fields

- File format: CSV with columns arranged for each variable.
- Core variables:
  - species: species name
  - id: species initial
  - replicate_treeID: tree identifier
  - Time_in_day: PreDawn or MidDay
  - leaf_water_potential_MPa: leaf water potential in MPa
  - number_of_leaves_measured: count of leaves measured
  - Month: abbreviated month of sampling
  - Year: year of sampling
  - Notes: any additional notes
- Units: leaf_water_potential_MPa in MPa
- Data notes: Blank cells indicate missing data; November sampling lacks recorded replicate numbers.

## Quality control and data issues

- Measurements were repeated and checked by the team.
- Missing replicate numbers for November; some data gaps indicated by blank cells.
- Data structured to support cross-dataset integration (e.g., with corresponding hydraulic conductance curves).

## Potential uses and data products

- End-user analysis: time-series exploration by species, time of day, and month; cross-species comparisons.
- Dashboards and pivot tables enabling self-serve data access.
- Supporting outputs and iterative improvements through feedback and sharing early prototypes.
- Integrations: align with related hydraulic conductance data to assess drought responses and safe operating space.

## Data support considerations

- Data integration: ensure consistent identifiers across datasets (species id, tree IDs) for merging with hydraulic curves.
- Data quality: address missing replicate numbers and fill or flag blank data appropriately.
- Documentation: maintain clear notes on measurement conditions and any anomalies to aid interpretation and reuse.