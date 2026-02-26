# This document is a supplement to the supporting documentation for data series detailed in: 'Clocaenog_supporting documentation_Data series.rtf'

## Dataset overview
- The dataset comprises 14 columns and 7,729 rows.
- Data describe experimental plots with climate treatment assignments across 1-9 plots, including control, warming, and drought treatments.
- Measurements were collected during 2013 and 2014 across multiple measurement campaigns (cycles 1-9).
- Site-specific environmental measurements include soil respiration, soil temperature, soil moisture, photosynthetically active radiation, and air temperature.
- A quality control flag is included to indicate faulty values.

## Variable definitions (A–N)

- A: Plot
  - Unit: Factor
  - Description: 1–9 correspond to treatments; Control plots 3,6,9; Warming plots 1,2,7; Drought plots 4,5,8.
- B: Climate treatment
  - Unit: Factor
  - Description: Experimental treatments—control, drought, or warming.
- C: Timestamp
  - Unit: dd/mm/yyyy hh:mm
  - Description: Date and time when measurement was taken.
- D: Cycle
  - Unit: Factor
  - Description: 1–9 measurement campaigns during 2013 and 2014.
- E: Date
  - Unit: dd/mm/yyyy
  - Description: .
- F: Hour
  - Unit: .
  - Description: .
- G: Month
  - Unit: .
  - Description: .
- H: Year
  - Unit: .
  - Description: .
- I: Soil respiration
  - Unit: µmol CO2 m^-2 s^-1
  - Description: Measurement provided by Licor using internal software.
- J: Soil temperature
  - Unit: °C
  - Description: Plot-based soil temperature at the site (0–5 cm).
- K: Soil moisture
  - Unit: m^3 m^-3
  - Description: Plot-based soil moisture at the site (0–10 cm).
- L: Photosynthetic active radiation
  - Unit: µmol photons m^-2 s^-1
  - Description: One site-based measurement for all plots.
- M: Air temperature
  - Unit: °C
  - Description: Plot-scale air temperature at the site.
- N: Flag for quality control
  - Unit: Factor
  - Description: Quality control: 1 = faulty values—don’t use; 0 = valid values are used.