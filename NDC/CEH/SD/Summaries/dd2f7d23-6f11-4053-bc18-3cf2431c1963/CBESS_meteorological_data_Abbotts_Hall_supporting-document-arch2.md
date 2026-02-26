# Coastal Biodiversity and Ecosystem Service Sustainability (CBESS) Meteorological Data for Abbotts Hall, Essex

## Overview
- Meteorological measurements at the Abbotts Hall site in Essex, UK, as part of CBESS.
- Staff: Timothy Hill.
- Sites: Essex Abbotts Hall and Morecambe Bay to represent contrasting habitats (saltmarsh and mudflat) with different soil types (clay in Essex, sandy in Morecambe) and varying inundation, creek structure, and vegetation.
- Timeframe and cadence: Half-hourly mean values from 15 December 2012 to 27 January 2015.

## Variables Observed
- Air temperature (T_air)
- Soil temperature at 10 cm (T_soil_10cm)
- Soil temperature at 20 cm (T_soil_20cm)
- Soil temperature at 30 cm (T_soil_30cm)
- Relative humidity (RH)
- Net radiation (Net_rad)
- Photosynthetically active radiation (PAR)
- Precipitation (Precip)
- Wind speed (Wind_Spd)
- Wind direction (Wind_Dir)
- Vapour Pressure deficit (VPD)

## Data Collection and Instrumentation
- Measurements recorded on Campbell Scientific dataloggers.
- Wind: 10 Hz measurements from CSAT3A anemometer at 4.3 m on a lattice tower; CR3000 logger.
- Other variables: recorded at 1/60 Hz (every minute) by a CR1000 with multiplexer.
- Air temperature and humidity measured with Vaisala HMP155A and converted to VPD.
- Precipitation: Environmental Measurements Limited ARG100 tipping bucket gauge.
- Net radiation: Kipp and Zonen NR Lite.
- PAR: Skye Instruments SKP215.
- Soil temperatures: CS 107 thermistors.
- Data processing: Mean half-hourly values calculated in Matlab; time stamps refer to the middle of the half-hour period (e.g., 00:15).

## Data Processing and Quality Control
- Calibration: 10 Hz wind data filtered for wind shadowing and quality flags; averaged to half-hourly means.
- Other meteorological measurements averaged to half-hourly means.
- Data checking: wind measurements filtered according to quality flags and wind shadowing.
- Gaps: caused by sensor malfunction or power loss; NA values indicate measurements not performed.

## Data Formats and Field Descriptions
- File format: csv.
- Key fields: Row Number, Season (Winter W / Summer S), Location (Morecambe M / Essex E), Site (Morecambe: Cartmel Sands CS, Warton Sands WS, West plain WP; Essex: Abbotts Hall AH, Fingringhoe Wick FW, Tillingham Marshes TM), Habitat (Mudflat MF, Saltmarsh SM), Quadrat Number (1–22), Scale (A=1m, B=1–10m, C=10–100m, D=100–upper), Year, Month, Day, Hour, Minute.
- Observed variables: T_air (°C), T_soil_10cm (°C), T_soil_20cm (°C), T_soil_30cm (°C), RH (%), Net_rad (W/m²), PAR (μmol m⁻² s⁻¹), Precip (mm per 30 min), Wind_Spd (m s⁻¹), Wind_Dir (degrees from North), VPD (kPa).