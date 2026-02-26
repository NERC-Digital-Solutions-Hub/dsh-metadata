# Data from automatic water monitoring buoy from Bassenthwaite Lake 2012, 2013, 2014 and 2015. Jones, I.D., Feuchtmayr, H., Maberly, S.C. (2017)

## Purpose and scope
- A dataset from an automatic lake monitoring buoy at Bassenthwaite Lake, Cumbria, England.
- Covers 2012–2015 and includes meteorological data and in-lake temperature profiles.
- Variables recorded: air temperature (°C), solar radiation flux (W/m²), wind speed (m/s), and lake temperatures at depths from 1 m to 18 m.

## Sampling regime and collection methods
- Instruments: buoy-mounted meteorological sensors and platinum resistance thermometers for lake temperature.
- Data cadence: measurements every 4 minutes; hourly averages computed (by a Campbell Scientific datalogger until 24 Jan 2013 and by an Oracle database from 24 Jan 2013 onwards).
- Time reference: all data in GMT.
- Data format: CSV with the following columns and depth-specific temperature measurements:
  - Date_GMT; Water_temperature at 1m, 2m, 3m, 4m, 5m, 6m, 8m, 10m, 12m, 14m, 16m, 18m; Air_Temperature; Pyranometer (solar radiation); Wind Speed.

## Quality control and limitations
- Data are raw and not yet calibrated or quality controlled.
- Visual checks performed; obvious hardware-related errors removed.
- Data gaps occur due to buoy maintenance or sensor/logger problems.
- Notable gap: loss of the temperature chain in January 2014; no lake temperature profile data after that date.

## Data structure and metadata
- Data provided as comma-separated values (CSV).
- Clear column definitions and units, with explicit depth references for each temperature measurement.
- Documentation notes data provenance and date range (2012–2015).

## Data usage and references
- Dataset has supported multiple ongoing scientific studies, including PhD work.
- Publications: Woolway, Maberly, Jones, Feuchtmayr (2014) on estimating the onset of thermal stratification in lakes from surface water measurements (Water Resources Research, 50(6), 5131-5140).

## Relevance for monitoring frameworks (implications for authors)
- Illustrates collection of high-frequency, multi-parameter environmental data from automated platforms.
- Highlights challenges for monitoring frameworks: raw data readiness, need for calibration, data gaps, metadata completeness, and data sharing considerations.
- Demonstrates the importance of documenting data provenance, data formats, and instrument transitions (datalogger to database) for transparency and reuse.