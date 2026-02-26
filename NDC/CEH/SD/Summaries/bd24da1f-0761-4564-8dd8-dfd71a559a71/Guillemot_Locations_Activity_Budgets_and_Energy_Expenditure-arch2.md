# Activity data from common guillemots from the Isle of May during the 2005-2006 annual cycle

## Overview
- Dataset of biologging and attendance data for common guillemots (Uria aalge) from the Isle of May National Nature Reserve, Scotland (56°11′N, 02°33′W) collected during the 2005-2006 annual cycle.
- Purpose aligns with environmental monitoring: derives standardized indicators of animal activity and environmental interaction over time.
- Data were collected on 13 individuals between 4 July 2005 and 21 June 2006, with sexing performed from feather DNA and data processing handled by Ruth Dunn.

## Data components
- IoM_Guillemot_SST_TAB_DEE.csv
  - 13 columns: ID, Sex, Date (D-M-Y), Logger-SST (°C), Inactive_h (hours/day), Diving_h (hours/day), Active_h (hours/day), Flight_h (hours/day), Colony_h (hours/day), DEE (daily energy expenditure, kJ), Twilight_diving, Day_diving, Night_diving.
- IoM_Guillemot_Locations.csv
  - 4 columns: ID, Date (D-M-Y), Long, Lat.
  - Provides two estimated daily locations per day, separated from the SST/DEE data.
- IoM_Guillemot_ColonyAttendance.csv
  - 2 columns: Date (D-M-Y), Density (0–5, daily colony attendance score; 0 = none; 5 = ~100 breeding sites occupied).

## Sampling design and data collection
- Deployments: chicks-rearing adults captured and fitted with GLS time-depth recorders (LT2400) to obtain depth readings and location data.
- Sampling rates (limited logger memory):
  - 16 s depth sampling for a 24 h period every 30 days (n = 9 loggers retrieved)
  - 32 s depth sampling for a 24 h period every 15 days (n = 4 loggers retrieved)
- Data retrieved from loggers upon recapture; loggers removed, and 3–5 body feathers collected for sexing (CHD I genes) under UK Home Office Licence.
- Derived outputs:
  - Daily activity budgets: hours/diving, hours/flying, hours/at colony, hours/active on water, hours/inactive on water.
  - Sea surface temperature (SST) values from bird-borne loggers.
  - Energy expenditure (DEE), location fixes, and proportions of dive activity by time of day (day/twilight/night).

## Temporal and spatial scope
- Study period: 4 July 2005 to 21 June 2006.
- Location: Isle of May National Nature Reserve, Scotland (biologging on colony-associated birds; 56°11′N, 02°33′W).

## Data provenance and access
- Collectors: Sarah Wanless, Mike Harris, Francis Daunt ( Isle of May team); Scottish Natural Heritage provided access.
- Data processing: Ruth Dunn.
- Context: dataset designed for standardised environmental monitoring outputs and potential integration with other data sources; intended for broad accessibility and reuse.

## Relevance for environmental monitoring and policy
- Provides standardized, longitudinal measures of animal behavior and energy use linked to environmental conditions (SST, spatial movements, colony attendance).
- Facilitates cross-study comparisons and integration with other monitoring datasets to enhance assessment of environmental health and policy performance over time.
- Emphasizes reproducibility and data sharing through clearly structured CSV files and explicit metadata in column definitions.