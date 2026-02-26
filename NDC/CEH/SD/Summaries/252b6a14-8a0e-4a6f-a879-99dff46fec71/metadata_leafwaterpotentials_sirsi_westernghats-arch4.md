# Western Ghats Leaf Water Potential measurements - seasonal cycle

- Overview
  - Time-series dataset of pre-dawn and mid-day leaf water potentials for 10 plant species (including trees and other flora).
  - Time span: September 2020 to May 2021; measurements every three months.
  - Purpose: when combined with hydraulic conductance vulnerability curves (measured in the project) to indicate a tree’s safe operating space under dry conditions and high vapour pressure deficit.
  - Location: near Sirsi, Western Ghats, India (14.49 N, 74.75 E; altitude 538 m).

- Collection and methods
  - Method: Scholander pressure chamber (Model 1505D) used on detached leaves.
  - Procedure: leaf inserted upside down, petiole fixed airtight and visible; chamber pressurized until liquid exudes from the leaf petiole; the pressure level, multiplied by -1, defines leaf water potential.
  - Timing: Predawn measurements 4–6 am (sunrise); mid-day measurements 12:30 pm–3 pm.
  - Instrument and site specifics: portable microscope used to observe exudation; measurements taken for pre-dawn and mid-day samples.

- Data structure and variables
  - Data stored as a CSV with columns ordered in a fixed structure.
  - Key variables:
    - species: species name
    - id: initial of species
    - replicate_treeID: Tree ID
    - Time_in_day: PreDawn or MidDay
    - leaf_water_potential_Mpa: leaf water potential in MPa
    - number_of_leaves_measured: count of leaves measured
    - Month: abbreviated month of sampling
    - Year: four-digit year
    - Notes: any additional notes
  - Additional context: measurement units are MPa for leaf water potential; the dataset notes that some data (e.g., replicate numbers for November) were not recorded at the time.

- Site and sampling details
  - Measurements taken across 10 species, including trees and other flora.
  - Sampling cadence: quarterly over the study period.
  - Location details, including precise coordinates and altitude, are provided to contextualize environmental conditions.

- Quality control and data gaps
  - Data were measured multiple times and quality-checked by the project team.
  - Notable gaps: missing replicate number for November sampling; blank cells denote missing data for the respective variable.
  - Notes indicate that data availability may be incomplete for certain months or variables, which should be considered in analyses.

- Context for use
  - When combined with complementary data (hydraulic conductance vulnerability curves from the same project), the measurements contribute to assessing plants' responses to drought and high VPD.
  - Useful for researchers or data leaders focusing on data governance, discoverability, and integration with related plant physiology datasets.