# Soil respiration in human-modified forests of Eastern Amazonia

## Data overview
- Dataset: SoilRespirationData.csv containing soil respiration measurements in 20 plots (each 250 x 10 m) across a disturbance gradient in the Brazilian Amazon.
- Disturbance classes (5 plots each): undisturbed primary forests, logged primary forests, logged-and-burned primary forests, and secondary forests.
- Temporal scope: data collected from January 2015 to November 2017.
- Project context: part of the NERC Human-modified Tropical Forests Programme (HMTF; grant NE/K016431/1).

## Data collection methods
- Plot design: five PVC collars installed per plot, arranged 50 m apart.
- Collar specifications: approximately 7 cm in size, ~2 cm belowground and ~5 cm aboveground; collars had a 10 cm diameter.
- Procedure: collars installed and allowed to settle for at least one week before first measurement.
- Measurements: soil CO2 efflux (soil respiration) measured with an infrared gas analyser (EGM5); immediately after each respiration measurement, soil temperature and humidity were recorded both inside and outside the collar; collar height also recorded.
- Frequency: measurements taken monthly.
- Additional measurements: after respiration measurement, soil temperature inside and outside the collar and soil moisture (via HydroSense II) were recorded.

## Spatial information
- Plot coordinates: 20 latitude/longitude pairs provided, corresponding to the microcatchments and plot locations (e.g., specific coordinates listed for 112_12, 112_8, 129_10, etc.).

## Data structure and contents
- File format: CSV (SoilRespirationData.csv) with the following columns:
  - Date: date of data collection
  - Catchment: microcatchment (~5,000 ha) where each plot is located
  - Transect: plot number within each basin
  - Plot code: unique plot identifiers combining catchment and transect
  - Forest: forest disturbance class before the 2015-16 El Niño
  - ElNino Fire: whether the plot burned during the 2015-16 El Niño (1 = fire, 0 = no fire)
  - Collar number: identifier for each soil respiration collar
  - Time: exact time of data sampling
  - Collar height: height of the soil collar (cm) at each measurement
  - CO2 initial: CO2 concentration at the start of the measurement
  - CO2 final: CO2 concentration at the end of the measurement
  - Flux: measured soil respiration flux
  - Temperature (inside the collar): internal collar temperature (°C)
  - Temperature (outside the collar): external collar temperature (°C)
  - Humidity (inside the core): soil humidity inside the collar (%)
  - Humidity (outside the core): soil humidity outside the collar (%)
  - Field notes: notes taken during field processing of samples
- Note: Each plot has a unique code derived from its catchment and transect numbers.