# Sup_Doc_NH3_SouthLanarkshire_indoors&outdoors

## Purpose and scope
- Data from two sites in a rural area of South Lanarkshire: one inside the hall of a dwelling, one outdoors in the dwelling's garden backing onto grassland on a large dairy farm.
- Dwelling owner operates the site; Centre for Ecology and Hydrology (Edinburgh) performs analysis.
- Uses CEH ALPHA® passive samplers to measure ammonia (NH3) concentrations in air, with monthly exposure cycles at the start of each month.

## Sampling method
- CEH ALPHA® sampler: passive device with citric acid–coated filter to capture NH3; protected by a white PTFE membrane positioned facing downwards.
- Replicates deployed to improve reliability; samplers mounted ~1.5 m above ground on a shelter.
- Exposure period: monthly; results converted to average NH3 in air using a known uptake rate of 0.003241315 m³ h⁻¹ and the exposure duration.

## Analysis and data handling
- Samplers extracted with deionised water; analysis performed with SEAL AA3 colorimetry to determine ammonium concentration, then converted to NH3 concentration in air.
- Data quality controls:
  - Coefficient of variation (CV) of replicates < 15% considered valid (flag 103 if accepted).
  - Values above calibration range may remain valid if re-measurement isn’t possible.
  - Missing data or metadata coded as -9999; datasets include site names and spatial identifiers.
- Final dataset: NH3_SouthLanarkshire_indoors_outdoors2019-2020.csv containing accepted values with appropriate flags.

## Dataset structure
- Each row represents one month of data for a single site.
- Columns include:
  - Site name, unique site identifier, network_id, parameter_id (alpha_NH3_g)
  - Measurement start/end dates and times (exposure period)
  - Measured ammonia concentration (µg NH3 m⁻³)
  - Less than detection limit flag, verification ID, unit ID (µg NH3 m⁻³)
  - Data capture percentage, validity flag, EMEP status code
  - Month-Year of measurement (MMM-YY)

## EMEP flags and data status
- EMEP codes describe data capture and quality issues, e.g.:
  - 999: data capture missing; -1 invalid
  - 781: value below detection limit; 780: below detection/quantification limit
  - 103: CV of replicates >15% but measurement considered valid
  - 559, 593, 591, etc.: contamination or local influences; many indicating valid data or specific concerns
- Flags help interpret data reliability and any adjustments or exclusions.

## Site information
- Inside site:
  - Start: 01/01/17; End: Ongoing
  - Latitude 55.64072, Longitude 3.59705; Inlet height 1.5 m
  - Location: in the hall of the dwelling
- Outside site:
  - Start: 01/01/17; End: Ongoing
  - Latitude 55.64072, Longitude 3.59705; Inlet height 1.5 m
  - Location: garden of the dwelling

## Additional context
- The two monitoring locations share coordinates, reflecting indoor and adjacent outdoor environments at the same dwelling.
- The dataset spans 2019–2020 (final dataset name) and reflects ongoing data collection since 2017. The proximity to a large dairy farm provides contextual relevance for interpreting NH3 concentrations.