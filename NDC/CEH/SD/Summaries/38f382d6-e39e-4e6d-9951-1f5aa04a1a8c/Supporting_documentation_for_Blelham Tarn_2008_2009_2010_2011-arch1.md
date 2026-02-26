# Sampling Regime and Collection Methods

- The dataset comes from an automatic lake monitoring buoy located at Blelham Tarn, Cumbria, England.
- Instruments measure a range of meteorological variables and in-lake temperature profiles.

## Measured variables
- Air temperature (°C)
- Solar radiation flux (W/m^2)
- Wind speed (m/s)
- Lake water temperatures at depths: 0.5, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10, and 12 m

## Data collection cadence and time reference
- Data are collected every 4 minutes.
- Hourly averages are calculated by a Campbell Scientific datalogger as the average over the previous hour (the value for 2 p.m. is the average from 1–2 p.m., excluding 1 p.m. data and including 2 p.m. data).
- Times are in GMT.
- Data cover 2008, 2009, 2010, and 2011.

## Data quality and limitations
- The dataset is raw and has not yet been calibrated or quality controlled.
- Visual checks have been performed and obvious hardware malfunctions removed.
- Gaps occur due to buoy maintenance or sensor/logger problems.

## Data format and structure
- Provided as a comma-separated values (CSV) file.
- Columns include:
  - Date_GMT (timestamp in GMT)
  - 0.5m, 1m, 2m, 3m, 4m, 5m, 6m, 7m, 8m, 9m, 10m, 12m water temperatures (°C)
  - Air_Temperature (°C)
  - Pyranometer (solar radiation, W/m^2)
  - Wind_Speed (m/s)

## Context, usage, and publications
- The buoy data are used in ongoing scientific studies, including PhD research.
- Notable publications incorporating this dataset:
  - Woolway et al. (2014) Water Resources Research: A novel method for estimating the onset of thermal stratification in lakes from surface water measurements.
  - Woolway et al. (2015) Inland Waters: Diel variability in epilimnetic temperature across five lakes in the English Lake District.
  - Woolway et al. (2016) PLoS ONE: Diel surface temperature range scales with lake size.

## Provenance and accessibility
- Data from the buoy underpin multiple studies, with datasets and metadata intended to be discoverable via data portals.