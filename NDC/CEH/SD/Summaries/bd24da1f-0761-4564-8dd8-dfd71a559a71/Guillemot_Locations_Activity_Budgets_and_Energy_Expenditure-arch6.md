# Activity data from common guillemots from the Isle of May during the 2005-2006 annual cycle

## Overview
- Biologging study of common guillemots (Uria aalge) from the Isle of May, Scotland, during 2005-2006.
- Data collected from 13 breeding adults using GLS/TDR loggers attached to Darvic leg rings; birds were recaptured to remove loggers and collect feathers for sexing.
- Timeframe: 4 July 2005 to 21 June 2006.

## Data collection and sampling design
- Deployment and retrieval: birds captured, tagged with GLS time-depth recorders (TDRs); loggers removed at recapture; 3–5 breast feathers collected for sexing using CHD genes.
- Sampling rates to balance detail and duration:
  - a) 16 s depth readings for a 24 h period every 30 days (n = 9 retrieved loggers)
  - b) 32 s depth readings for a 24 h period every 15 days (n = 4 retrieved loggers)
- Two daily location estimates per bird; location data provided separately from other metrics.

## Data files and structure
- IoM_Guillemot_SST_TAB_DEE.csv (13 columns)
  - ID, Sex, Date (D-M-Y), Logger-SST (°C), Inactive_h (hours), Diving_h (hours), Active_h (hours), Flight_h (hours), Colony_h (hours), DEE (daily energy expenditure in kJ), Twilight_diving, Day_diving, Night_diving
- IoM_Guillemot_Locations.csv (4 columns)
  - ID, Date (D-M-Y), Long, Lat
  - Note: two location estimates per day
- IoM_Guillemot_ColonyAttendance.csv (2 columns)
  - Date (D-M-Y), Density (0–5 scale; 0 no individuals to ~100 breeding sites occupied)

## Derived measures and indicators
- Daily activity budgets derived from loggers (hours spent diving, flying, at colony, active on water, inactive on water)
- Sea surface temperature (SST) recorded by bird-borne loggers
- Daily energy expenditure (DEE)
- Daily location fixes (lat/long)
- Proportions of dive activity by time of day (day, twilight, night)
- Colony attendance density (from daily time-lapse photography)

## Provenance and access
- Data collected by Scottish Natural Heritage with collaboration from Sarah Wanless, Mike Harris, and Francis Daunt; processed by Ruth Dunn.
- Isle of May National Nature Reserve provided access to the study site.