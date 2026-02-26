Hydro-PE HadUK-Grid Supporting information

- Purpose and product
  - Provides gridded daily potential evapotranspiration (PET) and PET with interception correction (PETI) over the UK at 1 km resolution (1969–2022).
  - PET: Penman–Monteith calculation for a well-watered grass surface.
  - PETI: PET plus interception correction on days with precipitation; designed to be consistent with MORECS v2.0 observations.
  - Units: kg m-2 d-1 (equivalent to mm d-1).

- Data origin and scope
  - Derived from the HadUK-Grid meteorological dataset (v1.0.3.0 for 1969–2020; v1.1.0.0 for 2021; v1.2.0 for 2022).
  - No differences between older and newer HadUK-Grid versions for the PET/PETI variables in overlapping periods.
  - Spatial grid: 1 km resolution aligned to the British National Grid (EPSG:27700); WGS84 coordinates also provided (EPSG:4326).

- Temporal coverage and time handling
  - Daily mean values from 1969-01-01 to 2022-12-31.
  - Monthly inputs interpolated to daily using quadratic interpolation; monthly values treated as representing the 15th of each month.
  - Interpolation preserves continuity when new years are added; the end of the old timeseries is kept intact to avoid inconsistencies.

- Input data and variables used
  - Required HadUK-Grid inputs (1969–2020 or 2021–2022 depending on year):
    - pv (monthly mean water vapour pressure, hPa)
    - psl (monthly mean sea level pressure, hPa)
    - sun (monthly total sunshine hours)
    - sfcWind (monthly mean wind speed at 10 m, m s-1)
    - tasmax (daily max temperature, °C)
    - tasmin (daily min temperature, °C)
  - For PETI additionally:
    - P (daily precipitation, mm d-1)
  - Ancillary data:
    - Surface altitude (EU-DEM v1.1)
    - Ångström coefficients a, b, c
  - Calculations require surface air pressure at grid box altitude p*, converted to Pa.

- Calculation methodology
  - PET: Penman–Monteith formulation parameterised for grass, using daily mean temperature and daily interpolated values for other inputs.
  - Net radiation: sum of net shortwave and net longwave, derived from sunshine hours, temperature and vapour pressure using MORECS v2.0 relationships.
  - Aerodynamic resistance and canopy/ stomatal resistances derived from wind, leaf area index, and MORECS v2.0 parameterisations.
  - Temperature inputs: daily mean temperature computed from tasmax and tasmin (special handling around month/month+1 to align rainfall timespan).
  - Key references and parameterisations pulled from MORECS v2.0 to ensure historical consistency.

- Interception correction (PETI)
  - On days with precipitation, compute canopy interception (CI) and canopy evaporation (EI).
  - EI used to adjust PET when interception occurs; CI is enhanced in spring/summer/autumn to account for multiple events per day.
  - PETI calculation follows MORECS v2.0 logic, including handling of zero or negative interception scenarios to avoid spurious PETI values.

- Data quality, gaps, and fixes
  - Several fixes implemented:
    - Zero wind speed initially caused NaNs in PET/PETI; fixed by raising 0 wind to the minimum non-zero daily wind.
    - St Kilda data gaps addressed by linear interpolation of monthly data to daily.
    - PETI-specific bugs: handling when canopy drying time or interception rate yields NaN or incorrect signs; fixes implemented to ensure PETI consistency.
  - Ongoing data management includes ensuring data quality at source, with explicit notes on minor bug impacts (generally small).

- Interpolation details and data integrity
  - Quadratic interpolation of monthly data to daily avoids abrupt transitions but can create small unphysical negatives in pv, sun, or sfcWind; negatives are corrected (pv/sun to 0; sfcWind set to the minimum non-zero value observed).
  - When updating with new HadUK-Grid years, the interpolation is applied to the combined series to preserve end-of-old-series continuity and maintain consistency.

- File format and documentation
  - Data distributed as netCDF files (CF Metadata Conventions v1.8; ACDD v1-3).
  - Daily mean values, 1969-01-01 to 2022-12-31.
  - Spatial grid: 1 km, EPSG:27700; WGS84 coordinates provided as well.
  - ArcGIS caveat: projected CF coordinates may display offset due to datum assumptions; adjust layers if using ArcGIS.

- Practical considerations for monitoring frameworks
  - Provides a policy-relevant hydrological proxy ( PET / PETI ) with clear methodology and lineage to MORECS, enabling temporal and spatial monitoring of evapotranspiration demand under UK conditions.
  - Open data format and CF-compliant metadata facilitate integration into dashboards, reports, and governance processes.
  - Versioning strategy ensures backward compatibility and coherent updates as HadUK-Grid data are extended; clear handling to avoid reprocessing and inconsistencies.
  - Data governance considerations: clear data provenance, documented calculations, and explicit notes on data quality and known issues support transparency and reproducibility; readiness for data sharing and governance in line with monitoring framework requirements.

- Acknowledgements and references
  - Supported by Natural Environment Research Council (NE/S017380/1; NE/X019063/1) as part of the Hydro-JULES programme.
  - Key methodological references include MORECS v2.0, Brutsaert (long-wave radiation), Linacre (net radiation), and Richards (saturation humidity).

- End-user guidance
  - Use PET for baseline evapotranspiration demand; use PETI where canopy interception is relevant on precipitation days.
  - Leverage the 1 km resolution for high-resolution regional monitoring; combine with ancillary data (e.g., land cover, soil moisture) for policy analyses.
  - Be mindful of ArcGIS datum caveats and interpolation-induced edge effects when interpreting time series or comparing across versions.