# (Hydro-PE HadUK-Grid) Supporting information

## Introduction
- Provides gridded daily potential evapotranspiration datasets (PET and PETI) at 1 km resolution across the UK for 1969–2022.
- PET (kg m-2 d-1) is calculated with Penman-Monteith for a well-watered grass surface.
- PETI (kg m-2 d-1) adds interception correction on days with non-zero precipitation to account for canopy interception evaporation.
- PET and PETI are designed for hydrological modelling and to be consistent with MORECS v2.0 observations.
- Latest version includes 2022 data and fixes minor data issues identified in earlier versions.
- Previous issues corrected: zero-wind interpolation NaNs, St Kilda data gaps (2009), and minor PETI calculation bugs; impacts considered minor.

## 2 Data and methods
### 2.1 Input data
- HadUK-Grid input data at 1 km: monthly means of pv (vapour pressure), psl (sea-level pressure), sun (sunshine hours), sfcWind (wind speed at 10 m), tasmax (daily max temp), tasmin (daily min temp).
- PETI additionally uses daily precipitation (P).
- Ancillary data: surface altitude (EU-DEM v1.1) and Ångström coefficients (a, b, c).
- Time span: HadUK-Grid data from 1862 to 2022; required variables available from 1969 onward.
- Data are interpolated from monthly to daily (quadratic interpolation) before calculations.

### 2.2 Penman–Monteith calculation
- PET computed daily from daily mean temperature and interpolated daily values of other inputs.
- Daily mean temperature derived by averaging tasmax and tasmin; for all days except the last, tasmin on day D and tasmax on day D+1 are used.
- Physical constants and parameterisations aligned with MORECS v2.0 to ensure consistency (well-watered short grass).
- Derived quantities include specific humidity, air density, net radiation (shortwave + longwave from sunshine, temperature and vapour pressure), aerodynamic resistance, and canopy-related resistances.
- Unit conversions and pressure adjustments are applied to align with surface altitude.

### 2.3 Interception correction
- On days with rainfall, PETI is less than or equal to PET by accounting for canopy interception water (CI) and canopy evaporation (EI).
- CI increases with precipitation and leaf area index; EI is computed assuming open-water evaporation (rs = 0) and continues until canopy is dry, after which PETI reverts toward PET.
- Special handling ensures valid PETI values when interception dynamics are extreme or PEI (potential interception) is negative.

### 2.4 Interpolation details
- Quadratic interpolation is used to daily values from monthly data, treating the 15th of each month as representative.
- Rare unphysical negatives for pv or sun are corrected to zero; wind speed negative adjustments use the minimum non-zero daily wind value to avoid division-by-zero in PET calculations.
- To avoid inconsistencies when new yearly data are added, the last year of existing daily data is combined with new monthly data and interpolated anew, preserving continuity but allowing the end-of-old-timespan data to remain extrapolated.

## 3 File format
### 3.1 Spatial information
- Data stored as netCDF files (CF v1.8, ACDD v1.3); daily means, one file per variable, at 1 km grid aligned to British National Grid (EPSG:27700).
- Latitude/longitude are also provided in WGS84 (EPSG:4326).
- Note: ArcGIS reading can offset layers if the datum differs from WGS84; adjust layers accordingly.

### 3.2 Time information
- Daily mean values from 1969-01-01 to 2022-12-31; monthly variables interpolated to daily with mid-month timestamps.

## 4 Acknowledgements
- Funded by Natural Environment Research Council (NE/S017380/1 and NE/X019063/1) as part of the Hydro-JULES programme.

## 5 References
- References to MORECS v2.0, HadUK-Grid, EU-DEM, and foundational radiation/evapotranspiration literature informing the methodology.