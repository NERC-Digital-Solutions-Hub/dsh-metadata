# Data from automatic water monitoring buoy from Bassenthwaite Lake 2008, 2009, 2010 and 2011. Jones, I., Feuchtmayr, H. (2017)

## Overview
- Dataset from an automatic lake monitoring buoy at Bassenthwaite Lake, Cumbria, England, covering 2008–2011.
- Measured variables: air temperature (°C), solar radiation flux (W/m^2), wind speed (m/s), and lake water temperature profiles at multiple depths.
- Data cadence: measurements every 4 minutes; hourly averages provided by a Campbell Scientific datalogger.
- Time reference: all data in GMT (UTC); dates span 2008–2011.

## Sampling regime and collection methods
- Instrumentation: meteorological sensors plus in-lake temperature sensors on the buoy.
- Depths for water temperature: 1, 2, 3, 4, 5, 6, 8, 10, 12, 14, 16, and 18 meters.
- Units:
  - Air temperature: degrees Celsius
  - Solar radiation: Watts per square metre
  - Wind speed: metres per second
  - Water temperature: degrees Celsius at each depth
- Data processing: hourly averages calculated from 4-minute data; formula counts the data from the current hour, with a described inclusion/exclusion pattern (e.g., 2 p.m. average uses data from 1–2 p.m., excluding 1 p.m., including 2 p.m.).

## Data structure and availability
- Data file format: comma-separated values (CSV).
- Columns:
  - Date_GMT (timestamp)
  - Water_temperature at 1m, 2m, 3m, 4m, 5m, 6m, 8m, 10m, 12m, 14m, 16m, 18m
  - Air_Temperature
  - Pyranometer (solar radiation)
  - Wind_Speed
- Descriptions accompany each column, specifying the measurement meaning and depth.

## Data quality and gaps
- Status: raw data not yet calibrated or quality controlled.
- Quality checks: visually inspected; obvious hardware-related errors removed.
- Gaps: due to buoy maintenance or sensor/logger problems.
- Notable gaps: February 2010, May 2011, and July 2011 (data not available during these periods due to maintenance).

## Data usage and impact
- The buoy data have supported ongoing scientific studies and PhD research.
- Related publications using the dataset:
  - Woolway et al. (2014) on estimating the onset of thermal stratification from surface measurements (Water Resources Research).
  - Woolway et al. (2015) on diel variability in epilimnetic temperature across five lakes (Inland Waters).
  - Woolway et al. (2016) on diel surface temperature range scaling with lake size (PLoS ONE).

## Implications for data strategy and governance (Data Leaders)
- Raw data status implies a need for calibration, QA/QC workflows before broad analytical use.
- Documentation of data gaps and maintenance windows is essential for accurate analysis and modeling.
- Rich multi-parameter time series across multiple depths enable cross-variable analyses (thermal structure, surface fluxes, atmospheric forcing).
- Proven research utility supports investment in metadata, data provenance, and interoperability with similar lake datasets for broader system-level insights.