# Clocaenog_supporting documentation_Data series.rtf

## Overview
- This document is a supplement to the supporting documentation for the data series described.
- Dataset specifics: 14 columns, 7729 rows.
- Focus: plot-level climate treatments and associated environmental measurements for GIS-based analysis and map visualisation.
- Measurements include soil respiration, soil temperature, soil moisture, photosynthetic active radiation, and air temperature, with data collected using standard instruments (Licor for respiration).

## Dataset structure and key variables
- A: Plot
  - Entry = Plot; Description: 1–9 correspond to treatments; Control plots 3,6,9; Warming plots 1,2,7; Drought plots 4,5,8.
- B: Climate treatment
  - Entry = Climate treatment; Description: experimental treatments control, drought or warming.
- C: Timestamp
  - Entry = Timestamp; Unit = dd/mm/yyyy hh:mm; Description: date and time when measurement was taken.
- D: Cycle
  - Entry = Cycle; Unit = Factor; Description: 1–9 measurement campaigns during 2013 and 2014.
- E: Date
  - Entry = Date; Unit = dd/mm/yyyy; Description: date of measurement.
- F: Hour
  - Entry = Hour; Unit = .; Description: hour of measurement (not explicitly labeled further).
- G: Month
  - Entry = Month; Unit = .; Description: month of measurement.
- H: Year
  - Entry = Year; Unit = .; Description: year of measurement.
- I: Soil respiration
  - Entry = Soil respiration; Unit = µmol CO2 m-2 s-1; Description: measured by Licor using internal software.
- J: Soil temperature
  - Entry = Soil temperature; Unit = °C; Description: plot-based soil temperature at 0–5 cm depth.
- K: Soil moisture
  - Entry = Soil moisture; Unit = m3 m-3; Description: plot-based soil moisture at 0–10 cm depth.
- L: Photosynthetic active radiation (PAR)
  - Entry = PAR; Unit = µmol photons m-2 s-1; Description: site-based measurement for all plots.
- M: Air temperature
  - Entry = Air temperature; Unit = °C; Description: plot-scale air temperature at the site.
- N: Flag for quality control
  - Entry = QC flag; Unit = Factor; Description: 1 = faulty values (don’t use), 0 = values used.

## Temporal and spatial scope
- Campaigns span 2013 and 2014 (Cycle 1–9).
- Measurements are tied to specific plots (1–9) with treatment classifications.
- Multiple climate-related variables collected at the site level, enabling spatial analyses when combined with plot-level mappings.

## Data quality and usage notes
- QC flag (N) indicates whether data points should be used (0) or excluded (1).
- Measurements are conducted with standard instruments (e.g., Licor for soil respiration); ensure unit consistency when integrating with other datasets.
- Data may be distributed across different resolutions; careful cleaning and harmonisation may be required before GIS integration.

## GIS and mapping considerations
- Use A and B to classify plots by treatment type for thematic maps.
- Map soil respiration (I), soil temperature (J), soil moisture (K), PAR (L), and air temperature (M) as layer variables, with plot-level associations.
- Leverage C, D, E, F, G, and H to build time-enabled (temporal) maps and time-series analyses.
- Respect the QC flag (N) to filter out unreliable observations before visualization or analysis.

## Practical workflow recommendations
- Join this dataset with spatial plot boundaries and site polygons to create map-ready layers.
- Create separate layers or attribute fields for each measured variable (I–M) and derive summary statistics by plot or treatment group.
- Implement data quality gating using N to ensure analyses and visuals only include vetted data.