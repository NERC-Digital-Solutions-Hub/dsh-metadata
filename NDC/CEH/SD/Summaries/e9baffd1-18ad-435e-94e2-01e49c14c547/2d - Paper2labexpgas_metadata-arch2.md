# Soil Gas Flux Data with Biochar and Wetted Treatments

## Overview
- A dataset describing soil gas flux measurements under different treatments (biochar amendment and periodic wetting) to monitor environmental health and policy-relevant performance over time.
- Uses standardized variables to capture sample identity, timing, treatments, measurement conditions, gas flux outputs, and soil properties.
- Aims to verify and publish data via appropriate portals, enabling consistent analysis and reporting.

## Data Structure (Key Variables)
- Sample and time identifiers
  - soilcoreno: unique soil sample/core identifier
  - timepoint: measurement timepoint
  - dayfromstart: days since the start of measurements
  - daysfromwettingevent: days since the last wetting event
  - datetime: date and time of the soil gas flux analysis
- Treatments
  - biochartreatment: whether biochar was amended
  - wettingtreatment: whether periodic high-water-content wetting occurred
  - fulltreatname: full name of the soil treatment (combination of biochar and wetted)
- Gas flux measurements and derived logs
  - mgCO2-Cfluxm2h1: CO2 flux (mg CO2-C per m2 per hour)
  - log10co2: base-10 log of (CO2 flux + 1); negative flux handling: add magnitude of negative flux to all flux values before logging
  - ugCH4-Cfluxm2h1: CH4 flux (ug CH4-C per m2 per hour)
  - log10ch4: base-10 log of (CH4 flux + 1) with same negative-flux adjustment
  - ugN2O-Nfluxm2h1: N2O flux (ug N2O-N per m2 per hour)
  - log10n2o: base-10 log of (N2O flux + 1) with same negative-flux adjustment
- Initial chamber and measurement context
  - CO2ppmt0, CH4ppmt0, N2Oppmt0: static chamber headspace concentrations at t0 (ppm)
  - tempair: ambient soil temperature at the time of measurement
  - datetime (duplicate in list): date-time of measurement event
- Soil and chamber physical properties
  - gravwatercontentproportion: gravimetric water content (as a proportion)
  - chambaream2: soil area within the static chamber (m2)
  - headvolm3: headspace volume of the static chamber (m3)
  - drysoilweightg: dry soil weight in the core (g)
  - biocharweightg: dry biochar weight added (g)
  - biocharfraction: biochar as a proportion of dry soil weight
  - particledensitygcm3: particle density of the soil (g/cm3)
  - totalporosity: total porosity = 1 - (bulk density / particle density)
  - wfpsproportion: water-filled pore space (gravimetric water content × (bulk density / total porosity))

## Data Processing and Outputs
- Log transforms
  - log10co2, log10ch4, log10n2o are computed as log10(flux + 1), with flux values adjusted for any negative values as described.
- Units
  - CO2 flux: mg CO2-C m-2 h-1
  - CH4 flux: ug CH4-C m-2 h-1
  - N2O flux: ug N2O-N m-2 h-1
- Outputs
  - Presents data in clear formats (reports, maps, charts) for interpretation and comparison across time and treatments.

## Data Quality and Management
- Data are verified, quality assured, cleaned, and transformed from established sources.
- Created datasets are stored and uploaded to appropriate data portals to support accessibility and reuse.

## Practical Use and Applications
- Compare environmental health indicators across treatment combinations (biochar vs none; wetted vs non-wetted) over time.
- Explore relationships between gas fluxes and soil/measurement conditions (temperature, moisture, soil properties, chamber geometry).
- Support evaluation of biochar and wetting practices on greenhouse gas emissions and soil health in monitoring programs.

## Challenges and Opportunities
- Increase the value of monitoring datasets by integrating with additional relevant data sources (e.g., climate, land use, or site history) to enable multi-factor analyses.
- Improve accessibility of underlying data used to generate outputs to promote transparency and reusability.