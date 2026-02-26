# Activity data from common guillemots from the Isle of May during the 2005-2006 annual cycle

## Overview
- Dataset of common guillemots Uria aalge from the Isle of May National Nature Reserve, Scotland (56°11′N, 02°33′W) collected during the 2005-2006 annual cycle.
- Biologging data collected by attaching GLS time-depth recorder (TDR) devices to Darvic leg-rings; loggers retrieved when birds were recaptured during the breeding season.
- Sexing performed using CHD I genes from body feathers collected at recapture.
- Data cover 13 individuals from 4 July 2005 to 21 June 2006.

## Data collection and devices
- GLS/TDRs used to record depth and location; loggers removed at recapture.
- Bird-borne loggers also recorded sea surface temperature (SST).
- Data processing included determining daily activity budgets and energy expenditure.

## Sampling design
- Two sampling regimes to balance resolution and duration:
  - a) Depth readings every 16 seconds for a 24-hour period every 30 days (n = 9 retrieved loggers).
  - b) Depth readings every 32 seconds for a 24-hour period every 15 days (n = 4 retrieved loggers).
- Limited memory size of TDRs influenced sampling rates and duration.

## Derived data and variables
- Daily activity budgets (hours per day): diving, flying, at the colony, active on water, inactive on water.
- Sea surface temperature values (SST) recorded by bird-borne loggers.
- Daily energy expenditure (DEE) in kilojoules.
- Location fixes (latitude and longitude) with two estimated daily locations.
- Proportions of dive activity by time of day: Twilight_diving, Day_diving, Night_diving.

## Colony attendance
- Attendance data collected via daily time-lapse photography from 7 October 2005 to 20 May 2006.
- Colony density scored daily on a scale from 0 to 5 (0 = no individuals; 5 = all ~100 breeding sites occupied).

## Dataset files and schema
- IoM_Guillemot_SST_TAB_DEE.csv
  - Columns: ID, Sex, Date (D-M-Y), Logger-SST (°C), Inactive_h (hours), Diving_h (hours), Active_h (hours), Flight_h (hours), Colony_h (hours), DEE (kJ), Twilight_diving, Day_diving, Night_diving.
- IoM_Guillemot_Locations.csv
  - Columns: ID, Date (D-M-Y), Long, Lat.
  - Two locations estimated per day; data separated from SST/DEE file.
- IoM_Guillemot_ColonyAttendance.csv
  - Columns: Date (D-M-Y), Density (0–5 scale).

## Access, provenance, and acknowledgments
- Access granted by Scottish Natural Heritage for Isle of May data.
- Data collection by Sarah Wanless, Mike Harris, and Francis Daunt; data processing by Ruth Dunn.