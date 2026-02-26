# Creation of the WATCHForcing Data and its use to assess global and regional reference crop evaporation over land during the twentieth century

- Purpose and scope
  - Develop a long-term, bias-corrected meteorological forcing dataset (WATCH Forcing Data, WFD) at 0.5° resolution to drive land surface models (LSMs) and general hydrological models (GHMs) over the 20th century.
  - Provide sub-daily forcing for LSMs and daily forcing for GHMs to enable assessment of external drivers of evaporation with full diurnal resolution.
  - Compare 1958–2001 (primary) with 1901–1957 (extension) to preserve statistical characteristics and enable sub-century context.

- Data construction and sources
  - 1958–2001 WFD
    - Based on ERA-40 reanalysis; bias-corrected and elevation-adjusted; bilinear downscaling to 0.5° MSG and cloud/aerosol adjustments applied to radiation and precipitation.
    - Variables include: wind speed (10 m), temperature (2 m), surface pressure, specific humidity (2 m), downward longwave and shortwave radiation, rainfall rate, snowfall rate.
    - Precipitation processed with six steps to adjust rainfall/snowfall at each grid box and time step while preserving ERA-40 rain/snow proportions; rainfall totals aligned with GPCCv4 and CRU wet-days data.
  - 1901–1957 WFD
    - Created by random re-ordering ERA-40 years to mimic the later period’s diurnal, seasonal, and covariance characteristics; bias and precipitation corrections applied consistently with 1958–2001 to maintain coherence.
    - Aerosol and cloud corrections applied to shortwave radiation using historical aerosol depths.
  - Precipitation validation and adjustments
    - Wet-day corrections to match CRU observations; monthly totals aligned with GPCCv4 full product; rain/snow proportions re-allocated to ERA-40 ratios.
    - Extreme events and tropical regions treated to maintain large-scale coherence across grid boxes.
  - Global and regional outputs
    - Forcing fields cover wind, temperature, surface pressure, humidity, radiation, precipitation (including rain and snow components).

- Reference evapotranspiration estimation
  - PET_rc (Penman–Monteith): standard formulation using resistances rs = 70 s/m and ra derived from 2 m wind speed.
  - PET_PT (Priestley–Taylor): alternative estimator that can be more reliable in humid regions.
  - Both PET_rc and PET_PT are converted to equivalent depths (mm/yr) for cross-method comparisons.

- Validation and data quality
  - Validation against FluxNet sites shows strong correlations for temperature, wind speed, downward longwave and shortwave radiation.
  - Precipitation correlations are moderate to weak; diurnal rainfall patterns are challenging to reproduce.
  - ERA-40 biases, particularly in pre-1958 years, influence interannual variability; pre-1958 data rely on randomized years and limited bias corrections for some variables.
  - Sub-daily precipitation patterns are less reliable; the dataset is best used for studying long-term forcing characteristics and regional hydrological responses rather than precise event-by-event reproduction.

- Global and regional findings (key trends)
  - PET_rc (1958–2001): no significant global trend; interannual variability is large; global VPD increases; net radiation and wind speed trends are regional; global precipitation shows no clear trend.
  - PET_PT and PET_rc divergences: PET_PT frequently differs substantially from PET_rc in certain regions, highlighting sensitivity to forcing choices and method, especially between humid and arid zones.
  - Precipitation and snowfall: global land precipitation is broadly steady (1958–2001) with regional variations; snowfall contributions vary by region with some declines (e.g., in certain basins) and others showing little change.
  - Basin-scale patterns (illustrative examples)
    - Orange River Basin: PET_rc average around 1586–1604 mm/yr across 1901–2001 with varying slopes; PET_PT averages around 1115–1131 mm/yr for 1901–2001.
    - Lena River Basin: PET_rc ~363–367 mm/yr; PET_PT ~313–314 mm/yr (1901–2001 intervals); VPD and wind show regionally varying trends.
    - Ganges–Brahmaputra Basin: PET_rc ~889–870 mm/yr (1901–2001); PET_PT ~799–768 mm/yr; precipitation and net radiation show notable regional changes across intervals.
  - These basin-level figures illustrate how PET_rc and PET_PT respond to changing forcing fields and how regional hydroclimate evolves over time.

- Practical implications for analysts
  - The WATCH Forcing Data provides a consistent, bias-corrected, long-term forcing resource suitable for evaluating environmental health and water-resource policies and for running large-scale hydrological and land-surface models across the 20th century.
  - The 1958–2001 dataset is robust for analyzing global/regional evaporation drivers; the 1901–1957 extension adds context but requires caution regarding interannual variability and decadal changes.
  - When interpreting evaporation regimes, consider PET_rc versus PET_PT differences, as method choice materially affects regionally specific results.
  - Access and further details are available via the WATCH project (eu-watch.org and related publications).

- Caveats and limitations
  - ERA-40 biases, especially in early years, affect pre-1958 data and interannual variability of PET_rc.
  - Pre-1958 data rely on randomized baselines and limited bias corrections for some variables, potentially dampening decadal trends.
  - Uncertainties remain in precipitation representation due to station coverage and gauge corrections, particularly in the tropics and high latitudes.
  - Sub-daily precipitation patterns remain less reliable; use is recommended for long-term forcing characteristics and regional hydrological responses rather than exact historical event reproduction.

- Appendix and replication notes
  - Appendix Table 1 presents the order of ERA-40 basis years used in theWATCH Forcing Data (1901–1957), detailing the interplay between WFD generations and ERA-40 baselines to achieve coherence and reproducibility.