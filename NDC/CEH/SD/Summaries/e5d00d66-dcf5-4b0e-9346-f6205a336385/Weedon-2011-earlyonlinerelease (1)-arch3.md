# Creation of the WATCHForcing Data and its use to assess global and regional reference crop evaporation over land during the twentieth century

- The WATCH Forcing Data (WFD) provides bias-corrected, long-term meteorological forcing for land-surface and hydrological models, enabling analysis of drivers of evaporation and hydrology across the 20th century.
- It combines ERA-40 as the basis for 1958–2001 with extensive bias corrections, metadata, and data governance to support model forcing and intercomparison. A special approach is used to construct 1901–1957 data.

## What the WATCH Forcing Data (WFD) is

- A global, 0.5-degree gridded forcing dataset for land surfaces.
- Key variables: wind speed at 10 m, air temperature at 2 m, surface pressure, specific humidity at 2 m, downward longwave and shortwave radiation, rainfall, and snowfall.
- Forcing data are designed for sub-daily (3-hourly) precipitation-related variables and daily to sub-daily steps for others, enabling analysis of external drivers of evaporation.

## Data sources and corrections (1958–2001)

- ERA-40 is the primary basis; extensive bias corrections applied to:
  - Temperature (bias-corrected to CRU observations, adjusted for monthly means and diurnal range).
  - Downward longwave and shortwave radiation (aerosol loads from HadGEM2-A, volcanic aerosols, cloud-cover corrections).
  - Precipitation (CRU wet-day counts, GPCC totals) with rain/snow partitioning and gauge corrections.
- Elevation corrections applied sequentially to temperature, pressure, humidity, and longwave radiation.
- Wet-day correction strategies preserve spatial coherence of precipitation events.
- Validation against FluxNet shows good agreement at monthly scales for temperature, humidity, radiation, and wind; precipitation validation is regionally variable, with challenges in tropical convective regions and polar areas.
- Data governance: explicit documentation of data sources, corrections, and validation to support reproducibility; outputs are intended to be openly shareable.

## WATCH Forcing Data (1958–2001): processing and resolution

- Spatial and temporal setup:
  - 0.5-degree grid; 3-hourly precipitation-related variables; some variables 6-hourly or interpolated.
- Processing steps:
  - ERA-40 data bilinearly interpolated from 1° to 0.5°; elevation and humidity constraints applied to prevent supersaturation.
  - Cloud-cover and aerosol corrections applied to shortwave radiation; tropospheric and stratospheric aerosols accounted for.
  - Rainfall/snowfall totals interpolated and blended while preserving ERA-40 ratios; wet-day counts adjusted to CRU; GPCC corrections applied; regional adjustments for tropical regions to match observed wet-day frequencies.
- Validation and limitations:
  - Temperature, humidity, radiation, and wind show strong monthly-scale agreement with flux towers; precipitation agreement is less robust in some sites due to sparse in-situ data and resolution effects.
  - Acknowledgement of differences between point flux towers and grid-box averages; sub-daily precipitation remains a general weakness in convective tropical regimes.

## WATCH Forcing Data (1901–1957)

- Rationale: To drive hydrological modeling across the full twentieth century, including pre ERA-40 coverage.
- Approach:
  - ERA-40 data re-ordered year-by-year and randomly allocated to 1901–1957 while preserving long-term statistics (extremes, variability) similar to 1958–2001.
  - Same preprocessing steps as 1958–2001, with adjustments to maintain diurnal-to-seasonal coherence and front coherence across grid boxes.
- Limitations:
  - Interannual/decadal trends before 1958 are less reliable due to randomization and sparse station coverage; potential decadal signals may be dampened in some regions.

## PET_rc and PET_PT: definitions and relevance

- PET_rc (reference crop PET): Penman–Monteith calculation using a standardized reference crop model; key parameters include surface resistance, aerodynamic resistance, and energy balance terms.
- PET_PT (Priestley–Taylor PET): a radiation-based alternative, useful in humid conditions; PET_PT = α × Δ/(Δ + γ) × A, with α ≈ 1.26.
- Purpose:
  - PET_rc provides area-averaged evaporation demand with full Penman–Monteith physics; PET_PT offers a sensitivity alternative to explore model responses to PET formulation.
  - Notable river-basin results show substantial regional differences between PET_rc and PET_PT, underscoring the importance of PET choice in hydrological modeling.

## Global and regional findings

- Global perspective (1958–2001):
  - Global mean PET_rc shows no significant global trend, but strong regional variations exist.
  - VPD increased, near-surface temperature rose markedly, and net radiation and wind patterns shifted; opposing influences often modulate the global PET_rc signal.
- Regional basins (illustrative examples):
  - Amazon, Congo, Niger, Murray-Darling, Ganges-Brahmaputra, Mackenzie, Lena, and others exhibit diverse PET_rc and PET_PT behavior driven by local changes in VPD, radiation, wind, and precipitation.
  - Precipitation trends on a global land basis (1958–2001) are not strongly significant, but several basins show detectable regional shifts that influence evaporative demand and hydrological responses.
  - Differences between PET_rc and PET_PT across basins can be large (regionally, tens to hundreds of mm/yr), explaining part of the spread in model outputs across studies.
- Basin-level notes (selected insights):
  - Orange River Basin: PET_rc and PET_PT show distinct historical patterns with positive average slopes in some periods and notable shifts in 1979–2001; net radiation and VPD also exhibit changes.
  - Lena River Basin: PET_rc relatively stable across periods; PET_PT shows modest increases in some eras; VPD trends are generally small but show changes in later periods.
  - Ganges-Brahmaputra: PET_rc declines from 1958–2001; PET_PT patterns and precipitation changes show regional variability; complex interactions with monsoonal dynamics.
  - Murray-Darling and others: basin-specific dynamics in PET RC/PT, radiation, VPD, wind, and precipitation reflect semi-arid and monsoonal influences, yielding diverse trends.
- Overall interpretation:
  - There is modest or no clear global trend in PET_rc, but pronounced regional changes in evaporative demand drivers (VPD, radiation, wind) and precipitation patterns across basins, with implications for water resources planning.

## Validation and data quality considerations for monitoring frameworks

- Validation:
  - FluxNet comparisons show good agreement for temperature, humidity, and radiation; precipitation validation is more challenging at three-hourly timescales, especially in convective tropical regions.
- Data governance and transparency:
  - The methodology is comprehensively documented; data are designed to be openly sharable for model forcing and intercomparison.
  - Clear caveats about data gaps, regional biases, and pre-1958 uncertainties are provided.
- Implications for monitoring frameworks:
  - Demonstrates rigorous data processing, bias correction, gap-filling, and the importance of documenting data provenance.
  - Highlights the necessity of metadata, versioning, and reproducibility, as well as the value of providing multiple PET formulations for sensitivity analyses.
  - Emphasizes validation against independent observations and careful treatment of data gaps and regional biases to support policy-relevant monitoring.

## Conclusions

- The WATCH Forcing Data (1958–2001) offers a robust, bias-corrected forcing dataset suitable for driving land surface and hydrological models across the twentieth century.
- The 1901–1957 WFD data enable historical hydrological statistics exploration, though with caveats about interannual variability and data limitations.
- PET_rc and PET_PT are complementary; regional differences underscore careful PET selection in modeling efforts.
- Global trends in the period are modest, but regional disparities in evaporation drivers and precipitation underscore important considerations for water resources planning.
- For monitoring frameworks, the study underscores the importance of addressing data gaps, biases, and coherence of precipitation events, along with rigorous metadata and reproducibility to inform policy decisions. 

Appendix note:
- Appendix Table 1 outlines the ERA-40 basis-year order used in the WATCH Forcing Data for 1901–1957, illustrating the alternation between ERA-40 and WFD basis years across the historical sequence.