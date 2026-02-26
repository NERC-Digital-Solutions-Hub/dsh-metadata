# Survey Overview

- Environmental Monitoring conducted as part of the NERC InSAR ToPS project at two Flow Country sites (Caithness and Sutherland) from September 2017 to November 2018 to monitor climate-related effects.
- Focus areas were chosen based on surface motion characteristics; sensors were deployed to measure key environmental variables.

## Study Area

- Knockfin Heights (Upland blanket bog, >300 m.a.s.l.), part of RSPB Forsinard estate, Sutherland, Scotland.
  - Characterised by erosion features (peat hags, drained/undrained pools, lochans) and a mix of sedge, sphagnum, heather, and grasses.
- Munsary (Lowland blanket bog, ~100 m.a.s.l.), part of Plantlife Munsary Nature Reserve, Caithness, Scotland.
  - Centre contains pool systems (Dubh Lochans) with high water tables and rare orchids; margins are shrubby peatlands.
  - History of grazing, peat extraction, and burning; peatland restoration (drain blocking) in recent years; area near-natural overall.

## Monitoring Setup and Equipment

- Sensors deployed at multiple sub-sites with a central site for precipitation; additional sensors for photosynthetically active radiation (PAR).
- Equipment across sites includes:
  - HOBO H21 USB Micro Station Weather/Energy Data Loggers
  - HOBO U20L-04 Water Level Data Loggers (0–4 m)
  - HOBO EC-5 Soil Moisture Smart Sensors
  - HOBOnet Rainfall Sensor (for some sub-sites)
  - HOBOnet PAR Sensor (for some sub-sites)
- Site coordinates provided for each sub-site and calibration/installation performed per manufacturers’ instructions.

## Data Collection and Processing

- Measurements collected every 30 minutes.
- Water level data calibrated quarterly to account for peat growth; water level relative to peat surface.
- PAR measurements started later due to equipment delays.
- Data downloaded approximately every 6 months and processed using HOBOWARE software.

## File Structure and Data Fields

- File naming follows a convention: Site (KH = Knockfin Heights, MUN = Munsary), ENV, SITE (A–F), WT (Water Level), with time-stamped observations.
- Within files, columns include:
  - Date, Time, Date_Time
  - Temp_Soil (°C)
  - Pressure_mbar
  - Water_Content (mg/g water)
  - Precipitation_mm
  - PAR_uE (μmol m^-2 s^-1)
  - Temp_Water (°C)
  - Water_level_meters

## Data Quality, Gaps, and Challenges

- Some sensors were lost due to deer damage or equipment failure.
- PAR measurements initiated later due to delays in equipment delivery.
- Data downloads occur infrequently (every ~6 months); calibration and processing rely on standardized software.
- Data management emphasizes traceability through descriptive file naming and metadata, facilitating reuse and discovery.

## References

- Alshammari, L., et al. (2018). Long-Term Peatland Condition Assessment via Surface Motion Monitoring Using the ISBAS DInSAR Technique over the Flow Country, Scotland. 10(7), 1103.