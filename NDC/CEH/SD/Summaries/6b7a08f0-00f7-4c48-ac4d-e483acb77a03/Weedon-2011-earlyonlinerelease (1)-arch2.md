# Creation of the WATCHForcing Data and its use to assess global and regional reference crop evaporation over land during the twentieth century

## Overview and aims
- Develop the WATCH Forcing Data (WFD) to drive land surface models (LSMs) and general hydrological models (GHMs) for the 20th century with diurnal completeness and standardized meteorological forcing.
- Provide global land forcing at half-degree resolution for 1958–2001 (based on ERA-40) and 1901–1957 (constructed to preserve sub-daily and inter-variable covariance).

## The WATCH Forcing Data (WFD) and data pipeline
- Forcing variables included: wind speed at 10 m, temperature at 2 m, surface pressure, specific humidity at 2 m, downward longwave and shortwave radiation, rainfall, snowfall.
- Spatial/temporal structure: 0.5-degree grid; global land points; 3-hourly data for radiation and wind/humidity; 6-hourly data interpolated to 3-hourly where needed.
- Data sources and corrections:
  - ERA-40 basis for 1958–2001; re-ordered ERA-40 years for 1901–1957.
  - Bias corrections and quality control using CRU observations (temperature, diurnal range) and GPCC precipitation.
  - Downward shortwave radiation corrected for aerosols with HadGEM2-based aerosol optical depths; cloud adjustments using CRU cloud observations.
  - Precipitation processed via six-step scheme to merge rainfall and snowfall, adjust wet days to CRU counts, ensure totals align with GPCC, and preserve event coherence.
- Validation:
  - Temperature, wind, and downwelling radiation show reasonable agreement with observations from FLUXNET-scale sites.
  - Precipitation well represented for daily totals but more uncertain at sub-daily scales, especially in convective regions.

## Estimation of reference crop evaporation (PET)
- PET_rc (Penman-Monteith with a reference crop)
  - Uses ERA-40–based forcing for net radiation, VPD, wind, and temperature; relies on standard reference-crop resistances.
- PET_PT (Priestley-Taylor)
  - Simpler radiation- and temperature-based method using available energy and VPD/wind information.
- Key interpretation:
  - PET_rc emphasizes energy balance and humidity interactions; more sensitive to VPD and wind — useful in arid to humid contexts.
  - PET_PT is robust in humid, energy-limited contexts but can diverge from PET_rc in some regions.
- Global vs. regional behavior:
  - Large regional differences in evaporation drivers across basins; substantial spread between PET_rc and PET_PT in several regions.

## Global and regional findings (20th century)
- PET_rc trends
  - Global 1958–2001: declines on average (-0.51 mm/yr) with large interannual variability.
  - 1901–1957: no significant global trend detected (data-sparse in early period limits reliability).
- Precipitation and water balance
  - No significant global change in land precipitation 1958–2001, though regional patterns vary and rainfall can exceed PET_rc in some basins.
- Data quality caveats
  - Pre-1958 data have limitations due to sparse observations and reliance on biased climatologies.
  - Sub-daily precipitation fidelity is variable; model outputs require careful validation against observations at appropriate scales.
- Implications
  - The WFD (1958–2001) provides a robust, diurnally resolved forcing dataset for century-scale hydrological studies.
  - The 1901–1957 extension enables exploration of early 20th-century hydrology but with acknowledged limitations in interannual variability fidelity.

## Basin-level highlights (from the provided data)
Note: Data entries for Murray-Darling Basin in this chunk are incomplete; the following highlights focus on available basins.

- Orange River Basin
  - PET_rc:
    - 1901–1957: average 1586.19 mm/yr; slope +1.2338 mm/yr^2; significant trend (Adjusted Slope P < 0.010).
    - 1958–2001: average 1604.15 mm/yr; slope +0.6463; not consistently significant across subperiods (Adjusted Slope P > 0.200).
    - 1979–2001: average 1623.47 mm/yr; slope −2.3898 (decline) with wide uncertainty.
  - PET_PT:
    - 1901–1957: average 1114.63 mm/yr; slope +0.2471.
    - 1958–2001: average 1123.40 mm/yr; slope +1.1023.
    - 1979–2001: average 1131.46 mm/yr; slope +0.7341.
  - Other drivers (net radiation, VPD, wind, rainfall, snowfall) show mixed but generally increasing rainfall signals in later periods and relatively stable wind; rainfall 1958–2001 increases (approx. 346–347 mm/yr) with notable late-period rises in some subranges.
- Lena River Basin
  - PET_rc:
    - 1901–1957: average 363.47 mm/yr; slope +0.1315.
    - 1958–2001: average 366.70 mm/yr; slope −0.0454.
    - 1979–2001: average 366.11 mm/yr; slope +0.5366.
  - PET_PT:
    - 1901–1957: average 312.82 mm/yr; slope +0.1505.
    - 1958–2001: average 313.48 mm/yr; slope +0.2437.
    - 1979–2001: average 314.73 mm/yr; slope +0.4203.
  - Net radiation and VPD show modest declines or stability in the 1958–2001 window; rainfall and precipitation signal a modest increase into the late 20th century; snowfall remains low but detectable.
- Ganges-Brahmaputra Basin
  - PET_rc:
    - 1901–1957: average 889.32 mm/yr; slope +0.0368.
    - 1958–2001: average 869.68 mm/yr; slope −2.2561 (notable decline).
    - 1979–2001: average 843.63 mm/yr; slope −1.8416.
  - PET_PT:
    - 1901–1957: average 798.70 mm/yr; slope +0.0968.
    - 1958–2001: average 767.99 mm/yr; slope −1.2596.
    - 1979–2001: average 752.00 mm/yr; slope −0.8951.
  - Other variables:
    - Net radiation shows a downtrend from 1901–1957 to 1958–2001 and further into 1979–2001.
    - VPD and wind are relatively stable with small declines; rainfall/precipitation trends are regionally variable, with some late-period increases in rainfall and notable fluctuations in snowfall.

- Murray-Darling Basin
  - In this excerpt, Basin entries are largely placeholders with missing values; no robust basin-level conclusions can be drawn from this chunk.

- Appendix note
  - Appendix Table 1 documents the order of ERA-40 basis years used in the WATCH Forcing Data 1901–1957, illustrating how ERA-40 and WFD years are alternated to build the 1901–1957 dataset.

## Practical guidance for analysts
- Use PET_rc when energy balance and humidity interactions are critical; use PET_PT for humid or energy-limited contexts where simpler formulations are advantageous.
- Be mindful of regional differences in drivers; global averages can obscure local dynamics.
- Account for data quality caveats in pre-1958 periods and sub-daily precipitation limitations when validating model outputs against observations.
- Leverage the standardized, well-documented provenance (ERA-40, CRU, GPCC, HadGEM aerosol corrections) to ensure reproducibility and cross-study comparability.

## Relevance for environmental-health and policy monitoring
- Provides a consistent, long-term forcing dataset suitable for monitoring potential evapotranspiration and regional water balance over the twentieth century.
- Enables examination of meteorological drivers (radiation, wind, humidity, precipitation) shaping regional water resources and agricultural demand.
- Highlights the necessity of data provenance, bias correction, and regional validation for credible long-term environmental health indicators.
- Demonstrates how integrating multiple data sources can produce a coherent dataset for policy-relevant assessments across extended horizons.

## Access, usage, and next steps
- WFD is intended for broad distribution to support hydrological and land-surface modeling and comparative assessments of the global and regional water balance over the twentieth century.
- Analysts should supplement WFD with independent observations for local validation and consider basin-specific contexts when interpreting long-term evaporation and precipitation trends.