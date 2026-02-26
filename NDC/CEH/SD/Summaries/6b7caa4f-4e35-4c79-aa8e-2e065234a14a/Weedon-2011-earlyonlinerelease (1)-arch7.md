# The WATCH Forcing Data 1958-2001: a meteorological forcing dataset for land surface- and hydrological-models.

- Purpose and scope
  - A gridded meteorological forcing dataset (WATCH Forcing Data, WFD) designed to drive land surface models (LSMs) and general hydrological models (GHMs) across the 20th century.
  - Provides full diurnal cycle, sub-daily forcing for LSMs and daily forcing for GHMs; supports analysis of external drivers of evaporation, soil moisture, and runoff.
  - Data are suitable for GIS-enabled analyses and map-based visualizations of forcing fields (wind, temperature, humidity, radiation, precipitation) at half-degree resolution.

- Data content and structure
  - Grid: half-degree latitude-longitude; roughly 67,420 land points; Antarctica excluded.
  - Variables: wind speed at 10 m, air temperature at 2 m, surface pressure, specific humidity at 2 m, downward longwave radiation, downward shortwave radiation, rainfall rate, snowfall rate.
  - Temporal resolution: 3-hourly for most variables (to capture diurnal and synoptic variability); some radiation/moisture fields at 6-hourly to optimize storage.
  - Time periods:
    - 1958-2001 (primary, bias-corrected dataset based on ERA-40 with additional corrections).
    - 1901-1957 (extension to earlier decades using re-ordered ERA-40 data while preserving diurnal/seasonal structure).

- Data generation, corrections and validation
  - Base data from ERA-40; elevation corrections applied after interpolation to the grid.
  - Temperature, pressure, humidity bias corrections using CRU observations and climatologies; humidity and pressure corrected consistently with temperature.
  - Radiation corrections:
    - Downward longwave: bias-corrected with ERA-40 consistency; no global SRB bias-correction required.
    - Downward shortwave: corrected monthly using CRU cloud data and aerosol corrections; includes direct/indirect aerosol effects and volcanic (AOD) adjustments.
  - Precipitation corrections:
    - Multi-step process to merge rain/snow, adjust wet-day frequency to CRU/GPCC, reallocate rain/snow using ERA-40-derived ratios, and apply gauge-catch corrections; emphasis on preserving coherent events and reducing spurious extremes.
  - Validation and interpretation:
    - Validated against FLUXNET sites for temperature, radiation, and humidity with generally good agreement; precipitation validation varies by site and timescale, often more challenging.
    - Spatial coherence of large-scale events maintained; sub-daily, convection-dominated precipitation may diverge at a grid-box level.

- Global and regional context
  - PET (rc) and PET (Priestley-Taylor) estimates included to assess potential evaporation under historical forcing.
  - Global trends (1958-2001): PET_rc shows a significant global decrease; VPD increases; net radiation and wind show global reductions; no single global trend for PET_rc when considering the full 1901-1957 window.
  - Basins and regions: regional differences in PET_rc, PET_PT, precipitation, and moisture balance; interpretations depend on local hydrology and data density.

- Basin-level perspectives (examples from the provided appendix data)
  - Orange River Basin
    - PET_rc and PET_PT values across intervals (1901-1957, 1958-2001, 1979-2001) show high potential evaporation in arid contexts with varying trends.
    - Net radiation and VPD indicate more energy-driven moisture balance in different periods; rainfall and snowfall patterns reflect regional climate variability.
  - Murray-Darling River Basin
    - PET_rc generally high in this region with notable long-term trends in some periods.
    - PET_PT and moisture variables show regionally varying responses; rainfall remains a major driver of hydrology with substantial interannual variability.
  - Lena River Basin
    - PET_rc and PET_PT values indicate humid to sub-Arctic conditions; rainfall is substantial, with snowfall contributing in winter months.
    - Net radiation and VPD show characteristic seasonal and decadal variation; moisture balance reflects high precipitation context.
  - Ganges-Brahmaputra River Basin
    - Very high rainfall regime; PET_rc and PET_PT reflect strong evaporative demand in humid conditions.
    - Net radiation and VPD exhibit regional variability; snowfall is minimal in many sub-basins but present in high-elevation areas.
  - Across basins, the appendix provides per-interval averages, slopes, and significance (p-values) for PET_rc, PET_PT, Net Rad, VPD, Wind, Rainfall, and Snowfall, illustrating regional and temporal trends.

- Usage notes for GIS specialists
  - Use WFD to create map-based representations of forcing fields (wind, temperature, humidity, radiation, precipitation) at 0.5-degree resolution with sub-daily detail for dynamic visualization and hydrological/land-surface modeling.
  - Exercise caution for pre-1958 signals; regional trends are more robust where station networks were denser and corrections more complete.
  - Enables cross-basin comparisons and spatially explicit assessments of potential evaporation drivers, evapotranspiration, and hydrological responses under historical climate conditions.

- Access and citation
  - The WATCH Forcing Data (WFD) is documented as WATCH Technical Report 22 and is available for land surface and hydrological modeling workflows.