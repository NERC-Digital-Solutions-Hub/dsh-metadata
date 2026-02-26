# EIDC dataset 3:
Short-term experiment with lighting rigs on caterpillar activity, Oxfordshire, UK, winter 2019

## Overview
- Short-term experiment to assess the impact of Artificial Light At Night (ALAN) on nocturnal caterpillar feeding behavior.
- Experiment uses lighting rigs with LED (≈5000 K) and HPS (≈2200 K) lamps and an unlit control.
- Locations: two arable sites with grass margin transects; sampling occurred across late January to mid-February 2020.
- Methodology and data handling align with prior related work on street lighting effects on insects.

## Study design and sampling
- 27 transects of 14 m established along grass margins at each site.
- Lighting rigs placed at the midpoint of selected transects; treatments assigned across transects to include LED, HPS, and unlit controls.
- On each sampling night, three active transects (LED, HPS, unlit) were present and separated by at least 60 m.
- Sampling times standardized: rigs switched on one hour before sunset; sweep-netting conducted 60–120 minutes after sunset (mean 89 minutes).
- Nights selected for mild temperatures (>6°C) to maximize caterpillar activity.
- Caterpillars identified on-site; samples stored frozen for later analysis.

## Spatial data and attributes
- Sites: North Farm and Wells Farm, with recorded approximate coordinates.
  - North Farm: ~51.6235, -1.1558
  - Wells Farm: ~51.7023, -1.0968
- Transects identified within each site (TransectID) and linked to a specific treatment (unlit, LED, HPS).
- Temporal context captured per sampling event:
  - Date of sampling
  - Sunset time (from Timeanddate.com)
  - Time of sampling (24-hour clock)
  - MinsPastSunset (minutes after sunset)
- Environmental and sampling data:
  - Larvae: number of larvae sampled per transect
  - DaysSinceStart: days since sampling began
  - Temp_forecast_BBC: forecasted minimum temperature for that date/site (°C)
  - Temp_Term_Sampling_time: actual temperature at sampling time (°C) when available
- Dataset and file: Boyes_et_al_2021_shortterm_rigs.csv

## Data quality, workflow, and provenance
- Standardised sweep-netting protocol; identifications by the lead author.
- Samples preserved at -20°C and catalogued with a dedicated recording form.
- Data entry in Excel using dropdown menus with validation; 24-hour data entry window.
- Records double-checked for errors; summary statistics and plots generated for quality checks.
- Data exported to current format to support statistical analysis.

## Data file schema (key fields)
- Date: sampling date
- Sunset: local sunset time for date/site
- Site_Name: North Farm or Wells Farm
- TransectID: transect identifier within site
- Time: sampling time (24-hour)
- MinsPastSunset: minutes since sunset at sampling time
- Treatment: unlit, LED, or HPS
- Larvae: number of larvae sampled on transect
- DaysSinceStart: days since start of sampling
- Temp_forecast_BBC: forecasted minimum temperature (°C)
- Temp_Term_Sampling_time: measured temperature at sampling (°C; n/a if unavailable)

## How this dataset can be used in GIS
- Map transect locations and treatment classes; visualize spatial distribution of sampling effort.
- Join larval counts with temporal fields to analyze spatial-temporal patterns by treatment.
- Integrate with weather data (Temp_forecast_BBC, Temp_Term_Sampling_time) for contextual analyses.
- Create time-enabled layers to explore changes across sampling nights and sunset-relative timing.
- Use coordinates to assess proximity effects between lit and unlit transects and to reproduce the experimental design spatially.

## Limitations and considerations
- Only two sites; short-term study limits generalizability.
- Sampling window limited to specific nights with mild temperatures; may bias activity observations.
- Some fields (e.g., Temp_Term_Sampling_time) may be unavailable for certain records.
- Data structure designed for reproducibility, but ensure alignment with the accompanying methods documentation when integrating with larger GIS projects.