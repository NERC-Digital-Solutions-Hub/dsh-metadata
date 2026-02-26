# Data from automatic water monitoring buoy from Esthwaite Water 2008, 2009, 2010 and 2011. Jones, I., Feuchtmayr, H. (2017)

## Overview
- Dataset from an automatic lake monitoring buoy at Esthwaite Water, Cumbria, England.
- Measured: air temperature, solar radiation, wind speed, and lake water temperatures at multiple depths.
- Temporal coverage: 2008–2011.
- Sampling: data recorded every 4 minutes; hourly averages computed from the 4-minute data and expressed in GMT.

## What is collected
- Air temperature (°C).
- Solar radiation flux (Pyranometer) (W/m^2).
- Wind speed (m/s).
- Lake water temperature at depths: 0.43, 1.43, 2.43, 3.43, 4.43, 5.43, 6.43, 7.43, 8.43, 9.43, 10.43, and 11.43 m (°C).

## Data processing and quality
- Data provided as raw (not calibrated or quality controlled).
- Visual checks performed; obvious hardware-related errors removed.
- Gaps due to buoy maintenance or sensor/logger problems.
- Notable incident: January 2010 ice cover and buoy damage led to loss of the temperature chain.

## Data structure and metadata
- File format: comma-separated values (CSV).
- Columns:
  - Date_GMT (Date and time in GMT of measurement).
  - 0.43m, 1.43m, ..., 11.43m (temperature at each depth, °C).
  - Air_Temperature (°C).
  - Pyranometer (Solar radiation flux, W/m^2).
  - Wind_Speed (m/s).
- Hourly values: calculated as the average over the previous hour, excluding data from the start of the hour and including data from the end of the hour.

## Provenance and usage
- Data has been used in multiple ongoing scientific studies and by PhD researchers.
- Publications citing the dataset include:
  - Woolway et al. (2014) Water Resources Research: A method for estimating onset of thermal stratification from surface measurements.
  - Woolway et al. (2015) Inland Waters: Diel variability in epilimnetic temperature across five lakes.
  - Mackay et al. (2012, 2014, 2011, 2016 in various journals): Studies on sediment focusing, phosphorus dynamics, and spatial heterogeneity in lakes.

## Access, discoverability, and governance considerations
- Structure is clearly labeled with a detailed data dictionary (temperature at multiple depths, air temperature, solar radiation, wind speed).
- Data is raw and not calibrated, underscoring the need for metadata on calibration status for reuse.
- Coverage is limited to 2008–2011 with documented data quality issues and gaps.
- Demonstrates how long-term, high-frequency environmental time series can underpin diverse analyses and cross-disciplinary research.

## Relevance for data leadership
- Illustrates the importance of:
  - Documenting data collection regimes and instrumentation.
  - Providing a clear data dictionary and unit conventions for discoverability.
  - Tracking quality control status and known issues to inform reuse decisions.
  - Maintaining provenance information to support attribution in downstream research.
- Highlights potential for data reuse in climate, limnology, and ecosystem studies, especially where high-frequency, multi-depth lake temperature data can inform stratification, mixing, and nutrient cycling analyses.