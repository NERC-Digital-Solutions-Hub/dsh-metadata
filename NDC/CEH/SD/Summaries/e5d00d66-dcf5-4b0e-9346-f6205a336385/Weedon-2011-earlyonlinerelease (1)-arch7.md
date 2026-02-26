# Creation of the WATCHForcing Data and its use to assess global and regional reference crop evaporation over land during the twentieth century

## Overview
- Presents the WATCH Forcing Data (WFD), a century-spanning, half-degree gridded meteorological forcing dataset for land surface and hydrological models.
- Enables assessment of external drivers of evaporation with sub-daily resolution and supports both global and regional analyses.
- Includes two temporal components:
  - 1958–2001: ERA-40-based forcing on a 0.5° grid.
  - 1901–1957: constructed by re-ordering ERA-40 data to preserve statistical characteristics, ensuring continuity with the 1958–2001 period.
- Provides global forcing variables (wind, temperature, humidity, pressure, radiation, rainfall, snowfall) across 67,420 land grid points, with 3-hourly radiation sampling and bias-corrected diurnal/seasonal consistency.

## Data structure and access
- Global forcing variables at 0.5° resolution: Wind (10 m), 2 m air temperature, surface pressure, 2 m specific humidity, downward longwave and shortwave radiation, rainfall rate, snowfall rate.
- Data density and coverage: Global land grid points defined by a land-sea mask; 3-hourly sampling for radiation-related terms; bias correction applied to ensure diurnal ranges align with observations where possible.
- Format and documentation: NetCDF with ALMA convention; publicly documented in the WATCH Technical Report; designed for GIS-based analyses and model intercomparison.

## Methodology and bias corrections
- 1958–2001 (ERA-40-based)
  - Spatial interpolation from ERA-40 to half-degree grid; elevation corrections for temperature, surface pressure, specific humidity, and longwave radiation.
  - Temperature bias correction using CRU monthly data; consistent diurnal ranges across the period.
  - Downward longwave radiation: no global bias correction relative to NASA SRB; validated against site data (e.g., FLUXNET).
  - Downward shortwave radiation: corrected monthly using CRU cloud cover and HadGEM2-A aerosol corrections; validated against FLUXNET.
  - Relative humidity and vapor pressure derived from corrected temperature, pressure, and specific humidity; cross-checked with CRU data.
  - Precipitation (rainfall and snowfall): six-step procedure to merge ERA-40 rainfall/snowfall with GPCCv4 and CRU wet-day data; rain/snow classification follows ERA-40 ratios; gauge-catch corrections applied; wet-day counts adjusted to maintain event coherence with CRU data.
  - Validation: good alignment with FLUXNET at monthly-to-daily scales for temperature, radiation, and precipitation; sub-daily precipitation patterns show larger uncertainties (typical for convective regimes).
- 1901–1957 (re-ordered ERA-40)
  - Years drawn randomly from ERA-40 with leap-year alignment to preserve long-term statistics; identical processing steps to maintain spatial coherence in frontal precipitation.
  - Acknowledges limitations due to sparse pre-1950 station coverage and reliance on climatologies in data-poor areas; potential biases in interannual variability.

## PET estimation and comparison
- Potential evapotranspiration (PET) estimated by two approaches:
  - PET_rc: Penman-Monteith for a reference crop (well-watered grass) with standardized surface and aerodynamic resistances.
  - PET_PT: Priestley-Taylor (simplified energy-driven formulation) for humid conditions.
- Inter-comparison: PET_PT often differs from PET_rc, sometimes by large amounts in arid regions; regional divergences influence model intercomparisons.

## Global and regional findings
- Global PET_rc trends (1958–2001)
  - Overall decline: approximately -0.51 mm/yr per year (1958–2001).
  - Substantial interannual variability; early periods featured higher vapor pressure deficit and temperatures, with later periods showing shifts in radiation, wind, and humidity.
  - 1901–1957 shows no significant global trend due to the randomized pre-1958 data and limited observational coverage.
- Global PET_pt trends
  - PET_PT shows local differences from PET_rc; regional disparities can exceed 1000 mm/yr in some basins, affecting model comparisons.
- Precipitation and moisture availability
  - No significant global trends in land precipitation (1958–2001), but regional patterns vary; some basins show declines (e.g., Congo, Niger), while others (Amazon) remain wet.
  - In arid basins, PET_rc generally exceeds precipitation, highlighting water-resource implications.
- Basin-scale focus and patterns
  - Eight large river basins examined (examples include Amazon, Congo, Niger, Murray-Darling, Lena, Ganges-Brahmaputra, Orange, etc.) exhibit:
    - PET_rc and PET_PT show regionally diverse trends across periods (1901–1957, 1958–2001, 1979–2001).
    - Net radiation and VPD exhibit notable shifts in several basins, influencing PET and water balance.
    - Precipitation and snowfall display contrasting trends by basin and period, underscoring regional heterogeneity.
  - Specific basin exemplars (based on Appendix data excerpts):
    - Orange River Basin: PET_rc and PET_PT trends vary by period; Net Rad and VPD show period-specific changes; rainfall and snowfall fluctuations noted.
    - Murray-Darling River Basin: PET_rc directional changes over periods; rainfall variability; net radiative flux and VPD adjustments observed.
    - Lena River Basin: PET_rc and PET_PT trends with modest changes; Net Rad and VPD show notable shifts; precipitation and snowfall exhibit regional signals.
    - Ganges-Brahmaputra River Basin: PET_rc declines in 1958–2001; PET_PT and precipitation trends indicate regional variability; VPD and wind show period-dependent changes.
- Data quality and limitations
  - Pre-1958 data are less reliable due to randomization and sparser observations; wind/pressure/humidity corrections applied primarily post-1958.
  - Validation shows robust agreement for temperature, radiation, and large-scale precipitation at monthly-to-seasonal scales; sub-daily precipitation remains challenging in convective regimes.
- Implications for GIS and data use
  - WFD provides a consistent, spatially coherent forcing dataset suitable for GIS-based hydrological and land-surface analyses, enabling map-based visualization of evaporation drivers and water balance across the century.
  - Users should consider regional biases and pre-1958 uncertainties; PET_rc and PET_PT offer complementary perspectives on evaporation potential.
  - The dataset supports scenario analyses and multi-model evaluations with documented uncertainty and validation.

## Practical guidance for GIS specialists
- Use the half-degree WFD to map PET_rc, PET_PT, precipitation, net radiation, VPD, wind, and snowfall across basins and regions for 1901–1957 and 1958–2001 (and 1979–2001 where available).
- Exercise caution when interpreting pre-1958 results; focus on robust regional patterns rather than global averages.
- Leverage PET_rc vs PET_PT comparisons to explore sensitivity of hydrological outputs to evaporation formulations.
- Integrate WFD with basin-specific validation data (e.g., FLUXNET, gauge observations) to contextualize model outputs and uncertainties.

## Concluding takeaway
- The WATCH Forcing Data provides a validated, century-spanning, bias-corrected forcing framework that enables robust GIS-based exploration of external drivers of evaporation and regional water balance, while emphasizing regional heterogeneity and data limitations inherent in early 20th-century observations.