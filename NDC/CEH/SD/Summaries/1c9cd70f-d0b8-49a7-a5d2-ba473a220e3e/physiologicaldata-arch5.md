# Metadata for physiology data

- The document describes three data sets derived from stickleback physiology experiments, with metadata and variable definitions to support discovery, interpretation, and reuse.

## Datasets overview

- Data set 1: Metabolism.csv
  - Purpose: Metabolic measurements via respirometry in threespine sticklebacks from multiple populations; whole-body metabolism (oxygen consumption) over weeks.
  - Key context: Population sampling range; reference: Pilakouta et al. 2020.
  - Data structure: Six columns
    - AcclimTemp: acclimation temperature in Celsius
    - PopTemp: habitat type (Cold or Warm) corresponding to origin
    - Pop: short population site codes (e.g., Ashn, GTS, CSWY, Myv) with W/C suffix for warm/cold
    - PopPair: sympatric or allopatric designation
    - Mass: body mass in grams
    - SMR: standard metabolic rate in mg O2/hr

- Data set 2: Sociability.csv
  - Purpose: Laboratory assessment of sociability in wild-caught sticklebacks from geothermal vs ambient populations; using video-tracked distances to conspecifics.
  - Key context: Reference: Pilakouta et al. 2023; Global Change Biology.
  - Data structure: Several columns
    - populationpair: allopatric or sympatric
    - population: population name
    - HabitatTemp: thermal habitat at origin (warm or cold)
    - Temp: acclimation temperature and trial temperature
    - ID: individual fish identifier
    - trial: trial number (1 or 2)
    - sociability: mean distance to stimulus shoal (cm) over 30-minute trial

- Data set 3: temperaturepreference.csv
  - Purpose: Temperature preference testing in geothermal and ambient sticklebacks; 24-hour settling in a temperature chamber to determine preferred temperature.
  - Key context: Reference: Pilakouta et al. 2023; Ecology and Evolution.
  - Data structure: Several columns
    - Test date: date of data collection
    - Population: sympatric or allopatric designation
    - Popn: population and thermal habitat (as in Data set 1)
    - TempPref: time spent in a preferred temperature (minutes)
    - LogTempPref: log transformation of TempPref
    - Mass: body mass (grams)
    - LogMass: log transformation of Mass
  - Quality note: Outliers checked; all data collected by the same person to control for observer differences

## Quality, provenance, and transformations

- Data provenance:
  - Datasets derived from published studies by Pilakouta and colleagues (2020, 2023).
- Data quality measures:
  - Outlier checks performed for temperature preference data.
  - Consistent data collection by a single observer for the temperature preference dataset to minimize observer bias.
  - Transformation metadata included (LogTempPref, LogMass) to support appropriate statistical analysis.
- Units and formats:
  - Explicit units provided or implied (e.g., SMR in mg O2/hr, Mass in grams, sociability in cm, Temp in Celsius, time in minutes).

## References

- Pilakouta et al. 2020. Multigenerational exposure to elevated temperatures leads to a reduction in standard metabolic rate in the wild. Functional Ecology, 34:1205-1214.
- Pilakouta et al. 2023. Geothermal stickleback populations prefer cool water despite multigenerational exposure to a warm environment. Ecology and Evolution, 13, e9654.
- Pilakouta et al. 2023. A warmer environment can reduce sociability in an ectotherm. Global Change Biology, 29:206-214.

## Governance and reuse considerations for Data Stewards

- Ensure metadata completeness and consistency across datasets to support discovery and reuse.
- Maintain clear documentation of variable definitions, units, and any transformations (e.g., LogTempPref, LogMass).
- Manage data sharing and access in line with data governance policies, including potential embargoes or attribution requirements tied to the Pilakouta publications.
- Facilitate interoperability by aligning population codes, habitat descriptors, and temperature terminology with other datasets in the repository.
- Prepare datasets for upload to relevant portals and ensure cataloging of data holdings with references to the associated publications.