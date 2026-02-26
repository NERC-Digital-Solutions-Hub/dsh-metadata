# Dissolved oxygen data recorded at five sites in the Hampshire Avon using miniDOT data loggers

## Overview
- Dissolved oxygen data collected at five sites in the Hampshire Avon (UK) using miniDOT data loggers.
- Temporal resolution: every minute; data logged during August 2014 to August 2015.
- Measurement resolution: DO data at 0.01 mg O2 per litre.
- Recorded variables include Unix timestamp, water temperature, DO, DO saturation, atmospheric pressure, and a quality flag.
- Derived DO saturation (CSat) computed from water temperature and atmospheric pressure using USGS DOTABLES; no salinity correction applied.
- Records are logged with missing values denoted as NA.
- Only records marked as good are used for analysis.

## Variable descriptions and data schema
- Unix.Timestamp: integer; Unix timestamp in seconds.
- Temp: numeric; water temperature in degrees Celsius.
- DO: numeric; dissolved oxygen in milligrams per litre.
- CSat: numeric; dissolved oxygen saturation in milligrams per litre (derived from Temp and atmospheric pressure).
- AbsPres_kPa: numeric; atmospheric pressure in kilopascals (from British Atmospheric Data Centre data).
- good.records: logical; TRUE or FALSE indicating whether the record is good. Only good records are used for analysis; records filtered by a daily envelope and then by a smooth spline comparison with a tolerance.
- All fields use NA to denote missing values.

## Data processing and quality control
- Quality assurance and data cleaning steps include:
  - Filtering records to retain only those deemed good via a per-day envelope check.
  - Further validation using a smooth spline to compare observed DO values against expected values within a tolerance.
- Data are prepared for analysis, with metadata added as needed and underlying data prepared for sharing where appropriate.
- Note: CSat is calculated without salinity correction.

## Site locations
- AS2 — River Sem — latitude 51.04572, longitude -2.110836
- CE1 — River Ebble — latitude 51.02816, longitude -1.92392
- CW2 — River Wylye — latitude 51.14304, longitude -2.203277
- GA2 — River Avon — latitude 51.31942, longitude -1.861853
- GN1 — River Nadder — latitude 51.04548, longitude -2.110481