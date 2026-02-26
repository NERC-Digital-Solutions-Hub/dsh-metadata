# SUPPORTING DOCUMENTATION:

- This document describes a cricket behavior study with an emphasis on data that could be represented and analyzed in GIS formats. It outlines data collection, structure, quality control, and processing, with three main data files and spatial context around burrows, populations, and weather.

## Overview
- Behavioral data were collected by video-recording male crickets around burrows using 140 infrared cameras, 24/7.
- Target behaviors were quantified as time spent (minutes) under observation, with temperature included as a covariate.
- The dataset comprises three data files, each tying observations to individuals, burrows, populations, and environments.
- Spatial context includes burrow locations, population localities, and weather sensor sites within a meadow in Asturias, North Spain.

## Datasets and data fields
- 2019_MaleBehaviour
  - Fields: Tag (individual ID), Pop (population of origin; 'H' = high altitude, 'L' = low altitude), Burrow (location), Behav (five behaviors: Outside, Feeding, Calling, Fleeing, Inside, plus SunAvailable/InSun), Date, Duration (minutes), Temp (mean ground-level temperature over duration).
- 2019_Populations
  - Fields: Population code, Locality name, Altitude, Coordinates (spatial reference for population locations).
- 2019_Specimens
  - Fields: Population, Tag, Sex (MA/Fa), Mass (g at release), Released (date).
- All datasets are arranged to support linking observations to individuals, burrows, and populations, enabling map-based analyses of spatial patterns in behavior and habitat use.

## Spatial relevance for GIS
- Burrows serve as primary spatial units for behavioral observations; each burrow is uniquely numbered for the season.
- Population localities provide latitude/longitude coordinates and altitude context for comparative analyses (high vs low altitude populations).
- Temperature sensors and weather data are spatially distributed around the meadow, enabling spatially explicit covariate analyses.
- Video cameras were installed at burrows (and selectively at female burrows), creating a spatially distributed observation network.

## Data collection and instrumentation
- Infrared cameras (Vivotek IP8330) monitored burrows; cameras connected to five computers with motion-activated recording software.
- Weather data collected via a central weather station (Davis Vantage Pro2) logging variables every ten minutes, plus six surface sensors (three above ground, three in buried burrow pipes).
- Calibration relied on time from computer clocks; no additional specialized calibration beyond standard equipment.

## Quality control and data processing
- Data quality checks used Access queries to detect inconsistencies (e.g., a cricket recorded as using two burrows simultaneously).
- Analytical workflow (per day): 
  - Step 1: rough pass across 16 cameras to identify burrow activity during each hour.
  - Step 2: per-camera detailed review to determine exact start times of observed behaviors.
- Observations were recorded in MS Excel and then imported into MS Access for further processing.
- To minimize observer bias across altitudes, nine observers managed video groups and cross-checked activity identifications.

## Experimental design and context
- Fieldwork occurred in spring 2019: 132 adult male crickets and 127 adult females collected from 10 locations in Asturias (five below 160 m, five above 1,200 m).
- Females were reared in a shared set of boxes; males were reared separately by population.
- On release (late April 2019), crickets were tagged with unique two-character IDs and assigned to artificial burrows around the meadow; cages were used temporarily to limit movement after release.
- Continuous, 24/7 recording continued through the breeding season; occupancy of burrows was monitored directly when not videoed.

## Field work and laboratory instrumentation
- Cameras: 140 IR cameras (Vivotek IP8330) with motion-activated recording software (i-Catcher).
- Weather: Central weather station plus six soil/ground sensors distributed around the meadow to capture microclimate variation.
- Data handling: Video-derived behavioral events were organized into a database (MS Access) after recording and verification.

## Data access, collaboration, and usage notes
- The authors invite collaboration and offer additional information and expertise for data analysis.
- Researchers planning to analyze these data are advised to contact Tom Tregenza prior to use.

## References
- Rodríguez-Muñoz, R., et al. (2010). Natural and sexual selection in a wild insect population. Science 328: 1269-1272.