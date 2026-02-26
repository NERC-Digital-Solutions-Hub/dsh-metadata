# (Hydro-PE HadUK-Grid) Supporting information

- The dataset provides gridded potential evapotranspiration (PET) and PET with interception correction (PETI) at 1 km resolution over the United Kingdom for 1969–2022.
- Derived from the HadUK-Grid meteorological dataset (v1.0.3.0 for 1969–2020, v1.1.0.0 for 2021, v1.2.0 for 2022).
- PET is calculated using the Penman–Monteith equation for a well-watered grass surface; PETI includes canopy interception corrections on days with precipitation. PET and PETI are in units of kg m^-2 d^-1 (equivalent to mm d^-1).
- PETI parameters are aligned with MORECS v2.0 parameterisations to ensure consistency with historical data (e.g., MORECS v2.0 documentation used for certain calculations).

1. Introduction and dataset evolution
- PET and PETI datasets cover 1969–2022 on a 1 km UK grid.
- 2022 data added; previous versions fixed minor errors identified in earlier releases.
- Known data quality notes and bug fixes:
  - Missing data previously occurred when wind speed interpolations produced zero values, causing divide-by-zero in PET; fixed by replacing 0 wind with the smallest non-zero daily wind value.
  - St Kilda data gaps (2009) fixed via linear time interpolation of monthly data.
  - PETI-specific issues: rare NaNs from drying-time calculations and negative interception rates; fixes ensure PETI=0 where appropriate.
- Input data are interpolated from HadUK-Grid onto the 1 km grid; the time series are kept contiguous when new years are appended.

2. Input data (2.1)
- Input dataset: HadUK-Grid v1.0.3.0 (1969–2020), v1.1.0.0 (2021), v1.2.0 (2022) on a 1 km UK grid.
- Variables used for PET and PETI:
  - Monthly mean vapour pressure (pv), monthly mean sea level pressure (psl), monthly total sunshine hours (Sun), daily 10 m wind speed (sfcWind), daily tasmax, tasmin.
- Variables used specifically for PETI:
  - Daily precipitation (rainfall)
- Ancillary data:
  - Surface altitude (EU-DEM v1.1), Ångström coefficients (a, b, c).
- Temporal handling:
  - Monthly data interpolated to daily with quadratic interpolation; monthly data represent the 15th of each month; daily values are then used for calculations.
- Temporal coverage and start times:
  - Dataset spans 1862–2022, but required inputs for PET/PETI begin in 1969.

3. Calculations and methods (2.2–2.3)
- Penman–Monteith calculation (2.2):
  - E_p (PET) calculated from daily mean temperature and daily interpolated values for other variables.
  - Daily mean temperature derived from tasmax and tasmin (with specific handling around day D and D+1 for multi-day averaging).
  - Several inputs derived from HadUK-Grid following MORECS v2.0 (net radiation, aerodynamic resistance, etc.), using parameters for a well-watered, short-grass surface.
  - Key derived quantities include specific humidity at saturation, air density, total net radiation, and aerodynamic/canopy resistances.
- Interception correction (2.3):
  - PETI applies interception correction on days with non-zero precipitation.
  - Canopy interception water (CI) calculated as a function of precipitation and leaf area index; interception evaporation rate (E_I) computed as open-water evaporation (r_s = 0).
  - PETI logic accounts for canopy drying and adjusts when precipitation ceases; in days with no precipitation, PETI equals PET.
  - In rare cases where PEI is negative or zero, corrections ensure PETI behaves consistently (e.g., PETI=0 when canopy does not dry, or when no interception occurs).

4. Interpolation details (2.4)
- Quadratic interpolation from monthly to daily resolution, with monthly timestamps treated as mid-month values.
- Handling of potential unphysical negative pv, sun, or sfcWind:
  - If pv or sun becomes negative, set to 0.
  - If sfcWind becomes negative, set to the minimum non-zero value observed in the daily interpolated wind dataset.
- To maintain consistency across dataset updates:
  - When adding new years, the last year of already interpolated daily data is held fixed, and interpolation is performed on the combined old daily data and new monthly data, preserving continuity and reducing end-of-timeseries changes.

5. File format and data structure
- Data are stored in netCDF format, CF Metadata Conventions v1.8 and ACDD v1-3.
- Data are organized as monthly files, one file per variable.
- File naming follows a year-month convention (structure details provided but partially garbled in the text).
- Spatial structure:
  - 1 km resolution, aligned to the British National Grid (EPSG:27700); WGS84 lat/lon provided (EPSG:4326).
  - Note: ArcGIS may offset projected-coordinate files due to datum assumptions; adjust layers accordingly.
- Temporal information:
  - Daily mean values from 1969-01-01 to 2022-12-31.
  - Monthly inputs are interpreted as mid-month timestamps for daily calculations.

6. Spatial and temporal information details
- Spatial: 1 km grid over Great Britain, EPSG:27700; includes latitude/longitude in WGS84 (EPSG:4326).
- Time: Daily data for 1969-01-01 to 2022-12-31; monthly data anchored to mid-month during interpolation.

7. Acknowledgements and references
- Supported by Natural Environment Research Council (NERC) awards NE/S017380/1 and NE/X019063/1 as part of the Hydro-JULES programme.
- Key references include MORECS v2.0, HadUK-Grid developments, and foundational hydrological/evapotranspiration literature (e.g., Brutsaert 1975; Linacre 1968; Richards 1971).