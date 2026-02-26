# PULA water quality data folder

- Overview
  - Contains 25 CSV files, each representing one water quality indicator.
  - Indicators cover Total Organic Carbon (TOC), major ions, a suite of trace metals, arsenic, selenium, molybdenum, cadmium, lead, and stable water isotopes δD and δ18O.
  - Data collected February 2017 – May 2018 from groundwater (GW) and surface water (SW) in the Gaborone Reservoir catchment, south-west Botswana.
  - Part of the NERC-funded PULA project to evaluate impacts of extreme rainfall and flooding on water quality across spatially variable physiography.

- Indicators included
  - TOC; Cl, F, Br, SO4, K, Al, Ca, Fe, Mg, Na; P, Cr, Mn, Co, Ni, Cu, Zn, As, Se, Mo, Cd, Pb; δD; δ18O.

- Sampling design and scope
  - 287 sampling occasions across 41 days, concentrated around ~15 campaigns.
  - Sampling aimed to span flood-drought-flood cycles; locations chosen to cover spatial variability and practical accessibility.
  - SW samples: grab samples from reservoirs/streams. GW samples: pumped grab samples after flushing wells.
  - Two samples collected per analysis type per occasion (for re-runs if needed).

- Collection, transport, and handling
  - Field allocation:
    - 2 × 30 mL for P, Cr, Mn, Co, Ni, Cu, Zn, As, Se, Mo, Cd, Pb (acidified with 5% HNO3 in the field).
    - 2 × 15 mL for TOC.
    - 2 × 10 mL for Al, Ca, Fe, K, Mg, Na.
  - Samples labeled in the field; data collection log kept for local sampling conditions.
  - Samples refrigerated and shipped from Botswana DWA to University of Aberdeen in 4 batches; analyses performed promptly upon arrival.

- Analytical methods and instrumentation
  - P, Cr, Mn, Co, Ni, Cu, Zn, As, Se, Mo, Cd, Pb: analyzed via Agilent 7900 ICP-MS (University of Aberdeen, Chemistry).
  - Al, Ca, Fe, K, Mg, Na: analyzed via MP-AES (University of Aberdeen, Biological Sciences).
  - TOC: measured with LABTOC (University of Aberdeen, Biological Sciences).
  - Stable isotopes (δD, δ18O): analyzed with TWIA-45-EP LGR (University of Aberdeen, Geosciences).
  - Analyses conducted following standard procedures for each instrument.

- Calibration, quality control, and data quality
  - Calibration ranges and detection limits provided for each parameter (with some parameters NA for certain periods).
  - Some data points exceeded maximum calibration or fell below detection limits; interpretation should consider these QC notes.
  - Pb data largely incomplete due to methodological shortcomings; many samples reported as below detection (shown as <LOD in CSV).
  - Data files annotate results as <LOD where applicable.
  - Field and lab QA/QC details are documented; caution advised when comparing values near detection/calibration limits.

- Data structure and format
  - Each of the 25 CSV files starts with a header row describing columns.
  - Columns include: water type (SW or GW), sampling location name (Botswana DWA nomenclature), longitude, latitude, elevation (m), followed by sampling dates (dd/mm/yy).
  - Coordinates provided in UTM; latitude/longitude in decimal degrees; elevation in metres.
  - Blank cells indicate no value recorded.
  - Spatial coverage and sampling dates vary across campaigns.

- Time frame and data processing
  - Data analyzed in phases across 2017 and 2018: pre-June–July 2017; June–July 2017; August–Nov 2017; January–May 2018.
  - Analyses and re-runs coordinated to align cumulative batches; final data reflect processing timeline described in the project notes.

- Reuse and monitoring relevance
  - Provides standardized, multi-parameter water quality snapshots over a defined flood-drought cycle in a geologically and land-use diverse catchment.
  - Suitable for trend analysis, cross-parameter comparisons, and integration with other environmental datasets.
  - Emphasizes need to couple datasets for enhanced value and to enable broader access to underlying data used to generate final outputs.