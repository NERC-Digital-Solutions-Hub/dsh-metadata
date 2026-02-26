# Creation of the WATCHForcing Data and its use to assess global and regional reference crop evaporation over land during the twentieth century

- Overview
  - Presents the WATCH Forcing Data (WFD) framework to drive land surface models and general hydrological models for twentieth-century analysis.
  - Provides meteorological forcing data for 1958–2001 (high-quality, sub-daily resolution) and 1901–1957 (statistically preserved, but less precise historical event reproduction).

- Data structure and content
  - Global, half-degree grid (67,420 land points; Antarctic excluded).
  - Variables include: wind (10 m), 2 m air temperature, surface pressure, 2 m specific humidity, downward longwave and shortwave radiation, rainfall rate, snowfall rate, and related land-sea mask handling (CRU ALMA convention).
  - Temporal resolution: shortwave, rainfall, snowfall at 3-hourly; wind, temperature, pressure, humidity at 6-hourly, with interpolation to 3-hourly as needed.
  - Storage format: netCDF with CRU land-sea mask; designed for multi-model use and cross-system consistency.

- Forcing data: 1958–2001
  - Basis: ERA-40 reanalysis (1958–2001) with extensive bias, aerosol, cloud, and radiation adjustments.
  - Corrections implemented:
    - Elevation and bilinear regridding to 0.5-degree grid.
    - Temperature, pressure, humidity bias corrections using CRU observations.
    - Longwave and solar radiation corrections accounting for aerosols and cloud changes.
    - Downward shortwave radiation corrected for tropospheric/stratospheric aerosols using HadGEM2-A data and 20th-century aerosol optical depths; validated against satellite products and FLUXNET.
  - Radiation alignment:
    - Downward longwave radiation adjusted to ERA-40 baseline (no global bias after corrections).
    - Shortwave corrected via CRU cloud cover and aerosol loads; includes tropospheric cloud-aerosol interactions.
  - Precipitation corrections:
    - Six-step process: interpolation, rain/snow merging, wet-day corrections to CRU counts, monthly totals to GPCCv4, rain/snow reassignment by original ratio, gauge-catch corrections.
    - Wet-day correction preserves spatial coherence of large-scale events; handles tropical extremes and outliers with realism safeguards.
  - Validation and limits:
    - FLUXNET-based validation at seven sites shows good agreement for near-surface temperature, radiation, and moisture; precipitation and wind have limitations, especially sub-daily and in convective regimes.
    - Grid-box (WFD) vs. point-scale (FLUXNET) differences acknowledged.

- Forcing data: 1901–1957
  - Construction approach:
    - Pre-1958 years are synthesized by randomly selecting ERA-40 years and reassigning them year-by-year to preserve global statistics while avoiding timing errors at sites.
    - Leap-year alignment maintained; same processing steps as for 1958–2001.
  - Quality caveats:
    - Pre-1958 data do not capture historical interannual variability and trends as accurately as post-1958 data due to limited observations and randomization.

- Potential evapotranspiration (PET) estimation
  - Two approaches:
    - PET_rc (Penman–Monteith): energy balance plus VPD and aerodynamic properties for a reference crop (well-watered grass).
    - PET_PT (Priestley–Taylor): radiation- and humidity-driven alternative, especially in humid regions.
  - Both converted to comparable mm water-depth units for model comparison.
  - Purpose: enable assessment of how net radiation, VPD, wind, and temperature drive PET_rc versus PET_PT across basins and time.

- Global and regional evapotranspiration and precipitation findings
  - Global view (1958–2001):
    - PET_rc generally tracks regional climate drivers; large regional differences in basins.
    - PET_PT can diverge from PET_rc in local conditions, highlighting representation sensitivity.
  - Basin-scale results:
    - Amazon, Congo: PET_rc often lower, rainfall-driven outputs dominate; regional variability exists.
    - Niger, Murray–Darling: PET_rc can dominate over rainfall in some analyses; basin-specific trends vary.
    - Winds, net radiation, and VPD show regional variability that modulates PET_rc and PET_PT differently.
  - Precipitation trends:
    - No consistent global trend 1958–2001; regional changes observed (e.g., some basins with decreases or increases).
  - Examples for specific basins (selected highlights from Appendix data):
    - Orange River Basin: PET_rc averages around 1,500–1,600 mm/yr across periods with modest to positive trends; PET_PT around ~1,100 mm/yr; net radiation and VPD show modest increases over some periods; rainfall and precipitation show basin-dependent changes.
    - Murray–Darling Basin: PET_rc typically higher than PET_PT; precipitation shows regional variability with periods of increase and decrease; net radiation and VPD trends vary by sub-period.
    - Lena River Basin: PET_rc relatively stable with small increases in some periods; PET_PT shows modest growth; net radiation and VPD exhibit period-specific changes; precipitation trends show regional variability.
    - Ganges–Brahmaputra Basin: PET_rc and PET_PT show historically high values with notable declines in PET_rc in 1958–2001; precipitation and rainfall demonstrate significant interannual and long-term variability.
  - Appendix-level context:
    - Appendix tables provide basin-by-basin time series and trend statistics for PET_rc, PET_PT, Net Rad, VPD, Wind, Rainfall, Snowfall, and Precipitation across 1901–1957, 1958–2001, and 1979–2001, including averages, slopes, effective sample sizes (Neff), and significance of trends.

- Practical notes for data support and reuse
  - The data enable self-contained forcing for land surface and hydrological models, with comprehensive documentation of corrections (CRU bias corrections, GPCC/CRU wet-day adjustments, aerosol corrections, and land/ocean mask considerations).
  - PET estimation methods (PET_rc and PET_PT) are explicitly documented to support reproducibility and permitting user-adjustments.
  - Validation against FLUXNET provides a practical reference for expected performance and limitations across climate regimes and land-cover types.
  - Users should be aware of pre-1958 biases and the limits of interannual variability, especially for variables not bias-corrected due to data scarcity.
  - The dataset supports cross-model comparisons and robust analyses of twentieth-century changes in evaporation, soil moisture, and runoff across major basins.