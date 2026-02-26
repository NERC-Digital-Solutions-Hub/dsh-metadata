# Overview of data

- Purpose and scope
  - Compilation of results from the stream metabolism component of the NERC Macronutrients consortium, led by Prof. Mark Trimmer, focusing on the role of lateral exchange in the seaward flux of carbon, nitrogen, and phosphorus.
  - Field measurements conducted to capture in situ atmospheric data in rivers with varying land-river connectivity within the Hampshire Avon catchment.

- Data collection and instrumentation
  - Four field campaigns using a SKYWATCH GEOS 11 high-precision portable weather station (JDC Electronic SA).
  - Station varied its height from about 1–4 m above the stream surface depending on morphology and access; factory-calibrated prior to campaigns (March 2013).
  - Sampling frequency: 15–30 seconds (subject to battery life).

- File structure and naming
  - 23 CSV data files accompany the overview, named as GEOS11_'SiteCode'_'Season'.CSV (e.g., Geos11_CE1_autumn.CSV).
  - Column headers include DateTime, Date, Time, Wind, Temperature, Humidity, Pressure, Direction.
  - NaN values indicate data not collected (e.g., due to battery or download issues) or data flagged as contaminated (e.g., insufficient wind for stable wind direction data).

- Site codes, locations, and campaigns
  - SiteCode mappings:
    - CE1: River Ebble (51.027499 °N, -1.9217089 °E)
    - GA2: River Avon (51.318289, -1.8600020)
    - GN1: River Nadder (51.043849, -2.1118158)
    - CW2: River Wylye (51.142475, -2.2033140)
    - AS1 (AP): Tributary of the River Sem (51.055413, -2.1568407)
    - AS2 (AS): River Sem (51.045826, -2.1104425)
  - Field campaigns and dates:
    - Spring 2013: 23/04 – 09/05/2013
    - Summer 2013: 31/07 – 16/08/2013
    - Autumn 2013: 29/10 – 11/11/2013
    - Winter 2014: 28/01 – 09/02/2014
  - Note: Field data collection at site CE1 did not occur in winter due to flooding.

- Data content and measurement specifics
  - Columns and units:
    - Wind: wind speed in m/s (resolution 0.1 m/s; accuracy ±2% or the measured value)
    - Temperature: air temperature in °C (resolution 0.1 °C; accuracy ±2% or 0.5 °C at 25 °C)
    - Humidity: relative humidity in % (resolution 0.1%; accuracy ±2% at 50% RH)
    - Pressure: atmospheric pressure in hPa (resolution 0.1 hPa; accuracy 0.5% or 1.5 hPa at 25°C)
    - Direction: wind direction in degrees from North (resolution 1°; accuracy ±3%)
  - Direction/compass calibration: internal compass calibrated in the field before campaigns and after battery changes to minimize drift.
  - Data quality notes: NaN values indicate missing or contaminated data; some columns may have gaps due to battery replacement, data download issues, or other technical difficulties.
  - Data provenance: data collected by field teams led by researchers associated with the NERC Macronutrients project, with explicit documentation on calibration and instrumentation. AGE reference to GEOS11 details is provided (last access 20.09.2016).