# Dissolved Oxygen concentrations from Durleigh Reservoir, 2018

## Summary for GIS Specialists
- Two fixed monitoring locations (L2 and L3) at Durleigh Reservoir with miniDOT loggers (bottom-water measurements).
- Data collected from 30 May 2018 to 5 Oct 2018 at 10-minute intervals.
- Provided as raw .txt files, one per location (L2 at 51.1210, -3.0403; depth 6 m; L3 at 51.1215, -3.0445; depth 4 m).
- Variables include timestamp, temperature, dissolved oxygen (mg/L), DO saturation (%), battery, and quality flag; salinity compensation shown as 0.0 ppt; saturation computed at 1013.0 mbar.
- Sensor details: L2 sensor 7392-875323; L3 sensor 7450-701302. Concatenated data files with timestamps: 2018Oct05 17:43:25 BST (L2) and 2018Oct05 18:04:04 BST (L3).
- Noted data quality issues: periods of sensor fouling and times when sensors were out of the water for cleaning or battery replacement (e.g., 13 June and 21 August 2018). DO values during fouling may be unreliable (e.g., 0% saturation). Data require cleaning prior to analysis.

## Data Files and Format
- Two raw data files (one per location) in .txt format:
  - Location 2 (L2): lat 51.1210, lon -3.0403, depth 6 m; sensor 7392-875323.
  - Location 3 (L3): lat 51.1215, lon -3.0445, depth 4 m; sensor 7450-701302.
- Columns include: Unix_Timestamp (s), UTC_Date_&_Time, Greenwich_Mmean_Time, Battery (V), Temperature (°C), Dissolved_Oxygen (mg/L), Dissolved_Oxygen_Saturation (%), Q (quality).
- DO values are raw; note that measurements were occasionally compromised by fouling or maintenance activities.

## Locations, Sensors and Measurements
- Location 2 (L2)
  - Coordinates: 51.1210, -3.0403
  - Depth: 6 m
  - Sensor: 7392-875323
- Location 3 (L3)
  - Coordinates: 51.1215, -3.0445
  - Depth: 4 m
  - Sensor: 7450-701302
- Measurements are time-stamped at 10-minute intervals; includes temperature and DO (mg/L) with DO saturation (%).

## Data Quality and Cleaning
- Data are provided as raw measurements requiring cleaning prior to analysis.
- Known issues include periods when sensors were fouled and periods when sensors were out of water (e.g., 13 June and 21 August 2018), which can lead to invalid DO readings or 0% saturation.
- Cleaning steps should include: flagging/removing fouled periods, handling gaps due to maintenance, validating units, and harmonizing time stamps.

## Temporal Coverage
- Timeframe: 30 May 2018 to 5 Oct 2018
- Sampling frequency: every 10 minutes

## GIS Applications and Workflow
- Potential workflows:
  - Import each location’s .txt as a delimited table and create two point features with coordinates, depth, and sensor metadata.
  - Build attributes: timestamp, temperature, DO (mg/L), DO saturation (%), battery, quality flag.
  - Convert UTC times to local time if needed and ensure consistent time zones for time-series analyses.
  - Create time-enabled layers or animations to visualize DO dynamics over the 2018 season.
  - QA/QC by removing or flagging fouled periods and gaps; annotate data quality where relevant.
  - If needed, combine datasets to compare DO dynamics between the two depths/locations or to integrate with reservoir hydrology layers.
- Cautions:
  - Data are raw; substantial cleaning is required before any GIS analysis.
  - Limited spatial coverage (two fixed points) may constrain interpolation or surface generation.

## Provenance and Citation
- Source: Slavin, E.I., and Wain, D.J. 2018. Dissolved Oxygen concentrations from Durleigh Reservoir, 2018.
- Metadata and dataset notes accompany the two raw TXT files; ensure citation when using or publishing products derived from this data.

## Key Considerations and Limitations
- Only two fixed locations; limited spatial representativeness for the reservoir.
- Data quality depends on sensor fouling and maintenance periods; rigorous cleaning needed.
- DO values are in mg/L with saturation percentages; verify units and calibration context for GIS analyses.
- Temporal resolution is high (10-minute intervals) but affected by quality issues; plan for gaps in time-series analyses.