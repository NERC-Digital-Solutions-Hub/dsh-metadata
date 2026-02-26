# Soil respiration in human-modified forests of Eastern Amazonia

## Overview
- Dataset of soil respiration measurements across 20 plots (each 250 x 10 m) in the Brazilian Amazon.
- Disturbance gradient with 5 plots per class: undisturbed primary forests, logged primary forests, logged-and-burned primary forests, and secondary forests.
- Measurements collected from January 2015 to November 2017 as part of the NERC Human-modified Tropical Forests Programme (HMTF; Grant NE/K016431/1).
- Data collected to enable analysis of soil CO2 efflux and how it relates to disturbance and microclimate.

## Data collection methods
- Five PVC collars installed per plot (approximately 7 cm diameter, 2 cm belowground, 5 cm aboveground; 50 m apart).
- Collars allowed to settle for at least a week before first measurement.
- Soil CO2 efflux measured with an infrared gas analyser (EGM5®); immediately after each measurement, soil temperature and humidity were recorded inside and outside the collar.
- Collar height recorded; measurements taken monthly.
- Additional measurements: soil moisture (via HydroSense II).

## Sampling design and location
- Each plot contains multiple collars for repeated measurements over time.
- Coordinates provided for collar locations (latitude/longitude) across plots; data describe microcatchments (~5,000 ha) and plot codes (catchment, transect, plot code).
- Forest disturbance class recorded for 2015–16 period (El Niño era considered) and whether plots burned during the 2015–16 El Niño.

## Data structure and key variables
- Data file: SoilRespirationData.csv
- Columns include:
  - Date: date of data collection
  - Catchment: microcatchment containing the plot
  - Transect: plot number within each catchment
  - Plot code: unique code combining catchment and transect
  - Forest: disturbance class before 2015–16 El Niño
  - ElNino Fire: whether the plot burned during the 2015–16 El Niño (1 = fire, 0 = no fire)
  - Collar number: identifier for each collar
  - Time: exact time of sampling
  - Collar height: collar height in cm
  - CO2 initial: initial CO2 concentration
  - CO final: final CO2 concentration
  - Flux: measured soil respiration flux
  - Temperature (inside the collar): temperature inside collar after sampling
  - Temperature (outside the collar): temperature outside collar after sampling
  - Humidity (inside the core): soil humidity inside collar after sampling
  - Humidity (outside the core): soil humidity outside collar after sampling
  - Field notes: any notes recorded during field processing

## Data provenance and usage notes
- Data were collected using standardized instruments (EGM5 IRGA for CO2 flux; HydroSense II for soil moisture).
- The dataset is suitable for GIS-based analyses of spatial patterns of soil respiration and its relationship with disturbance, El Niño fire history, and microclimatic conditions.
- Potential for integration with historical canopy disturbance data and fire history to contextualize spatial variability in soil CO2 efflux.