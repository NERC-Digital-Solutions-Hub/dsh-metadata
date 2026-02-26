# Soil respiration in human-modified forests of Eastern Amazonia

## Data overview
- Dataset: SoilRespirationData.csv, a comma-separated values file containing soil respiration measurements.
- Scope: 20 plots across a disturbance gradient in the Brazilian Amazon (undisturbed primary forests, logged primary forests, logged-and-burned primary forests, and secondary forests), with 5 plots per class.
- Timeframe: Data collected from January 2015 to November 2017.
- Project context: Part of the NERC Human-modified Tropical Forests Programme (HMTF), grant NE/K016431/1.

## Study design and plots
- Microcatchment context: Each plot lies within a microcatchment of approximately 5,000 hectares.
- Plot layout: Five PVC collars per plot, spaced 50 meters apart.
- Collar specifications: Approximately 7 cm in size with a 10 cm diameter; about 2 cm below ground and 5 cm above ground.
- Settling period: Collars were installed and allowed to settle for at least one week before measurements began.
- Measurements: Soil CO2 efflux (soil respiration) measured monthly using an infrared gas analyser (EGM5®).
- Concurrent measurements: After each respiration measurement, soil temperature and humidity were recorded inside and outside the collar; collar height was noted.

## Temporal and spatial coverage
- Temporal: Monthly data collection within the 2015–2017 window.
- Spatial: 20 plots with specified coordinates (latitude/longitude provided for each plot).

## Data structure and fields
- File format: CSV with the following columns:
  - Date: date of data collection
  - Catchment: microcatchment identifier (~5,000 ha)
  - Transect: plot number within each basin
  - Plot code: unique code combining catchment and transect
  - Forest: disturbance class prior to the 2015-16 El Niño
  - ElNino Fire: whether the plot burned during the 2015-16 El Niño (1 = fire, 0 = no fire)
  - Collar number: identifier for each soil respiration collar
  - Time: exact sampling time
  - Collar height: collar height in cm at each measurement
  - CO2 initial: CO2 concentration at the start of the measurement
  - CO final: CO2 concentration at the end of the measurement
  - Flux: measured soil respiration flux
  - Temperature (inside the collar): internal collar temperature (°C)
  - Temperature (outside the collar): external collar temperature (°C)
  - Humidity (inside the collar): internal soil humidity (%)
  - Humidity (outside the collar): external soil humidity (%)
  - Field notes: notes collected during field processing
- Coordinates: 20 pairs of latitude and longitude entries correspond to each plot location.

## Data provenance and access
- Provenance: Collected as part of the HMTF program under grant NE/K016431/1.
- Access: Data described and organized in the SoilRespirationData.csv file, with field notes providing processing context.