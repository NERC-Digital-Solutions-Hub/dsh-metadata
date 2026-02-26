# Soil respiration in human-modified forests of Eastern Amazonia

- Data overview
  - Dataset: SoilRespirationData.csv with soil respiration measurements from 20 plots (each 250 x 10 m) in the Brazilian Amazon.
  - Disturbance gradient across plots: undisturbed primary forests (n=5), logged primary forests (n=5), logged-and-burned primary forests (n=5), and secondary forests (n=5).
  - Temporal scope: January 2015 – November 2017.
  - Project context: Part of the NERC Human-modified Tropical Forests Programme (HMTF; Grant NE/K016431/1).

- Study design and sampling
  - Five soil respiration collars installed per plot, spaced ~50 m apart.
  - Collar specifications: about 7 cm in size, ~2 cm belowground and ~5 cm aboveground, 10 cm diameter.
  - Procedure: collars settled for at least one week before initial measurement.
  - Measurements: soil CO2 efflux (soil respiration) using an infrared gas analyser (EGM5®); performed monthly.
  - Collected ancillary data after each measurement: soil temperature and humidity inside and outside the collar; recorded collar height.
  - Instrumentation for soil moisture: HydroSense II.
  - Temporal cadence: monthly measurements over the study period.

- Geographic and site details
  - Plots distributed across a defined microcatchment (~5,000 ha) with coordinates provided for each collar location.
  - Coordinates (20 plots) include latitude and longitude entries (e.g., 112_12, -2.6927, -54.4515; 112_8, -2.6932, -54.4954; etc.), ensuring precise spatial context for spatial analyses.

- Data structure and key variables
  - Columns in SoilRespirationData.csv include:
    - Date: date of data collection
    - Catchment: microcatchment area
    - Transect: plot number within each basin
    - Plot code: unique code combining catchment and transect
    - Forest: disturbance class before 2015–16 El Niño
    - ElNino Fire: whether the plot burned during the 2015–16 El Niño (1 = fire, 0 = no fire)
    - Collar number: identifier for each soil respiration collar
    - Time: exact sampling time
    - Collar height: collar height in cm at measurement
    - CO2 initial / CO2 final: CO2 concentrations at start and end of measurement
    - Flux: measured soil CO2 efflux
    - Temperature (inside / outside the collar): in °C
    - Humidity (inside / outside the collar): % soil humidity
    - Field notes: notes from field processing
  - Data capture window and scope: 2015–2017 measurements across 20 plots representing disturbance gradients and potential El Niño-related fire events.

- Data provenance and funding
  - Data collected as part of the NERC HMTF programme (grant NE/K016431/1).
  - Data collection and documentation provide a standardised framework suitable for quality assurance, transformation, and re-use in environmental monitoring.

- Relevance for environmental monitoring and policy scrutiny
  - Provides a consistent, standardised dataset to assess how soil respiration responds to different disturbance regimes in tropical forests.
  - Supports cross-plot comparisons and temporal trend analyses to monitor environmental health and the effects of forest modification.
  - Facilitates integration with other environmental datasets (e.g., climate, soil moisture) to enhance interpretation of soil respiration dynamics.
  - Aligns with monitoring aims to verify data quality, enable data access, and store datasets in appropriate portals for broader use.