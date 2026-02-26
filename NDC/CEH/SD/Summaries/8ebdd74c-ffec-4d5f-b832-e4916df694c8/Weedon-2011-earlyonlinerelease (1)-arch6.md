# Creation of the WATCHForcing Data and its use to assess global and regional reference crop evaporation over land during the twentieth century.

- Purpose and scope
  - Describes the creation of the WATCH Forcing Data (WFD) at 0.5° resolution to drive land surface models (LSMs) and general hydrological models (GHMs) across the twentieth century.
  - Provides meteorological forcing for sub-daily (LSMs) and daily (GHMs) simulations to enable consistent assessment of external drivers of evaporation.
  - Covers two time spans: 1958-2001 (robust observations) and 1901-1957 (constructed to match 1958-2001 properties).

- Data architecture and variables
  - Global 0.5° grid (land points) with eight forcing variables:
    - Wind speed at 10 m, air temperature at 2 m, surface pressure, specific humidity at 2 m
    - Downward longwave radiation, downward shortwave radiation
    - Rainfall rate, snowfall rate
  - Temporal resolution:
    - 3-hourly for radiation and precipitation
    - 6-hourly for wind, temperature, humidity, and longwave radiation (interpolated to 3-hourly as needed)

- 1958-2001 WATCH Forcing Data (WFD)
  - Basis and corrections
    - ERA-40 surface variables form core dataset; bilinear interpolation from 1° to 0.5°; elevation corrections applied stepwise to temperature, pressure, humidity.
    - Monthly 2 m temperature bias-corrected against CRU observations; other variables corrected via inter-variable consistency checks.
    - Downward longwave radiation minimally adjusted; downward shortwave corrected for aerosol and cloud effects using HadGEM2-A AOD and CRU cloud data.
    - Aerosol corrections account for tropospheric/stratospheric aerosols and volcanic aerosols in clear and cloudy skies.
  - Precipitation processing (wet-day correction)
    - Refines ERA-40 precipitation to preserve spatial coherence of heavy events and reconciles rain/snow with CRU and GPCC data.
    - Monthly adjustments ensure consistency with gauge data, preserving event structure.
  - Validation and interpretation
    - Fluxnet-based validation shows strong matches for temperature and radiation terms; precipitation more variable due to footprint differences.
    - Generally good agreement at monthly and longer timescales; limitations at sub-daily scales, especially for precipitation and convection.

- 1901-1957 WATCH Forcing Data (WFD)
  - Rationale and method
    - Extends forcing back to 1901-1957 by re-ordering ERA-40 years to preserve diurnal-to-seasonal statistics and autocorrelation of 1958-2001.
    - Ensures spatial coherence of frontal rainfall at basin scale.
  - Limitations
    - No global bias corrections for pre-1958 winds, pressure, humidity, or downward longwave radiation; precipitation adjustments rely on CRU/GPCC with sparser station coverage, risking biases and reduced interannual variability.
    - Some under-representation of interannual/decadal variability due to limited early observations.

- Estimation of reference crop evaporation (PET)
  - PET_rc (Penman–Monteith) for a well-watered reference crop
    - Fixed surface resistance rs = 70 s/m; aerodynamic resistance ra = 208/u2 (u2 from 2 m wind).
    - Incorporates net radiation, vapor pressure deficit (VPD), and aerodynamic factors.
  - PET_PT (Priestley–Taylor)
    - PET_PT = alpha * Δ/(Δ+γ) * A with alpha ≈ 1.26 and A = net available energy.
  - Comparison and interpretation
    - PET_pt often higher in humid regions; substantial regional differences with PET_rc vs PET_PT.
    - Global trends (1958-2001): PET_rc declines globally (about 0.5 mm/yr); PET_PT shows larger, regionally varying differences.
    - Interannual variability of PET_rc is substantial and correlated with VPD.

- Global and regional findings (context for data users)
  - Global scale
    - Precipitation shows no significant global trend (1958-2001); PET_rc declines with notable regional variability; VPD and net radiation show regional changes that influence PET dynamics.
  - Basins and regional patterns (examples)
    - Large basins (e.g., Amazon, Congo, Niger, Murray-Darling, Ganges-Brahmaputra, Lena, Orange) exhibit basin-specific PET_rc vs PET_PT relationships and different temporal trends in PET, precipitation, net radiation, and VPD.
    - Some basins show increasing PET_PT or PET_rc in certain subperiods, others show declines; magnitudes and sign vary by region and period.
  - Representative data by period
    - The document tabulates PET_rc, PET_PT, Net Rad, VPD, Wind, Rainfall, Snowfall, and Precipitation by basin across 1901-1957, 1958-2001, and 1979-2001, with averages, slopes, and significance indicators, highlighting heterogeneous trends across regions.

- Validation, quality, and caveats
  - Validation against Fluxnet data supports reliability for temperature and radiation terms; moisture variables are acceptable but precipitation remains challenging at finer timescales.
  - Strengths: preserves diurnal cycles and covariance structure, suitable for hydrological modeling and climate impact assessments.
  - Limitations: potential biases in early ERA-40 years, sparse observations before 1950, uncertainties in aerosol/cloud corrections in some regions, and tropical precipitation adjustments.

- Practical implications for data support work
  - The WATCHForcing Data set provides a robust, well-documented forcing and PET data source for end-users building dashboards, analyses, and data products related to long-term hydrology and evapotranspiration across the twentieth century.
  - Enables self-service exploration of external drivers of evaporation, regional hydrological responses, and comparisons between PET_rc and PET_PT across epochs and regions.
  - Users should be mindful of period-specific uncertainties (notably pre-1958 data and tropical precipitation adjustments) and the differences between PET_rc and PET_PT when interpreting PET trends.

- Appendix notes (context for data consumers)
  - Appendix includes the order of ERA-40 basis years and an extensive basin-by-basin set of statistics (e.g., Orange River, Lena, Murray-Darling, Ganges-Brahmaputra) for PET_rc, PET_PT, Net Rad, VPD, Wind, Rainfall, Snowfall, and Precipitation across multiple intervals, with averages, slopes, Neff, and significance indicators.