# Overview

- This dataset captures key operational parameters of a point-of-use drinking water treatment system (POU DWTS), PAqua 1000D-2, operated to deliver biologically safe drinking water. The system uses ultrafiltration and in-situ electrochemically generated hypochlorous acid (HOCl) dosing for disinfection.
- Data span: 34 months from 1 November 2019 to 29 September 2022, collected at the University of the West of England (Frenchay Campus) and uploaded via the Grundfos Remote Manager interface.
- Purpose: long-term monitoring and remote diagnostics to assess system function, maintain water quality, and support the wider NERC project on sensors and treatment technologies for freshwater systems.

## Data collection and sensors

- Telemetry captured from Grundfos pumps and in-line sensors (s::can, Messtechnik GmbH, Austria); data uploaded to the Grundfos Remote Manager (GRM).
- Data collection cadence: every 5 minutes, with results stored as rolling 5-minute averages.
- Collaborators: Portsmouth Aqua Ltd set up monitoring; UWE Bristol downloaded and interpreted data; part of the NERC project NE/R003106/1; additional dataset available (Fox et al., 2022).

## Time span, data granularity, and gaps

- Time span: 2019-11-01 to 2022-09-29.
- Data granularity: 5-minute rolling averages for operational parameters.
- Data gaps: sporadic missing data between April and August 2020 due to a faulty SIM card; replacement fixed the issue. Missing values are labeled 'NA'; 0 is interpreted as the system not running correctly.

## Variables, units, and derived metrics

- Key operational parameters (Table 1 in accompanying documentation):
  - Date and Time: dd/mm/yyyy hh:mm
  - Flow rate: m3/h
  - Discharge pressure: bar
  - Transmembrane pressure (TMP): bar
  - Oxidation reduction potential (ORP): mV
  - Free available chlorine (FAC): ppm (mg/L)
  - Filtration flux: m3 m-2 h-1 (derived in Excel)
  - UF module permeability: m3 m-2 bar-1 h-1 (derived in Excel)
- Derived metrics:
  - Filtration Flux and UF Module Permeability calculated using specified formulas in Excel (provided in the dataset documentation).

## Quality control and data integrity

- Weekly quality control checks on pH, FAC, HOCl, and ORP for disinfectant and produced water; checks to ensure GRM data was accurately recorded.
- Regular health checks (every 3–6 months) performed by Portsmouth Aqua Ltd to ensure system health and data integrity.

## Data structure and metadata

- Dataset file: pou-dwts_operationaltelemetrydata_uk_nov2019-sep2022.csv
- Structure: 8 columns corresponding to Date/Time, Flow_Rate, Discharge_Pressure, TMP, ORP, FAC, Filtration_Flux, UF_MP
- Data provenance: collected via GRM, recorded by in-line sensors and pumps; dataset is part of the NERC project and linked to publications describing the long-term trial and data release.

## Data access, provenance, and related publications

- Related publications:
  - Clayton, G.E., Thorn, R.M.S., Fox, B.G., Reynolds, D.M. (2024). Long-term trial of a community-scale decentralized point-of-use drinking water treatment system. PLOS Water, 3(4): e0000187.
  - Fox, B.G., Thorn, R.M.S., Clayton, G.E., Reynolds, D.M. (2022). Operational and water quality data from a decentralised, low-maintenance drinking water treatment system trial, UK, November 2019 to February 2020. NERC EDS Environmental Information Data Centre.
- Data provenance: industrial collaboration with Portsmouth Aqua Ltd; data collection and monitoring via Grundfos Remote Manager; researchers at UWE Bristol responsible for downloading/interpreting data.

## Potential analytic uses for Analysts

- Identify correlations and time-lag relationships between flow rate, pressures (discharge and TMP), disinfection indicators (ORP, FAC), and filtration performance (filtration flux, UF permeability).
- Develop predictive models for system performance, maintenance needs, or disinfection efficacy under field conditions.
- Compare long-term trends with system health checks and remote diagnostics to optimize operation and scheduling.
- Validate hypotheses about decentralized POU DWTS performance and reliability using a large, real-world time-series dataset.