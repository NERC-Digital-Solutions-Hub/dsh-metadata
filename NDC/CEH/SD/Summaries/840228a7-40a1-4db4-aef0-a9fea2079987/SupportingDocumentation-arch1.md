# Dissolved oxygen data recorded at five sites in the Hampshire Avon (United Kingdom) using miniDOT data loggers

## Overview
- Data collected August 2014 to August 2015
- Five sites in the Hampshire Avon
- Data logged every minute with a DO resolution of 0.01 mg/L

## Variables and measurements
- Unix.Timestamp: integer, seconds since epoch
- Temp: water temperature in degrees Celsius
- DO: dissolved oxygen in milligrams per litre
- CSat: dissolved oxygen saturation in milligrams per litre (computed from Temp and atmospheric pressure using USGS DOTABLES; no salinity correction)
- AbsPres_kPa: atmospheric pressure in kilopascals (from British Atmospheric Data Centre)
- good.records: boolean indicating if a record is valid; only true records used
- Missing values are recorded as NA

## Data quality and processing
- Records filtered to include only good data
- Filtering approach: remove records using a daily DO minimum envelope and a smooth spline comparison with observed DO (tolerance applied)
- No correction applied for salinity

## Site locations
- AS2, River = Sem, lat 51.04572, lon -2.110836
- CE1, River = Ebble, lat 51.02816, lon -1.92392
- CW2, River = Wylye, lat 51.14304, lon -2.203277
- GA2, River = Avon, lat 51.31942, lon -1.861853
- GN1, River = Nadder, lat 51.04548, lon -2.110481