# pou-dwts_operationaltelemetrydata_uk_nov2019-sep2022.csv

- Overview
  - Dataset of key operational parameters from a point-of-use drinking water treatment system (PAqua 1000D-2) operated continuously to provide biologically safe drinking water.
  - Data collected over 34 months (1 November 2019 – 29 September 2022) at the University of the West of England, Frenchay Campus.
  - Monitoring based on ultrafiltration with in-situ electrochemically generated hypochlorous acid dosing for disinfection; data recorded via in-line sensors and uploaded to the Grundfos Remote Manager interface.
  - Industrial partner Portsmouth Aqua Ltd supported telemetry setup; UWE Bristol researchers downloaded and interpreted data.

- System description and scope
  - PAqua 1000D-2 uses ultrafiltration and HOCl dosing for disinfection.
  - Telemetry enables remote diagnosis of maintenance issues and system function.
  - Location coordinates: N51°29′56″, W2°32′39″.

- Timeframe, data source, and accessibility
  - Data collected via Grundfos Remote Manager; 5-minute rolling averages.
  - Sensors: in-line sensors and probes (s::can, Messtechnik GmbH, Austria).
  - Data gaps: sporadic data from April–August 2020 due to a faulty SIM card; resolved by replacement.
  - Data quality signals: missing values marked as NA; zeros likely indicate the system was not running.

- Data structure and content
  - Contains 8 data columns (A–H) detailed in Table 2 of the source document.
  - Key parameters captured:
    - Date and Time (dd/mm/yyyy hh:mm)
    - Flow_Rate (m3/hr)
    - Discharge_Pressure (bar)
    - TMP – Transmembrane Pressure (bar)
    - ORP – Oxidation Reduction Potential (mV)
    - FAC – Free Available Chlorine (ppm)
    - Filtration_Flux (m3 m-2 h-1)
    - UF_MP – UF Module Permeability (m3 m-2 bar-1 h-1)
  - Filtration flux and UF module permeability were calculated in Excel:
    - Filtration Flux = (Feed Flow × 100) / (A × B) [per Table 2 and Equation 1 in the source]
    - UF_MP = Filtration parameters (G) / TMP (D) [per Equation 2 in the source]

- Quality control and data governance
  - Weekly quality control checks on pH, FAC, HOCl (ORP), and produced water to ensure values stay within thresholds; verification of Grundfos Remote Manager data recording.
  - Health checks by Portsmouth Aqua Ltd every 3–6 months to ensure system performance.
  - Part of the NERC project “The development and implementation of sensors and treatment technologies for freshwater systems in India” (NE/R003106/1).
  - Data stewardship: collected by industrial and academic partners; researchers at UWE Bristol downloaded and interpreted data.
  - Related publications:
    - Clayton et al. (2024) Long-term trial of a community-scale decentralized point-of-use drinking water treatment system (PLOS Water).
    - Fox et al. (2022) Operational and water quality data from a decentralised, low-maintenance drinking water treatment system trial (NERC Environmental Information Data Centre).
  - Data structure and metadata support via associated datasets and DOIs; data suitable for monitoring and evaluation, with emphasis on data provenance and linkage to broader studies.