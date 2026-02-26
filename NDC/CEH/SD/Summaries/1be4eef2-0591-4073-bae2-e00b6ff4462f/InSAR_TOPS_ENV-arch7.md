# Survey Overview

## Overview
- Environmental Monitoring conducted as part of the NERC InSAR ToPS project in the Flow Country, Scotland, from September 2017 to November 2018.
- Aimed to monitor climate-related changes using surface motion data and environmental sensors.
- Study sites: Knockfin Heights (upland blanket peatland) and Munsary (lowland blanket peatland).

## Survey Area
- Locations and boundaries:
  - Knockfin Heights, Sutherland (NC94958) – upland blanket bog (>300 m a.s.l.), part of the RSPB Forsinard estate.
  - Munsary, Caithness (ND21677 46186) – lowland blanket bog, part of Plantlife Munsary Nature Reserve.
- Landscape characteristics vary by site, including peat hags, drained/undrained pools, lochans, sedge/heath/grass communities; Munsary contains Dubh Lochans with high water tables and rare plants.
- The Flow Country is described as Europe’s largest expanse of blanket bog.
- Figure 1 (referenced) shows site layout with equipment locations.

## Equipment and Sensors
- Equipment installed at each site, connected to Tempcon HOBO data loggers.
- Sensor suite per sub-site includes:
  - Soil moisture (EC-5)
  - Soil/air temperature sensors
  - Water level loggers (U20L-04)
  - PAR (photosynthetically active radiation) sensor
  - Rainfall sensor (HOBOnet metric)
- Additional central precipitation measurement site.
- Logging cadence: measurements every 30 minutes.
- Water level calibrated relative to peat surface; calibration every 3 months to track peat growth.
- PAR measurements started later due to equipment delivery delays.
- Some sensors were lost during the survey due to deer damage or equipment failure.
- Data download frequency: approximately every 6 months.
- Data processing: using HOBOWARE software.

## Data Naming, Structure and Schema
- File naming convention:
  - Site: KH = Knockfin Heights, MUN = Munsary
  - ENV = Environmental Monitoring Data
  - SITE = SUB SITE A-F
  - WT = Water Level (collected at different times)
- In-file column headings include:
  - Date, Time, Date_Time
  - Temp_Soil (°C)
  - Pressure_mbar
  - Water_Content (soil moisture in mg/g water)
  - Precipitation_mm
  - PAR_uE (μmol·m⁻²·s⁻¹)
  - Temp_Water (°C)
  - Water_level_meters
- Sub-site coordinates are provided in OSGB36 (e.g., Munsary A–G and Knockfin A–D with X/Y values).

## Data Quality, Gaps and Limitations
- Data gaps due to:
  - Sensor loss from wildlife (deer) and equipment failures
  - Delayed start for PAR measurements
- PAR data incomplete for part of the deployment
- Field data downloaded ~6-monthly; calibration adjustments conducted periodically

## References
- Alshammari, L., et al. (2018). Long-Term Peatland Condition Assessment via Surface Motion Monitoring Using the ISBAS DInSAR Technique over the Flow Country, Scotland. Remote Sensing, 10(7), 1103.