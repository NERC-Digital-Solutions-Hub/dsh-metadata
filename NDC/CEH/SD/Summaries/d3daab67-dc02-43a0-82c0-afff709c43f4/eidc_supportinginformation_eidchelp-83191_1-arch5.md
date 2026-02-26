# Overview

## Purpose and scope
- Dataset of key operational parameters from a point-of-use drinking water treatment system (PAqua 1000D-2) operating continuously to provide safe drinking water.
- 34 months of data (1 November 2019 – 29 September 2022) from a field trial at the University of the West of England, Frenchay Campus.
- Part of the NERC project “The development and implementation of sensors and treatment technologies for freshwater systems in India” (NE/R003106/1); related datasets referenced (Fox et al., 2022; Clayton et al., 2024).

## Data collection and provenance
- Collected via in-line sensors and a Grundfos Remote Manager interface; data downloaded/interpreted by UWE Bristol researchers.
- System uses ultrafiltration and in-situ electrochemically generated hypochlorous acid dosing for disinfection.
- Industrial partner Portsmouth Aqua Ltd installed the telemetry monitoring; data uploaded to Grundfos Remote Manager; downstream analysis by researchers at UWE Bristol.
- Sporadic data availability between April and August 2020 due to a faulty SIM card; issue later resolved.

## Location and temporal coverage
- Site: POU DWTS on UWE Bristol Frenchay Campus (coordinates provided in the document).
- Coverage: 34 months of telemetry data from 1 November 2019 to 29 September 2022.

## Data structure and content
- File: pou-dwts_operationaltelemetrydata_uk_nov2019-sep2022.csv
- 8 data columns with the following fields:
  - Date: Date and time (dd/mm/yyyy hh:mm)
  - Flow_Rate: Flow rate (m3/hr)
  - Discharge_Pressure: Discharge pressure (bar)
  - TMP: Transmembrane pressure (bar)
  - ORP: Oxidation-reduction potential (mV)
  - FAC: Free available chlorine (ppm)
  - Filtration_Flux: Filtration flux (m3 m^-2 h^-1)
  - UF_MP: UF module permeability (m3 m^-2 bar^-1 h^-1)
- Data are recorded with 5-minute resolution (rolling 5-minute averages) and exported from Grundfos Remote Manager; 5-minute averaging applied to several parameters.
- Filtration Flux and UF Module Permeability are computed in Excel using documented formulas.
- Additional parameters were collected for the wider project but not included in this dataset.
- Instrumentation noted: s::can (chlorinity/ORP) and Messtechnik GmbH; Grundfos Remote Manager used for data capture.

## Data quality and quality control
- Weekly quality control checks (QA/QC) performed on pH, FAC, ORP, HOCl, and produced water to ensure measurements stay within thresholds; verify proper functioning of the remote monitoring system.
- Regular “health” checks by Portsmouth Aqua Ltd every 3–6 months.
- Data quality notes:
  - Missing values are designated as NA.
  - Zeros likely indicate the POU-DWTS was not running correctly.

## Data gaps, limitations, and caveats
- Notable data gap: April–August 2020 due to intermittent telemetry caused by the faulty SIM card.
- Some data quality indicators depend on external instrumentation; interpretive context provided by the accompanying documentation.
- The dataset represents a single site and system configuration; broader generalizability should be considered with the linked datasets.

## Access, metadata, and related materials
- Associated publications:
  - Clayton et al. (2024), Long-term trial of a community-scale decentralized point-of-use drinking water treatment system (PLOS Water).
  - Fox, Thorn, Clayton, Reynolds (2022), Operational and water quality data from a decentralised, low-maintenance drinking water treatment system trial (NERC EDS).
- Data provenance and stewardship notes:
  - Data captured via Grundfos Remote Manager; managed by Portsmouth Aqua Ltd; downloaded/interpreted by UWE Bristol.
  - Part of a larger data ecosystem with linked datasets and publications; consult DOIs/EDS records for access and context.

## Governance, stewardship, and reuse considerations
- Ownership and stewardship: industrial partner (Portsmouth Aqua Ltd) with involvement from Grundfos and UWE Bristol; tied to the NE/R003106/1 project.
- Practical reuse guidance:
  - Maintain metadata alignment (column names, units, instrument sources, and QC status).
  - Account for data gaps and missing values (NA) and potential non-running zeros.
  - Reference related datasets/publications for context and supplementary variables (e.g., additional parameters from the broader project).
  - Document any interruptions (e.g., SIM card outage) and update data provenance records accordingly.

## Key takeaways for data stewards
- The dataset provides a well-documented, time-series telemetry Record from a real-world POU DWTS, suitable for remote monitoring and system diagnosis studies, with clear quality control procedures and explicit data gaps.
- Ensure ongoing metadata completeness, provenance clarity, and cross-reference with related data collections and publications to aid discovery and reuse.