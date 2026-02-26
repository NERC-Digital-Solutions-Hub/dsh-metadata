# Sampling Regime and Collection Methods

- Context: Dataset from an automatic lake monitoring buoy at Blelham Tarn, Cumbria, England, capturing air and water temperature, solar radiation, wind speed, and lake temperature profile.
- Purpose alignment: Provides a consistent data stream to support assessment of environmental health and policy performance over time.

## Instruments and Measurements

- Air temperature: measured in degrees C
- Solar radiation: solar radiation flux in Watts per square metre (Pyranometer)
- Wind speed: measured in metres per second
- Lake water temperature: measured at depths of 0.5, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10 and 12 metres using platinum resistance thermometers
- Coverage: data from 2008, 2009, 2010, 2011

## Data Collection and Processing

- Sampling cadence: measurements every 4 minutes
- Averaging: hourly averages computed by a Campbell Scientific datalogger; example: 2 p.m. value is the average from 1–2 p.m., excluding 1 p.m. but including 2 p.m.
- Time standard: all data in Greenwich Mean Time (GMT)

## Quality Control

- Data type: raw data prior to calibration and formal quality control
- QA steps: data visually checked; obvious hardware-related errors removed
- Gaps: due to buoy maintenance or sensor/logger problems

## Data Structure and Variables

- File format: comma-separated values (CSV)
- Key columns:
  - Date_GMT: date and time (GMT) of measurement
  - Water_temperature: temperatures at 0.5m, 1m, 2m, 3m, 4m, 5m, 6m, 7m, 8m, 9m, 10m, and 12m depths
  - Air_Temperature: air temperature in degrees C
  - Pyranometer: solar radiation flux in Watts per metre squared
  - Wind_Speed: wind speed in metres per second

## Temporal Coverage

- Timeframe: data spanning 2008–2011

## Uses and Notable References

- Applications: dataset used in several scientific studies and by PhD researchers
- Publications include:
  - Woolway et al. (2014) on estimating onset of thermal stratification in lakes (Water Resources Research)
  - Woolway et al. (2015) on diel variability in epilimnetic temperature (Inland Waters)
  - Woolway et al. (2016) on diel surface temperature range and lake size (PLOS ONE)

## Relevance for Environmental Monitoring Analysts

- Compliance with standardized data formats and hourly aggregations supports consistent environmental health assessment over time.
- Data are raw but documented with QA steps; suitable for calibration, quality control, and transformation to final monitoring outputs.
- Designed for storage and publication in portals; supports data sharing and reproducibility.
- Opportunities to increase value by integrating with other datasets and improving underlying data accessibility for broader analysis.