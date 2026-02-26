# This document is a supplement to the supporting documentation for data series detailed in: 'Clocaenog_supporting documentation_Data series.rtf'

## Dataset at a glance
- 14 columns and 7729 rows
- Experimental setup identifies 9 plots (A: Plot 1-9) with specified treatment mappings:
  - Control plots: 3, 6, 9
  - Warming plots: 1, 2, 7
  - Drought plots: 4, 5, 8
- Climate treatment (B) indicates control, drought, or warming
- Measurements collected across measurement campaigns (D: Cycle 1–9) during 2013–2014
- Timestamp fields (C, E, F, G, H) capture date, time, and temporal context
- Primary environmental measurements captured at plot scale:
  - Soil respiration (I): µmol CO2 m-2 s-1
  - Soil temperature (J): °C (0–5 cm depth)
  - Soil moisture (K): m3 m-3 (0–10 cm depth)
  - Photosynthetic active radiation (L): µmol photons m-2 s-1 (site-wide)
  - Air temperature (M): °C (plot-scale at site)
- Quality control flag (N): 1 = faulty values to exclude; 0 = values used

## Data column mapping and meaning
- A: Plot
  - Entry = Plot; Description = 1–9 treatments; mapping: Control 3,6,9; Warming 1,2,7; Drought 4,5,8
- B: Climate treatment
  - Entry = Climate treatment; Description = control, drought, or warming
- C: Timestamp
  - Entry = Date and time when measurement was taken; Description = dd/mm/yyyy hh:mm
- D: Cycle
  - Entry = Cycle; Description = 1–9 measurement campaigns during 2013–2014
- E: Date
  - Entry = Date; Description = dd/mm/yyyy
- F: Hour
  - Entry = Hour; Description = (not specified)
- G: Month
  - Entry = Month; Description = (not specified)
- H: Year
  - Entry = Year; Description = (not specified)
- I: Soil respiration
  - Entry = Soil respiration; Description = µmol CO2 m-2 s-1; Measured with Licor internal software
- J: Soil temperature
  - Entry = Soil temperature; Description = Plot-based soil temperature (0–5 cm) at the site; Unit = °C
- K: Soil moisture
  - Entry = Soil moisture; Description = Plot-based soil moisture (0–10 cm) at the site; Unit = m3 m-3
- L: Photosynthetic active radiation
  - Entry = PAR; Description = One site-based measurement for all plots; Unit = µmol photons m-2 s-1
- M: Air temperature
  - Entry = Air temperature; Description = Plot-scale air temperature at the site; Unit = °C
- N: Flag for quality control
  - Entry = QC flag; Description = 1 = faulty values — don’t use; 0 = values used

## Data collection and quality considerations
- Measurements are standardized and traceable to established instruments (e.g., Licor for soil respiration)
- Temporal coverage spans multiple campaigns during 2013–2014 (Cycles 1–9)
- QC flag provides a straightforward mechanism to filter unreliable values
- Data are prepared with explicit unit definitions and descriptive fields to support consistency across analyses

## Relevance for environmental monitoring and analysis
- Enables assessment of environmental health under controlled climate treatments (warming, drought, control)
- Facilitates standardised comparisons over time across plots and treatment types
- Supports integration with other datasets by providing explicit metadata (plot, treatment, timestamp, and quality indicators)
- Aligns with aims to verify data quality, apply standardised analysis, and present outcomes through clear formats (e.g., plots, charts, maps) while ensuring data storage and portal submission where applicable