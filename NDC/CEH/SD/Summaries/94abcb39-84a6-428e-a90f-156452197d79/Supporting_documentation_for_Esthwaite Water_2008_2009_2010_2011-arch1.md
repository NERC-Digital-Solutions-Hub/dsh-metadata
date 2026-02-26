# Data from automatic water monitoring buoy from Esthwaite Water 2008, 2009, 2010 and 2011. Jones, I., Feuchtmayr, H. (2017)

## Overview
- Dataset from an automatic lake monitoring buoy at Esthwaite Water, Cumbria, England.
- Instruments collect meteorological data (air temperature, solar radiation, wind speed) and in-lake temperature profiles.
- Time period: 2008–2011; measurements are recorded every 4 minutes with hourly averages provided.
- All data are in GMT.

## What data were collected
- Air temperature (°C)
- Solar radiation flux (Pyranometer) (W/m²)
- Wind speed (m/s)
- Lake water temperatures (°C) at depths: 0.43, 1.43, 2.43, 3.43, 4.43, 5.43, 6.43, 7.43, 8.43, 9.43, 10.43, 11.43 m

## Measurement details
- Location: Automatic buoy on Esthwaite Water; instruments include air temperature sensors, pyranometer, wind sensors, and platinum resistance temperature probes at multiple depths.
- Data cadence: 4-minute measurements; hourly averages computed by the datalogger (example: 2 p.m. average uses data from 1–2 p.m., with specific inclusion/exclusion of the hour’s endpoints).
- Data format: CSV with columns for Date_GMT, temperatures at each depth, air temperature, solar radiation, and wind speed.

## Data quality and gaps
- Raw data have not been calibrated or quality controlled; visuals checked and obvious hardware errors removed.
- Gaps due to buoy maintenance or sensor/logger problems.
- Notable incident: January 2010 ice cover caused buoy damage and loss of the temperature chain.

## Data structure
- Columns include:
  - Date_GMT
  - Water_temperature at 0.43m, 1.43m, 2.43m, 3.43m, 4.43m, 5.43m, 6.43m, 7.43m, 8.43m, 9.43m, 10.43m, 11.43m
  - Air_Temperature
  - Pyranometer (solar radiation)
  - Wind_Speed

## Data usage and publications
- The buoy dataset has supported multiple scientific studies, including:
  - 2014: A novel method for estimating the onset of thermal stratification in lakes from surface water measurements (Water Resources Research).
  - 2015: Diel variability in epilimnetic temperature for five lakes in the English Lake District (Inland Waters).
  - 2016: Diel surface temperature range scales with lake size (PLOS ONE).
  - 2014–2012: Studies on interannual atmospheric forcing and phosphorus cycling, sediment focussing, and spatial heterogeneity in small temperate lakes (Freshwater Biology; Fundamental and Applied Limnology; related works).
  
## How analysts can use this dataset
- Analyze correlations between atmospheric forcing (air temperature, solar radiation, wind) and lake thermal structure across depths.
- Investigate diel and seasonal temperature dynamics and onset of stratification.
- Develop or validate predictive models of stratification timing, heat content, and nutrient/SRD (phosphorus) dynamics.
- Compare surface vs. hypolimnetic responses and assess depth-dependent thermal gradients.
- Combine with other datasets and to generate actionable insights for lake management or ecological studies.

## Limitations and considerations
- Data are raw and require calibration and quality control for rigorous analyses.
- Gaps exist due to maintenance, sensor issues, and the 2010 ice disturbance.
- Data are from a single buoy at Esthwaite Water (2008–2011); regional extrapolation should be done cautiously.
- Time is GMT; conversion may be needed for local time contexts.