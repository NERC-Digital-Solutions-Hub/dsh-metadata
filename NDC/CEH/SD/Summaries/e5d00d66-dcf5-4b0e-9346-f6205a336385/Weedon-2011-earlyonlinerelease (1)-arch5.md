# Creation of the WATCHForcing Data and its use to assess global and regional = reference crop evaporation over land during the twentieth century

## Overview of basin-level results (Appendix Table 1 subset)

- Orange River Basin
  - PET_rc (mm/yr): 1901–1957 average 1586.19; slope 1.2338 (significant, p < 0.010). 1958–2001 average 1604.15; slope 0.6463. 1979–2001 average 1623.47; slope -2.3898.
  - PET_PT (mm/yr): 1901–1957 average 1114.63; slope 0.2471. 1958–2001 average 1123.40; slope 1.1023. 1979–2001 average 1131.46; slope 0.7341.
  - Net Radiant (W/m2): 1901–1957 average 96.75; slope -0.0030. 1958–2001 average 96.79; slope 0.0805. 1979–2001 average 97.17; slope 0.0648.
  - VPD (kPa): 1901–1957 average 1.4479; slope 0.0021. 1958–2001 average 1.4879; slope 0.0013. 1979–2001 average 1.5289; slope -0.0040.
  - Wind (m/s): relatively stable around ~2.2 across periods; small slopes.
  - Rainfall (mm/yr): 1958–2001 average ≈ 501.5 with positive slope; 1979–2001 ≈ 498–498 with small positive slope.
  - Snowfall: generally very small; near 0–0.1 mm/yr in later periods.

- Lena River Basin
  - PET_rc: 1901–1957 average 363.47; slope 0.1315. 1958–2001 average 366.70; slope -0.0454. 1979–2001 average 366.11; slope 0.5366.
  - PET_PT: 1901–1957 average 312.82; slope 0.1505. 1958–2001 average 313.48; slope 0.2437. 1979–2001 average 314.73; slope 0.4203.
  - Net Radiant: 1901–1957 average 29.05; slope 0.0137. 1958–2001 average 28.65; slope 0.0072. 1979–2001 average 28.65; slope -0.0658.
  - VPD: 1901–1957 average 0.2404; slope 0.0001. 1958–2001 average 0.2443; slope -0.0004. 1979–2001 average 0.2717; slope 0.0004.
  - Wind: near 1.7–1.9 m/s with generally small changes; some periods show slight declines.
  - Rainfall: 1958–2001 average 1426.27; slope 0.2336. 1979–2001 average 1426.74; slope -1.3292.
  - Snowfall: modest but increasing slightly in some periods; overall small contribution.

- Ganges-Brahmaputra River Basin
  - PET_rc: 1901–1957 average 889.32; slope 0.0368. 1958–2001 average 869.68; slope -2.2561. 1979–2001 average 843.63; slope -1.8416.
  - PET_PT: 1901–1957 average 798.70; slope 0.0968. 1958–2001 average 767.99; slope -1.2596. 1979–2001 average 752.00; slope -0.8951.
  - Net Radiant: 1901–1957 average 69.75; slope -0.0008. 1958–2001 average 67.01; slope -0.1230. 1979–2001 average 65.45; slope -0.1041.
  - VPD: 1901–1957 average 0.9467; slope 0.0003. 1958–2001 average 0.9570; slope -0.0032. 1979–2001 average 0.9281; slope -0.0035.
  - Wind: generally around 1.9–2.0 m/s with small fluctuations.
  - Rainfall: 1958–2001 average ≈ 1426.27; slope 0.2336. 1979–2001 average ≈ 1426.74; slope -1.3292.
  - Snowfall: small contribution, mostly under 30 mm/yr in late period intervals.

- Murray-Darling River Basin
  - (Note: The provided data snippet for this basin is incomplete/garbled in this chunk; the pattern in other basins is similar: PET_rc and PET_PT trends tied to changes in Net Rad, VPD, wind, and rainfall across the 1901–1957, 1958–2001, and 1979–2001 intervals.)

- Other basins (Lena, Orange, Ganges-Brahmaputra, etc.)
  - Across basins, PET_rc and PET_PT generally show:
    - PET_rc tends to be high and often increasing from 1901–1957 into 1958–2001, with notable but basin-dependent decadal shifts (e.g., some later intervals show declines or reduced trends in PET_rc).
    - PET_PT (radiation-driven) often shows similar directionality, with sustained increases in several basins during 1958–2001, and mixed results in 1979–2001.
    - Net Radiant and VPD trends commonly indicate rising atmospheric demand (higher VPD) and modest changes in available energy (Net Rad) across several basins.
    - Rainfall and Snowfall exhibit substantial regional variability; rainfall may increase in some basins and decrease in others over 1958–2001 and 1979–2001 intervals. Snowfall remains a small component in most basins but shows regional trends in higher-latitude regions.

- General patterns to inform interpretation
  - PET_rc shows basin-to-basin heterogeneity with periods of both increasing and decreasing trends, often linked to changes in VPD, net radiation, and wind alongside rainfall shifts.
  - PET_PT differences from PET_rc can be substantial in some basins, contributing to spread in multi-model comparisons and underlining the sensitivity to forcing and method.
  - Net Rad and VPD generally rise or fluctuate modestly, influencing PET_rc and PET_PT alongside radiation and wind changes.

## Data governance, provenance, and usability notes (Data Stewards perspective)

- Provenance and reproducibility
  - Data are derived from WATCH Forcing Data built on ERA-40 reanalysis with explicit bias corrections and corrections for cloud cover/aerosols; the basin-level results herein are part of a transparent, traceable lineage.
  - Period-specific ensembles: PET_rc and PET_PT results are documented for 1901–1957, 1958–2001, and 1979–2001 intervals, enabling reproducibility and cross-period comparisons.

- Metadata and data quality
  - The basin-level table provides comprehensive statistics per interval: average values, slopes (with confidence indicators), and Neff (effective sample sizes) along with adjusted p-values.
  - Caveats present in the broader document apply: pre-1958 data carry higher uncertainty and limited bias corrections; tropical wet-day corrections and ERA-40 biases can affect early-year signals; regional variability in corrections and data availability.

- Data accessibility and sharing
  - WATCH data are provided with documented processing steps and are intended for use in hydrological/climatological analyses, including PET_rc and PET_PT assessments.
  - The appendix notation and basin-by-basin statistics should be accompanied by metadata detailing data sources, corrections, units, and temporal coverage to support reuse.

- Standards and interoperability
  - Variables and units are consistently reported as PET_rc and PET_PT (mm/yr), Net Rad (W/m2), VPD (kPa), Wind (m/s), Rainfall (mm/yr), and Snowfall (mm/yr) across basins and periods; ensure consistent application across downstream models and cross-model comparisons.

- Recommendations for Data Stewards
  - Maintain thorough metadata for each basin-period combination, including provenance, variable definitions, units, and any region-specific corrections applied.
  - Use clear versioning and change logs when reprocessing or updating forcing data; document impact assessments for updates to ERA-40-based inputs or bias-correction schemes.
  - Provide access to preprocessing workflows or code used for bias corrections, rain/snow partitioning, and other corrections to support reproducibility.
  - Flag region- and period-specific biases and uncertainties (e.g., pre-1958 variability, tropical wet-day issues, ERA-40 pressure biases) to guide users in interpretation.
  - When deriving derivative products (e.g., PET_rc vs PET_PT), supply explicit definitions, assumptions (e.g., reference-crop surface resistance), and conversion notes to aid cross-model comparability.

## Key caveats and end notes (relevant to stewardship)

- Pre-1958 limitations: limited bias corrections in 1901–1957 can inflate or damp interannual variability in PET_rc for that era.
- Tropical regions: ERA-40 tends to overestimate wet days; corrections attempt to preserve coherence but residual biases may persist.
- ERA-40-related issues: early-period surface pressure biases can influence VPD and PET_rc in some years; global signals may reflect underlying data artifacts.

## Summary takeaway for Data Stewards

- The WATCH Forcing Data provide a carefully bias-corrected, semi-dynamical forcing dataset for the 20th century, enabling robust PET_rc assessments and cross-model comparisons, with explicit limitations and thorough validation context. Ensuring strong metadata, reproducible preprocessing workflows, and transparent documentation will support reliable discovery, governance, and reuse across data-driven hydrological and climatological workflows.