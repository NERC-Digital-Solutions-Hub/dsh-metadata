# Data from automatic water monitoring buoy from Bassenthwaite Lake 2008, 2009, 2010 and 2011. Jones, I., Feuchtmayr, H. (2017)

## Overview
- Continuous atmospheric and lake temperature data collected from an automatic buoy in Bassenthwaite Lake, Cumbria, England.
- Variables include air temperature, solar radiation, wind speed, and lake water temperatures at multiple depths (1–18 m).
- Timeframe: 2008–2011; data are provided as hourly averages derived from 4-minute measurements.
- GMT timestamps; data used in several scientific studies and by PhD researchers.

## Sampling Regime and Collection Methods
- Instrumentation: meteorological sensors and in-lake temperature sensors (platinum resistance thermometers) at depths of 1, 2, 3, 4, 5, 6, 8, 10, 12, 14, 16, and 18 meters.
- Measurements: air temperature (°C), solar radiation flux (W/m²) via pyranometer, wind speed (m/s), and lake temperatures (°C) at specified depths.
- Data cadence: raw measurements every 4 minutes; hourly averages computed by the datalogger (example: 2 p.m. value is average of 1–2 p.m., excluding 1 p.m. data, including 2 p.m. data).
- Data status: raw data not yet calibrated/quality controlled; visual checks performed; obvious hardware errors removed.

## Quality Control
- Visual inspection conducted; non-physical artifacts from hardware failures removed.
- Gaps attributed to buoy maintenance or sensor/logger problems.
- Periods with missing data: February 2010, May 2011, and July 2011 due to buoy/logger/telemetry maintenance.
- Data are suitable for exploratory analyses but require calibration/quality control for some quantitative applications.

## Data Structure
- Format: comma-separated values (CSV).
- Key columns:
  - Date_GMT: date and time (GMT) of measurement.
  - Water_temperature: temperatures at 1m, 2m, 3m, 4m, 5m, 6m, 8m, 10m, 12m, 14m, 16m, 18m (°C).
  - Air_Temperature: air temperature (°C).
  - Pyranometer: solar radiation flux (W/m²).
  - Wind_Speed: wind speed (m/s).

## Data Gaps and Limitations
- Some gaps due to maintenance (explicitly February 2010, May 2011, July 2011).
- Data are raw and not yet calibrated; users should apply quality control and calibration as needed for precise analyses.
- Possible limitations for local-scale analyses during maintenance periods or when sensors failed.

## Uses and Publications
- Utilised in studies addressing lake thermal dynamics and stratification:
  - "A novel method for estimating the onset of thermal stratification in lakes from surface water measurements" (Water Resources Research, 2014).
  - "Diel variability in epilimnetic temperature for five lakes in the English Lake District" (Inland Waters, 2015).
  - "Diel surface temperature range scales with lake size" (PLoS ONE, 2016).
- Data are actively used by current PhD students and researchers; dataset is part of ongoing scientific work.

## Access and Practical Considerations for Analysts
- Data are being used in multiple contemporary studies; suitable for correlation analyses between air conditions, solar radiation, wind, and vertical temperature profiles.
- Multi-depth measurements enable evaluation of vertical temperature gradients and stratification dynamics.
- Since data are raw, analysts should perform calibration/quality control and account for missing periods when modeling or inferring trends.
- Documentation notes that datasets created may be discoverable via portals with metadata, aiding reproducibility and data provenance.