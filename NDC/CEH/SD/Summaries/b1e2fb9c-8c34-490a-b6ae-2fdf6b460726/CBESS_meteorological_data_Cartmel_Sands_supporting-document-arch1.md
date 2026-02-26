# Coastal Biodiversity and Ecosystem Service Sustainability (CBESS) Meteorological Data for Cartmel Sands, Morecambe

- Purpose and scope
  - Meteorological measurements at Cartmel Sands, Morecambe, as part of the CBESS dataset.
  - Half-hourly mean values from 31 May 2013 to 26 January 2015.
  - Sites chosen to represent contrasting habitats (saltmarsh vs mudflat) and sediment types, across Essex and Morecambe Bay.
  - Saltmarsh regions differ in inundation frequency, creek structure, and vegetation; mudflat sites differ in sediment cohesiveness and mobility.

- Location and site design
  - Morecambe: Cartmel Sands (CS) – coordinates 54°10'40"N, 003°00'05"W.
  - Additional Morecambe sites: Warton Sands (WS), West Plain (WP).
  - Essex sites: Abbotts Hall (AH), Fingringhoe Wick (FW), Tillingham Marshes (TM).
  - Habitats: Mudflat (MF) and Saltmarsh (SM).

- Monitoring design and data cadence
  - Variables recorded: air temperature (T_air), soil temperature (T_soil_5cm, T_soil_10cm), relative humidity (RH), net radiation (Net_rad), photosynthetically active radiation (PAR), precipitation (Precip), wind speed (Wind_Spd), wind direction (Wind_Dir), vapour pressure deficit (VPD).
  - Half-hourly mean values calculated; time stamps correspond to the middle of the half-hour period (e.g., 00:15 for 00:00–00:30).
  - Measurements stored at the following intervals: 10 Hz wind measurements filtered and averaged; remaining meteorological measurements averaged to half-hourly means.
  - Observations collected using a Campbell Scientific CR5000 datalogger; wind via CSAT3 anemometer at 4.3 m on a lattice tower; other sensors for temperature, humidity, and radiation.

- Instruments, calibration, and data quality
  - Temperature and humidity sensors: Vaisala MP103A (converted to VPD).
  - Precipitation: Environmental Measurements Limited ARG100 tipping bucket rain gauge.
  - Net radiation: Kipp and Zonen NR Lite; PAR: Skye Instruments SKP215; soil temperature: type T thermocouples.
  - Calibration and data quality: 10 Hz wind data filtered for wind shadowing and quality flags; wind and other data averaged to half-hourly means; data quality flags used for filtering; gaps due to sensor malfunctions or power loss.
  - Data gaps and missing values: Gaps indicate sensor malfunction or power loss; NA values indicate measurements not performed.

- Data format and structure
  - File format: CSV.
  - Metadata and dataset fields include:
    - Season (Winter W, Summer S)
    - Location (Morecambe M, Essex E)
    - Site (CS, WS, WP for Morecambe; AH, FW, TM for Essex)
    - Habitat (Mudflat MF, Saltmarsh SM)
    - Quadrat Number (1–22)
    - Scale (A: 1 m; B: 1–10 m; C: 10–100 m; D: 100–upper)
    - Year, Month, Day, Hour, Minute
    - T_air, T_soil_5cm, T_soil_10cm
    - RH, Net_rad, PAR, Precip, Wind_Spd, Wind_Dir, VPD
  - Notes on formatting: Some field descriptions appear with line-wrapping artifacts; units and definitions follow standard meteorological conventions (e.g., Celsius for temperatures, % RH, kPa for VPD, W/m² for Net_rad, μmol m⁻² s⁻¹ for PAR, mm for Precip, m s⁻¹ for Wind_Spd, degrees for Wind_Dir).

- Data preparation and reuse considerations
  - Time reference and averaging applied to standardise to half-hourly intervals.
  - Data are suitable for correlational analyses between microclimate variables and habitat types or spatial scales.
  - Be mindful of missing data and data gaps when building models; consider data quality flags and sensor downtime in analyses.
  - Transparent provenance: dataset includes detailed sensor specifications, sampling intervals, calibration notes, and site/habitat metadata to support reproducibility and discoverability.

- Potential analytic applications (aligned with data characteristics)
  - Investigating microclimate differences between saltmarsh vs mudflat habitats and across Essex vs Morecambe Bay sites.
  - Correlating meteorological drivers (e.g., VPD, PAR, Net_rad) with habitat-specific ecological responses.
  - Developing predictive models of temperature, humidity, and radiation dynamics at high spatial granularity (site-quadrat scales).
  - Gap-aware time-series analyses and trend detection using standardized half-hourly data.