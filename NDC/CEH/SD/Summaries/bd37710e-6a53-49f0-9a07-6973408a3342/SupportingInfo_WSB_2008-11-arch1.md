# Supporting information for automatic water monitoring buoy data from Windermere South Basin 2008-2011

## Overview
- Dataset from an automatic lake monitoring buoy in Windermere South Basin, Cumbria, England.
- Covers 2008–2011.
- Includes meteorological measurements (air temperature, solar radiation) and in-lake temperature profiles at multiple depths (1–35 m) updated every 4 minutes; hourly averages are provided.

## Data availability and citation
- Source: NERC Environmental Information Data Centre.
- Citation: Jones, I.; Feuchtmayr, H. (2017). south basin, 2008 to 2011. NERC EIDC.
- DOI: https://doi.org/10.5285/bd37710e-6a53-49f0-9a07-6973408a3342

## Sampling regime and collection methods
- Instrumentation: Automatic buoy with meteorological sensors and platinum resistance thermometers for water temperature.
- Measured variables and units:
  - Water temperature: deg C at depths 1, 2, 4, 7, 10, 13, 16, 19, 22, 25, 30, and 35 m.
  - Air Temperature: deg C.
  - Pyranometer: Solar radiation flux, W/m^2.
  - Wind Speed: m/s.
- Sampling cadence: data collected every 4 minutes; hourly averages calculated by the datalogger.
- Hourly average calculation example: value for 2 p.m. is the average of data from 1–2 p.m., excluding the 1 p.m. reading and including the 2 p.m. reading.
- Time reference: all data in GMT (UTC±0); dates in 2008–2011.

## Quality control
- Data are raw and not yet calibrated or quality controlled.
- Visual checks performed; obvious hardware-related errors removed.
- Notable gap: ~10 days in 2010 due to logger/telemetry change.
- Additional gaps occur during buoy maintenance or sensor/logger issues.
- Data provenance and timeline documented.

## Data structure
- Format: CSV file.
- Columns:
  - Date GMT
  - 1m, 2m, 4m, 7m, 10m, 13m, 16m, 19m, 22m, 25m, 30m, 35m (Water temperature at specified depths, deg C)
  - Air Temperature (deg C)
  - Pyranometer (Solar radiation, W/m^2)
  - Wind Speed (m/s)

## Additional information
- The buoy data are used in several contemporary scientific studies, including PhD research.
- Publications utilizing the dataset include:
  - Woolway, R.I., Maberly S.C., Jones, I.D., Feuchtmayr, H. (2014) A novel method for estimating the onset of thermal stratification in lakes from surface water measurements. Water Resources Research, 50(6), 5131-5140.
  - Woolway, R.I., Jones, I.D., Feuchtmayr, H., Maberly S.C. (2015) A comparison of the diel variability in epilimnetic temperature for five lakes in the English Lake District. Inland Waters, 5, 139-154.
  - Woolway et al. (2016) Diel surface temperature range scales with lake size. PLoS ONE, 11(3): e0152466.