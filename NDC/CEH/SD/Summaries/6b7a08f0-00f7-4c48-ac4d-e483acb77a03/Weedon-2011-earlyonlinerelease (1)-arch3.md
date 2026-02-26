# The WATCH Forcing Data 1958-2001: a meteorological forcing dataset for land surface- and hydrological-models

## Overview
- Provides a standardized, high-resolution meteorological forcing dataset to drive land surface models (LSMs) and general hydrological models (GHMs) across the 20th century, enabling analyses of external drivers of hydrology relevant to environmental health monitoring and policy evaluation.
- Aims to resolve full diurnal cycles and support sub-daily to daily simulations of evaporation, soil moisture, and runoff; supports cross-region, policy-relevant environmental health indicators.

## Data structure and forcing variables
- Global gridded inputs at 0.5-degree resolution (~67,420 land points; excludes Antarctica) with a CRU land-sea mask.
- Variables include: wind speed at 10 m, air temperature at 2 m, surface pressure, specific humidity at 2 m, downward longwave and shortwave radiation, rainfall, and snowfall.
- Temporal resolution: primarily 3-hourly for most variables; some variables at 6-hourly with interpolation to 3-hourly steps.
- Primary period: 1958-2001 (based on ERA-40 reanalysis) with bias corrections and data adjustments.
- Pre-1958 extension: 1901-1957 created by reordering ERA-40 years to preserve statistical properties and diurnal/seasonal behavior (not intended to reproduce exact historical events). ERA-40 basis provides consistency; pre-1958 adjustments address sparse observations.

## Corrections and data fusion methodology
- Temperature, humidity, and pressure: elevation corrections after bilinear interpolation; bias corrections anchored to CRU observations where available.
- Downward longwave radiation: bias-corrected for internal consistency with ERA-40 and validated against FLUXNET data; no global SRB-based bias correction needed.
- Downward shortwave radiation: monthly aerosol corrections using HadGEM2-A aerosols and cloud-cover correlations; accounts for long-term aerosol loading.
- Precipitation (rainfall and snowfall): a six-step process including interpolation, rain/snow separation, adjustment of wet days to CRU counts, monthly GPCC totals for correction, and gauge-based correction to preserve spatial coherence of precipitation events; aims to maintain signal continuity across grid boxes.
- Validation: comparisons with FLUXNET show good agreement for temperature, wind, and radiation; precipitation validation is more challenging due to sub-grid variability and convective processes; regional/topographic mismatches acknowledged.

## PET estimation and comparison
- PET rc (Penman-Monteith for a reference crop) with fixed surface and aerodynamic resistances derived from wind data; PET PT (Priestley-Taylor) used as an alternative for comparison.
- Method choice materially affects outcomes; PET rc generally yields different global and basin-scale trends compared with PET PT, underlining model sensitivity and the importance of multiple formulations for uncertainty analysis.

## Global and regional findings (20th century)
- Global PET rc: no significant trend 1901-1957; modest global decline 1958-2001 (-0.51 mm/yr per year) with regional variability driven by temperature, VPD, net radiation, and wind changes.
- Basins show diverse responses (examples include Eight large river basins): some basins exhibit declines or increases in PET rc linked to wind speed, VPD, and other climate drivers; precipitation trends are not globally significant 1958-2001 but vary regionally.
- Validation and limitations: flux-tower comparisons show strong correlations for temperature, wind, and longwave radiation; precipitation correlations weaker due to sub-grid variability; large-windows (grid boxes) vs. point-scale observations introduce interpretive caveats; pre-1958 uncertainties remain due to sparse observations and reliance on ERA-40 years.

## Basin-specific highlights (selected basins from the provided data)
- Orange River Basin
  - PET rc (1901-1957): average ~1429 mm/yr with a negative slope (~-1.56 mm/yr^2); 1958-2001: average ~1449 mm/yr with a steeper negative slope (~-3.68 mm/yr^2); 1979-2001: average ~1623 mm/yr with negative slope (~-2.39 mm/yr^2).
  - PET PT (1901-1957): average ~959 mm/yr with slight positive slope; 1958-2001: average ~997 mm/yr with positive slope; 1979-2001: average ~1029 mm/yr with positive slope.
  - Rainfall shows positive trends in late periods, while snowfall remains small; overall basin-level trends in PET and precipitation are variable and period-dependent.
- Lena River Basin
  - PET rc (1901-1957): average ~363 mm/yr; 1958-2001: average ~367 mm/yr with a small negative slope; PET PT (1901-1957): ~313 mm/yr; 1958-2001: ~313 mm/yr with a small positive slope.
  - PET PT continues to rise modestly through 1979-2001; Net Radiation remains low; Rainfall shows modest increases in 1958-2001 and similar mild gains thereafter; VPD remains low with small trends.
- Ganges-Brahmaputra Basin
  - PET rc shows a decline from 1901-1957 to 1958-2001 (average ~798.7 to ~768 mm/yr) with a notable negative slope; 1979-2001: ~752 mm/yr continued decline.
  - PET PT declines more sharply in later periods (1901-1957 ~798.7; 1958-2001 ~767.99; 1979-2001 ~752.00).
  - Net Radiation and VPD show small-to-moderate shifts; Rainfall generally high with positive trends in some periods but overall variable; Snowfall remains small in many years.
- Note: The document includes additional basins (e.g., Murray-Darling, h) with detailed period-specific PET, Net Radiation, VPD, Rainfall, and Snowfall results; overall pattern is basin-dependent with no uniform global trend.

## Data access, outputs, and governance
- WATCH data (1958-2001) is intended for driving LSMs/GHMs and is publicly available with accompanying documentation.
- Documentation emphasizes transparent methodology, bias corrections, wet-day adjustments, aerosol corrections, and data provenance.
- The approach highlights governance considerations for monitoring frameworks: standardization, openness, reproducibility, and explicit handling of metadata and data lineage.
- Users are encouraged to consider multiple PET formulations (e.g., PET rc vs PET PT) to quantify uncertainty and assess health-relevant hydrological indicators.

## Implications for monitoring frameworks and policy decisions
- Standardization and openness of the forcing data support cross-regional environmental health monitoring and policy evaluation.
- Clear documentation of bias corrections, data adjustments, and validation supports governance and accountability.
- Trade-offs between data quality and usability are acknowledged; fragmentation of data access and metadata gaps can impede timely policy analyses.
- Encourages authors of monitoring frameworks to:
  - Employ data fusion from multiple sources with transparent bias corrections and validation.
  - Balance large-scale spatial coherence with sub-grid variability and scale mismatches.
  - Provide multiple, comparable metrics (e.g., PET rc vs PET PT) to capture sensitivity and uncertainty.
  - Document limitations, especially for earlier periods with sparse observations, to guide interpretation and future improvements.

## Appendix and data notes
- Appendix A includes the order of ERA-40 basis years used for the WATCH Forcing Data 1901-1957, illustrating the methodology for constructing pre-1958 data.
- The document emphasizes the role of rigorous metadata and data provenance to address common barriers faced by monitoring-framework authors.

## Key takeaways for authors of monitoring frameworks
- Prioritize data fusion from diverse sources, with transparent bias corrections and robust validation.
- Maintain spatial coherence for regional modeling while acknowledging sub-grid variability and scale differences.
- Provide multiple, comparable metrics to quantify uncertainty in health-relevant hydrological indicators.
- Clearly document limitations, especially for early periods with sparse observations, to guide policy interpretation and future data enhancement.