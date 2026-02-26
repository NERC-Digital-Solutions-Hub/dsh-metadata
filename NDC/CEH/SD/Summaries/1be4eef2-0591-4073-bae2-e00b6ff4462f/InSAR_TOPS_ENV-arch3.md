# Survey Overview

- Part of the NERC InSAR ToPS project evaluating climate impact on peatlands in the Flow Country, Caithness and Sutherland, from September 2017 to November 2018.
- Environmental monitoring focused on a range of sensors across sub-sites within two focus areas to capture soil moisture, soil temperature, water level, precipitation, and photosynthetically active radiation (PAR).

## Survey Area

- Knockfin Heights (RSPB Forsinard Estate): upland blanket bog (>300 m above sea level) with features such as peat hags, drained/undrained pools, lochans, and varied vegetation.
- Munsary (Plantlife Munsary Nature Reserve): lowland blanket peatland with numerous pool systems (Dubh Lochans), high water tables, and rare flora; area has a history of grazing, peat extraction, and burning, with recent restoration efforts (drain blocking).
- Study sites mapped with coordinates; layout includes permanent markers and monitoring equipment at multiple sub-sites.

## Equipment and Data Collection

- Equipment per sub-site: Tempcon HOBO data loggers, water level loggers (U20L-04), soil moisture sensors (EC-5), PAR sensors, rainfall sensor, and standard weather data logging.
- Data collection cadence: measurements every 30 minutes throughout the survey period.
- Water level: referenced to peat surface, calibrated quarterly to account for peat growth.
- PAR data: began later due to equipment delivery delays.
- Data handling: data downloaded approximately every six months; processed using HOBOWARE software.
- Site details: multiple sub-sites (A–F) at Munsary and Knockfin Heights, with precise OSGB36 coordinates provided.

## File Naming, Structure and Variables

- File naming convention: Site (KH = Knockfin Heights, MUN = Munsary) + ENV = Environmental Monitoring Data + SITE = SUB SITE A–F + WT = Water Level data (separate by collection time).
- Data columns (example): Date, Time, Date_Time, Temp_Soil, Pressure_mbar, Water_Content, Precipitation_mm, PAR_uE, Temp_Water, Water_level_meters.
- Documentation notes: site-specific names and observation numbers included in files; measurements include soil temperature, atmospheric pressure, soil moisture, precipitation, PAR, water temperature, and water level.

## Data Gaps and Challenges

- Some sensors were lost due to deer damage or equipment failure, reducing data completeness.
- PAR measurements started later than other metrics due to equipment delays.
- Data management relies on periodic downloads and calibration, with potential implications for continuous long-term datasets.

## References

- Alshammari, L., et al. (2018). Long-Term Peatland Condition Assessment via Surface Motion Monitoring Using the ISBAS DInSAR Technique over the Flow Country, Scotland.

## Implications for Monitoring Frameworks

- High-frequency, multi-variable monitoring across distinct peatland habitats supports assessment of climate-related environmental health signals and informs policy decisions.
- Standardized data practices observed (calibration routines, naming conventions, data processing via dedicated software) support data quality, provenance, and potential replication.
- Real-world challenges highlighted (data gaps from equipment loss, delayed sensor deployment) underscore the need for robust data governance, redundancy, and clear metadata to maintain usable datasets for evaluation and decision-making.