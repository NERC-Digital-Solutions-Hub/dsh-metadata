# Dissolved oxygen data recorded at five sites in the Hampshire Avon (United Kingdom) using miniDOT data loggers

## Overview
- Timeframe: August 2014 to August 2015
- Location: Five sites along the Hampshire Avon, United Kingdom
- Instrument and data: miniDOT data loggers; dissolved oxygen (DO) data recorded every minute
- Resolution: 0.01 mg O2 per litre

## Variables and data processing
- Unix.Timestamp: integer, seconds since epoch
- Temp: water temperature in degrees Celsius
- DO: dissolved oxygen in milligrams per litre
- CSat: DO saturation in milligrams per litre; calculated from temperature and atmospheric pressure using USGS DOTABLES; no salinity correction applied
- AbsPres_kPa: atmospheric pressure in kilopascals (from British Atmospheric Data Centre)
- good.records: logical flag indicating whether a record is considered good
  - Records filtered by daily DO envelope and a smooth spline comparison; records failing tolerance are marked not good
- Missing values: NA
- Data usage: only good records are used for analysis
- Data management note: metadata and data quality steps support verification and discoverability

## Site locations
- AS2 — River Sem: 51.04572, -2.110836
- CE1 — River Ebble: 51.02816, -1.92392
- CW2 — River Wylye: 51.14304, -2.203277
- GA2 — River Avon: 51.31942, -1.861853
- GN1 — River Nadder: 51.04548, -2.110481