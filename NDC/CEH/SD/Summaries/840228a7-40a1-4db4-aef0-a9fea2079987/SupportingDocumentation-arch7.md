# Dissolved oxygen data recorded at five sites in the Hampshire Avon (United Kingdom) using miniDOT data loggers

- Five sites in the Hampshire Avon studied with miniDOT data loggers
- Dissolved oxygen data recorded at a resolution of 0.01 mg O2 per litre
- Time period: August 2014 to August 2015
- Data logged every minute

## Variables and data fields
- Unix.Timestamp: integer, Unix time in seconds
- Temp: numeric, water temperature in degrees Celsius
- DO: numeric, dissolved oxygen in milligrams per litre
- CSat: numeric, dissolved oxygen saturation in milligrams per litre; calculated from temperature and atmospheric pressure using USGS DOTABLES
- AbsPres_kPa: numeric, atmospheric pressure in kiloPascals (from British Atmospheric Data Centre)
- good.records: logical, TRUE/FALSE indicating whether the record is good for analysis
  - Only good records are used
  - Filtering performed by day with a DO minimum envelope, then via a smooth spline; records marked not good if they exceed tolerance
- Missing values are coded as NA

## Calculations and data quality
- CSat values derived from water temperature and atmospheric pressure using USGS DOTABLES; salinity correction is not applied (assumed negligible)
- AbsPres_kPa sourced from British Atmospheric Data Centre
- Data quality control:
  - Records screened for plausibility with a DO envelope by day
  - Further filtered using a smooth spline comparison to observed values
  - Records failing tolerance are flagged as not good and excluded from analysis

## Site locations
- AS2 — River Sem: 51.04572, -2.110836
- CE1 — River Ebble: 51.02816, -1.92392
- CW2 — River Wylye: 51.14304, -2.203277
- GA2 — River Avon: 51.31942, -1.861853
- GN1 — River Nadder: 51.04548, -2.110481

## GIS-related considerations
- The dataset provides minute-scale spatially explicit DO measurements across five defined sites, enabling high-resolution mapping of DO dynamics over time
- Use the good.records flag to filter data for robust spatial-temporal analyses
- Temporal resolution supports detailed trend visualization; may require aggregation for certain map-based visuals
- Coordinates allow integration with basemaps and other geospatial layers for policy, client, or public-facing visualisations

## References and data sources
- CSat calculations reference USGS DOTABLES (no salinity correction)
- AbsPres_kPa values reference data from the British Atmospheric Data Centre