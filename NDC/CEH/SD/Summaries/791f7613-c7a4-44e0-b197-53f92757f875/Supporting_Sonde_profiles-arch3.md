# BLEL_Sonde_profiles.csv

## Overview
- Supporting information for NEC05744 project detailing water quality profiling at Blelham Tarn using a YSI EXO2 sonde.
- Aims to capture vertical profiles of key biological and physicochemical parameters to inform monitoring of lake health.

## Instrument and sampling design
- Instrument: YSI EXO2 sonde.
- Profiles collected at the lake’s deepest point from a monitoring buoy (approx. 14.5 m).
- Profiles recorded at 0.5 m depth intervals.
- Sampling frequency: weekly during the stratified period (May/June–November); fortnightly or monthly outside of this period.
- Years: 2016 and 2017.
- Sensor calibration: at least every six weeks per manufacturers’ specifications.

## Parameters measured
- Chlorophyll a (µg/L) determined by fluorescence (biomass indicator).
- Phycocyanin (µg/L) determined by fluorescence (cyanobacteria indicator) — not quality checked.
- Water temperature (°C).
- Conductivity (µS/cm) and specific conductivity (µS/cm).
- Oxygen saturation (%).
- Oxygen concentration (mg/L).
- pH.

## Data structure and notes
- Data fields: Date (dd/mm/yyyy), Chlorophyll a (µg/L by fluorescence), Phycocyanin (µg/L by fluorescence, not QA’d), temperature (°C), conductivity (µS/cm), specific conductivity (µS/cm), oxygen saturation (%), oxygen (mg/L), pH, depth (raw in meters), depth (rounded to 0.5 m).
- Depth is captured at 0.5 m resolution for consistency with the profiling interval.

## Quality, validation, and caveats
- Chlorophyll a fluorescence measurements show a relationship with chemically determined chlorophyll (R^2 = 0.56, p < 0.05), indicating partial validation against a chemical standard.
- Phycocyanin data not quality checked within this dataset, signaling potential data quality considerations for cyanobacteria indicators.
- Regular calibration enhances data reliability; however, some parameters (e.g., phycocyanin) may require additional QA/QC before use in formal assessments.

## Context and location
- Location: Blelham Tarn, Lake District, North West England.
- Monitoring buoy located at the lake’s deepest point.
- Figure reference: bathymetry and buoy location described (based on Ramsbottom 1976 depth charts).

## Reference
- Ramsbottom, A. (1976) Depth charts of the Cumbrian lakes, Freshwater Biological Association, Kendal.