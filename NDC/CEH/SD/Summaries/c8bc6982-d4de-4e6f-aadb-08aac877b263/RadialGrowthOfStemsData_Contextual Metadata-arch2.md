# Radial growth in stems in human-modified forests of Eastern Amazonia

- The dataset RadialGrowthOfStemsData.csv records litterfall measurements across 20 Amazonian forest plots (each 250 x 10 m) representing a gradient of prior human disturbance before the 2015-16 El Niño.
- Disturbance classes (5 plots each): undisturbed primary forests, logged primary forests, logged-and-burned primary forests, and secondary forests; classification based on satellite canopy disturbance analysis (1988–2010) and field assessments (fire scars, charcoal, logging debris).
- Timeframe: radial growth data collected from December 2014 to September 2018 as part of the NERC Human-modified Tropical Forests Programme (HMTF; Grant NE/K016431/1).

## Data collection methods

- In each plot, trees and palms were stratified into five DBH size classes: 10–19.99 cm, 20–29.99 cm, 30–39.99 cm, 40–49.99 cm, and ≥50 cm.
- At least 50 dendrometer bands per plot (10 bands per size class) were installed, including all lianas ≥10 cm DBH.
- Dendrometers installed 10 cm above the DBH point of measurement.
- A one-month settling period after installation to mark the zero line, followed by first measurement five months after marking, then monthly measurements.
- If a band was damaged, it was replaced and reinstalled; if a stem died, the band was removed and a new one installed on another tree in the same size class.
- Some stems showed negative growth due to bark water loss; negative values were not corrected, as positive growth includes water accumulation.

## Spatial and temporal context

- Coordinates for plots provided (20 plots across microcatchments), located in Eastern Amazonia with latitudes around -2 to -3 and longitudes around -54 to -55.

## Data structure and key fields

- File: RadialGrowthOfStems.csv
- Core fields:
  - Catchment, Transect, Plot: identifiers for each plot within catchments
  - Rainfor: plot code per ForestPlots database
  - Forest: disturbance class before the El Niño
  - Fire_ElNino: whether the plot burned during the 2015-16 El Niño
  - Tree_tag: unique identifier for each dendrometer-installed individual
  - Tree_code: composite code (bacia, plot, tree tag)
  - DBH: diameter at breast height (measured in 2014)
  - Life form: Tree (A), Liana (C), or Palm (P)
  - Re-installed: whether a dendrometer was re-installed during the study
  - Data-Dec14 onward: monthly data columns
  - mm-Dec14, mm-Jan15, etc.: radial growth in millimeters per month
  - OBS-Dec14, etc.: field notes for each month
- The dataset captures monthly radial growth measurements from Dec 2014 through Sep 2018, linked to disturbance history and El Niño context.

## Relevance for monitoring and analysis

- Provides a standardised, longitudinal dataset to compare stem radial growth across disturbance classes and over time.
- Enables exploration of growth responses to disturbance history, El Niño events, and canopy/forest structure changes.
- Supports integration with other datasets (e.g., canopy disturbance, climate data) to enhance environmental health assessments and policy-relevant monitoring.

## Data management and accessibility considerations

- Associated with the NERC HMTF programme data collection.
- Dataset structure includes cross-references to ForestPlots and explicit metadata on disturbance and fire events.
- For ongoing monitoring and broader use, consider sharing underlying data and methods via appropriate data portals to improve accessibility and re-use, aligning with the challenge of increasing dataset value and accessibility highlighted for analysts monitoring the environment.