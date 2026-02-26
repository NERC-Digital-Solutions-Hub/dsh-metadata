# Creation of the WATCHForcing Data and its use to assess global and regional reference crop evaporation over land during the twentieth century.

## Overview
- Presents basin-level and global estimates of reference crop evaporation using WATCH Forcing Data (WFD) for 1901–1957 and 1958–2001, with sub-periods (e.g., 1979–2001).
- Forcing includes PET_rc (Penman–Monteith) and PET_PT (Priestley–Taylor) calculations driven by WFD variables (Net Radiation, VPD, Wind, Rainfall, Snowfall, etc.).
- Documents data corrections, trend analyses, and regional differences critical for data governance, provenance, and reproducibility.

## Regional/basin data highlights (selected basins)

- Orange River Basin
  - PET_rc
    - 1901–1957: average 1586.19 mm/yr; slope 1.2338 (p < 0.010); Neff 31.
    - 1958–2001: average 1604.15 mm/yr; slope 0.6463 (p > 0.200); Neff 28.
    - 1979–2001: average 1623.47 mm/yr; slope -2.3898 (p < 0.200); Neff 15.
  - PET_PT
    - 1901–1957: average 1114.63 mm/yr; slope 0.2471.
    - 1958–2001: average 1123.40 mm/yr; slope 1.1023.
    - 1979–2001: average 1131.46 mm/yr; slope 0.7341.
  - Other variables (Net Radiation, VPD, Wind, Rainfall, Snowfall) show modest trends with notable variability in Net Radiation and Rainfall.

- Lena River Basin
  - PET_rc
    - 1901–1957: average 363.47 mm/yr; slope 0.1315; Neff 49.
    - 1958–2001: average 366.70 mm/yr; slope -0.0454; Neff 36.
    - 1979–2001: average 366.11 mm/yr; slope 0.5366; Neff 23.
  - PET_PT
    - 1901–1957: average 312.82 mm/yr; slope 0.1505; Neff 49.
    - 1958–2001: average 313.48 mm/yr; slope 0.2437; Neff 21.
    - 1979–2001: average 314.73 mm/yr; slope 0.4203; Neff 12.
  - Net Radiation, VPD, Wind, Rainfall, Snowfall values indicate gradual regional shifts with substantial seasonal/annual variability.

- Ganges-Brahmaputra River Basin
  - PET_rc
    - 1901–1957: average 889.32 mm/yr; slope 0.0368; Neff 32.
    - 1958–2001: average 869.68 mm/yr; slope -2.2561; Neff 7.
    - 1979–2001: average 843.63 mm/yr; slope -1.8416; Neff 8.
  - PET_PT
    - 1901–1957: average 798.70 mm/yr; slope 0.0968; Neff 41.
    - 1958–2001: average 767.99 mm/yr; slope -1.2596; Neff 10.
    - 1979–2001: average 752.00 mm/yr; slope -0.8951; Neff 15.
  - Net Radiation and VPD show regional declines in PET_rc and PET_PT trends; rainfall remains high and relatively stable around 1400–1427 mm/yr across periods.

- Murray-Darling River Basin
  - Data for this basin in the provided text are largely incomplete or missing (placeholders indicate unavailable values in this excerpt).

## Data structure, corrections, and provenance (governance-relevant aspects)
- PET_rc and PET_PT are computed from WFD forcing variables across specified periods, with explicit per-basin statistics (average, slope, slope range, Neff, and adjusted slope P values).
- Basis-year design and year-ordering:
  - Appendix indicates the ERA-40 basis-year order used to construct WFD for 1901–1957, including the mapping of basis years to actual calendar years.
- Data corrections and quality indicators:
  - Slopes come with significance indicators (Adjusted Slope P), providing an appraisal of trend robustness.
  - Neff indicates effective sample size per period, informing uncertainty assessment.
- Metadata and usage notes:
  - The detailed basin-by-basin tables support provenance tracking and cross-basin comparability for model forcing and validation efforts.

## Uncertainties and caveats (data stewardship context)
- Early period data (pre-1958) have limited observational coverage and rely on ERA-40 basis-year reassignments, which introduces spatial/temporal limitations and potential biases.
- Trends in PET_rc and PET_PT vary by basin and subperiod; not all regional trends are globally consistent, reflecting regional hydroclimate drivers and data density differences.
- Net Radiation, VPD, Wind, Rainfall, and Snowfall fields carry inherent uncertainties from reanalysis biases, limited gauge data, and corrections that may not fully capture local processes.
- Validation against dense observational networks (e.g., FLUXNET) shows generally good agreement for temperature and radiation but larger discrepancies for precipitation-driven variables at sub-daily scales.

## Data access, usage guidance, and governance notes
- The WATCH Forcing Data (including PET_rc and PET_PT results by basin) is documented and intended for use in land surface and hydrological modeling across the 20th century.
- Practical usage guidance:
  - Use PET_rc for moisture and energy balance–limited contexts; use PET_PT where moisture is not limiting, with caution in arid regions where differences from PET_rc may be large.
  - Interpret basin-specific trends with awareness of data density and period-specific uncertainties; avoid overgeneralizing regional signals from periods with sparse data.
- Data governance considerations:
  - The dataset emphasizes transparent provenance, corrections, and validation metrics to support reproducibility and responsible data sharing.
  - Pre-1958 interpretations should account for weaker observational support and the reliance on ERA-40-based reconstruction methods.
- Access and documentation:
  - The data and its methodological documentation are provided to support long-term hydrological modeling and governance, with explicit notes on corrections, uncertainties, and limitations.
- Appendix and institutional context:
  - Appendix table (ERA-40 basis-year ordering) underpins the century-spanning construction approach and should be consulted when tracing data lineage or reproducing the forcing dataset.