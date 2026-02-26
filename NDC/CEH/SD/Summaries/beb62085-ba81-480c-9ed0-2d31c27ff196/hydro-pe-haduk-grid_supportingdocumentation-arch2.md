# (Hydro-PE HadUK-Grid) Supporting information

- Provides gridded daily potential evapotranspiration (PET) and PET with interception correction (PETI) at 1 km resolution over the United Kingdom for 1969–2022.
- Derived from the HadUK-Grid meteorological dataset; two output variables:
  - PET (kg m-2 d-1), representing potential evapotranspiration for a well-watered grass surface.
  - PETI (kg m-2 d-1), PET with interception correction for canopy interception on days with precipitation.
- PETI is designed to be consistent with the MORECS v2.0 observation-based framework.

## Data scope and outputs

- Daily mean PET and PETI in kg m-2 d-1 (equivalent to mm d-1).
- Intended for hydrological modelling in the UK; aligns with past MORECS methodology and parameterisations for a grass surface.
- Time span: daily values from 1969-01-01 to 2022-12-31.
- Spatial grid: 1 km resolution, aligned to British National Grid (EPSG:27700); WGS84 coordinates provided as well.
- File structure: netCDF files (CF v1.8, ACDD v1-3); daily values with monthly-to-daily interpolation.

## Data versions and updates

- HadUK-Grid input versions:
  - 1969–2020: HadUK-Grid v1.0.3.0
  - 2021: HadUK-Grid v1.1.0.0
  - 2022: HadUK-Grid v1.2.0
- PET and PETI calculations for 1969–2020 are consistent across v1.0.3.0, v1.1.0.0, and v1.2.0; 2021 differs only where applicable to the new input year, and 2022 adds data.
- Interpolation to daily time-step uses quadratic interpolation; continuity preserved when updating with new yearly data by concatenating the old daily series with new monthly data and re-interpolating the new segment only.
- Data quality fixes:
  - Resolved NaNs caused by zero wind speeds during daily interpolation.
  - Fixed missing data for 2009 (St Kilda) by linear interpolation of monthly data.
  - PETI-specific bugs addressed (handling of negative PEI and zero PEI cases); overall impact deemed minor.

## Methods

- PET calculation:
  - Penman-Monteith equation for a well-watered grass surface.
  - Daily mean temperature used; other inputs interpolated from monthly means.
  - Inputs derived from HadUK-Grid and ancillary data (altitude, Ångström coefficients, etc.).
  - Net radiation computed from net shortwave and net longwave radiation using relationships from MORECS v2.0; surface temperature approximated from air temperature.
  - Aerodynamic resistance and canopy resistance computed following MORECS v2.0 methodology.
- Interception correction (PETI):
  - On days with rainfall, interception water CI is calculated via canopy interception models; E_I (evaporation from intercepted water) is estimated as open-water-like, then PETI transitions back to PET once canopy is dry.
  - Interception correction enhanced in spring, summer, autumn to account for multiple precipitation events per day.
- Interpolation details:
  - Monthly values interpolated to daily using quadratic interpolation, assuming mid-month timestamps.
  - To avoid introducing unphysical negative pv (vapor pressure) or sun values, pv and sun set to zero when negative; sfcWind set to the minimum non-zero value observed in the daily dataset.
  - Extrapolation at ends is managed by using a mid-month assumption, with precautions for continuity when updating with new years.

## Data structure and format

- Files: netCDF format, CF metadata compliant; data stored in monthly files per variable.
- Spatial information:
  - Grid: 1 km, British National Grid (EPSG:27700).
  - Projection coordinates in metres; latitude/longitude also provided in WGS84 (EPSG:4326).
  - Noted ArcGIS datum offset issue when reading non-WGS84 CF-projected files; adjustment may be needed for precise alignment.
- Time information:
  - Daily means from 1969-01-01 to 2022-12-31.
  - Monthly data interpolated to daily with a mid-month timestamp assumption.

## Quality, caveats, and usage considerations

- Dataset designed to support environmental monitoring and hydrological modelling; compatible with established MORECS parameterisations for comparability.
- Updates to incorporate new HadUK-Grid years are done in a way to preserve the integrity of the existing daily record while extending the time series.
- Users should be aware of interpolation choices and the handling of potential end-of-series extrapolation for older data when newer years are added.
- Minor, documented data corrections were applied to improve data integrity; overall impact of corrections is small.

## Access and usage considerations for Analysts Monitoring the Environment

- Data provenance: clearly links PET/PETI to HadUK-Grid inputs and MORECS-based parameterisations, with explicit version history and update protocol.
- Reusability: standardized 1 km gridded outputs suitable for broad environmental monitoring tasks, trend analysis, and policy performance assessment.
- Data accessibility: netCDF CF-conformant files designed for integration into standard analytical workflows; updates append new years to existing series to maintain continuity.

## Acknowledgements

- Supported by Natural Environment Research Council under specific grant awards as part of the Hydro-JULES programme.