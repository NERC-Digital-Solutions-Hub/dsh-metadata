(Hydro-PE HadUK-Grid) Supporting information

# Overview

- Presents gridded daily potential evapotranspiration (PET) and PET with interception correction (PETI) at 1 km resolution across the UK for 1969–2022.
- Derived from the HadUK-Grid meteorological dataset (v1.0.3.0 for 1969–2020, v1.1.0.0 for 2021, v1.2.0 for 2022).
- PET uses Penman-Monteith parameterised for a well-watered grass surface; PETI includes interception by vegetation on precipitation days.
- PET and PETI values are in kg m^-2 d^-1 (equivalent to mm d^-1).
- PETI calculations are designed to be consistent with MORECS v2.0 observations; parameterisations follow MORECS documentation where applicable.

# 1 Introduction (key points)

- Dataset intended for hydrological modelling and UK-scale analysis; PETI aligns with historical evapotranspiration approaches (MORECS v2.0).
- Latest version adds 2022 data and fixes minor errors found in earlier versions.
- Documented data quality fixes address specific interpolation and canopy interception calculation issues (described in detail in section 2.4 and 2.3).

# 2 Input data (what goes in)

- HadUK-Grid input: v1.0.3.0 (1969–2020), v1.1.0.0 (2021), v1.2.0 (2022) on a 1 km UK grid.
- Data are interpolated from meteorological stations onto land points of a uniform grid; timeseries span 1862–2022 (start year depends on variable/resolution).
- Required variables (monthly) used in PET computations: pv (vapour pressure), psl (sea level pressure), sun (sunshine hours), sfcWind (10 m wind), tasmax (daily max temp), tasmin (daily min temp).
- PETI additionally requires daily precipitation (P).
- Ancillary data: surface altitude (EU-DEM v1.1), Ångström coefficients (a, b, c).
- Monthly data are quadratically interpolated to daily time steps; the interpolation preserves contiguity across updates to avoid inconsistencies.

# 3 Penman–Monteith calculation (how PET is computed)

- PET (Ep) calculated with the Penman–Monteith equation, using daily mean temperature and daily interpolated values for other inputs.
- Temperature inputs: daily mean temperature derived from tasmax and tasmin; specific humidity, air density, net radiation, and other terms computed from HadUK-Grid variables following MORECS v2.0 methodologies.
- Parameters chosen for a well-watered short-grass surface; includes canopy resistance, aerodynamic resistance, stomatal resistance, and surface heat flux considerations.
- Net radiation calculated from net shortwave and net longwave radiation using radiation relationships consistent with MORECS v2.0.
- Several derived quantities (specific humidity at saturation, air density, etc.) are functions of input temperature and pressure.

# 4 Interception correction (how PETI is adjusted)

- On days with no precipitation, PETI equals PET.
- On days with precipitation > 0, interception CI and evaporation EI are estimated; canopy interception water evaporates faster than transpiration, requiring correction.
- EI is computed assuming open-water evaporation by setting canopy resistance r_s to zero; canopy dries and EI reduces until the canopy is dry, after which PETI returns toward PET with interception accounted for.
- The correction framework follows MORECS v2.0 and treats all precipitation as rainfall (not distinguishing rainfall vs. snowfall in interception dynamics).

# 5 Interpolation details (how daily values are created)

- Quadratic interpolation is used to convert monthly values to daily values; months are treated as representing the 15th day, with extrapolation at ends.
- To prevent unphysical negative pv, sun, or sfcWind after interpolation, pv and sun set to zero when negative, and sfcWind set to the minimum non-zero value observed in the daily interpolated series.
- When new years are added, the end of the existing daily series is preserved; interpolation is performed on the combined old-end plus new monthly data to maintain consistency and contiguity (end-of-old-timespan data may be extrapolated).

# 6 File format (how data are stored)

- Data are distributed as netCDF files, CF v1.8 and ACDD v1.3 compliant.
- Daily mean values are stored; data are organized in monthly files per variable.
- File naming structure is described in the documentation (note: there is a reference to a structure in the document, but exact naming is not reproduced here).
- Spatial grids: 1 km resolution, aligned to the British National Grid (BNG) with EPSG:27700; lat/lon provided in EPSG:4326.

# 7 Spatial information (where)

- 1 km UK grid (BNG), EPSG:27700; coordinates in metres.
- ArcGIS caveat: reading projected CF files in ArcGIS may offset layers by ~10–100 m due to datum assumptions; adjust layers accordingly.

# 8 Time information (when)

- Daily mean values from 1969-01-01 to 2022-12-31.
- Monthly inputs interpolated to daily with a mid-month timestamp assumption.

# 9 Acknowledgements

- Supported by Natural Environment Research Council (NERC) awards NE/S017380/1 and NE/X019063/1 as part of the Hydro-JULES programme.

# 10 References (context and sources)

- MORECS v2.0 methodology and documentation for PET calculation and related radiation, canopy, and aerodynamic concepts.
- HadUK-Grid project and methods for gridded UK climate observations.
- Supporting literature for net radiation, longwave/radiation adjustments, and interpolation approaches used in the dataset.