# Creation of the WATCHForcing Data and its use to assess global and regional reference crop evaporation over land during the twentieth century

- Overview
  - Presents century-spanning meteorological forcing data (WATCH Forcing Data, WFD) used for land-surface models (LSMs) and general hydrological models (GHMs).
  - Covers two eras: WFD 1958-2001 (bias-corrected from ERA-40) and WFD 1901-1957 (reordered ERA-40 to preserve diurnal statistics and seasonal patterns).
  - Variables per grid cell include wind (10 m), temperature (2 m), surface pressure, specific humidity (2 m), downward longwave radiation, downward shortwave radiation, rainfall, and snowfall.
  - Data structure: 6-hourly for most variables; 3-hourly interpolation available; precipitation adjusted to align with CRU/GPCC-based corrections.
  - Enables assessment of external drivers of evaporation and regional hydrological changes across the 20th century, with attention to PET (potential evapotranspiration) estimation via two methods.

- PET estimation approaches
  - PET rc (Penman-Monteith) uses standard reference-crop resistances and requires wind, temperature, humidity, and radiation data.
  - PET PT (Priestley-Taylor) is simpler (radiation/temperature-based) and often more suitable in humid regions.
  - Both PET estimates are converted to equivalent depths (mm) for comparability.
  - Key finding: PET rc generally exceeds PET PT, with regional differences; large local divergences between PET rc and PET PT can explain part of model disagreement in drought-prone basins.

- Basin-specific highlights (examples from the provided data)
  - Orange River Basin
    - PET rc: 1901-1957 average 1586.19 mm/yr; slope 1.2338 (adjusted P < 0.010). 1958-2001 average 1604.15 mm/yr; slope 0.6463 (P < 0.200). 1979-2001 average 1623.47 mm/yr; slope −2.3898 (P < 0.200).
    - PET PT: 1901-1957 average 1114.63; 1958-2001 average 1123.40 (slope 1.1023, P < 0.020); 1979-2001 average 1131.46 (slope 0.7341, P > 0.200).
    - Net radiation around 96–97 W/m2; VPD around 1.44–1.53 kPa; Wind ~2.2 m/s.
    - Rainfall around 346 mm/yr (1958-2001) and ~338 mm/yr (1979-2001); Snowfall small; notable PET trends differ by period.
  - Lena River Basin
    - PET rc: 1901-1957 average 363.47 mm/yr; 1958-2001 average 366.70; 1979-2001 average 366.11.
    - PET PT: 1901-1957 average 331.55; 1958-2001 average 313.48; 1979-2001 average 314.73.
    - Net radiation around 29–33 W/m2; VPD ~0.95–1.0 kPa; Wind ~1.7–2.0 m/s.
    - Rainfall: 1958-2001 ~1400.84 mm/yr; 1979-2001 ~1426.74 mm/yr; Snowfall ~25–26 mm/yr.
    - PET rc shows slight upward trend 1979-2001 (slope 0.5366) with modest earlier changes; PET PT shows mixed/less pronounced trends.
  - Ganges-Brahmaputra River Basin
    - PET rc: 1901-1957 average 889.32 mm/yr; 1958-2001 average 869.68 (slope −2.2561); 1979-2001 average 843.63 (slope −1.8416).
    - PET PT: 1901-1957 average 798.70; 1958-2001 average 767.99 (slope −1.2596); 1979-2001 average 752.00 (slope −0.8951).
    - Net radiation declines from ~70 W/m2 (1901-1957) to ~67 W/m2 (1958-2001); VPD around 0.95–1.0 kPa; Wind around 1.9–2.0 m/s.
    - Rainfall/Precipitation: 1958-2001 ~1426.27 mm/yr; 1979-2001 ~1426.74 mm/yr; Snowfall ~25–26 mm/yr.
    - Notable downward PET trends in several sub-periods; PET PT also shows declines with regional variability.
  - Murray-Darling River Basin
    - The provided excerpt includes limited complete numerical detail for Murray-Darling; indicates data exist for PET rc and PET PT across periods but specific values in this snippet are incomplete.
  - Appendix Table 1 (ERA-40 basis year order)
    - Documents the historical ordering of basis years used to construct WFD 1901-1957, illustrating the methodological approach to preserve global statistics and extreme behavior in the pre-1958 era.

- Data access and practical use
  - WFD 1958-2001 and WFD 1901-1957 are provided as part of the WATCH project; documentation and datasets are available through the EU-WATCH program and associated technical reports.
  - Analysts can use WFD to drive LSMs/GHMs for century-scale hydrological analyses, perform attribution studies, and compare model intercomparisons under historical forcing.
  - PET rc vs PET PT comparisons inform region-appropriate PET formulation choices, particularly when simulating humid vs arid climates.
  - The basin-level results highlight regional heterogeneity in evaporation drivers (wind, radiation, humidity, VPD) and the importance of local context when interpreting trends in PET and precipitation.

- Uncertainties and caveats
  - ERA-40-related uncertainties are higher in early years (1958-1978), affecting surface pressure, wind, and humidity and potentially introducing spurious variability in global VPD and PET rc.
  - Pre-1958 data rely more on climatology substitutions and have sparser observational constraints, which can damp decadal PET rc trends.
  - Wet-day correction methods improve coherence of frontal rainfall but may produce rare high outliers in arid regions.
  - Validation (e.g., with FLUXNET) shows good agreement for temperature and radiation but weaker correlations for sub-daily precipitation; footprint-scale differences vs grid-box averages are acknowledged.

- Conclusions for analysts
  - The WATCH Forcing Data provide a robust, consistent century-scale forcing dataset enabling detailed exploration of sub-daily meteorological drivers of evaporation and hydrological responses.
  - PET rc vs PET PT differences lead to region-dependent impacts on hydrological balances; careful selection of PET formulation is crucial for accurate regional assessments.
  - Regional basins exhibit substantial heterogeneity in evaporation drivers and trends, underscoring the need for basin-specific analysis and consideration of data-era uncertainties when interpreting long-term hydrological signals.