# Creation of the WATCHForcing Data and its use to assess global and regional reference crop evaporation over land during the twentieth century

## Overview
- Provides a consistent, bias-corrected forcing dataset (WATCH Forcing Data, WFD) at 0.5° resolution to drive land surface models and hydrological models across the 20th century.
- Data production split into two periods:
  - 1958–2001: WFD based on ERA-40 reanalysis, bias-corrected and adjusted to reproduce sub-daily diurnal cycles.
  - 1901–1957: WFD constructed by re-ordering ERA-40 data year-by-year to preserve diurnal-to-monthly variability and intervariable covariances with corrections.
- Aims to quantify external drivers of evaporation and related hydrological variables, enabling assessment of environmental health and policy performance over time.

## Data content and forcing data
- Variables (half-degree grid, 6-hourly for some, 3-hourly interpolation): 
  - 10 m wind speed, 2 m temperature, surface pressure, 2 m specific humidity
  - Downward longwave radiation, downward shortwave radiation
  - Rainfall rate, snowfall rate
- Spatial coverage: land points (Antarctica excluded); CRU land-sea mask; 0.5° grid.
- Temporal treatment:
  - 1958–2001: 3-hourly shortwave/longwave and precipitation; 6-hourly for other variables with 3-hour interpolation.
  - 1901–1957: year-by-year data construction to preserve temporal structure and covariances.
- Diurnal-to-subdaily variability preserved; data intended to support robust hydrological interpretation.

## Methodological advances, corrections, and data quality
- Elevation corrections applied sequentially to temperature, surface pressure, humidity, and longwave radiation.
- Bias corrections for ERA-40 temperature using CRU observations, including diurnal range adjustments.
- Shortwave radiation corrected for aerosols (HadGEM2-A) and volcanic aerosols; downwelling shortwave adjusted via CRU cloud data and ERA-40 cloud relationships; validation against SRB/FLUXNET where possible.
- Precipitation adjustments:
  - Interpolation to half-degree grid; wet-day counts aligned to CRU TS2.1; monthly totals corrected to GPCCv4.
  - Rain/snow partitioning preserved from ERA-40; gauge corrections applied; maintained coherence of frontal events for daily-scale hydrology.
- Transition management:
  - Year-end discontinuities removed via ramping for select variables (e.g., wind, temperature, pressure, longwave) between 1902–1957 and the 1958 transition.
- Pre-1958 data have greater limitations due to sparse observations and partial bias corrections.
- Data-generation steps and uncertainties highlighted for analysts.

## PET estimation methods
- Reference crop evapotranspiration (PET_rc) computed with Penman–Monteith for a well-watered grass reference crop (fixed stomatal/aerodynamic resistances).
- PET_PT (Priestley–Taylor) applied in humid regions (α = 1.26), as a regional alternative.
- Inter-comparisons illustrate regional differences and help explain variability across GHMs and LSMs.

## Global and regional findings
- Global (1958–2001):
  - PET_rc shows a statistically significant global decrease (approx. -0.51 mm/yr per year).
  - Associated drivers: increases in vapor pressure deficit (VPD), decreases in net radiation and wind speed, and rising 2 m air temperature.
  - 1901–1957 trends are weaker or not globally consistent due to early-period data limitations.
- Regional patterns:
  - Basin-scale variations in PET_rc, with some basins (e.g., Niger, Murray–Darling) showing notable decreases or complex behavior linked to moisture and radiation changes.
  - Humid basins (e.g., Amazon) often show rainfall exceeding PET_rc; other arid basins show strong PET_rc–moisture coupling.
  - Precipitation over land shows no uniform global trend 1958–2001, but regional changes exist (some basins decline, others stable).
- Variability and diurnal patterns:
  - The dataset preserves diurnal-to-submonthly variability, enabling more realistic interpretation of hydrological responses than purely daily methods.
- Validation and uncertainty:
  - Validation with FluxNET generally good for temperature, radiation, wind, and humidity at monthly-to-sub-monthly scales.
  - Precipitation validation more challenging due to gauge sparseness and footprint differences.
  - Early-century data (pre-1958) carry more uncertainty due to observation density and partial bias correction.
  - Some early 20th-century PET_rc trends may be influenced by data-generation methods and climatology substitutions in data-poor regions.

## Regional basins (selected highlights)
- Orange River Basin: PET_rc and PET_PT trends across 1901–1957, 1958–2001, and 1979–2001 show varying magnitudes and directions; net radiation and VPD changes accompany PET trends.
- Murray–Darling Basin: PET_rc and PET_PT exhibit notable interval changes; moisture and radiative drivers influence basin-scale trends.
- Lena Basin: moderate PET_rc and PET_PT trends across intervals; VPD and net radiation shifts contribute to changes.
- Ganges–Brahmaputra Basin: PET_rc and PET_PT trends show significant shifts post-1958; radiative and moisture drivers contribute to basin patterns.
- Ganges–Brahmaputra, Orange, Lena, Niger, Amazon, Congo, and others: Appendix provides per-basin statistics for PET_rc, PET_PT, Net Radiant Flux, VPD, Wind, Rainfall, Snowfall, and Precipitation, with averages, slopes, and significance (Adjusted Slope P).

## Appendix and data access for analysts
- Appendix includes the order of ERA-40 basis years used in WFD (1901–1957) and extensive basin-by-basin trend statistics for multiple variables across 1901–1957, 1958–2001, and 1979–2001.
- WFD is designed for model forcing and environmental monitoring; suitable for cross-study comparisons and long-term trend analyses of evaporation and its drivers.
- Analysts should carefully consider data-generation steps, bias corrections, aerosol/cloud adjustments, and uncertainties when interpreting results, particularly for the 1901–1957 period.

## Conclusions for monitoring
- WATCH data provide a robust forcing framework for evaluating global and regional evapotranspiration and hydrological responses, enabling consistent environmental monitoring and policy-relevant analyses.
- The 1901–1957 period, while informative for early-century statistics, requires caution due to data limitations and methodological choices.
- The integrated dataset supports scrutiny of external drivers of evaporation and environmental change, with explicit caveats on uncertainties and region-specific data quality.