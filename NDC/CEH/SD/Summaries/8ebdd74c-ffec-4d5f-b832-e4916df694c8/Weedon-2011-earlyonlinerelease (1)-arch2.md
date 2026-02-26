# The WATCH Forcing Data 1958-2001: a meteorological forcing dataset for land surface- and hydrological-models

- Used to drive land surface models (LSMs) and general hydrological models (GHMs) with diurnal-cycle-resolving meteorological forcing for the 20th century.
- Provides forcing for 1958–2001 (and a coherently constructed precursor for 1901–1957) to support evaporation, soil moisture, and runoff assessments and climate-change impact analyses.
- Based on ERA-40 reanalysis for the late 20th century (1958–2001); 1901–1957 constructed by re-ordering ERA-40 years to preserve diurnal-to-seasonal statistics and interannual characteristics.

- Data content and coverage
  - Global land-grid variables at 0.5° resolution (diurnal-to-seasonal statistics preserved):
    - Temperature-related: wind speed at 10 m, 2 m air temperature, surface pressure, 2 m specific humidity
    - Radiative: downward longwave and shortwave radiation
    - Hydrological: rainfall rate, snowfall rate
  - Temporal resolution: 3-hourly data for some variables, 6-hourly for others
  - Basis and corrections:
    - ERA-40 as the basis with bias corrections against CRU observations
    - Radiation adjustments account for aerosols, cloud cover, and historical aerosol depths
    - Precipitation corrected through a six-step process to maintain large-scale coherence and realistic wet-day distributions
  - Post-processed variables include PET rc (Penman–Monteith reference evapotranspiration for a well-watered grass) and PET PT (Priestley–Taylor), along withNet Radiation and VPD, Wind, Rainfall, Snowfall, and Precipitation, enabling basin- and region-specific analyses

- Data construction and corrections
  - Temperature, humidity, and pressure
    - Elevation and bias corrections; consistency to avoid supersaturation
    - CRU observations used for monthly bias checks and diurnal-range adjustments
  - Radiation
    - Downward longwave corrected for aerosols; shortwave adjusted for clouds and aerosol loadings using 20th-century aerosol depths
  - Precipitation
    - Six-step workflow to balance interpolation, rain/snow partitioning, wet-day counts, GPCC totals, ERA-40 proportions, and gauge corrections
    - Wet-day coherence emphasized; outliers limited to avoid spurious forcing of other variables
  - Humidity and precipitation consistency
    - Post-processing aligns rain/snow composition with observed regimes better than simple 0°C-cutoffs
  - Validation and caveats
    - FluxNet-based validation: good agreement for temperature, radiation, and wind at monthly scales; precipitation correlations weaker at sub-daily scales
    - Regional/topographic effects can introduce local discrepancies; interannual variability may be damped for pre-1958 data due to methodology
    - Caution advised when using PET-based forcing in arid vs. humid regions; PET rc vs PET PT show notable differences

- Validation and caveats (summary)
  - FluxNet validation supports reliability of key forcings for many basins at seasonal-to-monthly scales
  - Sub-daily precipitation metrics are less robust; regional biases can occur due to elevation and representativeness
  - Pre-1958 data have limitations in bias correction and interannual variability transmission

- Global and regional findings (relevant to analysts)
  - PET rc and PET PT
    - PET rc and PET PT provide complementary views of evaporation potential under different moisture/energy constraints
    - Global PET rc trends can be small or variable due to opposing drivers (temperature, wind, humidity, radiation)
  - Basin-level patterns (examples from selected basins)
    - Orange River Basin
      - PET rc averages: ~1586 mm/yr (1901–1957) rising to ~1604 mm/yr (1958–2001); slope changes from positive to variable (1958–2001: 0.65 mm/yr, with a wide slope range)
      - PET PT shows similar high values with modest positive trends in early periods and mixed trends later
      - Net Radiation remains near ~97 W/m2 across periods; VPD shows modest increases
    - Lena River Basin
      - PET rc: ~363–366 mm/yr across periods; slight long-term changes (1901–1957: +0.13 mm/yr; 1958–2001: −0.05 mm/yr)
      - PET PT: ~312–366 mm/yr with varying trends; regional differences across periods
      - Net Radiation and VPD show notable temporal evolution; Wind and Rainfall vary by period
    - Ganges-Brahmaputra River Basin
      - PET rc generally high: ~890 mm/yr (1901–1957) decreasing toward ~870 mm/yr (1958–2001) and ~843 mm/yr (1979–2001)
      - PET PT: ~799–798 mm/yr (1901–1957 to 1958–2001) with declines in later periods
      - Precipitation and Rainfall: substantial basinal variability; Snowfall generally small but present in some subregions; VPD and Wind show periodic changes
    - Murray-Darling River Basin
      - Data excerpt is incomplete in this chunk; overall approach emphasizes region-specificPET and moisture dynamics
  - Precipitation and moisture
    - Global precipitation trends are not uniform; regional patterns dominate basin-scale interpretations
    - In arid basins, PET rc often exceeds precipitation, signaling stronger evaporative demand relative to supply

- Practical takeaways for analysts
  - Use WFD as a standardized, traceable forcing dataset for long-term hydrological and land-surface experiments, with awareness of pre-1958 limitations and regional biases
  - When evaluating evaporation drivers, differentiate PET rc and PET PT outputs and consider basin-specific moisture availability and regional context
  - Leverage FluxNet validation for region- and scale-appropriate reliability assessment; treat sub-daily precipitation metrics with caution
  - Global averages can mask substantial regional variability; emphasize basin- or region-level analyses for environmental monitoring and policy evaluation

- Appendix note
  - Appendix Table 1 outlines the order of ERA-40 basis years used in the WATCH Forcing Data, illustrating the sequencing of ERA-40 and WFD years to construct 1901–1957 forcing