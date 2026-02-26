# Sampling Regime and Collection Methods

## Overview
- Dataset from an automatic lake monitoring buoy at Blelham Tarn, Cumbria, England.
- Instruments measure air temperature, solar radiation, wind speed, and in-lake temperatures.
- Records cover 2008–2011 and are reported in GMT.

## Data Collected
- Variables and units:
  - Air_Temperature: degrees Celsius (°C)
  - Pyranometer: solar radiation flux in Watts per square meter (W/m²)
  - Wind_Speed: metres per second (m/s)
  - Water_temperature at depths: 0.5, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10, and 12 metres (°C)
- Depths observed include 0.5 m through 12 m (with gaps where applicable).

## Sampling Cadence and Time Reference
- Data recorded every 4 minutes by a Campbell Scientific datalogger.
- Hourly averages are calculated from the 4-minute data (example: the 2 p.m. value is the average from 1–2 p.m., excluding 1 p.m. data and including 2 p.m. data).
- All times are in Greenwich Mean Time (GMT).

## Data Quality and Limitations
- Data are raw (not calibrated or quality controlled yet).
- Visual checks performed; obvious hardware malfunctions corrected.
- Gaps occur due to buoy maintenance or sensor/logger problems.

## Data Structure and Access
- Data provided as a CSV file with columns:
  - Date_GMT
  - 0.5m, 1m, 2m, 3m, 4m, 5m, 6m, 7m, 8m, 9m, 10m, 12m (water temperatures at specified depths)
  - Air_Temperature
  - Pyranometer
  - Wind_Speed
- Column descriptions specify measurement meaning and units.

## Publications and Use
- Dataset has been used in several scientific studies:
  - 2014: A novel method for estimating the onset of thermal stratification in lakes from surface water measurements (Water Resources Research)
  - 2015: A comparison of the diel variability in epilimnetic temperature for five lakes in the English Lake District (Inland Waters)
  - 2016: Diel surface temperature range scales with lake size (PLOS ONE)
- Publications involve collaboration among multiple researchers and institutions.

## Implications for Data Governance (Data Leaders)
- Calibration and quality control: raw data require formal calibration and systematic QC before release to downstream users.
- Metadata and discoverability: clear column definitions, units, depths, and time references aid discoverability; ensure comprehensive metadata accompanies the dataset.
- Data completeness and updates: monitor and document gaps, maintenance events, and sensor issues; plan for updates or reprocessing if calibration pipelines are added.
- Data sharing and collaboration: dataset already supporting published research; consider governance for access, licensing, and reuse across partner networks.