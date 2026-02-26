# Soil Gas Flux Measurements Dataset (CO2, CH4, N2O) with Biochar and Wetted Treatments

- Overview
  - A dataset of soil gas flux measurements taken from individual soil cores across different treatments and timepoints.
  - Captures chemical fluxes (CO2, CH4, N2O) and related soil, chamber, and treatment parameters to support map-based visualization and spatial analysis.

- Key identifiers and treatments
  - soilcoreno: Unique identifier for each soil core/sample.
  - timepoint: Specific measurement timepoint for a given gas analysis.
  - fulltreatname: Full name of the soil treatment (e.g., biochar presence and wetted status).
  - temperaturetreatment: Soil temperature condition during sampling.
  - biochartreatment: Whether the sample is un-amended or amended with biochar.
  - wettingtreatment: Whether the sample is periodically wetted to a high water content or not.
  - datetime: Date and time of the soil gas flux measurement (presented twice in the schema).

- Temporal context
  - dayfromstart: Days from the start of measurements for this gas analysis.
  - daysfromwettingevent: Days from the last wetting event for this gas analysis.

- Gas flux measurements (core variables and transformations)
  - mgCO2-Cfluxm2h1: CO2 flux (mg C per m2 per hour).
  - log10co2: Log10(flux + 1) for CO2, with a rule to add the magnitude of any negative flux to the flux value before logging.
  - ugCH4-Cfluxm2h1: CH4 flux (mg C per m2 per hour).
  - log10ch4: Log10(flux + 1) for CH4, applying the same negative-flux adjustment as CO2.
  - ugN2O-Nfluxm2h1: N2O flux (mg N per m2 per hour).
  - log10n2o: Log10(flux + 1) for N2O, with the same handling for negative flux values.

- Gas concentrations at the start (t0)
  - CO2ppmt0: CO2 concentration in the static chamber headspace at t0 (ppm).
  - CH4ppmt0: CH4 concentration in the headspace at t0 (ppm).
  - N2Oppmt0: N2O concentration in the headspace at t0 (ppm).

- Thermal and soil properties
  - tempair: Air temperature at the time of measurement.
  - gravwatercontentproportion: Gravimetric water content as a proportion.
  - chambaream2: Chamber surface area (m2).
  - headvolm3: Headspace volume of the static chamber (m3).
  - drysoilweightg: Dry weight of soil in the core (g).
  - biocharweightg: Dry weight of biochar added to the soil (g).
  - biocharfraction: Proportion of biochar relative to dry soil weight.
  - particledensitygcm3: Particle density of the soil (g/cm3).
  - totalporosity: Total porosity, computed as 1 - (bulk density / particle density).
  - wfpsproportion: Water-filled pore space, calculated as gravimetric water content multiplied by (bulk density / total porosity).

- Notes on data handling and用途
  - Log transform details: log10 values are computed as log10(flux + 1), with an adjustment that uses the magnitude of any negative flux when applying the transformation.
  - Time alignment: dayfromstart and daysfromwettingevent support understanding of treatment and moisture dynamics over time.
  - GIS integration: The dataset provides rich flux and soil/microclimate attributes but does not include spatial coordinates; linking to a spatial layer is needed to map flux data geographically.

- Considerations for data quality and GIS use
  - Ensure consistency of units across records (CO2, CH4, N2O flux units, ppm values, weights, and porosity metrics).
  - Be aware of duplicate datetime entries in the schema and reconcile duplicates during data import.
  - When visualizing spatial patterns, attach accurate site locations to soilcoreno entries to enable map-based analyses.