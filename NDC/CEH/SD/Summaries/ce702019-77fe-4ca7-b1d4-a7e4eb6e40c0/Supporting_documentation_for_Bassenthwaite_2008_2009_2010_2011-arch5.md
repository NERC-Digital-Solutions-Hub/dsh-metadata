# Data from automatic water monitoring buoy from Bassenthwaite Lake 2008, 2009, 2010 and 2011. Jones, I., Feuchtmayr, H. (2017)

## Overview
- Dataset from an automatic lake monitoring buoy at Bassenthwaite Lake, Cumbria, England.
- Measured variables: air temperature, solar (Pyranometer) radiation, wind speed, and lake water temperatures at multiple depths.
- Depths for water temperature: 1m, 2m, 3m, 4m, 5m, 6m, 8m, 10m, 12m, 14m, 16m, 18m.
- Data cadence: every 4 minutes; hourly averages computed by a Campbell Scientific datalogger.
- Time reference: all data in GMT (UTC); dates cover 2008–2011.

## Data collection regime and instruments
- Instrumentation includes meteorological sensors and in-lake temperature sensors on a buoy.
- Water temperature at specified depths is reported in degrees Celsius.
- Solar radiation is reported as flux in Watts per square metre; wind speed in metres per second.

## Quality control and data quality notes
- Data are raw and have not yet been calibrated or quality controlled.
- Visual checks performed; obvious hardware faults removed.
- Data gaps occur due to buoy maintenance or sensor/logger issues.
- Specific gaps: February 2010, May 2011, and July 2011 during buoy/logger/telemetry maintenance.

## Data structure and metadata
- Format: comma-separated values (CSV).
- Columns:
  - Date_GMT: date and time (GMT) of measurement.
  - Water_temperature at 1m, 2m, 3m, 4m, 5m, 6m, 8m, 10m, 12m, 14m, 16m, 18m (temperatures in °C).
  - Air_Temperature (°C).
  - Pyranometer (Solar radiation flux in W/m^2).
  - Wind_Speed (m/s).
- Documentation notes: data values correspond to measurements generated every 4 minutes; hourly means reflect the interval 1–2 p.m. etc., excluding data at the start of the hour and including data at the end of the hour.

## Temporal coverage
- Years included: 2008, 2009, 2010, 2011.

## Usage and references
- The buoy dataset is used in several scientific studies, including:
  - Woolway, R.I., Maberly S.C., Jones, I.D., Feuchtmayr, H. (2014). A novel method for estimating the onset of thermal stratification in lakes from surface water measurements. Water Resources Research, 50(6), 5131-5140.
  - Woolway, R.I., Jones, I.D., Feuchtmayr, H., Maberly S.C. (2015). A comparison of the diel variability in epilimnetic temperature for five lakes in the English Lake District. Inland Waters, 5, 139-154.
  - Woolway, R.I., Jones, I.D., Maberly S.C., et al. (2016). Diel surface temperature range scales with lake size. PLoS ONE, 11(3): e0152466.
- The dataset is also used by PhD students in ongoing research.

## Particular challenges and governance considerations for Data Stewards
- Data governance needs: ensure metadata includes instrument types, depths, time zone, sampling regime, and data lineage; plan for calibration and quality control steps.
- Calibrated/QA status: dataset currently raw; schedule and document calibration/quality assurance processes before sharing as a finalized dataset.
- Data completeness: monitor and document maintenance periods to maintain a complete provenance log and transparent data gaps.
- Interoperability: ensure column naming conventions and units are consistent with other datasets (noting the specific depths available).
- Updates and provenance: establish procedures for updating the dataset and documenting any reprocessing or re-calibration.