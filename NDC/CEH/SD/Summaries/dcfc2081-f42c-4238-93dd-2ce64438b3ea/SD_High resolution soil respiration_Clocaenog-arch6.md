# This document is a supplement to the supporting documentation for data series detailed in: 'Clocaenog_supporting documentation_Data series.rtf'

## Overview
- Metadata supplement for a dataset with 14 columns and 7,729 rows.
- Experimental setup: climate treatment study at plot level with treatments including Control, Warming, and Drought.
- Includes 9 plots with predefined treatment mappings and 2013–2014 measurement campaigns.

## Dataset composition
- Plots: A indicates Plot, coded as a Factor with 9 plots.
- Treatments: B describes climate treatment (control, drought, warming) corresponding to each plot.
- Time/data collection: C (Timestamp), D (Cycle), E (Date), F (Hour), G (Month), H (Year) capture temporal context.
- Measurements: I–M describe environmental measurements:
  - I: Soil respiration (µmol CO2 m-2 s-1), measured via LICOR software
  - J: Soil temperature (°C) at 0–5 cm
  - K: Soil moisture (m3 m-3) at 0–10 cm
  - L: Photosynthetic active radiation (µmol photons m-2 s-1) site-wide
  - M: Air temperature (°C) at plot level
- Quality: N indicates quality control flag (1 = faulty values to exclude; 0 = valid values)

## Column definitions (concise)
- A – Plot: Entry = Plot; Type = Factor; Description = plot-level identifier with 1–9 mappings (see below)
- B – Climate treatment: Entry = Climate treatment; Type = Factor; Description = control, drought, or warming
- C – Timestamp: Entry = Timestamp; Type = (datetime); Description = date and time of measurement (dd/mm/yyyy hh:mm)
- D – Cycle: Entry = Cycle; Type = Factor; Description = measurement campaigns 1–9 (during 2013–2014)
- E – Date: Entry = Date; Type = Date (dd/mm/yyyy)
- F – Hour: Entry = Hour; Type = (numeric or categorical); Description = hour of measurement
- G – Month: Entry = Month; Type = (numeric); Description = month of measurement
- H – Year: Entry = Year; Type = (numeric); Description = year of measurement
- I – Soil respiration: Entry = Soil respiration; Unit = µmol CO2 m-2 s-1; Description = measurement by LICOR
- J – Soil temperature: Entry = Soil temperature; Unit = °C; Description = plot-based soil temp at 0–5 cm
- K – Soil moisture: Entry = Soil moisture; Unit = m3 m-3; Description = plot-based soil moisture at 0–10 cm
- L – Photosynthetic active radiation: Entry = PAR; Unit = µmol photons m-2 s-1; Description = site-wide measurement
- M – Air temperature: Entry = Air temperature; Unit = °C; Description = plot-scale air temperature
- N – Quality control: Entry = QC flag; Type = Factor; Description = 1 = faulty values (do not use), 0 = valid values

## Experimental design and temporal context
- Treatments per plot: A describes Plot; B maps to 9 plots with controls and treatment groups (Control plots 3, 6, 9; Warming plots 1, 2, 7; Drought plots 4, 5, 8).
- Campaigns: D indicates 9 measurement campaigns across 2013–2014 (Cycle 1–9).
- Temporal components: E (Date), F (Hour), G (Month), H (Year) provide granular time context for each observation.

## Data quality and usage notes
- N QC flag identifies unusable values (1 = faulty; 0 = usable); use this to filter data prior to analysis.
- Data are intended to support cross-plot and cross-treatment analyses, trend identification, and creation of data products (dashboards, reports) for end users.

## How this supports data use and data products
- Enables self-serve exploration by providing standardized column definitions and units.
- Facilitates cleaning and integration with other datasets by explicit data types, units, and QC indicator.
- Supports documentation of the experimental design (plot-level treatments, campaigns) for accurate interpretation and reproducibility.