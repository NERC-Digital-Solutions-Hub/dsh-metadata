# Creation of the WATCHForcing Data and its use to assess global and regional reference crop evaporation over land during the twentieth century

- This data chunk provides basin-scale time-series statistics for reference evapotranspiration metrics and key meteorological drivers across multiple basins, focusing on 1901–1957 and 1958–2001 (with some 1979–2001 subsets).
- Variables covered (per basin and interval):
  - PET_rc (mm/yr): Penman–Monteith PET for a well-watered reference crop.
  - PET_PT (mm/yr): Priestley–Taylor PET as an alternative estimate.
  - Net Rad (W/m^2): Net radiative flux at the surface.
  - VPD (kPa): Vapor pressure deficit.
  - Wind (m/s): Mean wind speed.
  - Rainfall and Precipitation (mm/yr): Surface precipitation metrics.
  - Snowfall (mm/yr): Snow precipitation component where applicable.
- Data structure notes:
  - For each basin, values are given as: interval, variable, average, slope (units/yr), slope min, slope max, Neff (effective sample size), and Adjusted Slope P (statistical significance indicator).
  - Some intervals include incomplete data (e.g., Murray-Darling) or sparse Neff, with corresponding interpretive caution.
  - Appendix table also documents the order of ERA-40 basis years used in WATCH Forcing Data (1901–1957).

- Orange River Basin (c)
  - PET_rc (1901–1957): average 1586.19 mm/yr; slope 1.2338 (significant, P < 0.010).
  - PET_rc (1958–2001): average 1604.15 mm/yr; slope 0.6463 (not significant at conventional levels; P > 0.200).
  - PET_rc (1979–2001): average 1623.47 mm/yr; slope −2.3898 (not significant at conventional levels; P > 0.200).
  - PET_PT (1901–1957): average 1114.63 mm/yr; slope 0.2471 (not clearly significant; P > 0.200).
  - PET_PT (1958–2001): average 1123.40 mm/yr; slope 1.1023.
  - PET_PT (1979–2001): average 1131.46 mm/yr; slope 0.7341.
  - Net Rad: 1901–1957 average 96.75; slope −0.0030; 1958–2001 average 96.79; slope 0.0805 (p-values indicate modest or uncertain significance).
  - VPD: 1901–1957 average 1.4479; slope 0.0021; 1958–2001 average 1.4879; slope 0.0013; 1979–2001 average 1.5289; slope −0.0040 (generally not clearly significant).
  - Wind: ~2.20 m/s across periods with small, non-significant slopes.
  - Rainfall: 1958–2001 average 346.47 mm/yr; slope 0.8493 (not consistently significant); 1979–2001 average 337.84; slope 3.8769 (not consistently significant.
  - Snowfall: small and mostly negligible; slopes near zero; significance not indicated.

- Lena River Basin (f)
  - PET_rc: 1901–1957 average 363.47 mm/yr; slope 0.1315 (not strongly significant); 1958–2001 average 366.70; slope −0.0454; 1979–2001 average 366.11; slope 0.5366.
  - PET_PT: 1901–1957 average 331.55; slope 0.1970; 1958–2001 average 313.48; slope 0.2437; 1979–2001 average 314.73; slope 0.4203.
  - Net Rad: 1901–1957 average 29.05; slope 0.0137; 1958–2001 average 28.65; slope 0.0072; 1979–2001 average 28.65; slope −0.0658.
  - VPD: 1901–1957 average 0.2404; slope 0.0001; 1958–2001 average 0.2443; slope −0.0004; 1979–2001 average 0.2453; slope 0.0004.
  - Wind: ~1.69 m/s across periods; slopes near zero with modest significance in some intervals.
  - Rainfall: 1958–2001 average 1400.84 mm/yr; slope 0.1620; 1979–2001 average 1426.74; slope 0.9950 or 0.?? (values show variability across sub-intervals; significance generally low).
  - Snowfall: 1958–2001 average 132.34 mm/yr; slope −0.1109; 1979–2001 average 131.41; slope 0.2453; generally not statistically significant.

- Ganges-Brahmaputra River Basin (h)
  - PET_rc: 1901–1957 average 889.32 mm/yr; slope 0.0368; 1958–2001 average 869.68; slope −2.2561 (significant for 1958–2001, P < 0.001); 1979–2001 average 843.63; slope −1.8416 (significant at P < 0.010).
  - PET_PT: 1901–1957 average 798.70; slope 0.0968; 1958–2001 average 767.99; slope −1.2596 (P < 0.001); 1979–2001 average 752.00; slope −0.8951 (not consistently significant).
  - Net Rad: 1901–1957 average 69.75; slope −0.0008; 1958–2001 average 67.01; slope −0.1230 (P < 0.001); 1979–2001 average 65.45; slope −0.1041.
  - VPD: 1901–1957 average 0.9467; slope 0.0000; 1958–2001 average 0.9570; slope −0.0032 (P < 0.001); 1979–2001 average 0.9281; slope −0.0035.
  - Wind: ~1.69 m/s (1901–1957) to ~1.69 m/s (1958–2001); slopes small and typically not significant.
  - Rainfall/Precipitation: 1958–2001 average around 1426–1400 mm/yr with positive slopes (e.g., 0.2336 for PET-related precipitation indicators); 1979–2001 shows larger short-term fluctuations with generally non-significant long-term slopes.
  - Snowfall: small contributions; slopes near zero; significance generally not indicated.

- General interpretation for this data chunk (Data Support perspective):
  - PET_rc trends show regional variability: some basins exhibit significant increases or decreases across periods, while others show non-significant changes.
  - PET_PT tends to track PET_rc but with basin-specific differences in magnitude and significance; some basins show modest positive trends over mid-century to late-century intervals.
  - Net Radiant and VPD trends indicate shifts in atmospheric demand and radiative balance, with several basins showing notable late-20th-century declines in net radiation and small but regionally variable VPD changes; significant signals are basin- and interval-dependent.
  - Rainfall and Snowfall show substantial inter-annual to decadal variability; many basins display no consistent long-term trend in precipitation, while some show positive or negative tendencies that may influence PET and evapotranspiration indirectly.
  - Data quality notes:
    - Neff values indicate variable sample sizes across basins and intervals; some periods have robust sampling while others are sparse.
    - Adjusted Slope P values are provided, with many basins showing non-significant trends (P > 0.05), underscoring regional heterogeneity and uncertainties in longer-term homogenization of meteorological inputs.
  - These basin-specific trends are intended to inform hydrological and land-surface modeling efforts that rely on consistent, long-term forcing, while highlighting the importance of regional interpretation and uncertainty in historical climate driver changes.

- Appendix-related notes
  - Appendix Table 1 documents the order of ERA-40 basis years used in the WATCH Forcing Data 1901–1957, illustrating the data construction approach that alternates ERA-40 and WATCH-derived inputs to form a long historical record.