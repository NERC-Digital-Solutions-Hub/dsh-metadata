# Coastal Biodiversity and Ecosystem Service Sustainability (CBESS) Meteorological Data for Abbotts Hall, Essex

## Overview
- CBESS meteorological dataset documenting half-hourly weather measurements at the Abbotts Hall site in Essex.
- Time span: 15 December 2012 to 27 January 2015 (half-hourly mean values).
- Location coordinates: 51°47'9"N, 0°52'1"E.
- Staff responsible: Timothy Hill.
- Designed to support understanding of coastal biodiversity and ecosystem services through data-driven insights and comparisons across CBESS sites.

## Dataset content and scope
- Sites and habitats covered (CBESS-wide context):
  - Essex: Abbotts Hall (AH), Fingringhoe Wick (FW), Tillingham Marshes (TM).
  - Morecambe Bay sites: Cartmel Sands (CS), Warton Sands (WS), West Plain (WP).
  - Habitat types include Mudflat (MF) and Saltmarsh (SM).
- Observations:
  - Variables include air temperature (T_air), soil temperatures at 10 cm, 20 cm, and 30 cm (T_soil_10cm, T_soil_20cm, T_soil_30cm), relative humidity (RH), net radiation (Net_rad), photosynthetically active radiation (PAR), precipitation (Precip), wind speed (Wind_Spd), wind direction (Wind_Dir), and vapour pressure deficit (VPD).
  - Wind measurements: 10 Hz wind data from a CSAT3A anemometer at 4.3 m, logged with CS CR3000.
  - Other meteorological data: recorded at 1 Hz (every minute) using CS CR1000 with multiplexer.
  - VPD derived from air temperature and humidity measurements (converted from Vaisala HMP155A).
- Data processing:
  - Mean values computed to half-hourly intervals (e.g., 00:15 references the period 00:00–00:30).
  - Matlab used for computing mean half-hourly values.
- Data formats and metadata:
  - Primary file format: CSV.
  - Data gaps caused by sensor malfunction or power loss; NA entries indicate measurements not performed.

## Measurement, instrumentation, and workflow
- Instruments and systems:
  - Campbell Scientific dataloggers; CSAT3A anemometer; CS CR3000; CS CR1000; Vaisala HMP155A; EML ARG100 tipping bucket rain gauge; Kipp and Zonen NR Lite; Skye Instruments SKP215; CS 107 thermistors.
- Calibration and quality control:
  - 10 Hz wind data filtered for wind shadowing and data quality flags; downsampled to half-hourly means.
  - Other meteorological measurements averaged to half-hourly.
  - Wind data filtered according to quality flags and wind shadowing during data checks.
- Location and site context details:
  - Essex and Morecambe Bay sites were chosen to represent contrasting sediment types; saltmarsh sites reflect two soil types (clay in Essex; sandy in Morecambe Bay) and different inundation frequencies, creek structures, and vegetation.

## Data structure and field definitions
- Core fields (sample of columns):
  - Row Number
  - Season (Winter W, Summer S)
  - Location (Morecambe M, Essex E)
  - Site (AH, FW, TM for Essex; CS, WS, WP for Morecambe)
  - Habitat (Mudflat MF, Saltmarsh SM)
  - Quadrat Number (1–22)
  - Scale (A=1m, B=1–10m, C=10–100m, D=100–upper limit)
  - Year, Month, Day, Hour, Minute
  - T_air (°C)
  - T_soil_10cm (°C)
  - T_soil_20cm (°C)
  - T_soil_30cm (°C)
  - RH (%)
  - Net_rad (W m^-2)
  - PAR (μmol m^-2 s^-1)
  - Precip (mm per 30 min)
  - Wind_Spd (m s^-1)
  - Wind_Dir (degrees from North)
  - VPD (kPa)
- Units and formats are specified for each field (e.g., temperatures in Celsius, PAR in μmol m^-2 s^-1, wind in m s^-1, etc.).

## Access, formats, and data quality
- Data format: CSV files for raw and processed meteorological observations.
- Data quality and gaps:
  - Gaps due to sensor malfunction or power loss.
  - NA values denote measurements not performed.
  - Data are subjected to quality control, including wind shadowing corrections and quality flags for wind measurements.

## How to use and integrate
- Suitable for linking meteorological conditions with coastal biodiversity data and ecosystem service assessments.
- Can be integrated with other CBESS datasets to compare habitat types (saltmarsh vs mudflat) and sites across Essex and Morecambe Bay.
- Useful for building dashboards or self-serve data exploration tools that track environmental drivers over time at half-hour resolution.
- Data processing notes to aid reproducibility: half-hourly means computed in Matlab; time stamps correspond to the midpoint of each half-hour interval.