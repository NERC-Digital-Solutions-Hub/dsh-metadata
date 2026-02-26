# Metadata for physiology data

## Overview
- Three data sets describing physiology, sociability, and temperature preference in threespine sticklebacks.
- Comparisons involve geothermal vs ambient populations to assess effects of warmer environments.
- Data provenance includes controlled lab methods and references to foundational studies.
- Emphasis on metadata quality, data provenance, and potential data sharing and transformation needs.

## Data set 1: Metabolism.csv
- Description: Metabolic rate measured via respirometry on sticklebacks from multiple populations; whole-body metabolism tracked in a flow-through chamber over weeks.
- Key reference: Pilakouta et al. 2020. Multigenerational exposure to elevated temperatures leads to a reduction in standard metabolic rate in the wild. Functional Ecology.
- Columns:
  - AcclimTemp: acclimation temperature (°C)
  - PopTemp: habitat type (Cold or Warm)
  - Pop: site code (e.g., Ashn, GTS, CSWY, Myv) with W/C suffix for temperature
  - PopPair: sympatric or allopatric
  - Mass: weight (g)
  - SMR: standard metabolic rate (mg O2/hr)

## Data set 2: Sociability.csv
- Description: Lab-based sociability measurements using wild-caught sticklebacks from geothermal and ambient populations; fish tracked via video to determine mean distance to the stimulus shoal.
- Key reference: Pilakouta et al. 2023. A warmer environment can reduce sociability in an ectotherm. Global Change Biology.
- Method: video imaging; standardized densities; focal fish social interactions quantified across temperatures and population pairings.
- Columns:
  - populationpair: allopatric or sympatric
  - population: population name
  - HabitatTemp: thermal habitat of origin (warm or cold)
  - Temp: acclimation/ testing temperature
  - ID: individual fish identifier
  - trial: trial number (1 or 2)
  - sociability: mean distance (cm) from focal to stimulus shoal over 30-min trial

## Data set 3: temperaturepreference.csv
- Description: Lab-based temperature preference trials using wild-caught sticklebacks from geothermal and ambient populations; 24-hour chamber to determine preferred temperature.
- Key reference: Pilakouta et al. 2023. Geothermal stickleback populations prefer cool water despite multigenerational exposure to a warm environment. Ecology and Evolution.
- Method: fish allowed to settle on a preferred temperature for 24 hours; time spent in each temperature recorded; same person collected all data to control for observer bias.
- Columns:
  - Test date: date of data collection
  - Population: sympatric or allopatric population designation
  - Popn: population and habitat as in Data set 1
  - TempPref: time spent in a preferred temperature (minutes)
  - LogTempPref: log-transformed TempPref
  - Mass: weight (g)
  - LogMass: log-transformed Mass

## References
- Pilakouta et al. 2020. Multigenerational exposure to elevated temperatures leads to a reduction in standard metabolic rate in the wild. Functional Ecology, 34, 1205-1214.
- Pilakouta et al. 2023. Geothermal stickleback populations prefer cool water despite multigenerational exposure to a warm environment. Ecology and Evolution, 13, e9654.
- Pilakouta et al. 2023. A warmer environment can reduce sociability in an ectotherm. Global Change Biology, 29, 206-214.