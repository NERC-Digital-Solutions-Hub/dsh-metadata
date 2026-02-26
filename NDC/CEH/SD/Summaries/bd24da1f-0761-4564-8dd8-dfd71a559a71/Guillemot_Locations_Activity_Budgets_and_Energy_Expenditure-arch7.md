# Activity data from common guillemots from the Isle of May during the 2005-2006 annual cycle

## Overview
- Geographically: Isle of May National Nature Reserve, Scotland (56°11′N, 02°33′W).
- Species: common guillemots (Uria aalge), chick-rearing adults.
- Time period: 4 July 2005 to 21 June 2006.
- Data collected with bird-borne GLS time-depth recorders (TDR) to capture location, depth, and temperature metrics.
- Sexing of individuals performed via CHD I gene analysis from feathers; study involved 13 birds.
- Processing and backing data by Ruth Dunn; access granted by Scottish Natural Heritage.

## Data collection and methods
- Biologging setup: GLS/TDR devices mounted on Darvic leg-rings; retrieved upon recapture.
- Sampling design: two rates to balance depth resolution and duration
  - 16-second depth readings for a 24-hour period every 30 days (n = 9 loggers retrieved).
  - 32-second depth readings for a 24-hour period every 15 days (n = 4 loggers retrieved).
- Derived data from raw biologging: daily activity budgets (hours), sea surface temperature (SST) from bird-borne loggers, energy expenditure (DEE), daily location fixes, and the proportion of dive activity by time of day (day/twilight/night).
- Colony attendance data: collected via daily time-lapse photography from 7 Oct 2005 to 20 May 2006.

## Data files (structure and contents)
- IoM_Guillemot_SST_TAB_DEE.csv
  - Columns: ID, Sex, Date (D-M-Y), Logger-SST (°C), Inactive_h, Diving_h, Active_h, Flight_h, Colony_h, DEE (kJ), Twilight_diving, Day_diving, Night_diving.
  - Provides per-individual daily metrics including SST and energy expenditure.
- IoM_Guillemot_Locations.csv
  - Columns: ID, Date (D-M-Y), Long, Lat.
  - Contains two location estimates per day for each individual to capture movement.
- IoM_Guillemot_ColonyAttendance.csv
  - Columns: Date (D-M-Y), Density (0–5 scale).
  - Daily colony attendance density scores mapped to 0 = no individuals to 5 = ~100 breeding sites occupied.

## GIS-relevant aspects and opportunities
- Spatial data: per-day geolocations for each bird (two points per day), enabling movement path construction and habitat use mapping.
- Temporal alignment: dates accompany all data files, allowing synchronization of location, SST/DEE, and colony attendance for integrated analyses.
- Potential map products:
  - Movement trajectories and home-range estimates for individual guillemots.
  - Spatial overlays of SST with diving, foraging, and energy expenditure patterns.
  - Temporal maps of colony attendance density linked to location data.
  - Multi-layer GIS visuals combining activity budgets, depth behavior, and environmental conditions.
- Data integration considerations:
  - Two locations per day require pairing or interpolation where necessary.
  - Differences in sampling frequency and missing data across individuals.
  - Units: SST in °C; DEE in kJ; time in hours; density on a 0–5 scale; coordinates in degrees (no CRS specified; plan to assign WGS84/EPSG:4326).
- Data quality and preparation notes:
  - Limited memory of TDRs led to two different sampling schemes.
  - Weekly/daily data gaps may occur; careful temporal resampling needed for consistent analyses.
  - Data provenance indicates formal processing and quality checks; original access was granted by heritage authority.

## Provenance and usage notes
- Access and processing:
  - Scottish Natural Heritage granted access; data collected by Sarah Wanless, Mike Harris, and Francis Daunt; data processing by Ruth Dunn.
- Licensing:
  - Feathers used for sexing under UK Home Office Licence.
- Scope for GIS work:
  - Suitable for retrospective movement and habitat analyses at site and landscape scales.
  - Useful for validating spatial patterns of colony attendance and environmental associations with foraging effort.