# Creation of the WATCHForcing Data and its use to assess global and regional reference crop evaporation over land during the twentieth century

## Overview of the WATCH Forcing Data (WFD)

- Provides diurnally resolved meteorological forcing at half-degree resolution to drive land surface models (LSMs) and global hydrological models (GHMs) for the 20th century.
- Time periods:
  - 1958–2001 based on ERA-40 reanalysis
  - 1901–1957 based on re-ordered ERA-40 data to preserve statistical characteristics
- Variables include 10 m wind, 2 m air temperature, surface pressure, 2 m specific humidity, downward longwave and shortwave radiation, rainfall, snowfall; temporal resolution 3-hourly for radiative and wind variables, 6-hourly for others (interpolated to 3-hourly where needed)
- Data corrections and adjustments:
  - Temperature, pressure, humidity bias-corrected toward CRU data; elevation corrections applied sequentially
  - Downward shortwave radiation corrected for aerosol effects using 20th-century aerosol depths and cloud cover; longwave largely not bias-corrected to SRB
  - Rainfall/snowfall reconciled with GPCC totals and CRU wet-day counts; rain/snow partitioning tied to ERA-40 ratios
- Validation and calibration:
  - FluxNET site comparisons show generally good agreement for temperature and radiation; precipitation validation more variable due to scale and variability differences
- PET estimation:
  - PET_rc: Penman–Monteith for a reference crop
  - PET_PT: Priestley–Taylor, often applied in humid climates
  - PET values converted to equivalent depths (mm) for cross-model comparisons
- Global and regional findings (highlights):
  - Global PET_rc shows no significant trend from 1958–2001, despite rising VPD and shifts in net radiation and wind
  - 2 m air temperature increases are substantial, especially 1979–2001
  - PET_PT shows larger regional differences and can reconcile some inter-model dispersion
  - Precipitation: no robust global trend 1958–2001, but regional changes exist; arid basins show PET_rc typically exceeding precipitation
- Regional basins and key patterns (illustrative examples from the provided data):
  - PET_rc and PET_PT values, their regional slopes, and Net Rad, VPD, Wind, Rainfall, Snowfall, and Precipitation statistics are reported for periods 1901–1957, 1958–2001, and 1979–2001 in individual basins (e.g., Orange, Lena, Ganges–Brahmaputra, Murray–Darling, etc.)
  - Across basins, PET_rc slopes and PET_PT slopes vary by period; some periods show significant trends (e.g., certain 1958–2001 estimates with p-values indicating significance)
  - Rainfall and Snowfall show regional variability with notable changes in some basins; Net Rad and VPD exhibit period-dependent trends
- Appendix note:
  - Appendix Table 1 outlines the order of ERA-40 basis years used in WFD for 1901–1957, illustrating the data construction process

## Regional Basin Insights (based on the provided data)

- Orange River Basin
  - PET_rc: 1586.19 (1901–1957) → 1604.15 (1958–2001); notable early-to-mid-period slope; 1979–2001 shows a decline in slope
  - PET_PT: 1114.63 (1901–1957) → 1123.40 (1958–2001); modest positive trend overall
  - Net Rad: ~96–97 W/m2 with small positive slopes; VPD ~1.45–1.53 kPa; Rainfall ~305–347 mm/yr with increases in later periods
- Lena River Basin
  - PET_rc: ~363.5 (1901–1957) → ~366.7 (1958–2001); modest positive slopes
  - PET_PT: ~312.8 (1901–1957) → ~314.7 (1958–2001); small positive trend
  - Net Rad: ~29–33 W/m2; VPD ~0.94–0.97 kPa; Rainfall ~1400–1427 mm/yr; Snowfall present with seasonal variability
- Ganges–Brahmaputra River Basin
  - PET_rc: ~889.3 (1901–1957) → ~869.7 (1958–2001); PET_rc shows regional declines in later periods
  - PET_PT: ~798.7 (1901–1957) → ~767.99 (1958–2001); declines more pronounced in PET_PT
  - Rainfall: ~1426 mm/yr (1958–2001) with notable interannual variability
  - Net Rad: ~69–67 W/m2; VPD ~0.93–0.96 kPa; Wind ~1.9–2.0 m/s
- Murray–Darling River Basin
  - Data in the provided excerpt are incomplete; note that basin-level trends vary and are sensitive to period and variable definitions
- Appendices and consistency
  - The document provides extensive basin-scale time-series statistics for PET_rc, PET_PT, Net Rad, VPD, Wind, Rainfall, Snowfall, and Precipitation across multiple intervals, highlighting regional heterogeneity in climate drivers of PET

## Limitations and Uncertainties

- ERA-40 biases, especially in early periods (1950s–1970s), can affect VPD and PET_rc estimates; pre-1958 series less reliable due to data generation and bias correction limitations
- Pre-1958 data generation reduces interannual variability and trends for certain variables; caution is required when using WFD for early 20th-century analyses
- Sparse gauge coverage in some regions prior to 1950 introduces potential biases in regional trend assessments
- Validation shows good representation for temperature and radiation, but precipitation and sub-daily variability remain challenging in some basins

## Implications for Monitoring, Policy, and Data Sharing

- WFD provides a consistent, diurnally resolved forcing dataset for climate impact modelling, enabling robust inter-model comparisons and long-term environmental monitoring
- PET_rc and PET_PT offer complementary perspectives on potential evaporation, underscoring the importance of selecting appropriate PET formulations for hydrological assessments
- The standardised dataset supports tracking regional hydrological changes and evaluating environmental health and policy performance over time
- Accessibility and reuse:
  - WFD is documented as a WATCH technical resource and archived for use with LSMs and GHMs, facilitating data integration and cross-program data reuse
  - The dataset aligns with the Analysts Monitoring the Environment archetype’s aims of standardized data, verifiability, and accessible underlying data for broad scrutiny and policy evaluation