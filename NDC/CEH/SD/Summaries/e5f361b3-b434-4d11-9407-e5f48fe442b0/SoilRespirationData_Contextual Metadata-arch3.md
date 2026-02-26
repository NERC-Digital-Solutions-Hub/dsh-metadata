# Soil respiration in human-modified forests of Eastern Amazonia

## Data overview
- Dataset: SoilRespirationData.csv
- Scope: soil respiration measurements in 20 plots (each 250 x 10 m) across a disturbance gradient
  - Undisturbed primary forests (n = 5)
  - Logged primary forests (n = 5)
  - Logged-and-burned primary forests (n = 5)
  - Secondary forests (n = 5)
- Temporal coverage: January 2015 – November 2017
- Project context: part of the NERC Human-modified Tropical Forests Programme (HMTF; Grant NE/K016431/1)

## Data collection methods
- Plot layout: five PVC collars per plot, 50 m apart, ~7 cm diameter; collar design: ~2 cm belowground, ~5 cm aboveground
- Setup: collars installed, then left to settle for at least one week prior to first measurement
- Measurement device: infrared gas analyser (EGM5®) for soil CO2 efflux (soil respiration)
- Concurrent measurements: soil temperature and humidity inside and outside the collar; collar height recorded
- Sampling frequency: monthly
- Additional measurements: soil temperature outside/inside the collar and soil moisture (HydroSense II)

## Coordinates
- 112_12: lat -2.692730152, lon -54.45151688
- 112_8: lat -2.69324643, lon -54.49539451
- 129_10: lat -2.725951403, lon -54.77663458
- 129_11: lat -2.705519412, lon -54.78594958
- 129_5: lat -2.714345657, lon -54.74854442
- 260_1: lat -3.002284908, lon -54.89462363
- 260_4: lat -3.019839972, lon -54.85655864
- 260_5: lat -2.983683637, lon -54.8784902
- 261_10: lat -3.018342392, lon -55.00475269
- 261_9: lat -3.039979322, lon -55.01475925
- 357_2: lat -3.313911602, lon -54.90926129
- 357_3: lat -3.300101698, lon -54.89018373
- 357_4: lat -3.282666327, lon -54.85423058
- 357_6: lat -3.256891326, lon -54.88828639
- 357_9: lat -3.263337936, lon -54.8927975
- 363_3: lat -3.296348926, lon -54.96326329
- 363_6: lat -3.335934405, lon -54.95587735
- 363_7: lat -3.320031001, lon -54.9603092
- 69_11: lat -2.573649434, lon -54.67078647
- 69_8: lat -3.305382653, lon -54.91197787

## Details of data structure
- File format: CSV (SoilRespirationData.csv)
- Columns:
  - Date: date of data collection
  - Catchment: microcatchment (~5,000 ha) where each plot is located
  - Transect: plot number within each basin
  - Plot code: unique code combining catchment and transect numbers
  - Forest: disturbance class before the 2015-16 El Niño
  - ElNino Fire: whether the plot burned during the 2015-16 El Niño (1 = fire, 0 = no fire)
  - Collar number: identifier for each soil respiration collar
  - Time: exact time of data sampling
  - Collar height: collar height in cm at each measurement
  - CO2 initial: CO2 concentration at start of measurement
  - CO final: CO2 concentration at end of measurement
  - Flux: measured soil respiration flux
  - Temperature (inside the collar): temperature inside the soil collar post-sampling (°C)
  - Temperature (outside the collar): temperature outside the soil collar post-sampling (°C)
  - Humidity (inside the core): soil humidity inside the collar (%)
  - Humidity (outside the core): soil humidity outside the collar (%)
  - Field notes: notes taken during field processing