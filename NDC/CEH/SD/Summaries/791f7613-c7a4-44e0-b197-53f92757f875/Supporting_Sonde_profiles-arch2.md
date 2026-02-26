# Supporting information

- File: BLEL_Sonde_profiles.csv
- Collected by Emma Gray for the project NEC05744
- Purpose: Profile water quality parameters to monitor environmental health at Blelham Tarn over time using standardized data collection methods

## What was collected
- Parameters via YSI EXO2 sonde:
  - Chlorophyll a (phytoplankton biomass indicator) via fluorescence
  - Phycocyanin (cyanobacteria indicator) via fluorescence
  - Temperature
  - Conductivity
  - Specific conductivity
  - Oxygen saturation (%)
  - Oxygen concentration (mg/L)
  - pH
- Depth-resolved profiles at 0.5 m intervals in the water column

## Temporal coverage and site
- Location: Blelham Tarn, Lake District, NW England
- Monitoring buoy located at the lake’s deepest point (14.5 m)
- Sampling frequency (2016–2017):
  - Weekly during the stratified period (May/June–November)
  - Fortnightly or monthly outside the stratified period

## Instrumentation and calibration
- Instrument: YSI EXO2 sonde
- Calibration: Sensors calibrated at least every six weeks (per manufacturer specifications)
- Chlorophyll a validation: Fluorescence-derived chlorophyll a compared with chemically determined measurements; R² = 0.56, p < 0.05

## Data structure and content
- Fields:
  - Date (dd/mm/yyyy)
  - Chlorophyll a (µg/L, fluorescence)
  - Phycocyanin (µg/L, fluorescence; not quality checked)
  - Water temperature (°C)
  - Conductivity (µS/cm)
  - Specific conductivity (µS/cm)
  - Oxygen (% saturation)
  - Oxygen (mg/L)
  - pH
  - Depth (m – raw)
  - Depth (m – rounded to 0.5 m)

## Location context and reference
- Figure: Location of Blelham Tarn and buoy at the deepest point
- Bathymetry source: Ramsbottom (1976)

## Data quality and use considerations
- Phycocyanin data not quality checked
- Chlorophyll a relationship with chemical measurements indicates applicability with some uncertainty (R² = 0.56)

## Relevance to environmental monitoring aims
- Provides standardized, depth-resolved water quality data suitable for temporal trend analysis and assessment of environmental health and policy performance
- Aligns with ongoing monitoring responsibilities and data-stewardship practices (calibration, clear data structure, and documentation) to enable data reuse and potential data sharing

## Reference
- Ramsbottom, A. (1976) Depth charts of the Cumbrian lakes, Freshwater Biological Association, Kendal