# Soil Gas Flux Measurements with Biochar Treatment: Variable Descriptions

## Overview
- Dataset captures soil gas flux measurements and related properties for samples with and without biochar amendment.
- Includes per-sample core identifiers, timepoints, measurement times, gas concentrations in headspace, and cumulative gas flux metrics.
- Combines physical soil properties (moisture, density, bulk density, chamber area/volume) with treatment information to enable analysis of biochar effects on CO2, CH4, and N2O fluxes.

## Key Variables
- soilcoreno: Individual number assigned to each soil core/sample.
- timepoint: Timepoint of measurements.
- biochartreatment: Indicates whether the sample is un-amended or amended with biochar.
- dayfromstart: Days from the start of measurements for this gas analysis.
- hourfromstart: Hours from the start of measurements for this gas analysis.
- ugCO2-Cfluxg-1cumu: Cumulative CO2 flux (micrograms CO2-C per gram dry soil).
- ngCH4-Cfluxg-1cumu: Cumulative CH4 flux (nanograms CH4-C per gram dry soil).
- ngN2O-Nfluxg-1cumu: Cumulative N2O flux (nanograms N2O-N per gram dry soil).
- ugCO-Cfluxg-1cumu: Cumulative CO flux (micrograms CO-C per gram dry soil).
- CO2ppmt0: CO2 ppm in the static chamber headspace at time 0.
- CH4ppmt0: CH4 ppm in the headspace at time 0.
- N2Oppmt0: N2O ppm in the headspace at time 0.
- COppmt0: CO ppm in the headspace at time 0.
- tempair: Temperature of the soil at the time of gas measurement.
- gravwatercontentproportion: Gravimetric soil water content (as a proportion).
- chambaream2: Chamber area (square meters) inside which measurements occur.
- headvolm3: Headspace volume of the static chamber (cubic meters).
- datetimefirst: Date and time of the first soil gas flux measurement.
- drysoilweightg: Dry soil weight in grams for the core.
- biocharweight: Dry weight of biochar added to the soil.
- biocharfraction: Proportion of biochar relative to dry soil weight.
- bulkdensitygcm3: Soil bulk density (g/cm^3).
- wfpsproportion: Water-filled pore space (calculated from gravimetric water content, bulk density, and porosity).
- maximumwhc: Maximum water holding capacity of the soil.
- proportionofwhc: Proportion of the maximum water holding capacity at the time of gas sampling.

## Data Use and Insights
- Compare biochar-treated samples vs. controls to assess impact on CO2, CH4, and N2O fluxes over time.
- Analyze relationships between gas fluxes (instantaneous and cumulative) and soil properties (moisture, temperature, bulk density, WHC).
- Explore time dynamics using dayfromstart and hourfromstart to identify peak flux periods.
- Use datetimefirst to align this dataset with other time-stamped measurements for integrated analyses.

## Data Quality & Preparation
- Expect potential variability in data formats and missing values across timepoints or samples.
- Standardize units across gas flux metrics (e.g., convert all cumulative flux values to consistent units if combining with other datasets).
- Validate time-related fields (dayfromstart, hourfromstart) against datetimefirst to ensure consistency.
- Verify biochar-related fields (biocharweight, biocharfraction) are coherent with the corresponding dry soil weight.
- Check gravwatercontentproportion, wfpsproportion, and maximumwhc for logical bounds (0–1 or appropriate ranges).

## Potential Data Products & Visualizations
- Self-serve dashboards showing:
  - Gas flux (CO2, CH4, N2O) over time by biochar treatment.
  - Cumulative flux trajectories by sample and treatment.
  - Relationships between gas flux and soil moisture, temperature, and WHC.
- Summary reports comparing treatment groups at key timepoints (e.g., first measurement, end of measurement period).
- Interactive charts linking datetimefirst with gas concentrations at t0 and subsequent timepoints.

## Practical Considerations
- Ensure clear documentation of field names (as provided) when sharing with end users to facilitate correct interpretation.
- Consider linking this dataset with external data (e.g., weather records) via datetimefirst for richer context.