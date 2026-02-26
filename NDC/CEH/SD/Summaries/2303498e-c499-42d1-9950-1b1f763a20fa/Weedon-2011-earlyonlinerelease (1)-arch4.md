# Creation of the WATCHForcing Data and its use to assess global and regional reference crop evaporation over land during the twentieth century

## Overview
- Describes the creation of WATCH Forcing Data (WFD) to drive land surface models (LSMs) and general hydrological models (GHMs) within the EU WATCH project.
- Provides global forcing data at 0.5-degree resolution with sub-daily (3-hourly) timing for the twentieth century to capture diurnal cycles.
- Uses ERA-40 reanalysis as the basis for 1958–2001, with re-ordered ERA-40 data to extend to 1901–1957.
- Aims to understand external drivers of evaporation and regional variations, with validation against FLUXNET observations.

## Data and processing approach
- Variables and resolution:
  - Forcing variables include wind speed at 10 m, temperature at 2 m, surface pressure, specific humidity at 2 m, downward longwave and shortwave radiation, rainfall rate, and snowfall rate.
  - Global coverage at half-degree grid points (CRU land-sea mask; Antarctica excluded).
- Temporal structure:
  - 3-hourly data for most variables; precipitation components processed monthly but applied at sub-daily steps.
- Corrections and bias adjustments (1958–2001):
  - Temperature bias corrected using CRU observations; diurnal ranges aligned to CRU references.
  - Downward longwave radiation generally aligned with validation; no global longwave bias correction required after validation.
  - Downward shortwave radiation corrected for aerosol effects using HadGEM2-A aerosol depths.
  - Aerosol corrections include direct and indirect effects on clear-sky and cloudy-sky radiation.
  - Precipitation processing involved interpolation, rain/snow partitioning using ERA-40 proportions, alignment of wet-day counts with CRU, scaling to GPCCv4, and gridded gauge-catch corrections to preserve heavy precipitation coherence.
- Data structure and processing notes:
  - Bilinear interpolation from ERA-40 coarse grid to 0.5-degree mask; elevation adjustments applied to temperature, pressure, humidity, and longwave.
  - Wet-day corrections emphasize spatial coherence of significant precipitation events across grid boxes.
- Forcing data by period:
  - 1958–2001: derived directly from ERA-40 with bias corrections and adjustments.
  - 1901–1957: created by re-ordering ERA-40 years year-by-year to preserve global statistics, diurnal-to-monthly variation, autocorrelation, and cross-variable covariances, while maintaining coherence with the 1958–2001 period.
  - Limitations for 1901–1957: historical events may not be fully reconstructed; interannual/decadal variability may be underrepresented due to randomization and limited station coverage.

## PET estimation
- Reference evapotranspiration (PET_rc):
  - Estimated with Penman–Monteith framework (six of eight forcing variables; u2 derived from 10 m wind).
- PET_PT:
  - Priestley–Taylor method, used for comparison and interpretation relative to PET_rc.
- Units and interpretation:
  - PET values expressed in mm/yr; PET_pt tends to exceed PET_rc in humid regions and can differ by large margins in some locations.

## Global and regional findings (1958–2001 and beyond)
- PET_rc global signal:
  - Global average annual PET_rc shows a downward trend over 1958–2001 (~-0.51 mm/yr per year), with regional basins exhibiting diverse responses.
  - The 1901–1957 period shows no significant global trend in PET_rc.
- Basin-level patterns:
  - Basins display varied responses (increases or decreases in PET_rc and PET_PT) depending on shifts in wind, radiation, humidity, and temperature.
  - Precipitation changes are not globally uniform; some basins exhibit declines or increases, while others show little change.
  - In several arid basins, PET_rc often exceeds precipitation, highlighting potential hydrological stress.
- Surface energy and moisture terms:
  - Net radiation and VPD (vapour pressure deficit) show regional variations tied to historical changes in radiation balance and atmospheric moisture content.
- Overall interpretation:
  - Global averages can obscure contrasting regional shifts; basin-scale analyses reveal heterogeneous trends in PET, radiation, and precipitation.

## Validation and uncertainties
- Validation against FLUXNET:
  - Temperature, downward longwave/shortwave radiation, and wind speed show good agreement at monthly scales.
  - Precipitation correlations are weaker, especially at sub-daily scales, due to model-observation differences and coarse representation of precipitation processes.
  - Topography and land-cover representation can influence comparisons with tower measurements.
- Key caveats:
  - Early-20th-century data (1901–1957) rely on randomized baselines and limited station coverage, reducing confidence in decadal trends.
  - ERA-40 biases in early years and the absence of full bias corrections for some variables contribute to variability in PET_rc.
  - Interannual variability and basin-scale trends in VPD and PET_rc before 1958 may be partly artifacts of the data-generation approach.

## Basin highlights (selected examples)
- Orange River Basin:
  - PET_rc: 1901–1957 average 1586.19 mm/yr with a positive slope (1.2338 mm/yr per year); 1958–2001 average 1604.15 mm/yr with a smaller positive slope (0.6463); 1979–2001 average 1623.47 mm/yr with a negative slope in that period.
  - PET_PT: 1901–1957 average 1114.63 mm/yr; 1958–2001 average 1123.40 mm/yr; 1979–2001 average 1131.46 mm/yr.
  - Net Radiation: 1901–1957 average 96.75 W/m2; 1958–2001 average 96.79 W/m2.
  - VPD and Wind show small to moderate shifts across periods.
- Lena River Basin:
  - PET_rc: 1901–1957 average 363.47 mm/yr; 1958–2001 average 366.70 mm/yr; 1979–2001 average 366.11 mm/yr.
  - PET_PT: 1901–1957 average 312.82 mm/yr; 1958–2001 average 313.48 mm/yr; 1979–2001 average 314.73 mm/yr.
  - Net Radiation: relatively low, with modest increases in later periods; VPD and Wind show regional shifts.
- Ganges–Brahmaputra Basin:
  - PET_rc: 1901–1957 average 889.32 mm/yr; 1958–2001 average 869.68 mm/yr.
  - PET_PT: 1901–1957 average 798.70 mm/yr; 1958–2001 average 767.99 mm/yr.
  - Precipitation and Net Rad exhibit regionally differing trends; many components show declines in the later period.
- Other basins (examples):
  - PET_rc and PET_PT show mixed trends across 1901–1957, 1958–2001, and 1979–2001, with some basins experiencing notable increases or decreases in PET and changes in net radiation, wind, and precipitation regimes.
  - Snowfall contributions and rainfall patterns vary by basin, influencing PET estimates and hydrological balance.

## Data access, governance, and implications for data leaders
- The WATCH Forcing Data provides a robust, century-spanning, high-resolution meteorological forcing dataset suitable for driving large-scale hydrological and land-surface models.
- Strengths relevant to data leadership:
  - Explicit documentation of corrections, bias adjustments, and the rationale for each processing step.
  - Preservation of cross-variable relationships and spatial coherence of precipitation events, enabling coherent multi-variable analyses.
  - Validation against independent observations (e.g., FLUXNET) to support confidence in model inputs.
- Governance considerations:
  - Clear provenance, data transformations, and period-specific methodologies (1958–2001 from ERA-40; 1901–1957 by year-by-year re-ordering).
  - Transparent limitations, particularly for the early 20th century (data sparsity, potential ERA-40 biases, and underrepresentation of interannual variability).
  - Metadata richness (per-variable units, basins, periods, slopes, Neff, and adjusted P-values) that supports reproducibility and auditability.
- Practical implications:
  - Use of WFD requires awareness of pre-1958 data caveats; users should interpret long-term trends with caution and consider period-specific biases.
  - The data structure facilitates modular updates and potential bias-correction improvements as new information becomes available.
  - The approach supports cross-institution collaboration through standardized, well-documented forcing inputs and validation benchmarks.

## Conclusions
- The WATCH Forcing Data constitutes a comprehensive, high-resolution, century-spanning meteorological forcing dataset designed to drive LSMs/GHMs, with validated performance against field measurements.
- For 1958–2001, the data reflect real meteorological events and climate trends; for 1901–1957, the data retain statistical properties suitable for hydrological statistics but do not reconstruct exact historical events.
- Methodology emphasizes spatial coherence and cross-variable fidelity, enabling robust large-scale hydrological analyses, while remaining transparent about limitations in early-period data and ERA-40 biases.