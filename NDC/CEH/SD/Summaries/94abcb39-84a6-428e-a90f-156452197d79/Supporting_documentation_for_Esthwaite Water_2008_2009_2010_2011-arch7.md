# Data from automatic water monitoring buoy from Esthwaite Water 2008, 2009, 2010 and 2011. Jones, I., Feuchtmayr, H. (2017)

## Overview
- Dataset from an automatic lake monitoring buoy at Esthwaite Water, Cumbria, England.
- Measures meteorological variables and in-lake temperatures across depth profiles.
- Time span: 2008–2011.
- Data intended for use in scientific analyses and for informing map-based data products.

## Sampling regime and collection methods
- Instruments on the buoy: meteorological sensors and in-lake temperature sensors.
- Measured variables:
  - Air temperature (°C)
  - Solar radiation flux (W/m²)
  - Wind speed (m/s)
  - Lake water temperatures at depths: 0.43, 1.43, 2.43, 3.43, 4.43, 5.43, 6.43, 7.43, 8.43, 9.43, 10.43, 11.43 m
- Data cadence: every 4 minutes; hourly averages calculated by the data logger (average of the interval ending at the hour, excluding the start of the hour, including the end of the hour).
- Time reference: GMT (Greenwich Mean Time).

## Quality Control
- Data are raw and have not been calibrated or fully quality controlled.
- Visual checks performed; obvious hardware-related errors removed.
- Data gaps due to buoy maintenance or sensor/logger issues.
- Notable event: January 2010 ice cover caused buoy damage and loss of the temperature chain.

## Data structure and contents
- Format: comma-separated values (CSV) file.
- Columns include:
  - Date_GMT: date and time of measurement (GMT)
  - 0.43m, 1.43m, 2.43m, 3.43m, 4.43m, 5.43m, 6.43m, 7.43m, 8.43m, 9.43m, 10.43m, 11.43m: water temperature in °C at each depth
  - Air_Temperature: air temperature in °C
  - Pyranometer: solar radiation flux in W/m²
  - Wind_Speed: wind speed in m/s

## Publications and usage
- The buoy data have supported several studies, including:
  - Onset of thermal stratification in lakes from surface measurements
  - Diel variability in epilimnetic temperature across multiple lakes
  - Interannual variations affecting hypolimnetic phosphorus dynamics
  - Investigations into spatial heterogeneity and sediment processes in small lakes

## GIS considerations and how to use
- Suitable for creating time-resolved, depth-profile temperature visualizations and maps of thermal structure.
- Potential GIS applications:
  - Temporal mapping of surface-to-depth temperature gradients and stratification events
  - Visualization of diel temperature cycles across depths
  - Integration with other GIS layers (meteorology, lake morphometry) for spatial analyses
- Data preparation notes:
  - Data are raw; calibration and full QA/QC are not applied. Plan to calibrate or quality-check as needed for GIS analyses.
  - Be mindful of data gaps due to maintenance or the 2010 ice event; align time series to GMT (or convert if a local time is required).
  - Depth-specific temperature series enable cross-section or iso-therm mapping over time.
- Limitations:
  - Uncalibrated data; use with caution for quantitative thresholds without additional QA.
  - Gaps and potential sensor-related issues may affect continuity; incorporate gap-filling or masking as appropriate for analyses.