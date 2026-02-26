# ReadMe file for Rainfall.csv

## Overview
- Provides hourly rainfall data used in studies investigating soil greenhouse gas emissions from sheep urine deposited on unimproved montane grassland.
- Recorded with a HOBO® RG3 Data Logging rain gauge connected to a Pendant Event data logger (Tempcon Instrumentation Ltd., Sussex, UK).

## Data content and structure
- Contains records for hours in which rainfall was detected; hours with 0 mm rainfall are not logged.
- Columns:
  - Date_time: Date and time of the recorded event (format: dd/mm/yyyy hh:mm).
  - Hourly_rain: Total rainfall recorded over the hour in millimetres (mm).

## Data collection and provenance
- Equipment: HOBO RG3 Data Logger with Pendant Event data logger.
- Units: Millimetres for rainfall; date/time in dd/mm/yyyy hh:mm.

## Usage and quality considerations
- Authors must be acknowledged if data are reused or reproduced.
- Data should undergo standard quality assurance, cleaning, and transformation consistent with environmental monitoring practices.
- Be aware of gaps due to non-logged zero-rain hours; consider implications for time-series analyses and potential imputation if a continuous series is required.