# Stem respiration in human-modified forests of Eastern Amazonia

## Overview
- Dataset: StemRespirationData.csv containing stem respiration measurements for trees across 20 plots in Eastern Amazonia.
- Disturbance gradient: undisturbed primary, logged primary, logged-and-burned primary, and secondary forests (5 plots per class).
- Timeframe: data collected June 2015 to July 2018; part of the NERC Human-modified Tropical Forests Programme (HMTF).

## Data collection methods
- Stem collars installed on at least 13 trees per plot, 20 cm above dendrometers; PVC collars (~5 cm height, ~10 cm diameter).
- CO2 efflux measured with infrared gas analyser (EGM5); measurements taken every 3 months.
- If a tree died, collar removed and replaced in the same DBH size class; new collar installed.
- Five DBH classes used for stratification: 10–19.99 cm, 20–29.99 cm, 30–39.99 cm, 40–49.99 cm, ≥50 cm.
- Disturbance classification based on satellite canopy disturbance (1988–2010) and field assessments (fire scars, charcoal, logging debris).

## Spatial and temporal scope
- Coordinates provided for plots (20 locations across catchments) with precise latitude/longitude values.
- Temporal sequence spans 2015–2018, with measurements every three months.

## Data structure and content
- File format: CSV with the following columns:
  - Date
  - Catchment
  - Transect
  - Plot code
  - Forest (disturbance class before 2015–16 El Niño)
  - Fire (binary: 1 = fire, 0 = no fire)
  - Tree TAG
  - Time
  - Collar height
  - CO2 initial
  - CO final
  - Flux
  - Field notes
- Each row corresponds to a collar-based measurement event; notes cover field processing details.