# Fortnightly measurements Clocaenog 2015-2016 data structure supplement

- This document supplements the supporting documentation for data series described in Clocaenog_supporting documentation_Fortnightly measurements.rft.
- It details the data structure for two datasets collected together in 2015-2016:
  - Fortnightly measurments_Clocaenog_2015-2016_site.csv
  - Fortnightly measurments_Clocaenog_2015-2016_soil respiration.csv

## Dataset overview

- Dataset 1: Fortnightly measurments_Clocaenog_2015-2016_site.csv
  - Structure: 20 columns, 32 rows
  - Key contents:
    - Date (A): Day/Month/Year
    - Rainfall (B): mm, described as site level
    - Throughfall measurements across Plot1 to Plot9 (C–J)
    - Water table depth measurements across Plot1–Plot9 (L–T)
  - Each column is labeled with a descriptive header indicating the plot or measurement (e.g., Plot1 - Warming, Plot3 - Control, Plot9 - Control) and whether it represents rainfall, throughfall, or water table depth.

- Dataset 2: Fortnightly measurments_Clocaenog_2015-2016_soil respiration.csv
  - Structure: 38 columns, 32 rows
  - Key contents:
    - Date (A): Day/Month/Year
    - Soil respiration for Plot1 to Plot9 across different treatments (B–J)
    - Soil temperature for Plot1–Plot9 (K–S)
    - Soil moisture for Plot1–Plot9 (T–W)
    - Photosynthetic active radiation (PAR) for Plot1–Plot9 (AC–AJ, AK–AJ area)
  - Column headers indicate per-plot measurements and units:
    - Soil respiration: mg CO2-C m-2 hr-1 or mg CO2-C m-2 hr-1 (varies by column)
    - Soil temperature: degrees Celsius (°C)
    - Soil moisture: Vol%
    - PAR: µmol m-2 s-1

## Common structure and interpretation cues

- Both datasets share a Date column (A) to align observations across measurements.
- Plot-specific measurements are labeled by description, such as:
  - Warming, Control, Drought, etc., for each plot (Plot1–Plot9).
- Units to be aware of:
  - Rainfall: mm
  - Throughfall: mm
  - Water table depth: mixed units (cm and mm seen in dataset descriptions)
  - Soil respiration: mg CO2-C m-2 hr-1 or mg CO2-C m-2 hr-1 (depending on column)
  - Soil temperature: °C
  - Soil moisture: Vol%
  - PAR: µmol m-2 s-1
- The dataset structure supports joining by Date to compare surface-level (site) measurements with soil process measurements across plots and treatments.
- The detailed headers and units per column enable precise data cleaning, validation, and preparation for dashboards or reports, facilitating self-serve analysis by end users.