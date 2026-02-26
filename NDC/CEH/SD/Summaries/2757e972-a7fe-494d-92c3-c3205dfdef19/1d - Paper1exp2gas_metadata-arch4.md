# Soil Gas Flux Measurements Dataset

## Overview
- Dataset records soil core samples with gas flux measurements over time, including a treatment variable indicating biochar amendment.
- Captures both cumulative gas production (CO2, CH4, N2O, CO) and initial headspace gas concentrations, alongside environmental and soil characteristics.
- Supports evaluation of biochar effects on soil gas emissions and enables data-driven decision making and collaboration across data users.

## Key dataset schema

- Identification and treatment
  - soilcoreno: Individual soil sample/core identifier
  - biochartreatment: Indicates if the sample is un-amended or amended with biochar

- Temporal context
  - timepoint: Timepoint of measurements
  - dayfromstart: Days since the start of measurements
  - hourfromstart: Hours since the start of measurements
  - datetimefirst: Date and time of the first soil gas flux measurement

- Gas flux (cumulative) measurements
  - ugCO2-Cfluxg-1cumu: Cumulative CO2 flux (ug CO2-C per g dry soil)
  - ngCH4-Cfluxg-1cumu: Cumulative CH4 flux (ng CH4-C per g dry soil)
  - ngN2O-Nfluxg-1cumu: Cumulative N2O flux (ng N2O-N per g dry soil)
  - ugCO-Cfluxg-1cumu: Cumulative CO flux (ug CO-C per g dry soil)

- Gas concentrations in headspace at t0
  - CO2ppmt0: CO2 ppm in the static chamber headspace at t0
  - CH4ppmt0: CH4 ppm in the static chamber headspace at t0
  - N2Oppmt0: N2O ppm in the static chamber headspace at t0
  - COppmt0: CO ppm in the static chamber headspace at t0

- Environmental and soil context
  - tempair: Air temperature at the time of gas measurement
  - gravwatercontentproportion: Gravimetric soil water content (proportion)
  - chambaream2: Chamber soil area (m2)
  - headvolm3: Static chamber headspace volume (m3)
  - drysoilweightg: Dry soil weight in the core (g)
  - biocharweight: Dry biochar weight added to the soil
  - biocharfraction: Biochar portion of dry soil weight (proportion)
  - bulkdensitygcm3: Soil bulk density (g/cm3)
  - wfpsproportion: Water-filled pore space (gravimetric content × (bulk density / total porosity))
  - maximumwhc: Maximum water holding capacity of the soil
  - proportionofwhc: Proportion of maximum WHC at the time of gas sampling

## Measurement details and units
- Cumulative gas fluxes are given with specific units per gas:
  - CO2: ug CO2-C flux g-1 dry soil
  - CH4: ng CH4-C flux g-1 dry soil
  - N2O: ng N2O-N flux g-1 dry soil
  - CO: ug CO-C flux g-1 dry soil
- Headspace concentrations at t0 are in ppm (parts per million) for each gas (CO2, CH4, N2O, CO).
- Temporal and environmental fields enable normalization and context-aware analysis.

## Data governance and quality considerations
- Metadata richness: Field descriptions outline each variable, aiding discoverability and reuse.
- Standardization needs: Ensure consistent units across studies (e.g., ug vs ng, g vs kg) and consistent interpretation of timepoint, dayfromstart, and hourfromstart.
- Data integration: The presence of biochar treatment, time-based measurements, and multiple gases supports cross-study comparisons if standardized.
- Accessibility: The dataset appears to be self-describing, which supports transparency and collaborative use, but clarity on data provenance and update cadence would further strengthen governance.

## Relevance for Data Leaders
- Systems thinking: The dataset exemplifies a multi-faceted data product combining core identifiers, treatment encoding, temporal sequencing, gas flux outcomes, and environmental context.
- User needs and co-ownership: Rich metadata supports diverse analyses (emission modeling, treatment effects) and may invite collaboration with policy or research colleagues.
- Data availability and discoverability: Comprehensive field-level descriptions improve prioritization of data gaps and facilitate finding relevant variables for analyses.
- Data quality and standards: Clear variable definitions and units assist in ensuring data quality, comparability, and reuse across networks and partners.
- Collaboration potential: The dataset’s cross-cutting variables (biochar treatment, soil properties, gas flux) provide a foundation for broader communities of practice around soil gas emission research.