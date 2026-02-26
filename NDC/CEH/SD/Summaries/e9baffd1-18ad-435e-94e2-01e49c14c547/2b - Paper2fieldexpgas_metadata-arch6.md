# Soil Gas Flux Measurements Dataset with Biochar Treatment

## Overview
- Records soil gas flux measurements (CO2, CH4, N2O) using static chamber methods.
- Includes treatment details (biochar), site, timepoints, and a range of environmental and soil properties.
- Provides both raw flux values and derived log-transformed metrics to support analysis and visualization.

## Data fields and schema

- Sampling and timing
  - sampleno: individual soil sample number
  - timepoint: timepoint of measurements
  - dayfromstart: days since the start of measurements
  - datetime: date and time of the soil gas flux measurement
  - datetimefirst: date and time of the first soil gas flux measurement
  - dayofyear: day of the year of the measurement
  - site: site number from which the soil was sampled
  - biochartreatment: whether the sample is un-amended or amended with biochar
  - fulltreatname: full name of the soil treatment (biochar and wetted)

- Gas flux measurements (uncorrected)
  - mgCO2-Cfluxm2h1: CO2 flux (mg C per m2 per h)
  - ugCH4-Cfluxm2h1: CH4 flux (µg C per m2 per h)
  - ugN2O-Nfluxm2h1: N2O flux (µg N per m2 per h)

- Gas flux transformations (derived)
  - log10co2: log10(flux + 1) for CO2
  - log10ch4: log10(flux + 1) for CH4
  - log10n2o: log10(flux + 1) for N2O
  - Note: If there is a negative flux in the previous column, the positive magnitude of this negative flux is added to every flux value before logging.

- Initial/headspace concentrations
  - CO2ppmt0: CO2 ppm in the static chamber headspace at t0
  - CH4ppmt0: CH4 ppm in the static chamber headspace at t0
  - N2Oppmt0: N2O ppm in the static chamber headspace at t0

- Environmental and chamber context
  - tempair: air temperature at gas measurement
  - volwatercontentproportion: volumetric water content (proportion)
  - gravwatercontentproportion: gravimetric water content (proportion)
  - chambaream2: area of the static chamber (m2)
  - headvolm3: volume of the static chamber headspace (m3)
  - dayfromstart: see above (timing consistency)

- Soil physical properties
  - bulkdensitygcm3: bulk density of soil (g/cm3)
  - particledensitygcm3: particle density of soil (g/cm3)
  - wfpsproportion: water-filled pore space (derived; proportion)

- Biochar-related
  - biocharadditiontha: amount of biochar added to the soil (tonnes per hectare)

## Data handling and processing notes
- Derived log values are computed with a log10(flux + 1) transformation to accommodate zero values, with a specific rule for negative fluxes (adjustment by adding the magnitude of any negative flux prior to logging).
- Data integrates measurements across sites, treatments, and timepoints to enable temporal and treatment effect analyses.
- Includes both raw headspace concentrations and measurement context to support robust interpretation and quality checks.

## How this supports data use and outputs
- Enables self-serve analyses via dashboards or pivot tables by exposing key fields (fluxes, logs, treatments, timing, and environmental covariates).
- Facilitates combining with other datasets (site attributes, soil properties) to explore treatment effects, temporal trends, and relationships with moisture, temperature, and soil characteristics.
- Provides a comprehensive metadata footprint (identifiers, timing, treatment, environmental context, and derived metrics) to aid discovery, reproducibility, and re-use.