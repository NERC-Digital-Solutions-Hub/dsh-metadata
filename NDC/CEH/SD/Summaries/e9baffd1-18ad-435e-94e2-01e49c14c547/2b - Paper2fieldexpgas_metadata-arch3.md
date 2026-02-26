# Soil Gas Flux Measurements with Biochar Treatments - Data Dictionary

## Overview
- A dataset capturing soil gas flux measurements (CO2, CH4, N2O) from soil samples under biochar treatment and control conditions.
- Includes raw flux values, log-transformed flux values, static chamber headspace concentrations at t0, and a range of environmental and soil properties.
- Records are organized by sample, timepoint, site, and treatment, enabling analysis of treatment effects over time and across locations.
- Contains metadata on treatment naming and biochar dosage, as well as chamber geometry and measurement timing.

## Key Variables and Measurements
- sampleno: Individual number assigned to the soil sample.
- timepoint: Timepoint of measurements.
- biochartreatment: Indicates if the sample is un-amended or amended with biochar.
- site: The site number where the soil was collected.
- fulltreatname: Full name of the soil treatment (e.g., biochar and wetted).
- dayfromstart: Days since the start of measurements.
- mgCO2-Cfluxm2h1: CO2 flux (mg CO2-C per m2 per hour).
- log10co2: Log base 10 of (CO2 flux + 1). If a negative flux exists in the previous column, the magnitude of the negative flux is added to every flux value before applying the log.
- ugCH4-Cfluxm2h1: CH4 flux (units indicated as ug CH4-C per m2 per hour; labeled as such in the dataset).
- log10ch4: Log base 10 of (CH4 flux + 1), with the same negative-flux adjustment rule as for CO2.
- ugN2O-Nfluxm2h1: N2O flux (units indicated as ug N2O-N per m2 per hour).
- log10n2o: Log base 10 of (N2O flux + 1), with the same negative-flux adjustment rule as above.
- CO2ppmt0: CO2 ppm in the static chamber headspace at time t0.
- CH4ppmt0: CH4 ppm in the static chamber headspace at time t0.
- N2Oppmt0: N2O ppm in the static chamber headspace at time t0.
- tempair: Temperature of the soil air at the time of the gas measurement.
- volwatercontentproportion: Volumetric water content of the soil (as a proportion).
- gravwatercontentproportion: Gravimetric water content of the soil (as a proportion).
- chambaream2: Area of soil within the static chamber (in m2).
- headvolm3: Volume of the static chamber headspace (in m3).
- datetime: Date and time of the soil gas flux measurement.
- datetimefirst: Date and time of the first soil gas flux measurement.
- dayofyear: Day of the year when the gas flux measurement occurred.
- biocharadditiontha: Amount of biochar added to the soil (tonnes per hectare).
- bulkdensitygcm3: Bulk density of the soil (g/cm3).
- particledensitygcm3: Particle density of the soil (g/cm3).
- wfpsproportion: Water filled pore space of the soil (calculated from gravimetric water content and bulk density).

## Data Transformations and Units
- CO2 flux: mg CO2-C per m2 per hour.
- CH4 flux: ug CH4-C per m2 per hour (note discrepancy in label vs unit; dataset uses ugCH4-Cfluxm2h1).
- N2O flux: ug N2O-N per m2 per hour.
- Log-transformed flux columns use log10(flux + 1) with a special handling: if the prior flux value is negative, the absolute magnitude of that negative flux is added to all flux values before logging.
- Headspace concentrations: ppm for CO2, CH4, and N2O at t0.
- Environmental and soil properties are in standard units (e.g., temp in degrees C, volumetric and gravimetric water contents as proportions, densities in g/cm3).
- Chamber geometry and headspace volume provide context for flux calculations.

## Experimental Design and Metadata
- Treatments:
  - biochartreatment differentiates between un-amended and biochar-amended samples.
  - fulltreatname provides the full descriptive name of the treatment.
  - biocharadditiontha records the dose of biochar applied (t/ha).
- Temporal coverage:
  - dayfromstart and datetime/datetimefirst capture timing relative to the start and exact timestamps.
  - dayofyear facilitates seasonal or annual comparisons.
- Spatial coverage:
  - site identifies the sampling location; sampleno associates measurements to individual soil samples.
- Soil and environmental covariates:
  - tempair, volwatercontentproportion, gravwatercontentproportion, bulkdensitygcm3, particledensitygcm3, wfpsproportion.
- Measurement setup:
  - chambaream2 and headvolm3 detail the chamber geometry used to derive gas fluxes.

## Data Quality, Access, and Governance Considerations
- Metadata completeness: The dataset includes detailed field descriptions for each variable, supporting understanding and reuse.
- Data standardization: Clear units and descriptions aid cross-study comparability; however, the CH4 flux unit label and actual unit may require verification to ensure consistency.
- Data sharing: The descriptions emphasize the importance of openly sharing underlying data to enable verification and reuse, noting potential barriers when sharing datasets publicly.
- Data provenance and governance: Clear association of samples with treatments, sites, and measurement times supports traceability and data governance needs in monitoring frameworks.
- Practical challenges for monitoring frameworks:
  - Ensuring consistent metadata across datasets to avoid silos and facilitate integration.
  - Managing and sharing complex datasets with transformations (e.g., log-transformed variables) to avoid misinterpretation.
  - Maintaining up-to-date metadata and data quality standards at the source of data generation.