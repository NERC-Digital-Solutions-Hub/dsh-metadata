# Clocaenog_supporting documentation_Data series.rtf

## Overview
- Supplement to the supporting documentation for data series; dataset contains 14 columns and 7729 rows.
- Captures a climate-treatment experiment across plots with three treatments: Control, Warming, and Drought.
- Plot-treatment mapping: Control plots 3, 6, 9; Warming plots 1, 2, 7; Drought plots 4, 5, 8.
- Measurement campaigns span 2013 and 2014 (Cycle 1–9).

## Data structure and key columns
- A (Plot): Plot identifier; categorical factor. Description links each plot to a treatment group.
- B (Climate treatment): Experimental treatment category — control, drought, or warming.
- C (Timestamp): Date and time of measurement (dd/mm/yyyy hh:mm).
- D (Cycle): Measurement campaign number (1–9) across 2013–2014.
- E (Date): Date of measurement (dd/mm/yyyy).
- F (Hour): Hour of measurement.
- G (Month): Month of measurement.
- H (Year): Year of measurement.
- I (Soil respiration): Soil respiration in µmol CO2 m-2 s-1; measured with Licor software.
- J (Soil temperature): Soil temperature at 0–5 cm (°C).
- K (Soil moisture): Soil moisture at 0–10 cm (m3 m-3).
- L (Photosynthetic active radiation): PAR in µmol photons m-2 s-1; one site-based measurement for all plots.
- M (Air temperature): Plot-scale air temperature at the site (°C).
- N (Flag for quality control): QC indicator; 1 = faulty values (do not use), 0 = values used.

## Data quality and governance
- Quality control flag (N) guides data usability; ensure exclusion of flagged values.
- Units are specified for I, J, K, and L to support consistent analysis.
- Metadata alongside columns provides context for data discovery and reuse (e.g., treatment mapping, measurement timing).

## Implications for data strategy and usage
- Clear, fully described schema supports governance, discoverability, and cross-plot analysis for treatment effects on soil respiration, temperature, moisture, and light.
- Time-series structure (timestamps, cycles, and date components) enables trend and cycle-based analyses across 2013–2014.
- Distinct separation between plot-level measurements (I–M) and site-level PAR (L) highlights considerations for data integration and scale in analyses.
- The explicit QC flag facilitates data cleaning workflows and ensures data quality is enforceable in downstream products.

## Provenance and access notes
- Dataset documented as a supplement to the main Clocaenog data series documentation.
- Measurements are reported as described and originate from field measurements (Licor) and site sensors for environmental variables.