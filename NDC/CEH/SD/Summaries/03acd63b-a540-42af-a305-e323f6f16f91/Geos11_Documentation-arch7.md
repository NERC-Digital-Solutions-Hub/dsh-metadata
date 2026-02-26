# Overview of data

## Scope and Purpose
- Compilation of results from the stream metabolism component of the NERC Macronutrients consortium, led by Prof. Mark Trimmer, studying lateral exchange in the seaward flux of C, N, and P.
- Field data collected in Hampshire Avon catchment to measure in situ atmospheric conditions that accompany riverine measurements.
- Data collected with a high-precision GEOS 11 weather station to enable integration with riverine metabolism data.

## Field Campaigns and Data Collection
- Four field campaigns conducted to measure atmospheric data in rivers of varying land-river connectivity.
- Campaign timing:
  - Spring 2013: 23/04 – 09/05/2013
  - Summer 2013: 31/07 – 16/08/2013
  - Autumn 2013: 29/10 – 11/11/2013
  - Winter 2014: 28/01 – 09/02/2014
  - Note: Data collection was not performed at site CE1 in winter 2014 due to flooding.
- Instrument: SKYWATCH GEOS 11 high-precision portable weather station (JDC Electronic SA). Factory calibrated prior to field measurements (March 2013).
- Sampling frequency: 15 to 30 seconds, depending on battery life and field conditions.
- Positioning: Station positioned about 1–4 meters above the stream surface, depending on stream morphology and access.

## Geographic Sites and Timing
- River sites (mapped by SiteCode and coordinates):
  - CE1: River Ebble (51.027499°N, -1.9217089°E)
  - GA2: River Avon (51.318289°N, -1.8600020°E)
  - GN1: River Nadder (51.043849°N, -2.1118158°E)
  - CW2: River Wylye (51.142475°N, -2.2033140°E)
  - AS1 (aka AP): Tributary of the River Sem (51.055413°N, -2.1568407°E)
  - AS2 (aka AS): River Sem (51.045826°N, -2.1104425°E)
- File naming convention: GEOS11_'SiteCode'_'Season'.CSV (e.g., Geos11_AP_autumn.CSV)
- Seasons in file naming reflect the field campaigns (autumn, spring, summer, winter).

## Data Files and Naming Convention
- Total: 23 CSV data files accompany the overview.
- Example patterns:
  - Geos11_AP_autumn.CSV, Geos11_AP_spring.CSV, Geos11_AP_summer.CSV, Geos11_AP_winter.CSV
  - Geos11_AS_autumn.CSV, Geos11_AS_spring.CSV, Geos11_AS_summer.CSV, Geos11_AS_winter.CSV
  - Geos11_CE1_autumn.CSV, Geos11_CE1_spring.CSV, Geos11_CE1_summer.CSV, Geos11_CE1_winter.CSV
  - Geos11_CW2_autumn.CSV, Geos11_CW2_spring.CSV, Geos11_CW2_summer.CSV, Geos11_CW2_winter.CSV
  - Geos11_GA2_autumn.CSV, Geos11_GA2_spring.CSV, Geos11_GA2_summer.CSV, Geos11_GA2_winter.CSV
  - Geos11_GN1_autumn.CSV, Geos11_GN1_spring.CSV, Geos11_GN1_summer.CSV, Geos11_GN1_winter.CSV
- Each file corresponds to a particular site and season, enabling seasonal GIS analyses and cross-site comparisons.

## Columns and Measurements
- Core columns:
  - DateTime: Date and time (MM/DD/YYYY hh:mm:ss)
  - Date: Date (MM/DD/YYYY)
  - Time: Time (hh:mm:ss)
  - Wind: Wind speed [m/s] (resolution 0.1 m/s; accuracy ±2% or measured value)
  - Temperature: Air temperature [°C] (resolution 0.1 °C; accuracy ±2% or 0.5 °C at 25 °C)
  - Humidity: Relative humidity [%] (resolution 0.1 %RH; accuracy ±2% at 50 %RH)
  - Pressure: Atmospheric pressure [hPa] (resolution 0.1 hPa; accuracy 0.5% or 1.5 hPa at 25 °C)
  - Direction: Wind direction [°N] from GEOS11 internal compass (resolution 1°; accuracy ±3%)
- Data quality notes:
  - NaN entries indicate data not collected (e.g., due to battery changes, data download issues) or data contaminated (e.g., insufficient wind for stable direction data).
  - Wind direction and other sensor readings rely on in-field calibration and instrument-specific procedures.

## Data Quality, Provenance, and GIS Integration Considerations
- Provenance: Data collected under the NERC Macronutrients project, with field leadership and publication details referenced in the overview.
- Calibration: GEOS 11 units factory-calibrated before field deployment; field calibration and recalibration applied as per GEOS 11 manual.
- GIS relevance:
  - Spatially referenced by site coordinates and season-encoded data files, suitable for joining with GIS layers of river networks and catchment boundaries.
  - Multi-season time stamps enable temporal analyses of atmospheric conditions in relation to stream metabolism measurements.
  - NaN handling required for gaps in temporal data during processing and analysis.
- Data availability: 23 accompanying CSV files providing comprehensive atmospheric context for the four field campaigns.