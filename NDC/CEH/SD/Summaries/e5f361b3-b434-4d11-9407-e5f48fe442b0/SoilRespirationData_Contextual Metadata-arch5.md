# Soil respiration in human-modified forests of Eastern Amazonia

## Overview
- Dataset: Soil respiration measurements from 20 plots (each 250 x 10 m) across a disturbance gradient in the Brazilian Amazon.
- Disturbance classes: undisturbed primary forests, logged primary forests, logged-and-burned primary forests, and secondary forests (5 plots per class).
- Study period: January 2015 to November 2017.
- Program/ funding: Part of the NERC Human-modified Tropical Forests Programme (HMTF; Grant NE/K016431/1).

## Study design and disturbance classification
- Plot selection: 20 plots distributed across four disturbance classes.
- Classification basis: canopy disturbance assessed via satellite image chronosequence (1988–2010) and field assessments of fire scars, charcoal, and logging debris.

## Data collection methods
- Collars: Five PVC collars per plot, spaced ~50 m apart; collar dimensions ~7 cm (with 10 cm diameter) and installed so about 2 cm belowground and 5 cm aboveground.
- Settling period: Collars left to settle for at least one week before first measurement.
- Measurements: Soil CO2 efflux measured with an infrared gas analyser (EGM5®). Immediately after each respiration measurement, soil temperature and humidity were recorded inside and outside the collar; collar height was noted.
- Temporal cadence: Monthly measurements.
- Additional measurements: Temperature inside and outside the collar and soil moisture (measured with HydroSense II) taken after each measurement.

## Spatial and temporal coverage
- Coordinates and plot identifiers: Precise latitude/longitude coordinates provided for each plot (e.g., 112_12, 112_8, 129_10, etc.).
- Timeframe: January 2015 – November 2017.
- Catchment context: Each plot located within a microcatchment (~5,000 ha) and assigned a plot code combining catchment and transect numbers.

## Dataset structure and variables
- Data format: CSV file named SoilRespirationData.csv.
- Column headings and meanings:
  - Date: date of data collection
  - Catchment: microcatchment
  - Transect: plot number within each basin
  - Plot code: unique code combining catchment and transect
  - Forest: disturbance class before the 2015–16 El Niño
  - ElNino Fire: whether the plot burned during the 2015–16 El Niño (1 = fire, 0 = no fire)
  - Collar number: identifier for each soil respiration collar
  - Time: exact time of data sampling
  - Collar height: collar height (cm) at measurement
  - CO2 initial: CO2 concentration at start of measurement
  - CO final: CO2 concentration at end of measurement
  - Flux: measured soil respiration flux
  - Temperature (inside the collar): internal collar temperature (°C)
  - Temperature (outside the collar): external collar temperature (°C)
  - Humidity (inside the collar): internal soil humidity (%)
  - Humidity (outside the collar): external soil humidity (%)
  - Field notes: notes recorded during field processing

## Provenance and governance
- Origin: Data collected as part of a coordinated field program (HMTF) addressing human-modified tropical forests.
- Documentation: Metadata includes detailed field procedures, collar specifications, and measurement timing to support data discovery and reuse.
- Stewardship implications: Clear documentation of disturbance context, measurement methods, and timing supports data quality, interoperability, and discoverability for researchers and practitioners.

## Data quality and usage considerations
- Temporal and spatial replication: 20 plots across four disturbance classes with monthly measurements and multiple collars per plot support robust comparisons.
- Metadata richness: Comprehensive field and instrument metadata provided, aiding reproducibility and appropriate use.
- Site-specific factors: Disturbance history (including El Niño fire events) and plot-level metadata should be considered when analyzing soil respiration responses across forest types.