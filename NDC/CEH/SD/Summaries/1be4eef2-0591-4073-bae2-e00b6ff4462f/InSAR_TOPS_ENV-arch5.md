# Survey Overview

- Part of the NERC InSAR ToPS project, conducted at two Flow Country sites (Caithness and Sutherland) from September 2017 to November 2018 to monitor climate impact.
- Study sites:
  - Knockfin Heights: upland blanket peatland (>300 m a.s.l.), part of the RSPB Forsinard estate.
  - Munsary: lowland blanket peatland, part of Plantlife Munsary Nature Reserve.
- Environmental monitoring focused on sensors measuring soil moisture, soil/air temperature, water level, precipitation (central site), and photosynthetically active radiation (PAR).

## Survey Area

- Two principal sites in Flow Country, the largest expanse of blanket bog in Europe.
- Knockfin Heights features erosive peat landscapes (hags, pools, lochans) with varying vegetation.
- Munsary features extensive pool systems (Dubh Lochans), high water tables, and near-natural conditions after historic grazing and peat restoration.

## Equipment and Data Collection

- Equipment installed at multiple sub-sites (Munsary A–G, Knockfin A–D, E/F) connected to Tempcon HOBO data loggers.
- Sensors include: HOBO weather station, U20L-04 Water Level loggers (0–4 m), EC-5 Soil Moisture sensors, and PAR sensors; central precipitation measurement.
- Measurements collected every 30 minutes; water level calibrated quarterly to account for peat growth.
- PAR measurements started later due to equipment delays; some sensors were lost to deer damage or equipment failure.
- Data were downloaded approximately every 6 months and processed using HOBOWARE software.
- Measurements referenced relative to peat surface for water level; calibration and documentation aligned with manufacturer instructions.

## Data Management, File Naming, and Metadata

- File naming follows a structured convention:
  - Site codes: KH (Knockfin Heights), MUN (Munsary)
  - ENV = Environmental Monitoring Data
  - SITE = Sub-site A–F
  - WT = Water Level
- Data file headers include:
  - Date, Time (GMT, 24h)
  - Date_Time (combined)
  - Temp_Soil (°C)
  - Pressure_mbar
  - Water_Content (soil moisture in mg/g water)
  - Precipitation_mm
  - PAR_uE (μmol m⁻² s⁻¹)
  - Temp_Water (°C)
  - Water_level_meters
- Central precipitation data is captured at a single location per site.
- Detailed site coordinates (OSGB36) provided for Munsary and Knockfin sub-sites.
- All equipment installations and calibrations followed manufacturer instructions (reference: Tempcon).

## Data Quality, Limitations, and Challenges

- Data gaps due to deer damage and equipment failures.
- PAR data started later than other measurements due to late equipment delivery.
- Data transfer of large datasets presented logistical constraints; although mitigated by semi-annual downloads and calibration checks.
- Calibration of water level and ongoing maintenance required to ensure data accuracy over time.

## Reference

- Alshammari, L., et al. (2018). Long-Term Peatland Condition Assessment via Surface Motion Monitoring Using the ISBAS DInSAR Technique over the Flow Country, Scotland. 10(7), 1103.