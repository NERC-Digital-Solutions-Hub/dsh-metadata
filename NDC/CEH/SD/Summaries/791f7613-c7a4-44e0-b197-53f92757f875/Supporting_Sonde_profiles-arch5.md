# BLEL_Sonde_profiles.csv

## Overview
- Supporting information file BLEL_Sonde_profiles.csv collected by Emma Gray for project NEC05744.
- Uses a YSI EXO2 sonde to record vertical profiles of water quality parameters in Blelham Tarn.
- Parameters include chlorophyll a (phytoplankton biomass indicator), phycocyanin (cyanobacteria indicator), temperature, conductivity, specific conductivity, oxygen (saturation and mg/L), and pH.
- Profiles taken at 0.5 m depth intervals in the lake, from the monitoring buoy at the deepest point (14.5 m).

## Instrumentation and parameters
- Instrument: YSI EXO2 sonde.
- Parameters collected: Chlorophyll a (µg/L) via fluorescence; phycocyanin (µg/L) via fluorescence (not quality checked); water temperature (°C); conductivity (µS/cm); specific conductivity (µS/cm); oxygen (% saturation); oxygen (mg/L); pH; depth (raw and rounded to 0.5 m).
- Chlorophyll a fluorescence measurements have been compared to chemically determined chlorophyll with a reported R² = 0.56 (p < 0.05), indicating a moderate relationship.

## Sampling design and schedule
- Sampling conducted in Blelham Tarn during 2016 and 2017.
- Frequency: weekly during the stratified period (May/June to November); fortnightly or monthly outside of this period.
- Sampling depth resolved to 0.5 m increments, covering the water column from surface toward the deep point.

## Data quality and processing
- Sensor calibrations performed at least every six weeks, following manufacturer specifications.
- Phycocyanin data noted as not quality checked.
- Chlorophyll a comparison to chemical measurements provided as a quality check reference.

## Data structure and variables
- Data fields: Date (dd/mm/yyyy); Chlorophyll a (µg/L) from fluorescence; Phycocyanin (µg/L) from fluorescence (not QC’d); Water temperature (°C); Conductivity (µS/cm); Specific conductivity (µS/cm); Oxygen (% saturation); Oxygen (mg/L); pH; Depth (m, raw); Depth (m, rounded to 0.5 m).
- Data arrangement supports vertical profiling at 0.5 m depth intervals within the lake.

## Location and context
- Location: Blelham Tarn, Lake District, North West England.
- Monitoring buoy located at the lake’s deepest point (14.5 m).
- Figure referenced for location context (depth bathymetry from Ramsbottom 1976).

## Provenance and reference
- Collected for project NEC05744.
- Reference material: Ramsbottom, A. (1976) Depth charts of the Cumbrian lakes. Freshwater Biological Association, Kendal.

## Data governance considerations for Data Stewards
- Ensure metadata captures instrument (YSI EXO2), parameter definitions, units, calibration frequency, and sampling schedule.
- Document quality flags: chlorophyll a validated against chemical measurements (R², p-value) and note that phycocyanin data are not quality checked.
- Maintain clear provenance: collector, project name, and collection period (2016–2017) with location context.
- Note any limitations or non-interoperable aspects (e.g., raw depth vs. 0.5 m rounded depth) to aid discoverability and reuse.
- Ensure data sharing, updates, and versioning plans are defined, given the historical nature and structured depth profiling.