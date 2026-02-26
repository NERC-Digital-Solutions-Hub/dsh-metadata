# Overview of data

- Purpose and context
  - Compilation of results from the stream metabolism component of the NERC Macronutrients consortium led by Prof. Mark Trimmer, investigating lateral exchange in the seaward flux of C, N and P.
  - Data collected in the field by L. Rovelli, K. Attard, and Assoc. Prof. H. Stahl under Prof. R.N. Glud.

- Data collection and campaigns
  - Four field campaigns measured in situ atmospheric data in rivers with varying land-river connectivity within the Hampshire Avon catchment.
  - Seasons: Spring 2013, Summer 2013, Autumn 2013, Winter 2014.
  - Site codes and rivers: CE1 (Ebble), GA2 (Avon), GN1 (Nadder), CW2 (Wylye), AS1/AP (Tributary of Sem), AS2/Sem (Sem).
  - CE1 winter data not collected due to flooding.
  - Field dates: Spring (23/04–09/05/2013), Summer (31/07–16/08/2013), Autumn (29/10–11/11/2013), Winter (28/01–09/02/2014).
  - Equipment: SKYWATCH GEOS 11 high-precision portable weather station (factory-calibrated prior to March 2013).

- Data files and structure
  - 23 accompanying CSV data files named Geos11_'SiteCode'_'Season'.CSV (e.g., Geos11_CE1_autumn.CSV, Geos11_GA2_spring.CSV, Geos11_GN1_winter.CSV, etc.).
  - Column headers include DateTime, Date, Time, Wind, Temperature, Humidity, Pressure, Direction.
  - Sampling frequency: 15–30 seconds (limited by battery life).

- Data contents and quality indicators
  - Wind: speed in m/s; resolution 0.1 m/s; accuracy ±2% or measured value.
  - Temperature: °C; resolution 0.1 °C; accuracy ±2% (or 0.5 °C at 25 °C).
  - Humidity: %rH; resolution 0.1%; accuracy ±2% at 50% rH.
  - Pressure: hPa; resolution 0.1 hPa; accuracy ±0.5% (or 1.5 hPa at 25 °C).
  - Direction: wind direction in degrees; resolution 1°; accuracy ±3% (calibrated in field).
  - NaN values indicate data not collected (e.g., battery replacement, data download, or windy data issues) or flagged as contaminated.

- Site details and coordinates
  - SiteCode coordinates provided for each location (e.g., CE1 Ebble 51.027499 N, -1.9217089 E; GA2 Avon 51.318289, -1.8600020; GN1 Nadder 51.043849, -2.1118158; CW2 Wylye 51.142475, -2.2033140; AS1/AP Sem tributary 51.055413, -2.1568407; AS2/Sem 51.045826, -2.1104425).

- Data provenance and stewardship
  - Data produced by field scientists under the NERC Macronutrients consortium; aim to support standardized environmental monitoring and enable data storage/portal submission where appropriate.

- Relevance to environmental monitoring and policy
  - Provides standardized meteorological context for riverine ecosystem studies, enabling temporal and spatial comparisons and integration with other environmental datasets to assess environmental health and policy performance over time.