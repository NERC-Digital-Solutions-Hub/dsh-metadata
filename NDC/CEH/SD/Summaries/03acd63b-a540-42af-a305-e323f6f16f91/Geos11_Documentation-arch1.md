# Overview of data

## Context and purpose
- Compilation of results from the stream metabolism component of the NERC Macronutrients consortium, led by Prof. Mark Trimmer, focusing on the role of lateral exchange in the seaward flux of C, N, and P.
- Field measurements conducted in Hampshire Avon catchment to support analysis of atmospheric conditions affecting river metabolism.

## Field campaigns and sites
- Four field campaigns measuring in situ atmospheric data:
  - Spring 2013 (23/04 – 09/05/2013)
  - Summer 2013 (31/07 – 16/08/2013)
  - Autumn 2013 (29/10 – 11/11/2013)
  - Winter 2014 (28/01 – 09/02/2014)
  - Note: Data collection not performed at site CE1 during winter due to flooding.
- River/site codes and locations:
  - CE1: River Ebble
  - GA2: River Avon
  - GN1: River Nadder
  - CW2: River Wylye
  - AS1 (AP): Tributary of River Sem
  - AS2 (AS): River Sem
  - Precise coordinates provided for each site
- File structure: 23 CSV files named Geos11_'SiteCode'_'Season'.CSV
- Field deployment details: GEOS 11 weather station positioned 1–4 m above stream surface; sampling every 15–30 s (subject to battery life)

## Instrumentation and data collection
- Instrument: SKYWATCH GEOS 11 high-precision portable weather station (JDC Electronic SA).
- Calibration and quality control:
  - Factory-calibrated prior to March 2013.
  - Compass/direction calibrated in the field before campaigns and after battery changes to minimize drift.
- Sampling considerations: data gaps (NaN) occur due to battery changes, data download, weather conditions, or other technical issues.

## Data columns and structure
- Columns included in each file:
  - DateTime
  - Date
  - Time
  - Wind (m/s): resolution 0.1 m/s; accuracy ±2% or measured value
  - Temperature (°C): resolution 0.1 °C; accuracy ±2% (or 0.5 °C at 25 °C)
  - Humidity (%rH): resolution 0.1 %rH; accuracy ±2% at 50 %rH
  - Pressure (hPa): resolution 0.1 hPa; accuracy 0.5% (or 1.5 hPa) at 25 °C
  - Direction (°N): wind direction from GEOS 11 compass; resolution 1°; accuracy ±3°
- NaN values indicate missing data due to battery/data issues or contamination (e.g., insufficient wind to stable collect wind direction data)

## Data provenance and metadata
- Project and leadership: data from the NERC Macronutrients consortium; field collection led by Prof. R.N. Glud; data contributors include L. Rovelli, K. Attard, and Assoc. Prof. H. Stahl; associated with Prof. Mark Trimmer’s team.
- Documentation notes: detailed information on GEOS11 equipment and calibration procedures; site coordinates and season-specific campaigns are explicitly recorded.

## Considerations for analysis
- Data quality and coverage:
  - Seasonal and site coverage varies; ensure handling of missing data and zero/low-wind periods.
  - Notable gap: CE1 winter dataset missing due to flooding.
- Potential analytic uses:
  - Correlate atmospheric variables (wind, temperature, humidity, pressure, wind direction) with stream metabolism metrics.
  - Integrate these atmospheric measurements with hydrological and biogeochemical data to model C, N, and P flux dynamics.
  - Use metadata (site locations, seasons, calibration notes) to standardize comparisons across sites and campaigns.