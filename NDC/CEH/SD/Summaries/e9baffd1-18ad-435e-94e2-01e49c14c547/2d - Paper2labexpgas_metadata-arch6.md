# soilcoreno

## Overview
- A dataset of soil gas flux measurements (CO2, CH4, N2O) from soil cores under varying treatments.
- Treatments include biochar amendment and periodic wetting (high water content), with records across multiple timepoints from the start and days since wetting events.
- Includes both measurement data (fluxes and headspace concentrations) and extensive soil/sample metadata (weights, densities, porosity, moisture) to support analysis and data product creation.

## Data schema: key variables
- Sample and treatment identifiers
  - soilcoreno: Individual soil sample/core number
  - timepoint: Timepoint of measurements
  - dayfromstart: Days from the start of measurements
  - daysfromwettingevent: Days from the last wetting event
  - datetime: Date and time of the soil gas flux measurement
  - temperaturetreatment: Soil temperature at measurement
  - biochartreatment: Indicates biochar amendment (yes/no)
  - wettingtreatment: Indicates periodic wetting to high water content (yes/no)
  - fulltreatname: Full name of the soil treatment (combining biochar and wetting)
- Gas flux measurements
  - mgCO2-Cfluxm2h1: CO2 flux (mg CO2-C per m2 per hour)
  - log10co2: log10(flux + 1) of CO2; if a flux is negative, the magnitude of the negative flux is added before logging
  - ugCH4-Cfluxm2h1: CH4 flux (mg CH4-C per m2 per hour)
  - log10ch4: log10(flux + 1) for CH4 with same negative-flux handling
  - ugN2O-Nfluxm2h1: N2O flux (mg N2O-N per m2 per hour)
  - log10n2o: log10(flux + 1) for N2O with same negative-flux handling
- Static chamber headspace concentrations at t0
  - CO2ppmt0, CH4ppmt0, N2Oppmt0: ppm in headspace at t0
- Environmental and soil measurements
  - tempair: Air temperature at time of measurement
  - gravwatercontentproportion: Gravimetric soil water content (as a proportion)
- Chamber and measurement geometry
  - chambaream2: Soil area within the static chamber (m2)
  - headvolm3: Headspace volume of the static chamber (m3)
  - datetime: Date and time of the soil gas flux measurement (duplicate reference to time)
- Soil mass and amendments
  - drysoilweightg: Dry soil weight in the core (g)
  - biocharweightg: Dry biochar weight added to soil (g)
  - biocharfraction: Biochar proportion relative to dry soil weight
- Soil physical properties
  - particledensitygcm3: Particle density (g/cm3)
  - totalporosity: Total porosity (calculated as 1 - bulk density/particle density)
  - wfpsproportion: Water-filled pore space (gravimetric water content × (bulk density / total porosity))

## Derived fields and transformations
- Log transforms (log10co2, log10ch4, log10n2o) computed as log10(flux + 1).
- If a flux value is negative, the magnitude of the negative flux is added to all flux values prior to logging, per the dataset’s transformation rule.

## Data quality and usage considerations
- Measurements cover multiple treatments and timepoints, enabling comparison across biochar presence and wetting regimes.
- Consistent units across flux measurements, with corresponding log-transformed counterparts for analyses that require normalization.
- Duplicate datetime reference appears; ensure deduplication if combining records from multiple sources.
- Derived fields rely on treatment naming (fulltreatname) to interpret combined effects (biochar plus wetting).

## Potential data products and use cases for Data Support
- Self-serve dashboards comparing gas flux trends by treatment over time and soil conditions.
- Tables and plots linking soil moisture (gravimetric content, WFPS) and temperature to CO2, CH4, and N2O fluxes.
- Summary metrics by treatment (average flux, variability) and by timepoint.
- Integrated reports combining flux data with soil properties (porosity, densities) for modeling emissions under different management practices.
- Data packages with clear unit definitions, transformations applied (log10 with negative-flux handling), and metadata for re-use in policy or management contexts.