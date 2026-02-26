# Dissolved oxygen data recorded at five sites in the Hampshire Avon (United Kingdom) using miniDOT data loggers at a resolution of 0.01 mg O2 per litre over the period August 2014 to August 2015 with data logged every minute.

## Overview
- Data collected at five sites in the Hampshire Avon, UK
- Instrument: miniDOT data loggers
- Resolution: 0.01 mg O2 per litre
- Time period: August 2014 to August 2015
- Logging frequency: every minute

## Variable descriptions and data formatting
- Unix.Timestamp: integer; seconds since epoch
- Temp: numeric; water temperature in degrees Celsius
- DO: numeric; dissolved oxygen in milligrams per litre
- CSat: numeric; dissolved oxygen saturation in milligrams per litre
  - DO and CSat values are calculated from water temperature and atmospheric pressure using USGS DOTABLES; no salinity correction applied (assumed negligible)
- AbsPres_kPa: numeric; atmospheric pressure in kiloPascals (from British Atmospheric Data Centre)
- good.records: boolean; TRUE if the record is considered good
  - Only good records are used for analysis
  - Records are screened by DO minimum envelope by day and then by a smooth spline comparison with the observed value, applying a tolerance to mark records as not good
- Missing values: NA

## Site locations
- AS2 — River: Sem; latitude: 51.04572; longitude: -2.110836
- CE1 — River: Ebble; latitude: 51.02816; longitude: -1.92392
- CW2 — River: Wylye; latitude: 51.14304; longitude: -2.203277
- GA2 — River: Avon; latitude: 51.31942; longitude: -1.861853
- GN1 — River: Nadder; latitude: 51.04548; longitude: -2.110481

## Data quality, processing, and governance considerations
- Quality control: good.records flag indicates records suitable for analysis; filtering ensures data quality
- Metadata includes site codes, river associations, and precise coordinates for discoverability and interoperability
- Provenance: DO values derived from measured DO and temperature, with saturation estimates based on temperature and atmospheric pressure using USGS DOTABLES
- Assumptions and limitations:
  - No salinity correction applied
  - Atmospheric pressure sourced from a designated data centre
  - Data are presented with missing values as NA, suitable for auditing and reprocessing if needed

## Data handling and sharing (implications for Data Stewards)
- Ensure metadata remains aligned with site identifiers and coordinates for discoverability
- Maintain transparency on quality filtering criteria (envelope, spline tolerance) for reproducibility
- Preserve source and method notes (treatment of saturation, lack of salinity correction) to inform downstream users and governance
- Facilitate updates by tracking good.records decisions and any re-evaluations of records
- Provide access to the full time series with clear handling of NA values and timestamps for integration into larger datasets or portals