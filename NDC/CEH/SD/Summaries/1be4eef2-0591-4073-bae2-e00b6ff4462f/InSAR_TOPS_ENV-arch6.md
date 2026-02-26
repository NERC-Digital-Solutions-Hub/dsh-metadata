# Survey Overview

- Objective and scope
  - Environmental Monitoring conducted as part of the NERC InSAR ToPS project
  - Two sites in the Flow Country, Caithness and Sutherland, Scotland
  - Time period: September 2017 to November 2018
  - Sensors collected soil moisture, soil temperature, water level at sub-sites; central site collected precipitation; photosynthetically active radiation (PAR) measured where available

- Study Area
  - Knockfin Heights: upland blanket peatland (>300 m a.s.l.), part of the RSPB Forsinard estate
  - Munsary: lowland blanket peatland, part of Plantlife Munsary Nature Reserve
  - Site characteristics include peat hags, drained/undrained pools, lochans, sedge/heather/grass communities; Munsary contains Dubh Lochans and rare plants; peatland restoration activity nearby

- Equipment and Logging Details
  - Equipment deployed at each site, connected to Tempcon HOBO data loggers
  - Sensor types include:
    - HOBO H21 USB Micro Station Weather/Energy Data Logger
    - HOBO U20L-04 Water Level Data Logger (0-4 m)
    - HOBO EC-5 Soil Moisture Sensor
    - HOBOnet Rainfall Sensor
    - HOBOnet PAR Sensor
  - Data collection every 30 minutes
  - Water level calibrated relative to peat surface; calibration every 3 months to account for peat growth
  - PAR measurements started later due to equipment delivery delays
  - Data downloads approximately every 6 months
  - Data processing performed with HOBOWARE
  - Some sensors were lost due to deer damage or equipment failure

- Data Management, Naming, and Structure
  - File naming convention:
    - Site: KH (Knockfin Heights) or MUN (Munsary)
    - ENV = Environmental Monitoring Data
    - SITE = SUB SITE A-F
    - WT = Water Level
  - Within files, column headers include:
    - Date, Time, Date_Time
    - Temp_Soil (°C)
    - Pressure_mbar
    - Water_Content (mg/g water)
    - Precipitation_mm
    - PAR_uE (μmol m^-2 s^-1)
    - Temp_Water (°C)
    - Water_level_meters
  - Site coordinates provided in OSGB36 format (e.g., Munsary A–G, Knockfin A–D)
  - Data coverage varies by sensor and site, with occasional gaps due to sensor loss or delays

- Data Quality, Gaps, and Challenges
  - Patchy data availability across sensors and sites
  - PAR measurements not available at all sub-sites initially
  - Equipment loss and failures (e.g., wildlife interference)
  - Calibration needed to account for peat growth affecting depth measurements

- Outputs and Potential Uses
  - Time-series data for peatland conditions (soil moisture, soil temperature, water level, precipitation, PAR)
  - Enables cross-site comparison and climate impact assessment on peatland dynamics
  - Structured data ready for processing, analysis, and potential dashboard or self-serve exploration

- References
  - Alshammari, L. et al. (2018). Long-Term Peatland Condition Assessment via Surface Motion Monitoring Using the ISBAS DInSAR Technique over the Flow Country, Scotland

- Notes for Data Support
  - Clear data provenance and sensor metadata support data integration with other datasets (e.g., InSAR outputs)
  - Consistent naming conventions and time-intervals facilitate combining data across sites
  - Data quality improvement opportunities include expanding PAR coverage, robust sensor maintenance, and automation of metadata capture (e.g., calibration logs) to support downstream analyses and dashboards