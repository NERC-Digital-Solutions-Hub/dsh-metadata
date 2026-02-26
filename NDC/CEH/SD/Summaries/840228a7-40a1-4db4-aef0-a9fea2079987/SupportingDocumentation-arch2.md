# Dissolved oxygen data recorded at five sites in the Hampshire Avon (United Kingdom) using miniDOT data loggers at a resolution of 0.01 mg O 2 per litre over the period August 2014 to August 2015 with data logged every minute.

## General
- Data collection at five sites in the Hampshire Avon, UK.
- Instrumentation: miniDOT data loggers.
- Temporal span: August 2014 to August 2015.
- Temporal resolution: every minute.
- Data handling aim: produce standardized environmental health datasets for monitoring and policy evaluation.

## Variable description for miniDOT datasets
- Unix.Timestamp: integer; Unix time in seconds.
- Temp: numeric; water temperature in degrees Celsius.
- DO: numeric; dissolved oxygen in milligrams per litre.
- CSat: numeric; dissolved oxygen saturation in milligrams per litre; calculated from temperature and atmospheric pressure using USGS DOTABLES; no salinity correction applied (assumed negligible).
- AbsPres_kPa: numeric; atmospheric pressure in kilopascals (from British Atmospheric Data Centre).
- good.records: logical; TRUE if the record is deemed good, FALSE otherwise.
  - Filtering process: screen DO with a daily minimum envelope, then apply a smooth spline; compare spline to observed value and mark as not good within a tolerance.
- Missing values: NA for all fields.

## Site locations
- AS2 — River: Sem; latitude 51.04572; longitude −2.110836
- CE1 — River: Ebble; latitude 51.02816; longitude −1.92392
- CW2 — River: Wylye; latitude 51.14304; longitude −2.203277
- GA2 — River: Avon; latitude 51.31942; longitude −1.861853
- GN1 — River: Nadder; latitude 51.04548; longitude −2.110481

## Data quality and processing
- Only good records (good.records = TRUE) are used for analysis.
- Quality control involves daily envelope screening and smooth spline checks to identify and exclude anomalous readings.
- Data are described with consistent units and sources (e.g., DO saturation calculated from temperature and atmospheric pressure; salinity corrections not applied).

## Data storage, access, and use
- Datasets are prepared for storage and uploading to appropriate data portals.
- Emphasis on transparency and reproducibility by documenting data fields and quality filters.
- Outputs (e.g., analyses, maps, charts) are derived from standardized, quality-assured data to support environmental monitoring and policy assessment.

## Particular Challenges
- Increasing the value of monitoring datasets by combining DO data with other relevant environmental data (avoiding single-use datasets).
- Enabling access to the underlying data used to create final outputs to support broader scrutiny and reuse.