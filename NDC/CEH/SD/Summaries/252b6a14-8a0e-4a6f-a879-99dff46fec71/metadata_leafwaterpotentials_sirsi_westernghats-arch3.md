# Western Ghats Leaf Water Potential measurements - seasonal cycle

- Overview
  - Time-series of pre-dawn and mid-day leaf water potentials for 10 plant species, collected Sep 2020–May 2021.
  - Data, when combined with hydraulic conductance vulnerability curves from the same project, indicate a tree’s safe operating space under dry conditions and high vapour pressure deficit.

- Site and collection method
  - Location: Sirsi, Western Ghats, India (latitude 14.49 N, longitude 74.75 E; altitude 538 m).
  - Measurement method: Scholander pressure chamber; leaves detached and pressed to determine water potential (predawn 4–6 am; mid-day 12:30–3 pm).
  - Sampling frequency: approximately every three months.

- Dataset and structure
  - File: LeafWaterPotentials_Sirsi_WesternGhats.csv
  - Key variables (columns):
    - species (plant species)
    - id (initials of species)
    - replicate_treeID (Tree ID)
    - Time_in_day (PreDawn or MidDay)
    - leaf_water_potential_Mpa (MPa)
    - number_of_leaves_measured
    - Month (abbreviated)
    - Year (YYYY)
    - Notes
  - Units: leaf_water_potential_MPa in MPa; number_of_leaves_measured as count.

- Data details and quality
  - Data collected for 10 species; time points span Sep 2020 to May 2021.
  - Quality checks: measurements repeated and verified by the team.
  - Gaps: replicate_number missing for November sampling; blank cells indicate missing data.
  - Metadata gaps: note that some metadata may be incomplete, and missing replication data affected at least one sampling event.

- Relevance to environmental monitoring and governance
  - Provides essential physiological indicators for monitoring plant water status and drought resilience.
  - Supports assessment of safe operating space when used with corresponding hydraulic vulnerability data.
  - Highlights data governance considerations for monitoring frameworks: metadata completeness, timely data sharing, and transparent underlying data.