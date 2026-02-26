# Soil Gas Flux Measurement Dataset: Variable Descriptions

## Overview
- A data schema detailing soil gas flux measurements (CO2, CH4, N2O) collected using static chambers, including sample metadata, treatment information, and measurement context to support data integration, cleaning, and analysis.

## Core identifiers and timing
- soilcoreno: Unique identifier for each soil sample/core.
- timepoint: Timepoint of measurements.
- dayfromstart: Days from the start of measurements.
- dayfromstartstring: Day from start as a string.
- datetime: Date and time of the soil gas flux measurement.
- midpointday: Time halfway between the current and previous timepoint.
- timeinterval: Length of time between the last and current timepoint (numeric).
- timeintervalstring: Length of time between timepoints as a string.

## Treatment, site, and context
- biochartreatment: Whether the sample is un-amended or amended with biochar.
- fulltreatname: Full name of the soil treatment (biochar and wetted).
- biocharweight: Dry biochar weight added to the soil.
- biocharfraction: Proportion of biochar added relative to dry soil weight.
- temperaturetreatment: Soil temperature under the treatment.
- nitrogentreatment: Molecule labeled with 15N (e.g., NH4+ or NO3−).
- wettingtreatment: Whether the sample was periodically wetted to a high water content.
- site: Site number from which the soil was collected.
- gravwatercontentproportion: Gravimetric soil water content as a proportion.
- wfpsproportion: Water-filled pore space proportion (derived from gravimetric content, bulk density, and porosity).

## Soil physical properties
- chambaream2: Soil chamber area (m²).
- headvolm3: Volume of the static chamber headspace (m³).
- bulkdensitygcm3: Bulk density of the soil (g/cm³).
- postmixbulkdensity: Bulk density after soil mixing (g/cm³).
- particledensitygcm3: Particle density (g/cm³).
- totalporosity: Total porosity, computed as 1 - (bulk density / particle density).

## Gas flux measurements and related data
- mgCO2-Cfluxm2h1: CO2 flux (mg CO2-C per m² per hour).
- log10co2: Log10 of CO2 flux plus 1 (log10(flux + 1)); if a flux is negative, the magnitude of the negative flux is added before logging.
- ugCH4-Cfluxm2h1: CH4 flux (mg CH4-C per m² per hour) [note: unit description uses ug but context indicates CH4-C flux].
- log10ch4: Log10 of CH4 flux plus 1 with the same negative-flux handling as CO2.
- ugN2O-Nfluxm2h1: N2O flux (mg N2O-N per m² per hour).
- log10n2o: Log10 of N2O flux plus 1 with the same negative-flux handling.
- CO2ppmt0: CO2 concentration in the static chamber headspace at time 0 (ppm).
- CH4ppmt0: CH4 concentration in the headspace at time 0 (ppm).
- N2Oppmt0: N2O concentration in the headspace at time 0 (ppm).
- tempair: Temperature of the soil air at the time of measurement.
- drysoilweightg: Dry soil weight in the core (grams).

## Derived and related fields
- midpointday, timeinterval, timeintervalstring: Used for temporal analysis and interpolation between measurements.
- totalporosity: Derived porosity used in interpreting moisture and gas transport.
- log10 transformations: Applied to flux values with a +1 offset and special handling for negative flux values to preserve mathematical validity.

## Notes on data handling and quality
- Flux values are transformed using log10(flux + 1), with adjustments when flux is negative (using the magnitude of the negative flux for logging).
- Multiple related fields capture both raw flux measurements and their transformed equivalents to facilitate different analysis approaches.
- Measurements include both raw measurement values and the contextual metadata necessary to interpret effects of biochar addition, moisture regime, temperature, and nitrogen labeling on gas fluxes.

## How this supports data use and analysis
- Enables combining datasets across timepoints, sites, and treatments to assess effects on CO2, CH4, and N2O fluxes.
- Supports creation of dashboards and self-serve analyses focusing on treatment effects, moisture regimes, and soil properties.
- Provides clear units and definitions to aid data cleaning, validation, and comparison with other studies.
- Facilitates calculation of derived metrics (e.g., porosity-related indices, time-based flux trends) while maintaining a link to raw measurements and context.