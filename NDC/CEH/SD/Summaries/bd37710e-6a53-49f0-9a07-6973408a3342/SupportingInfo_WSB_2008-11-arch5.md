# Supporting information for automatic water monitoring buoy data from Windermere South Basin 2008-2011

## Overview
- Dataset from an automatic lake monitoring buoy in Windermere South Basin, Cumbria, England.
- Covers 2008–2011; includes air temperature, solar radiation, wind speed, and lake temperature profiles.
- Lake temperatures recorded at depths: 1, 2, 4, 7, 10, 13, 16, 19, 22, 25, 30, and 35 m.
- Measurements every 4 minutes; hourly averages calculated by a Campbell Scientific datalogger.
- All data presented in GMT (dates 2008–2011).

## Data availability and citation
- Available via the NERC Environmental Information Data Centre; DOI provided.
- Data are raw (not calibrated or quality controlled) but have been visually checked; obvious hardware errors removed.
- Notable data gap: ~10 days in 2010 due to logger/telemetry changes.
- Other gaps result from buoy maintenance or sensor/logger problems.
- Dataset has been used in multiple scientific studies and publications.

## Sampling regime and collection methods
- Instrumented buoy collects meteorological data and in-lake temperatures.
- Temperature sensors are platinum resistance thermometers.
- Data flow: measurements every 4 minutes; hourly averages produced by the datalogger.
- Data columns include Date GMT, water temperatures at specified depths, Air Temperature, Pyranometer (solar radiation), and Wind Speed.

## Quality Control
- Data are raw and not calibrated or quality controlled for sharing.
- Visual checks performed; corrections made for obvious hardware malfunctions.
- A 10-day data gap in 2010 due to logger changes; other gaps due to maintenance or sensor/logger issues.

## Data structure
- CSV format with columns:
  - Date GMT
  - Water temperature at 1m, 2m, 4m, 7m, 10m, 13m, 16m, 19m, 22m, 25m, 30m, 35m (°C)
  - Air Temperature (°C)
  - Pyranometer (Solar radiation flux, W/m²)
  - Wind Speed (m/s)
- Each row represents an hourly average; units and depths are defined in descriptions.

## Additional information and usage
- Buoy data cited in several publications (2014, 2015, 2016) and used by PhD researchers.
- Examples include methods for estimating onset of thermal stratification and diel temperature variability studies.

## Data governance considerations for Data Stewards
- Metadata consistency: ensure clear naming, units, depth annotations, and time zone (GMT).
- Provenance: document instrument types (Campbell Scientific datalogger) and data generation process.
- Accessibility and preservation: confirm DOI and long-term archiving; provide versioning and clear data lineage.
- Data quality and updates: clearly separate raw vs. processed/calibrated data; provide calibration plans and QA procedures; log data revisions.
- Handling gaps: record known gaps (e.g., 2010 logger change) and maintain metadata about reasons and expected updates.
- Interoperability and reuse: maintain machine-readable format (CSV) with comprehensive metadata; include a README or metadata file; specify licensing/citation requirements for reuse.