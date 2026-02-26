# Hourly data (air temperature, solar radiation, wind speed and lake temperature profile) from automatic water monitoring buoy from Windermere South Basin 2016 to 2018. Feuchtmayr, H., Jones, I.D., Clarke, M., Maberly S.C. (2021)

## Overview
- Data from an automatic lake monitoring buoy in Windermere South Basin, Cumbria, England.
- Time period: 2016–2018.
- Variables: air temperature (°C), solar radiation flux (W/m^2), wind speed (m/s), and lake water temperature profiles.

## Sampling regime and collection methods
- Instruments measure data every 4 minutes.
- Hourly averages are calculated from the previous hour using data from the current hour (GMT), e.g., 2 p.m. value = average of 1–2 p.m., excluding 1 p.m. data and including 2 p.m. data.
- Water temperatures sampled at depths: 1, 2, 4, 7, 10, 13, 16, 19, 22, 25, 30, and 35 meters using platinum resistance thermometers.
- All data recorded in GMT (UTC).

## Data structure
- File format: CSV.
- Columns include:
  - Date GMT (timestamp)
  - Water temperature at 1m, 2m, 4m, 7m, 10m, 13m, 16m, 19m, 22m, 25m, 30m, 35m (°C)
  - Air Temperature (°C)
  - Pyranometer (solar radiation flux in W/m^2)
  - Wind Speed (m/s)

## Quality control
- Data are raw and not calibrated or quality controlled.
- Visual checks performed; obvious hardware-derived errors removed.
- Data gaps attributed to buoy maintenance or sensor/logger problems.

## Spatial and temporal context for GIS use
- Single buoy provides vertical water temperature profiles and surface meteorology for Windermere South Basin.
- Suitable for time-series analysis and creating vertical temperature profiles; may require merging with additional spatial data for broader GIS mapping.

## Limitations and caveats
- Not fully calibrated or QC’d; single location limits spatial generalization.
- Gaps exist due to maintenance and sensor issues.
- Derived analyses should account for potential sensor drift or calibration needs.

## Funding and references
- Funding: Natural Environment Research Council (NERC) award NE/R016429/1, UK-SCaPE programme.
- Related work: Doubek et al. (2021) on storm-induced temperature changes in lakes using long-term, high-frequency data.