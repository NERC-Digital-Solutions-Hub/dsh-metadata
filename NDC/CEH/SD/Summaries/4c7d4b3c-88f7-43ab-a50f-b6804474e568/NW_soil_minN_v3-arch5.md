# Details of data structure to ' NW_soil_minN.csv '

## Overview
- Supplement describing the data structure of NW_soil_minN.csv
- 9 columns, 512 rows
- Contains soil NH4-N and NO3-N + NO2-N concentrations and soil moisture
- Data from a grassland fertiliser trial (2016), North Wyke Research Station (Rothamsted Research)

## Dataset contents

- Date: Date of sampling
- N_app: Fertiliser application indicator; values 1, 2, or 3 denote applications
  - 1st & 2nd applications: 90 kg ha-1
  - 3rd application: 60 kg ha-1
- Block: Blocking factor in the randomised block design (1–4)
- Plot: Plot identifier (1–16)
- Treatment: Fertiliser type
  - AN = ammonium nitrate
  - U = urea
  - IU = inhibited urea (agrotain)
  - C = 0N control
- Soil_NH4_mgNkg: Ammonium concentration in soil
  - Units: mg NH4-N per kg soil (dry weight basis)
- Soil_NO3_NO2_mgNkg: Nitrate + nitrite concentration in soil
  - Units: mg NO3-N per kg soil (dry weight basis)
- moisture_dry: Soil moisture on a dry-weight basis
  - Units: g H2O per g dry soil
- moisture_wet: Soil moisture on a wet-weight basis
  - Units: g H2O per g wet soil

## Sampling and dataset generation details

- Soil sample depth: 0–10 cm (sampled using a 25 mm diameter corer)
- For each plot, 6–8 samples were taken and bulked
- Extraction: 50 g fresh soil to 100 ml 2 M KCl
  - Shaken for 60 minutes at 150 rpm
- NH4-N analysis: Discrete photometric analysis
- NO3-N + NO2-N analysis: Discrete photometric analysis
- Soil moisture determination: Drying at 105°C for at least 24 hours

## Data provenance and context

- Supplement to Supporting_documentation_CINAg_experiments_final_check_v2.1.pdf
- Linked to data series within CINAg experiments
- Location and timing: Grassland fertiliser trial, 2016, North Wyke Research Station (Rothamsted Research)

## Data governance and quality considerations for Data Stewards

- Metadata completeness
  - Ensure explicit documentation of each column (names, definitions, units, methods)
  - Preserve information on sampling depth, replication, plot design, and fertilizer treatment scheme
- Unit consistency and clarity
  - Maintain clear units: mg N kg-1 (dry weight) for soil inorganic N; moisture units as specified
- Provenance and traceability
  - Maintain links to supporting documentation and experimental context (CINAg supplement)
- Data interoperability
  - Use standardized column names and coding for treatments (AN, U, IU, C) to enable cross-dataset integration
- Limitations and scope
  - Data limited to 0–10 cm depth, single site and year (2016)
  - Bulked sub-samples per plot; potential implications for variability and representativeness
- Data maintenance
  - Documentation of any data processing steps (e.g., how bulked samples were generated)
  - Plans for updates or versioning if data are extended or reprocessed

## Potential uses and considerations for users

- Assess effects of different N fertiliser types on soil inorganic N pools (NH4-N, NO3-N + NO2-N)
- Explore relationships between soil moisture (dry/wet basis) and inorganic N concentrations
- Analyze treatment and block effects within the randomized design
- Combine with supporting CINAg documentation for broader data integration and reproducibility