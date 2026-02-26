# Western Ghats Leaf Water Potential measurements - seasonal cycle

## Overview
- Time-series of pre-dawn and mid-day leaf water potentials for 10 plant species (trees and plants), collected September 2020 to May 2021 with measurements every three months.
- Site near Sirsi, Western Ghats, India (lat 14.49 N, lon 74.75 E; altitude 538 m).
- Data, when combined with hydraulic conductance vulnerability curves from the same project, indicate a tree’s safe operating space under dry and high vapour pressure deficit conditions.

## Collection and Measurement Method
- Leaf water potential was measured on detached leaves using a Scholander pressure chamber (Model 1505D, PMS Instrument).
- Procedure: leaf inserted upside down, petiole airtight and visible; chamber pressurized; the pressure at which liquid begins to exude from the leaf petiole is observed. The pressure level multiplied by minus 1 (-1) is interpreted as the leaf water potential.
- Time windows: predawn (4:00–6:00 a.m.) and mid-day (12:30–3:00 p.m.).

## Data Structure and Variables
- Data stored in a CSV with columns arranged as:
  - species: plant species name
  - id: initial of species
  - replicate_treeID: tree ID
  - Time_in_day: PreDawn or MidDay
  - leaf_water_potential_Mpa: leaf water potential in MPa
  - number_of_leaves_measured: count of leaves measured
  - Month: abbreviated sampling month
  - Year: sampling year
  - Notes: any additional notes
- Key units: leaf_water_potential_Mpa in MPa; time captured as PreDawn or MidDay; Month as abbreviated name.

## Scope, Coverage and Metadata
- Covers 10 species (trees and other plants) at a single site near Sirsi, Western Ghats.
- Sampling cadence: every three months from Sep 2020 to May 2021.
- Location details provided with exact coordinates and altitude for reproducibility.

## Quality Control and Limitations
- Measurements were repeated and data checked by the team.
- Limitations:
  - Missing replicate_treeID numbers for November sampling (not recorded at the time).
  - Blank cells indicate missing data for that variable.
- Notes indicate that the method relies on the pressure at which exudation begins, interpreted as leaf water potential (negative sign applied).

## Usage, Sharing and Governance
- The dataset can be uploaded to relevant data portals and catalogues; alignment with project-wide data sharing practices is implied.
- Metadata and structure support integration with related data from the same project (e.g., hydraulic conductance vulnerability curves).
- Emphasizes documentation of data collection context, measurement method, timing, and any data gaps to support discoverability and reuse.

## Related Data
- Related measurements within the same project include hydraulic conductance vulnerability curves, which can be combined with these leaf water potential data to analyze plant water stress and safe operating ranges.