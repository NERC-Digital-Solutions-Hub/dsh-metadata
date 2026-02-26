# BLEL_Sonde_profiles.csv

## Overview
- Supporting information for a dataset collected on Blelham Tarn using a YSI EXO2 sonde.
- Collected by Emma Gray for project NEC05744 (2016–2017).
- Profiles include multiple water quality parameters across the water column at 0.5 m intervals, focusing on the lake’s deepest point (14.5 m) from a monitoring buoy.

## Parameters measured
- Chlorophyll a (µg/L) determined by fluorescence (also chemically measured for validation)
- Phycocyanin (µg/L) determined by fluorescence (not quality checked)
- Temperature (°C)
- Conductivity (µS/cm)
- Specific conductivity (µS/cm)
- Oxygen saturation (%)
- Oxygen concentration (mg/L)
- pH
- Depth: raw (m) and depth rounded to 0.5 m

## Sampling design and frequency
- Instrument: YSI EXO2 sonde
- Profiling interval: 0.5 m depth increments in the water column
- Spatial location: monitoring buoy at the deepest point of Blelham Tarn
- Temporal frequency: weekly during the stratified period (May/June–November); fortnightly or monthly outside this period
- Calibration: sensors calibrated at least every six weeks (per manufacturer specifications)

## Data structure and quality notes
- Data fields include: Date (dd/mm/yyyy), Chlorophyll a, phycocyanin, temperature, conductivity, specific conductivity, oxygen saturation, oxygen (mg/L), pH, depth (raw), depth (rounded)
- Chlorophyll a validated against chemical measurements with R² = 0.56 (p < 0.05), indicating a moderate correlation
- Phycocyanin values are not quality checked
- No additional metadata about data quality checks beyond the mentioned calibration

## Spatial and temporal context
- Location: Blelham Tarn, Lake District, North West England
- Deepest point referenced (14.5 m) per bathymetry from Ramsbottom (1976)

## Access, provenance, and references
- File name: BLEL_Sonde_profiles.csv
- Collected by: Emma Gray
- Reference for depth context: Ramsbottom, A. (1976) Depth charts of the Cumbrian lakes, Freshwater Biological Association, Kendal

## Considerations for data use and governance
- Data gaps may arise due to irregular sampling outside the stratified period and potential quality checks limitations on some parameters
- Data discoverability is aided by clear field definitions and calibration notes; provenance tied to a named project and collector
- Users should consider the moderate agreement between fluorescence-based chlorophyll and chemical measurements when using chlorophyll data for trend analysis or cross-study comparisons