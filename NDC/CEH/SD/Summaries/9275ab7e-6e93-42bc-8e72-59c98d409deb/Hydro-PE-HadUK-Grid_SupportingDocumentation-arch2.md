# Potential evapotranspiration derived from HadUK-Grid 1km gridded climate observations 1969-2021 (Hydro-PE HadUK-Grid) Supporting information

- What this dataset contains
  - Gridded potential evapotranspiration (PET) and PET with interception correction (PETI) at 1 km resolution across the United Kingdom for 1969–2021.
  - PET calculated using Penman-Monteith for a well-watered grass surface; PETI adds interception correction on days with precipitation.
  - Two variables: daily total PET (kg m-2 d-1, equivalent to mm d-1) and daily total PETI (kg m-2 d-1).

- Data origin and purpose
  - Derived from the HadUK-Grid meteorological dataset (v1.0.3.0 for 1969–2020; v1.1.0.0 for 2021; no differences for 1969–2020 between versions).
  - Developed for hydrological modelling in the UK; PETI aligned with MORECS v2.0 documentation.

- Input data and ancillary information
  - HadUK-Grid input data on a 1 km UK grid:
    - Monthly mean water vapour pressure (pv), monthly mean sea level pressure (psl), monthly total sunshine hours (sun), monthly mean wind speed at 10 m (u10),
    - Daily max/min air temperatures (tasmax, tasmin),
    - Daily precipitation (P) for PETI calculations.
  - Ancillary data: surface altitude (EU-DEM v1.1) and Ångström coefficients (a, b, c).
  - Monthly data are interpolated to daily time steps using quadratic interpolation to produce daily PET/PETI values.

- Calculation details
  - PET calculation
    - Penman-Monteith equation parameterised for a well-watered grass surface.
    - Daily mean temperature derived from tasmax and tasmin (with specific handling around day boundaries for consistency with rainfall timespan).
    - Net radiation assembled from net shortwave and net longwave radiation using relationships from MORECS v2.0; canopy and aerodynamic resistances derived as in MORECS v2.0.
  - PETI calculation
    - On days with rainfall, interception by the canopy is considered; interception water CI and evaporation from canopy EI are computed, with a spring–summer–autumn enhancement (up to factor 2) for multiple events in a day.
    - PETI is PET adjusted by canopy interception, following the MORECS v2.0 approach.
  - Parameter consistency
    - Parameters tied to a well-watered short grass surface; several inputs derived to match MORECS v2.0 documentation.

- Interpolation and time handling
  - Monthly variables are quadratically interpolated to daily values, using mid-month timestamps.
  - To prevent inconsistencies when adding new years, the last year of already-interpolated daily data is held fixed while new monthly data are interpolated into a contiguous series.

- File format and spatial/time information
  - Output format: NetCDF (CF v1.8) with AC DD v1-3 conventions; daily mean values stored in monthly files per variable.
  - Spatial grid: 1 km resolution aligned to the British National Grid (EPSG:27700); WGS84 coordinates (EPSG:4326) provided.
  - Time coverage: daily values from 1969-01-01 to 2021-12-31; monthly timestamps assumed at mid-month during interpolation.

- Known caveats and considerations
  - Potentially unphysical negative pv or sun values due to quadratic interpolation; such values are set to zero.
  - End-of-time-series extrapolation adjustments may cause small discontinuities when new years are appended.
  - There is a known ArcGIS reading offset when CF-compliant files reference a non-WGS84 datum; adjust layers in ArcGIS accordingly.

- Access, usage, and acknowledgements
  - Data are intended for hydrological modelling and environmental monitoring; designed to be compatible with standard datasets and modelling frameworks.
  - Acknowledged support from Natural Environment Research Council (NE/S017380/1) as part of the Hydro-JULES programme.

- References (key sources)
  - MORECS v2.0 documentation and methodology.
  - HadUK-Grid data documentation.
  - Foundational works on radiation and evapotranspiration modelling (Brutsaert 1975; Linacre 1968; Richards 1971; etc.).