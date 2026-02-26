# Overview

- Purpose and scope
  - Dataset of key operational parameters for a point-of-use drinking water treatment system (POU DWTS), PAqua 1000D-2, using ultrafiltration and in-situ electrochemically generated hypochlorous acid dosing for disinfection.
  - Collected during a long-term, continuous operation aimed at providing biologically safe drinking water.

- Location and time frame
  - POU DWTS located at the University of the West of England, Frenchay Campus (coordinates: N51.498888, W2.544166).
  - Data span: 1 November 2019 to 29 September 2022 (34 months).

- Data source and collection
  - Operational telemetry from in-line sensors and probes uploaded to the Grundfos Remote Manager interface.
  - Data collected every 5 minutes to provide rolling 5-minute averages.
  - Industrial partner Portsmouth Aqua Ltd configured monitoring; researchers at UWE Bristol downloaded and interpreted data.
  - Sensors used include s::can, Messtechnik GmbH, Austria; data recorded via Grundfos Remote Manager.

- Data gaps and quality
  - Sporadic data availability between April and August 2020 due to a faulty SIM card; resolved with a replacement.
  - Missing values marked as 'NA'; a value of 0 likely indicates the system was not running.
  - Weekly quality checks on pH, free available chlorine (FAC), and oxidation-reduction potential (ORP) of HOCl and produced water; system health checks every 3–6 months by Portsmouth Aqua Ltd.

- Data structure and content
  - The dataset comprises 8 columns (Table 2) in the file pou-dwts_operationaltelemetrydata_uk_nov2019-sep2022.csv:
    - Date: Date and time (dd/mm/yyyy hh:mm)
    - Flow_Rate: Flow rate (m3/hr)
    - Discharge_Pressure: Discharge pressure (bar)
    - TMP: Transmembrane pressure (bar)
    - ORP: Oxidation-reduction potential (mV)
    - FAC: Free available chlorine (ppm or mg/L)
    - Filtration_Flux: Filtration flux (m3 m-2 h-1), calculated in Excel
    - UF_MP: UF module permeability (m3 m-2 bar-1 h-1), calculated in Excel
  - Filtration flux and UF module permeability are derived via specific Excel formulas (provided in the documentation).

- Related data, methods, and provenance
  - Part of wider NERC project: The development and implementation of sensors and treatment technologies for freshwater systems in India (NE/R003106/1).
  - Related publications:
    - Clayton et al. (2024): Long-term trial of a community-scale decentralized point-of-use drinking water treatment system (PLOS Water).
    - Fox et al. (2022): Operational and water quality data from a decentralised, low-maintenance drinking water treatment system trial (NERC EDS Environmental Information Data Centre).

- Data structure and access notes
  - The dataset focuses on core operational telemetry parameters; additional parameters exist in the wider project but are not included in this dataset.
  - Data were collected and stored via the Grundfos Remote Manager interface, with interpretation performed by UWE Bristol researchers.