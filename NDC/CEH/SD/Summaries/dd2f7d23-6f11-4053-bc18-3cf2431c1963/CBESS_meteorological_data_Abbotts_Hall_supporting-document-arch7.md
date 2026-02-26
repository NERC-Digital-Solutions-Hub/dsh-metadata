# Coastal Biodiversity and Ecosystem Service Sustainability (CBESS) Meteorological Data for Abbotts Hall, Essex

## Overview
- Meteorological dataset collected at the Abbotts Hall site in Essex for coastal biodiversity and ecosystem service sustainability studies.
- Half-hourly mean values from 15/12/2012 to 27/01/2015.
- Data include key atmospheric and soil parameters collected with field instruments and logged for GIS-based analysis and map visualisation.

## Location and Sampling Design
- Observation sites represent contrasting habitats and sediment types.
- Essex and Morecambe Bay saltmarsh regions differ in inundation frequency, creek structure, and vegetation; mudflat sites differ in sediment type (clay vs. coarse, mobile sediments).
- Essex site: Abbotts Hall (AH) at 51°47'9"N, 0°52'1"E; additional Essex sites include Fingringhoe Wick (FW) and Tillingham Marshes (TM).
- Morecambe Bay sites: Cartmel Sands (CS), Warton Sands (WS), West Plain (WP).
- Spatial scale categories:
  - A: 1 m
  - B: 1–10 m
  - C: 10–100 m
  - D: 100 m and above
- Quadrat-based observations (1–22) across habitats (Mudflat, Saltmarsh).

## Measurements and Instrumentation
- Meteorological variables observed:
  - Air temperature (T_air)
  - Soil temperature at 10 cm (T_soil_10cm), 20 cm (T_soil_20cm), 30 cm (T_soil_30cm)
  - Relative humidity (RH)
  - Net radiation (Net_rad)
  - Photosynthetically active radiation (PAR)
  - Precipitation (Precip)
  - Wind speed (Wind_Spd)
  - Wind direction (Wind_Dir)
  - Vapour pressure deficit (VPD)
- Instrumentation and data logging:
  - Wind: CSAT3A anemometer at 10 Hz, on a lattice tower at 4.3 m; logged by CS CR3000.
  - Other variables: recorded at 1/60 Hz (every minute) by a CS CR1000 with multiplexer.
  - Air temperature and humidity: Vaisala HMP155A; conversions to VPD.
  - Precipitation: Environmental Measurements Limited (EML) ARG100 tipping bucket rain gauge.
  - Net radiation: Kipp and Zonen NR Lite.
  - PAR: Skye Instruments SKP215.
  - Soil temperatures: CS 107 thermistors.
- Data processing:
  - Mean half-hourly values calculated in Matlab.
  - Time reference for values corresponds to the middle of the half-hour interval (e.g., 00:15 for 00:00–00:30).

## Data Quality, Processing, and Checks
- Calibration and quality control:
  - 10 Hz wind data filtered for wind shadowing and quality flags; averaged to half-hourly means.
  - Remaining meteorological measurements averaged to half-hourly means.
- Data checking:
  - Wind measurements filtered according to data quality flags and wind shadowing.
- Data gaps:
  - Gaps indicate sensor malfunction or power loss.
  - NA values indicate measurements not performed.

## Data Format and Structure
- File format: CSV.
- Dataset fields (examples):
  - Time and location: Year, Month, Day, Hour, Minute; Season; Location (Morecambe or Essex); Site (e.g., AH, FW, TM, CS, WS, WP); Habitat (Mudflat or Saltmarsh); Quadrat Number; Scale (A–D).
  - Climate/meteorological variables: T_air, T_soil_10cm, T_soil_20cm, T_soil_30cm, RH, Net_rad, PAR, Precip, Wind_Spd, Wind_Dir, VPD.
- Scale and location metadata enable GIS-based aggregation and mapping across sites and habitats.

## Notes for GIS Use
- The dataset supports spatial analyses across contrasting coastal habitats (Essex and Morecambe Bay) with explicit site, habitat, and spatial scale metadata.
- Temporal coverage is limited to December 2012 through January 2015 with half-hourly resolution, suitable for linking meteorological context to coastal biodiversity and ecosystem service assessments.