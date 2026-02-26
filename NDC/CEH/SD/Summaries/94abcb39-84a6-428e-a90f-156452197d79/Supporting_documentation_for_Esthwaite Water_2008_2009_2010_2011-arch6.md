# Data from automatic water monitoring buoy from Esthwaite Water 2008, 2009, 2010 and 2011. Jones, I., Feuchtmayr, H. (2017)

## Overview
- Automated lake monitoring buoy deployed in Esthwaite Water, Cumbria, England.
- Measurements include air temperature, solar radiation (pyranometer), wind speed, and lake temperature profiles at multiple depths (0.43 m to 11.43 m).
- Data cadence: every 4 minutes; hourly averages calculated by a Campbell Scientific datalogger.
- All data are in GMT; dates span 2008–2011.

## Sampling regime and instruments
- In-lake temperature measured at depths: 0.43, 1.43, 2.43, 3.43, 4.43, 5.43, 6.43, 7.43, 8.43, 9.43, 10.43, and 11.43 m.
- Meteorological sensors include air temperature, pyranometer (solar radiation flux), and wind speed.
- Data stored in a comma separated values (CSV) file with clearly labeled columns.

## Quality control and limitations
- Raw data not yet calibrated or quality controlled.
- Visual checks conducted; obvious hardware-related errors removed.
- Data gaps occur due to buoy maintenance or sensor/logger problems.
- Notable anomaly: ice cover in January 2010 led to buoy damage and loss of the temperature chain.
- Users should expect incomplete data records and consider calibration/validation for precise analyses.

## Data structure and access
- Columns include: Date_GMT, temperature at each depth (0.43 m to 11.43 m), Air_Temperature, Pyranometer, Wind_Speed.
- Values for water temperatures are in degrees Celsius; solar radiation in Watts per square meter; wind speed in metres per second.
- The dataset is designed to support re-use in various analyses (e.g., vertical temperature profiles, surface-forcing relationships, and temporal variability).

## Usage, notes, and references
- The dataset has supported multiple scientific studies, including:
  - 2014: A novel method for estimating the onset of thermal stratification in lakes (Water Resources Research).
  - 2015: Diel variability in epilimnetic temperature across five lakes (Inland Waters).
  - 2016: Diel surface temperature range and lake size (PLoS ONE).
  - Additional related work in Freshwater Biology and other venues (2011–2014).
- Data have also been utilized by PhD researchers, indicating ongoing use in current studies.

## Practical considerations for data users
- Be mindful that hourly averages are computed over the previous hour (e.g., the 2 p.m. value averages 1–2 p.m., excluding 1 p.m. data and including 2 p.m. data).
- Treat the data as raw and uncalibrated; consider calibration and quality control before downstream analyses.
- Account for possible data gaps due to maintenance, sensor issues, or the 2010 ice-related incident when analyzing long-term trends.