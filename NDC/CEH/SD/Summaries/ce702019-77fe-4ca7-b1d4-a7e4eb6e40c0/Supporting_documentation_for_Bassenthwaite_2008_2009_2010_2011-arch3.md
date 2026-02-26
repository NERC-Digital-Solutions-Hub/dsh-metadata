# Data from automatic water monitoring buoy from Bassenthwaite Lake 2008, 2009, 2010 and 2011. Jones, I., Feuchtmayr, H. (2017)

## Overview
- High-frequency environmental monitoring dataset from an automatic lake buoy at Bassenthwaite Lake, Cumbria, England.
- Variables include air temperature, solar radiation, wind speed, and lake water temperatures at multiple depths (1–18 m).
- Measurements recorded every 4 minutes; hourly averages calculated and reported in GMT.
- Time period: 2008, 2009, 2010, and 2011.
- Dataset has been used in multiple scientific publications.

## Sampling regime and collection methods
- Instrumented buoy provides meteorological data (air temperature, solar radiation flux, wind speed) and in-lake temperature profiles.
- Water temperatures are measured with platinum resistance thermometers at depths of 1, 2, 3, 4, 5, 6, 8, 10, 12, 14, 16, and 18 meters.
- Data processing yields hourly averages from 4-minute measurements.

## Quality control and data gaps
- Data are raw and not yet calibrated or quality-controlled; visual checks performed and obvious hardware errors removed.
- Data gaps occur due to buoy maintenance, sensor, or logger issues.
- Notable gaps: February 2010, May 2011, and July 2011.

## Data structure and format
- Data provided as a comma-separated values (CSV) file.
- Columns include:
  - Date_GMT: Date and time of measurement (GMT).
  - Water_temperature at depths: 1m, 2m, 3m, 4m, 5m, 6m, 8m, 10m, 12m, 14m, 16m, 18m (degrees C).
  - Air_Temperature (degrees C).
  - Pyranometer: Solar radiation flux (Watts per square metre).
  - Wind_Speed (metres per second).

## Data provenance and usage
- The buoy dataset is utilized in ongoing research, including PhD work.
- Cited publications linked to the dataset:
  - Woolway et al. (2014) on estimating onset of thermal stratification from surface measurements (Water Resources Research).
  - Woolway et al. (2015) on diel variability in epilimnetic temperature (Inland Waters).
  - Woolway et al. et al. (2016) on diel surface temperature range and lake size (PLoS ONE).

## Relevance for monitoring frameworks
- Demonstrates value of multi-parameter, high-frequency monitoring for assessing lake thermal dynamics and stratification.
- Highlights practical considerations for monitoring design: need for calibration/QA, explicit metadata, handling data gaps, and ensuring data provenance.
- Data structure (depth-resolved temperatures, synchronized meteorological variables) supports integrated environmental health assessments and policy evaluation.

## Metadata, governance, and accessibility considerations
- Metadata provided at column level and depth specification; GMT noted for temporal consistency.
- Data have been shared publicly via publication use; potential governance considerations include calibration status, data cleaning, and transparent reporting of gaps.
- The dataset exemplifies sharing data to support evidence-based decision making while balancing quality assurance and data management needs.