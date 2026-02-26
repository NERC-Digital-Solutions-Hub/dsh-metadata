# Overview

- A dataset of key operational parameters from a point-of-use drinking water treatment system (POU DWTS), PAqua 1000D-2, operating on ultrafiltration with in-situ electrochemically generated hypochlorous acid dosing for disinfection.
- Collected from a POU DWTS at the University of the West of England, Frenchay Campus, over 34 months (1 Nov 2019 – 29 Sep 2022).
- Telemetry via the Grundfos Remote Manager interface, with data recorded as rolling 5-minute averages from in-line sensors and probes.
- Study conducted under the wider NERC project “The development and implementation of sensors and treatment technologies for freshwater systems in India” (NE/R003106/1); additional dataset available (Fox et al., 2022).
- Industrial partner Portsmouth Aqua Ltd installed telemetry monitoring; UWE Bristol researchers downloaded and interpreted the data.
- Sporadic data availability between April–August 2020 due to a faulty SIM card (resolved with a new SIM card); missing values are marked as NA; 0 may indicate the system was not running correctly.

## Data scope and purpose

- Aimed at diagnosing system performance, monitoring operation remotely, and supporting maintenance decisions.
- Data supports understanding how the treatment system functioned over a long-term trial and enables analysis of operational stability and water quality outcomes.

## Data collection and generation

- Instrumentation: in-line sensors (s::can, Messtechnik GmbH, Austria) and Grundfos Remote Manager interface; data collected from Grundfos pumps and sensors.
- Data cadence: 5-minute intervals, with values averaged over each window.
- Period and site: 1 Nov 2019 – 29 Sep 2022, University of the West of England, Frenchay Campus.
- Data management: industrial partner set up telemetry; UWE Bristol downloaded and interpreted data.
- Notable data issue: April–August 2020 data gaps due to a faulty SIM card; issue rectified later.

## Nature and units of recorded values

- Date and Time: dd/mm/yyyy hh:mm.
- Flow_Rate: m3/hr.
- Discharge_Pressure: bar.
- TMP (Transmembrane Pressure): bar.
- ORP (Oxidation Reduction Potential): mV.
- FAC (Free Available Chlorine): ppm (mg/L).
- Filtration_Flux: m3 m^-2 h^-1 (calculated in Excel).
- UF_MP (UF Module Permeability): m3 m^-2 bar^-1 h^-1 (calculated in Excel).
- Additional parameters were recorded for the broader NERC project but are not included in this dataset.
- Filtration Flux and UF_MP calculations rely on specific Excel formulas described in the data notes.

## Quality control

- Weekly quality control checks on key parameters (pH, FAC, HOCl/ORP) and overall system health, ensuring values stayed within thresholds and that Grundfos Remote Manager was recording correctly.
- 3–6 month “health” checks by Portsmouth Aqua Ltd to ensure ongoing proper operation.

## Data structure

- The dataset comprises 8 columns as detailed in Table 2:
  - Date (Date and Time)
  - Flow_Rate (m3/hr)
  - Discharge_Pressure (bar)
  - TMP (Transmembrane Pressure, bar)
  - ORP (mV)
  - FAC (ppm)
  - Filtration_Flux (m3 m^-2 h^-1)
  - UF_MP (m3 m^-2 bar^-1 h^-1)
- Data is recorded via Grundfos Remote Manager; missing values are indicated as NA, and a value of 0 likely indicates the system was not running.
- The 5-minute rolling average was used for all reported values.

## Provenance and availability

- Part of the NE/R003106/1 project; broader data and related publications available:
  - Clayton et al. (2024): Long-term trial of a community-scale decentralized point-of-use drinking water treatment system (PLOS Water).
  - Fox et al. (2022): Operational and water quality data from a decentralised, low-maintenance drinking water treatment system trial (NERC EDI Centre).
- Primary data collection and hosting involved Grundfos Remote Manager and collaboration between industrial partner and UWE Bristol researchers.
- Data may be accompanied by additional datasets in the referenced works.

## References

- Clayton GE, Thorn RMS, Fox BG, Reynolds DM (2024). Long-term trial of a community-scale decentralized point-of-use drinking water treatment system. PLOS Water.
- Fox BG, Thorn RMS, Clayton GE, Reynolds DM (2022). Operational and water quality data from a decentralised, low-maintenance, drinking water treatment system trial, UK, November 2019 to February 2020. NERC EDS Environmental Information Data Centre.