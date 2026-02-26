# Data from a meteorological station next to Esthwaite Water 2008, 2009, 2010 and 2011.

- ## Overview
  - Location: meteorological station on top of a boat house, Cumbria, England, next to Esthwaite Water.
  - Period: data collected in 2008–2011.
  - Variables: air temperature (degrees C) and wind speed (m/s).
  - Sampling frequency: instruments measure data every 4 minutes; hourly averages are calculated by a Campbell Scientific datalogger.
  - Time reference: all data recorded in GMT.
  - Data status: raw data not yet calibrated or quality controlled; visually checked; obvious hardware errors removed; gaps due to maintenance or sensor/logger problems.
  - Usage: used in several current scientific studies including PhD work.

- ## Sampling regime and collection methods
  - Instruments provide a range of meteorological measurements; hourly averages are computed from the 4-minute measurements by the datalogger.
  - Example rule: the hourly value for 2 p.m. is the average of data between 1 p.m. and 2 p.m., excluding 1 p.m. data and including 2 p.m. data.

- ## Quality control
  - Data are raw and have not undergone calibration or formal quality control.
  - Visual checks performed; non-representative data due to hardware issues removed.
  - Gaps reflect maintenance events or sensor/logger problems.

- ## Data structure and format
  - Delivery format: comma separated values (CSV).
  - Columns:
    - Date_GMT: date and time of measurement (GMT).
    - Air_Temperature: air temperature in degrees C.
    - Wind_Speed: wind speed in metres per second.
  - Documentation notes: data are provided with units and time reference; 2008–2011 scope; hourly averaging method described.

- ## Data management and governance considerations for Data Stewards
  - Metadata to capture: location, instruments, sampling regime, units, datum (GMT), data status (raw, not QC’d), and calculation method for hourly averages.
  - Provenance: clear record of collection methods, instrument type, and data processing steps (hourly averaging, post-collection quality checks).
  - Accessibility and reuse: dataset is active in scientific studies; for sharing, dataset should be QC’d and accompanied by detailed documentation to ensure appropriate use.

- ## Limitations and caveats
  - Raw data require calibration and formal QC before broad reuse.
  - Data gaps exist due to maintenance and hardware issues.
  - Single-site data limit spatial representativeness; interoperability requires explicit method metadata (hourly averaging, GMT, units).

- ## Practical implications for reuse
  - For downstream analyses, perform calibration and formal QC.
  - Ensure alignment of time references (GMT) and unit conventions (°C, m/s).
  - Consider integrating with other datasets with harmonized metadata and clear provenance.