# High-resolution temperature and precipitation measurements for fire-affected locations in Australia (2019-2020) and Tenerife (2020-2021)

## Data overview
- High-resolution measurements of temperature and precipitation depth in 10-minute intervals.
- Two fire-affected locations: Madre del Agua, Tenerife (Spain) and Thompson reservoir, Victoria (Australia).

## Data files
- T_Pdepth_ma.csv (Madre del Agua, Tenerife)
- T_Pdepth_ts.csv (Thompson reservoir, Australia)

## What, Where, When, How, Why, Who
- What: Temperature (Temp) and precipitation depth (P) in 10-minute intervals.
- Where: Madre del Agua (Tenerife) UTM 28N 28 R 343340 3119657; Thompson reservoir (Victoria) UTM 55 H 441956 5822296.
- When: Madre del Agua 17/11/2020 to 19/11/2021; Thompson reservoir 28/03/2019 to 13/01/2020.
- How: RainWise Rainew raingauge coupled to Onset HOBO pendant datalogger (UA-003-64).
- Why: Monitoring environmental parameters related to runoff occurrence.
- Who: Dr Jonay Neris Tome, Dr Carmen Sánchez-García, Dr Cristina Santín, Prof. Stefan Doerr, Dr Gary Sheridan.

## Data quality and completeness
- Completeness: Full record.
- Features: Date and time (dd/mm/yyyy hh:mm), temperature (Temp: o C), precipitation depth (P: mm).
- Periodicity: 10-minute intervals.

## Variables and units
- Temperature: degrees Celsius (o C)
- Precipitation depth: millimeters (mm)
- Timestamp format: day/month/year hour:minute

## Temporal and spatial coverage
- Temporal: Two separate active periods corresponding to fire-affected sites in each region.
- Spatial: Two sites with precise UTM coordinates provided.

## Observations
- Madre del Agua: 9723 observations
- Thompson: 10050 observations

## Data support considerations for users
- Ensure consistent time zones and timestamp formatting when merging with other datasets.
- Validate cross-site alignment given differing monitoring periods.
- Leverage the two CSV files to create comparative analyses of temperature and rainfall responses in post-fire environments.
- Potential data products: time-series dashboards, comparative charts, and runoff-event analyses to support watershed management and post-fire recovery studies.