# Metadata for physiology data

## Overview
- Describes three data sets generated from threespine sticklebacks across geothermal and ambient populations.
- Aims to enable analyses of metabolism, sociability, and temperature preference, with data checked for outliers and collected to control observer variance.
- Provides dataset-level context, structure, and provenance to support data integration and re-use.

## Data set 1: Metabolism.csv
- Purpose: Measure whole-body metabolism via respirometry in a flow-through chamber over weeks.
- Key metric: Standard metabolic rate (SMR) in mg O2/hr.
- Columns (six): 
  - AcclimTemp (C): acclimation temperature
  - PopTemp: habitat type (Cold or Warm)
  - Pop: site code (e.g., Ashn, GTS, CSWY, Myv) with W/C suffix for warm/cold
  - PopPair: sympatric or allopatric
  - Mass (g): specimen mass
  - SMR (mg O2/hr): standard metabolic rate
- Population context: Icelandic sites with varying thermal habitats.
- Source: Pilakouta et al. 2020; Multigenerational exposure to elevated temperatures leads to a reduction in standard metabolic rate in the wild. Functional Ecology 34, 1205-1214.

## Data set 2: Sociability.csv
- Purpose: Assess sociability via video-tracked distances in wild-caught sticklebacks from geothermal and ambient populations.
- Key metric: sociability (mean distance to stimulus shoal in cm) over 30-minute trials.
- Columns (primary): 
  - populationpair: allopatric or sympatric
  - population: population name
  - HabitatTemp: thermal habitat at population of origin (Warm or Cold)
  - Temp: acclimation and trial temperature
  - ID: individual fish ID
  - trial: trial number (1 or 2)
  - sociability: mean distance (cm) to stimulus shoal
- Population context: comparisons across geothermal vs ambient ecotypes; controlled fish densities.
- Source: Pilakouta et al. 2023; A warmer environment can reduce sociability in an ectotherm. Global Change Biology 29, 206-214.

## Data set 3: Temperature preference data (temperature preference.csv)
- Purpose: Determine temperature preference by allowing fish to settle on preferred temperature in a chamber.
- Key metric: time spent in preferred temperature (minutes); included log-transformed variants.
- Columns (primary): 
  - Test date: date of data collection
  - Population: sympatric or allopatric
  - Popn: population and habitat (as in Data set 1)
  - TempPref: time spent in a preferred temperature (minutes)
  - LogTempPref: log-transformed TempPref
  - Mass (g): mass
  - LogMass: log-transformed mass
- Data quality: outliers checked; single observer collected all data to reduce observer bias.
- Population context: multigenerational exposure to warm environments; geothermal vs ambient comparisons.
- Source: Pilakouta et al. 2023; Geothermal stickleback populations prefer cool water despite multigenerational exposure to a warm environment. Ecology and Evolution 13, e9654.

## Data quality and provenance
- All three datasets reference controlled collection methods and published studies.
- Noted quality controls include outlier checks (dataset 3) and consistent data collection to minimize observer variation (dataset 3).

## References
- Pilakouta et al. 2020. Multigenerational exposure to elevated temperatures leads to a reduction in standard metabolic rate in the wild. Functional Ecology 34, 1205-1214.
- Pilakouta et al. 2023. A warmer environment can reduce sociability in an ectotherm. Global Change Biology 29, 206-214.
- Pilakouta et al. 2023. Geothermal stickleback populations prefer cool water despite multigenerational exposure to a warm environment. Ecology and Evolution 13, e9654.