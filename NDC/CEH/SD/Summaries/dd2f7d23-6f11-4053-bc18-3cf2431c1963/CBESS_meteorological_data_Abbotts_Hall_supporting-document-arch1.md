# Coastal Biodiversity and Ecosystem Service Sustainability (CBESS) Meteorological Data for Abbotts Hall, Essex

- Purpose and scope
  - Meteorological measurements at the Abbotts Hall site in Essex for the CBESS project, describing environmental conditions relevant to coastal biodiversity and ecosystem services.
  - Site selection includes contrasting habitats to capture variability: Essex vs Morecambe Bay, saltmarsh with clay vs sandy soils, and mudflat habitats with differing sediment types and inundation patterns.

- Location and sampling period
  - Primary site: Abbotts Hall, Essex (51°47'9"N, 0°52'1"E).
  - Additional sites for contrast: Morecambe Bay saltmarsh and mudflat locations; specific sites include Cartmel Sands, Warton Sands, West Plain (Morecambe) and Abbotts Hall, Fingringhoe Wick, Tillingham Marshes (Essex).
  - Sampling cadence: half-hourly mean values from 15 December 2012 to 27 January 2015.
  - Time stamps: half-hour interval mid-point (e.g., 00:15 covers 00:00–00:30).

- Measured variables
  - Air temperature (T_air) and soil temperatures at 10 cm, 20 cm, and 30 cm (T_soil_10cm, T_soil_20cm, T_soil_30cm).
  - Relative humidity (RH) and Vapour Pressure Deficit (VPD).
  - Net radiation (Net_rad) and Photosynthetically Active Radiation (PAR).
  - Precipitation (Precip) and wind speed (Wind_Spd) and wind direction (Wind_Dir).

- Instrumentation and data collection
  - Wind: 10 Hz measurements with CS CSAT3A anemometer at 4.3 m on a lattice tower; data logged by CS CR3000.
  - Other meteorological variables: logged at 1/60 Hz (every minute) by CS CR1000 with multiplexer.
  - Air temperature and humidity: measured with Vaisala HMP155A sensors and converted to VPD.
  - Precipitation: Environmental Measurements Limited ARG100 tipping-bucket rain gauge.
  - Net radiation: Kipp and Zonen NR Lite.
  - PAR: Skye Instruments SKP215.
  - Soil temperatures: CS 107 thermistors.
  - Data processing: mean half-hour values calculated in Matlab.

- Data quality, calibration, and checks
  - Calibration and quality control: 10 Hz wind data filtered for wind shadowing and quality flags before forming half-hour means.
  - General data checks: wind data filtered using quality flags and shadowing considerations.
  - Gaps and missing values: indicate sensor malfunction or power loss; NA values indicate measurements not performed.
  - Time reference is the middle of each half-hour period.

- Data formats and structure
  - Primary file format: CSV.
  - Dataset field descriptions include: Season (Winter, Summer), Location (Essex, Morecambe), Site (e.g., AH, FW, TM; CS, WS, WP), Habitat (Mudflat, Saltmarsh), Quadrat Number (1–22), Scale (A–D with defined ranges), Year, Month, Day, Hour, Minute, and the measured variables (T_air, T_soil_10cm, T_soil_20cm, T_soil_30cm, RH, Net_rad, PAR, Precip, Wind_Spd, Wind_Dir, VPD).

- Notable notes
  - Gaps may arise from sensor issues or power interruptions.
  - Mean values reflect half-hour periods; time labeling corresponds to the mid-point of each interval.
  - Dataset maintained by staff including Timothy Hill.