# Activity data from common guillemots from the Isle of May during the 2005-2006 annual cycle

## Overview
- Biologging study of 13 common guillemots (Uria aalge) from the Isle of May National Nature Reserve, Scotland, covering the 2005-2006 annual cycle.
- Methods: birds captured as chick-rearing adults, fitted with GLS time-depth recorders (TDRs); loggers recovered during re-capture; sexing via CHD gene analysis.
- Data collection period: 4 July 2005 to 21 June 2006.
- Two sampling regimes due to memory limits: 
  - a) depth readings every 16 s for 24 h every 30 days (n = 9 loggers retrieved)
  - b) depth readings every 32 s for 24 h every 15 days (n = 4 loggers retrieved)
- Derived measures include daily activity budgets, sea surface temperature (SST) from bird-borne loggers, energy expenditure, location fixes, and diel patterns of diving.
- Colony attendance tracked in parallel via daily time-lapse photography (7 Oct 2005 – 20 May 2006).
- Data provenance: access granted by Scottish Natural Heritage; data collected by Sarah Wanless, Mike Harris, and Francis Daunt; data processed by Ruth Dunn.

## Data files and structure
- IoM_Guillemot_SST_TAB_DEE.csv (13 columns)
  - ID, Sex, Date, Logger-SST (°C), Inactive_h, Diving_h, Active_h, Flight_h, Colony_h, DEE (kJ), Twilight_diving, Day_diving, Night_diving
- IoM_Guillemot_Locations.csv (4 columns)
  - ID, Date, Long, Lat (two locations estimated per day)
- IoM_Guillemot_ColonyAttendance.csv (2 columns)
  - Date, Density (0–5 scale; 0 = none, 5 = all sites occupied)

## Data collection and processing details
- Field methods: attachment and retrieval of GLS-TDR devices from chick-rearing adults; devices limited by memory necessitating two sampling schemes.
- Sexing: using CHD genes from collected feathers.
- Derived outputs: daily hours in various behaviours (diving, flying, at colony, active/inactive on water), daily energy expenditure, proportions of dive activity by time of day, SST per day, and daily colony attendance density.

## Relevance for monitoring frameworks
- Provides integrated behavioral, energetic, spatial, and environmental indicators that can inform seabird-based environmental health monitoring.
- Enables linking seabird activity and energetics to local SST and spatial distribution, supporting policy assessment and trend analysis.

## Data quality, metadata, and governance considerations
- Strengths: clear provenance, explicit sampling regimes, and well-defined column metadata and units.
- Limitations and considerations:
  - Small sample size (n=13) may limit generalizability.
  - Two different sampling schemes require harmonization for longitudinal comparisons.
  - Potential data gaps due to device memory limits and retrieval success; reliance on multiple data streams (SST, locations, colony density) necessitates careful data integration.
  - Metadata clarity on licensing and data sharing is implicit from publication context; explicit reuse rights are not stated here.
- Governance aspects aligned with monitoring practices:
  - Data collection and processing credits are provided; underlying data are organized into separate, well-documented CSV files, facilitating reuse with appropriate provenance.