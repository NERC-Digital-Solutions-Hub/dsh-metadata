# Soil Gas Flux Measurement Dataset (Biochar Treatment)

## Overview
- A dataset of soil gas flux measurements (CO2, CH4, N2O) across samples and timepoints, incorporating biochar treatment and related soil/measurement metadata.
- Designed to support discovery, reuse, and governance of large datasets within an organization or network.

## Key fields and data structure
- Sample and treatment identifiers
  - sampleno: individual soil sample number
  - timepoint: timepoint of measurements
  - biochartreatment: whether the sample is un-amended or amended with biochar
  - site: site number the soil was taken from
  - fulltreatname: full name of the soil treatment (e.g., biochar and wetted)
  - dayfromstart: days since the start of measurements
- Gas flux measurements (each with primary and log-transformed values)
  - mgCO2-Cfluxm2h1: CO2 flux (mg CO2-C per m2 per h)
  - log10co2: log10(flux + 1) of CO2; if previous flux is negative, add magnitude of negative flux before logging
  - ugCH4-Cfluxm2h1: CH4 flux (mg CH4-C per m2 per h)
  - log10ch4: log10(flux + 1) with same negative-flux handling rule
  - ugN2O-Nfluxm2h1: N2O flux (mg N2O-N per m2 per h)
  - log10n2o: log10(flux + 1) with same negative-flux handling rule
- Static chamber headspace and concentrations at start
  - CO2ppmt0, CH4ppmt0, N2Oppmt0: gas concentrations in ppm in the static chamber headspace at t0
- Measurement context and environmental data
  - tempair: air temperature at time of gas measurement
  - volwatercontentproportion: volumetric water content (proportion)
  - gravwatercontentproportion: gravimetric water content (proportion)
  - chambaream2: chamber footprint area (m2)
  - headvolm3: headspace volume (m3)
  - datetime: date and time of the soil gas flux measurement
  - datetimefirst: date and time of the first soil gas flux measurement
  - dayofyear: day of year of the measurement
- Treatment and soil properties
  - biocharadditiontha: amount of biochar added (tonnes per hectare)
  - bulkdensitygcm3: soil bulk density (g/cm3)
  - particledensitygcm3: soil particle density (g/cm3)
  - wfpsproportion: water-filled pore space (derived from gravimetric water content and bulk density/porosity)

## Data quality, processing, and standards
- Units are specified for all primary flux measurements (e.g., mg CO2-C m-2 h-1; mg CH4-C m-2 h-1; mg N2O-N m-2 h-1) and related concentrations (ppm).
- Derived log-transformed variables use log10(flux + 1) with a defined handling rule when prior flux is negative.
- Data are quality assured, cleaned, and transformed prior to sharing; measurement context (static chamber) is documented for reproducibility.
- Documentation includes full treatment names and measurement conditions to support accurate interpretation and reuse.

## Data governance, sharing, and metadata
- Datasets are uploaded to relevant data portals and catalogued for discovery.
- Metadata includes measurement methods, units, data transformations, and temporal/spatial context to aid reuse.
- Sharing limitations and embargoes may apply; update mechanisms should be in place to reflect new measurements or corrections.
- Data stewards may need to chase data from creators to complete metadata or fill gaps; clear guidance and tooling should be provided to data creators.

## Practical considerations for Data Stewards
- Ensure metadata completeness: capture sampleno, timepoint, site, fulltreatname, dayfromstart, datetime, dayofyear, and all measurement fields with units.
- Maintain interoperability across formats and systems; standardize field names and unit conventions.
- Manage data update workflows: track versioning, provenance, and any reprocessing of flux calculations or log transformations.
- Consider user needs: provide clear definitions of measurement methods (static chamber), data processing rules (log10 handling), and interpretation guidelines for biochar-related treatments.

## Challenges to anticipate
- Incomplete view of user needs or priorities for gas-flux datasets.
- Timely acquisition of data from multiple data creators.
- Ensuring all data creators adhere to metadata and formatting standards.
- Heterogeneity of systems and formats across sites or studies.
- Handling and transferring large datasets efficiently.
- Integrating legacy or outdated databases with bespoke interoperability solutions.