# Activity data from common guillemots from the Isle of May during the 2005-2006 annual cycle

## Overview
- Dataset of common guillemots (Uria aalge) from the Isle of May National Nature Reserve, Scotland.
- Collected during the 2005-2006 annual cycle using biologging devices (GLS time-depth recorders) attached to Darvic leg-rings on chick-rearing adults.
- 13 individuals tracked from 4 July 2005 to 21 June 2006; birds were recaptured to retrieve loggers and feather samples for sexing under UK Home Office Licence.
- Aimed to record extended-time data with two sampling schemes to balance resolution and duration.

## Data collection and processing
- Two sampling schemes due to memory limits:
  - Depth readings every 16 s for a 24 h period every 30 days (n = 9 loggers recovered).
  - Depth readings every 32 s for a 24 h period every 15 days (n = 4 loggers recovered).
- Derived daily data include:
  - Activity budgets: hours spent diving, flying, at the colony, active on water, inactive on water.
  - Sea surface temperature (SST) from bird-borne loggers.
  - Energy expenditure (DEE) and location fixes.
  - Proportions of dive activity by time of day (day, twilight, night).
- Colony attendance recorded via daily time-lapse photography from 7 Oct 2005 to 20 May 2006.

## Data files and schemas
- IoM_Guillemot_SST_TAB_DEE.csv (13 columns):
  - ID, Sex, Date (D-M-Y), Logger-SST (°C), Inactive_h, Diving_h, Active_h, Flight_h, Colony_h, DEE (kJ), Twilight_diving, Day_diving, Night_diving.
- IoM_Guillemot_Locations.csv (4 columns):
  - ID, Date (D-M-Y), Long, Lat. Two daily location estimates.
- IoM_Guillemot_ColonyAttendance.csv (2 columns):
  - Date (D-M-Y), Density (0–5 scale; 0 = no individuals; 5 = all ~100 breeding sites occupied).

## Data provenance and access
- Data collected with explicit permissions:
  - Access granted by Scottish Natural Heritage.
  - Collected by Sarah Wanless, Mike Harris, Francis Daunt; data processing by Ruth Dunn.
  - Feather collection conducted under UK Home Office Licence.
- Data is organized into three CSV files with clearly defined fields, aiding discoverability and reuse.

## Potential uses for data leadership and governance
- Study of activity budgets, energy expenditure, space use, and colony attendance dynamics in a marine seabird population.
- Cross-study comparisons of biologging-derived metrics (DEE, SST, activity states) with standardized metadata.
- Evaluation of data quality, provenance, and licensing requirements for long-term ecological datasets.
- Planning for data standards, documentation, and discoverability to support reuse by policy colleagues and external partners.

## Data quality and limitations
- Limited sample size (13 individuals) and two sampling schemes with differing resolutions.
- Location data provides two daily estimates, which may affect spatial analyses.
- Derived metrics depend on logger memory constraints and sampling cadence; users should account for potential biases due to sampling design.