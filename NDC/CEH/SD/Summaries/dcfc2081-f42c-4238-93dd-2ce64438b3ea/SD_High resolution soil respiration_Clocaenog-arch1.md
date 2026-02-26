# Clocaenog_supporting documentation_Data series.rtf

## Overview
- A supplementary dataset description for data series used in the Clocaenog study.
- Dataset characteristics: 14 columns, 7729 rows.
- Focuses on climate treatments, plot-level measurements, and environmental conditions collected during 2013–2014.

## Dataset structure
- Each row represents a measurement instance across plots and times.
- 14 columns capturing plot identifiers, treatments, timestamps, campaigns, and environmental/biophysical measurements.
- Data quality is flagged per row to indicate usable observations.

## Variables and units (A–N)
- A: Entry = Plot; Unit = Factor; Description = 1 to 9; treatment mapping: Control plots 3,6,9; Warming plots 1,2,7; Drought plots 4,5,8.
- B: Entry = Climate treatment; Unit = Factor; Description = Experimental treatments: control, drought, or warming.
- C: Entry = Timestamp; Unit = dd/mm/yyyy hh:mm; Description = Date and time of measurement.
- D: Entry = Cycle; Unit = Factor; Description = 1–9 measurement campaigns during 2013 and 2014.
- E: Entry = Date; Unit = dd/mm/yyyy; Description = (date of measurement).
- F: Entry = Hour; Unit = ; Description = (hour of measurement).
- G: Entry = Month; Unit = ; Description = (month).
- H: Entry = Year; Unit = ; Description = (year).
- I: Entry = Soil respiration; Unit = µmol CO2 m^-2 s^-1; Description = Measurement via Licor software.
- J: Entry = Soil temperature; Unit = °C; Description = Plot-based soil temperature at 0–5 cm.
- K: Entry = Soil moisture; Unit = m^3 m^-3; Description = Plot-based soil moisture at 0–10 cm.
- L: Entry = Photosynthetic active radiation; Unit = µmol photons m^-2 s^-1; Description = Site-based measurement for all plots.
- M: Entry = Air temperature; Unit = °C; Description = Plot-scale air temperature at site.
- N: Entry = Flag for quality control; Unit = Factor; Description = QC: 1 = faulty values – don't use; 0 = values used.

## Experimental design and coverage
- Treatments:
  - Control plots: 3, 6, 9
  - Warming plots: 1, 2, 7
  - Drought plots: 4, 5, 8
- Climate treatment (B) captures control, drought, or warming conditions.
- Temporal span: Measurement campaigns across 2013 and 2014 (cycles D 1–9).
- Measurements include soil respiration, soil temperature, soil moisture, PAR, and air temperature.

## Measurement methods and quality
- Soil respiration measured using Licor; recorded with Licor’s internal software.
- Quality control flag (N) indicates whether observations should be used (0) or are faulty (1) and should be discarded.
- Site-level radiation (PAR) is a single value per site for all plots; other variables are plot-specific.

## How this data can be used (Analysts perspective)
- Identify correlations between soil respiration and environmental variables (soil temp, moisture, PAR, air temp) under different climate treatments.
- Compare warming, drought, and control plots to assess treatment effects on soil respiration.
- Develop predictive models of soil respiration as a function of temperature, moisture, and radiation across campaigns.
- Integrate with other datasets by respecting the structure (A–N) and QC flag to ensure robust analyses.

## Practical considerations and caveats
- Data scale and accessibility: values are organized at the plot level with campaign-level timing; ensure alignment with other local datasets if integrating.
- Data quality: apply QC flag (N) to filter observations; 1 indicates faulty values to exclude.
- Temporal resolution: campaigns span 2013–2014; consider potential seasonal and inter-annual variability when modeling.
- Data provenance: measurements come from Licor instrumentation; reference the internal software documentation for exact measurement procedures.