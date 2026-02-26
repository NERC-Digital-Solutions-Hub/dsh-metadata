# Soil Gas Flux Measurements Dataset with Biochar Amendment - Data Description

## Overview
- A data dictionary describing soil gas flux measurements over time across multiple sites, including biochar treatment information.
- Captures both raw flux measurements and derived/log-transformed values, along with environmental and soil properties to support environmental monitoring and policy evaluation.

## Key Data Fields (Variables and Meanings)
- sampleno: Individual number assigned to the soil sample.
- timepoint: Timepoint of measurements.
- biochartreatment: Whether the sample is un-amended or amended with biochar.
- site: Site number where the soil was sampled.
- fulltreatname: Full name of the soil treatment (biochar and wetted).
- dayfromstart: Day from the start of measurements.
- mgCO2-Cfluxm2h1: CO2 gas flux (mg CO2-C per m2 per hour).
- log10co2: Log10(flux + 1) of CO2 flux; negative flux handling: if negative, add the magnitude of the negative flux to all flux values before logging.
- ugCH4-Cfluxm2h1: CH4 gas flux (mg CH4-C per m2 per hour).
- log10ch4: Log10(CH4 flux + 1); negative flux handling as for CO2.
- ugN2O-Nfluxm2h1: N2O gas flux (mg N2O-N per m2 per hour).
- log10n2o: Log10(N2O flux + 1); negative flux handling as above.
- CO2ppmt0: CO2 ppm in the static chamber headspace at time t0.
- CH4ppmt0: CH4 ppm in the static chamber headspace at time t0.
- N2Oppmt0: N2O ppm in the static chamber headspace at time t0.
- tempair: Temperature of the soil/air at the time of the gas measurement.
- volwatercontentproportion: Volumetric water content of soil (as a proportion).
- gravwatercontentproportion: Gravimetric water content of soil (as a proportion).
- chambaream2: Soil area within the static chamber (m2).
- headvolm3: Volume of the static chamber headspace (m3).
- datetime: Date and time of the soil gas flux measurement.
- datetimefirst: Date and time of the first soil gas flux measurement.
- dayofyear: Day of year on which the gas flux measurement occurred.
- biocharadditiontha: Amount of biochar added to the soil (tonnes per hectare).
- bulkdensitygcm3: Bulk density of the soil (g/cm3).
- particledensitygcm3: Particle density of the soil (g/cm3).
- wfpsproportion: Water-filled pore space of the soil (gravimetric water content × (bulk density / total porosity)).

## Data Processing Details
- Log transforms (log10co2, log10ch4, log10n2o) use log10(flux + 1) with a special rule: if the original flux is negative, the positive magnitude of that negative flux is added to every flux value before logging.

## Measurement Context and Experimental Design
- Measurements capture gas fluxes (CO2, CH4, N2O) from soil under different biochar treatments.
- Includes both raw flux values (mg CO2-C, mg CH4-C, mg N2O-N per m2 per hour) and corresponding headspace concentrations (ppm at t0).
- Environmental context includes soil temperature, moisture metrics, and chamber dimensions to support flux calculations and comparisons across samples and timepoints.

## Data Management and Accessibility
- Datasets are intended to be stored and uploaded to appropriate data portals, ensuring standardized access for analysis and reuse.
- Encourages sharing underlying data used to create final outputs to enhance transparency and interoperability.

## Challenges and Opportunities
- Challenge: Increase the value of monitoring datasets by integrating with other relevant data sources beyond single-use outputs.
- Challenge: Improve accessibility of underlying data for broader use by others.