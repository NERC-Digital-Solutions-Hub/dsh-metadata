Dissolved oxygen data recorded at five sites in the Hampshire Avon (United Kingdom) using miniDOT data loggers at a resolution of 0.01 mg O 2 per litre over the period August 2014 to August 2015 with data logged every minute.

## Overview
- High-resolution time series of dissolved oxygen (DO) at five sites in the Hampshire Avon collected with miniDOT loggers.
- Temporal coverage: August 2014 – August 2015; data recorded every minute.
- Resolution: 0.01 mg/L for DO.

## Variables and data types
- Unix.Timestamp: integer; Unix time in seconds.
- Temp: numeric; water temperature in degrees Celsius.
- DO: numeric; dissolved oxygen in mg/L.
- CSat: numeric; DO saturation in mg/L, calculated from temperature and atmospheric pressure using USGS tables; no salinity correction applied.
- AbsPres_kPa: numeric; atmospheric pressure in kiloPascals (from British Atmospheric Data Centre data).
- good.records: logical; TRUE if the record is considered good.
- Missing values: NA for all fields where data are absent.

## Data quality and processing
- Only good.records are used for analysis.
- Quality control steps:
  - Day-by-day DO minimum envelope screening.
  - Smooth spline comparison between observed DO and spline value; records outside a defined tolerance are marked not good.
- Data cleaning results in a dataset focused on reliable observations; DO records are filtered accordingly.
- No salinity correction applied to CSat.

## Site locations
- AS2 — River Sem: 51.04572, -2.110836
- CE1 — River Ebble: 51.02816, -1.92392
- CW2 — River Wylye: 51.14304, -2.203277
- GA2 — River Avon: 51.31942, -1.861853
- GN1 — River Nadder: 51.04548, -2.110481