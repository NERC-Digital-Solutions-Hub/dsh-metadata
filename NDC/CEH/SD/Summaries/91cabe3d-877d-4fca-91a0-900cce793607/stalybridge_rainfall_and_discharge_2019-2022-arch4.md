# Stalybridge Rainfall and Discharge 2019-2022

## Overview
- Dataset of rainfall and runoff from ten experimental microcatchments (A–J; 0.4–3.9 ha) on Stalybridge Moor, upland peatland in the UK.
- Timeframe: 2019–2022, capturing pre- and post-gully blocking to assess effects on storm flow.
- Study design: Before-After-Control-Intervention (BACI) to evaluate different gully blocking methods; microcatchments A, D, G, J serve as unrestored controls throughout the period.
- Purpose: Determine how gully blocking methods influence storm flow response and peak discharge.

## Experimental Design and Interventions
- Pre-intervention period: May 2019–March 2020.
- Gully blocking conducted 16–25 March 2020; post-intervention period thereafter.
- Dam designs varied by microcatchment:
  - B: 22 standard cobblestone dams.
  - C: 7 cobblestone (lower gully) + 13 peat dams (middle/upper).
  - E: 10 piped-peat dams (later modified).
  - F: 6 peat dams.
  - H: 6 peat dams.
  - I: 20 timber dams.
- Post-restoration design changes:
  - E (from 25/03/2020): open 150 mm pipe initially; later capped at 64 mm.
  - I (from 25/03/2020): timber dam slots reduced incrementally (first 150×40 mm, then 50×40 mm on later dams).

## Data Collection and Methods
- Measurements at microcatchment outlets using v-notch weirs; pressure transducers record water depth behind the weir.
- Barometric compensation applied using an above-water sensor to convert pressure to water depth.
- Rainfall recorded with tip-bucket gauges (0.2 mm per tip) at specific microcatchments; other locations patched from nearest available gauge when needed.
- Sampling interval: 5-minute timesteps; data loggers downloaded monthly.
- Field notes used to identify and omit spurious discharge data (e.g., vegetation in the weir) and mark as no data where appropriate.

## Data Processing and Units
- Discharge (Q): litres per second (L/s); derived from depth above the v-notch using calibration.
- Rainfall: millimetres (mm).
- Time coverage: continuous measurements from May 2019 to February 2022 (gaps due to instrument failure).
- Data are provided as CSV files per calendar year for each microcatchment, with consistent column structure:
  - DateTime (GMT)
  - Rainfall (mm)
  - Discharge (L/sec)

## Data Structure and Access
- File naming convention: [site]_[microcatchment]_[year]_rainfall_discharge.csv (e.g., stalybridge_e_2021_rainfall_discharge.csv).
- Geographic references:
  - V-notch weir locations (UK grid references provided for A–J).
  - Rain gauge locations provided (UK grid references for B, E, G, I).
- Calibration and QA:
  - Manual stageboard readings used to calibrate depth to discharge.
  - Visual QC across discharge records with rainfall context to identify anomalies; erroneous periods removed and marked as no data.

## Data Quality, Gaps, and Considerations for Use
- Irregular gaps due to instrument failure; some rainfall data patched from neighboring microcatchments when gauges failed.
- Post-intervention period includes changes to dam designs in E and I, which should be considered in analyses of pre/post effects.
- Data designed to support understanding of how gully-blocking strategies influence stormflow and peak discharge in upland peat systems.

## Relevance for Data Leaders
- Demonstrates end-to-end data lifecycle: sensor deployment, data collection at high temporal resolution, BACI-style experimental design, detailed metadata, and clear data products for reuse.
- Highlights the importance of documenting interventions and their timing, sensor calibration, and data quality controls to enable cross-site data integration and governance.
- Provides a ready-to-use, well-structured dataset for analyses of data availability, granularity, and the impact of management actions on hydrological responses in a broader network. 

## References
- Shuttleworth, E.L. et al. (2019) Rest Restoration of blanket peat moorland delays stormflow from hillslopes and reduces peak discharge. Journal of Hydrology X, 2, p. 100006.