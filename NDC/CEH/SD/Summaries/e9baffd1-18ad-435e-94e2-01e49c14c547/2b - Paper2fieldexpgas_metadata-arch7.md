# Soil Gas Flux Measurements Metadata

- Purpose and use for GIS: A dataset of soil gas flux measurements designed to be mapped and explored spatially across sites, treatments, and time to support GIS-based analysis and visualization.

## Core data structure

- Identifiers and treatments
  - sampleno: Individual soil sample number
  - biochartreatment: Indicates if the sample is un-amended or amended with biochar
  - site: Site number where the soil was sampled
  - fulltreatname: Full name of the soil treatment (biochar and wetted)

- Time and temporal context
  - timepoint: Timepoint of measurements
  - dayfromstart: Days from the start of measurements
  - datetime: Date and time of the soil gas flux measurement
  - datetimefirst: Date and time of the first soil gas flux measurement
  - dayofyear: Day of the year of the gas flux measurement

- Gas flux measurements and transformations
  - mgCO2-Cfluxm2h1: CO2 flux (mg CO2-C per m2 per hour)
  - log10co2: Base-10 log of (CO2 flux + 1); negative flux handling as specified
  - ugCH4-Cfluxm2h1: CH4 flux (as indicated, unit in field name; described as mg CH4-C flux per m2 per hour)
  - log10ch4: Base-10 log of (CH4 flux + 1); negative flux handling as specified
  - ugN2O-Nfluxm2h1: N2O flux (as indicated, unit in field name; described as mg N2O-N flux per m2 per hour)
  - log10n2o: Base-10 log of (N2O flux + 1); negative flux handling as specified

- Chamber headspace concentrations
  - CO2ppmt0: CO2 ppm in the static chamber headspace at t0
  - CH4ppmt0: CH4 ppm in the static chamber headspace at t0
  - N2Oppmt0: N2O ppm in the static chamber headspace at t0

- Environmental and soil conditions
  - tempair: Temperature of the soil at the time of gas measurement
  - volwatercontentproportion: Soil volumetric water content (proportion)
  - gravwatercontentproportion: Soil gravimetric water content (proportion)
  - wfpsproportion: Water-filled pore space (gravimetric content × (bulk density / total porosity))

- Chamber and soil properties
  - chambaream2: Soil area within the static chamber (m2)
  - headvolm3: Volume of the static chamber headspace (m3)
  - biocharadditiontha: Amount of biochar added to the soil (tonnes per hectare)
  - bulkdensitygcm3: Soil bulk density (g/cm3)
  - particledensitygcm3: Soil particle density (g/cm3)

## Data relationships and preparation considerations

- Spatial and temporal linkage: Use site, timepoint, datetime, and dayofyear to align measurements across time and locations for mapping.
- Derived variables: log10co2, log10ch4, log10n2o provide log-transformed flux values for visualization of distributions and anomaly detection.
- Unit awareness: Be mindful of units across fields (CO2 in mg CO2-C m-2 h-1; CH4/N2O flux fields with their stated prefixes) when joining or displaying data on maps.
- Data quality and preprocessing: Requires data cleaning and potential unit harmonization, handling of negative flux values prior to log transformations, and validation of chamber geometry and soil property fields for accurate spatial analysis.

## GIS-focused use cases

- Map spatial patterns of gas flux across sites and treatments.
- Visualize flux magnitudes alongside soil properties (bulk density, water content) and biochar treatment effects.
- Create time-series map animations using datetime/doy data to show flux dynamics over the measurement period.
- Combine static chamber measurements with flux data to model flux drivers in a geospatial context.