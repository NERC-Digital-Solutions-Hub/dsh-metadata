# Guillemot_Isle_of_May_1982-2019_metadata

## Overview
- Metadata for the Guillemot Isle of May dataset spanning 1982–2019.
- Captures population dynamics, breeding outcomes, chick development, parental behavior, diet, prey characteristics, and adult survival/mass.
- Includes both raw counts and derived/summary metrics, with explicit references to year-to-year changes and related environmental factors.

## Data Structure and Key Variables
- Population and demography
  - Year
  - Pairs
  - Pairst-1 (breeding pairs in year t-1)
  - PopGR (rate of change in breeding numbers between years)
- Environmental context
  - SST (Sea Surface Temperature in February–March for area 56°-57°N, 1°-3°W in year t)
  - SSTt-1 (same region in year t-1)
- Breeding outcomes
  - N_hatched (number of chicks hatched)
  - N_fledged (number of chicks fledged)
  - Fled_success (proportion of hatched chicks that fledged)
  - Fled_Age (mean age of chick at fledging, days)
- Chick metrics
  - Chick_Mass_N (number of chicks weighed)
  - Chick_Mass_x (mean mass in g)
  - Chick_M_SEM (standard error of mean chick mass)
  - Chick_growth_index (mean mass at fledging divided by mean age at fledging in days)
  - Chick_lineargrowth (growth rate in g/mm for chicks with wing lengths 25–59 mm)
- Parental and care indicators
  - 2_adults_present (proportion of chicks with two adults present)
  - 2_adults_SE (standard error for two-adult presence)
  - NoAdult_present (proportion of chicks with no adult present)
  - Parental_effort (index of parental effort)
  - PESE (standard error of parental effort)
  - Time_togther (time adults spent together after feeding, in minutes)
  - FeedsD_1 (number of fish fed to a chick in a day)
  - Fish_samples (number of fish identified)
- Diet composition
  - PropDiet_SE (proportion of chick diet by mass from sandeels; standard error)
  - PropDiet_Clup (proportion of diet from Clupeidae)
  - PropDiet_others (proportion from other species)
- Prey characteristics and energy
  - SE_length (mean length of a sandeel, cm)
  - Clup_length (mean length of a Clupeidae, cm)
  - SE_energy (mean energy value of a sandeel, kJ)
  - Clup_energy (mean energy value of a Clupeidae, kJ)
- Adult survival and mass
  - AdSurvival (mean adult survival from year t to t+1)
  - AdS_LowCI (Lower bound of 95% CI for adult survival)
  - AdS_UpCI (Upper bound of 95% CI for adult survival)
  - Ad_M_N (number of breeding adults that were weighed)
  - Ad_Mass_x (mean mass of breeding adults, g)
  - Ad_M_SEM (standard error of the mean mass of breeding adults)

## Temporal and Spatial Scope
- Temporal: yearly measurements from 1982 to 2019.
- Spatial: environmental context limited to a defined area (56°-57°N, 1°-3°W) for SST in February–March, with year-specific values for t and t−1.

## Measurements, Units, and Derived Metrics
- Units implied by variable names:
  - SST in degrees Celsius
  - Mass in grams
  - Age in days
  - Time in minutes
  - Proportions and indices (dimensionless)
  - Energies in kilojoules
- Derived/summary metrics include:
  - PopGR, Chick_growth_index, Chick_lineargrowth
  - Fled_Age, PropDiet_SE, AdS_LowCI/AdS_UpCI
- Standard errors and confidence intervals are provided for several key estimates to support uncertainty assessment.

## Data Quality, Provenance, and Access
- Includes standard error metrics and confidence intervals for several measurements, enabling uncertainty quantification.
- Data describe both raw counts (e.g., N_hatched, N_fledged) and derived metrics (e.g., growth indices), requiring clear provenance and transformation documentation.
- Metadata supports discoverability and reuse by researchers and data users needing time-series seabird and environmental associations.

## Stewardship Actions and Best Practices
- Data governance
  - Maintain clear definitions and units for all variables; ensure consistency across years (1982–2019).
  - Document calculation methods for derived metrics (e.g., Chick_growth_index, Chick_lineargrowth, AdSurvival).
  - Track data lineage from raw observations to derived values; record any data cleaning or transformations.
- Data quality and interoperability
  - Verify year-to-year continuity and handle gaps or missing values appropriately.
  - Ensure compatibility with external data portals and catalogues; provide metadata for discovery (variables, units, time span, area of SST).
- Access, updating, and sharing
  - Upload updated datasets to relevant portals and maintain catalogue entries.
  - Communicate any embargo or access restrictions and ensure metadata remains synchronized with data releases.
- Documentation and user support
  - Provide methodological notes on data collection protocols (sampling effort, weighing procedures, diet assessment) to aid reuse.
  - Include provenance notes for environmental variables (SST) and choices of regional bounds for SST calculations.