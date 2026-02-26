# Soil respiration in human-modified forests of Eastern Amazonia

- A dataset describing soil respiration measurements (SoilRepirationData.csv) across 20 plots (each 250 x 10 m) in the Brazilian Amazon.
- Study gradient includes undisturbed primary forests, logged primary forests, logged-and-burned primary forests, and secondary forests (n=5 plots per class).
- Data collection period: January 2015 to November 2017; part of the NERC Human-modified Tropical Forests Programme (HMTF; grant NE/K016431/1).

## Data collection methods

- Five PVC collars per plot (50 m apart) used to measure soil CO2 efflux (soil respiration). Collars are about 7 cm in size, with approximately 2 cm belowground and 5 cm aboveground, and a 10 cm diameter.
- Collars installed and allowed to settle for at least one week before first measurement.
- Measurements taken with an infrared gas analyser (EGM5®) to obtain CO2 flux.
- Immediately after each respiration measurement, soil temperature and humidity were recorded both inside and outside the collar; collar height was noted.
- Frequency: monthly measurements.
- Additional measurements: soil/air temperature inside and outside collars, soil moisture (via HydroSense II).
- Data include field notes from sample processing.

## Spatial coordinates

- Plot locations are given as latitude/longitude coordinates for each plot (20 plots across the study area). Coordinates are presented alongside plot identifiers (e.g., 112_12, 112_8, 129_10, etc.).

## Data structure and fields

- Data are stored in SoilRespirationData.csv with the following columns:
  - Date: date of data collection
  - Catchment: microcatchment (~5,000 ha) where each plot is located
  - Transect: plot number within each basin
  - Plot code: unique code combining catchment and transect
  - Forest: forest disturbance class prior to 2015-16 El Niño
  - ElNino Fire: whether the plot burned during the 2015-16 El Niño (1 = fire, 0 = no fire)
  - Collar number: identifier for each soil respiration collar
  - Time: exact time of data sampling
  - Collar height: collar height (cm) at each measurement
  - CO2 initial: CO2 concentration at the start of measurement
  - CO final: CO2 concentration at the end of measurement
  - Flux: measured soil respiration flux
  - Temperature (inside the collar): temperature inside the collar (°C)
  - Temperature (outside the collar): temperature outside the collar (°C)
  - Humidity (inside the core): soil humidity inside the collar (%)
  - Humidity outside the core: soil humidity outside the collar (%)
  - Field notes: notes from field processing

## Provenance and access

- Data collected as part of the NERC HMTF programme; dataset description notes the grant and study context.
- CSV file attached contains the full dataset, including explicit plot-level disturbance classifications and El Niño-related fire status.

## Data quality, governance, and usage considerations for data leaders

- Provides longitudinal, multi-plot, multi-collar measurements enabling analyses of how soil respiration responds to disturbance type, temperature, humidity, and moisture.
- Metadata confirms disturbance classification, plot-level fire history, and precise measurement conditions, aiding reproducibility and cross-study comparisons.
- Users should consider potential variability due to collar placement, monthly sampling cadence, and environmental conditions when modeling respiration flux.
- The dataset includes explicit provenance (study program, grant), which supports traceability and alignment with broader data-sharing or collaboration efforts.
- The presence of coordinates and a detailed field-data dictionary supports discoverability and interoperability across related datasets and platforms.