# SARS-CoV-2 qPCR and water chemistry data from wastewater at six sites in England and Wales between March and July 2020, with associated Covid-19 positive test and related-death data collated from other sources

## Overview
- Dataset describing SARS-CoV-2 RNA concentrations in wastewater at six UK sites (Wales and Northwest England) from March to July 2020, linked to local Covid-19 positive tests and related deaths.
- Aims to support environmental monitoring and policy performance assessment through standardized, comparable outputs.
- Data are Open Government Licence with citation required; DOI provided.

## Data content and structure
- Two CSV files:
  - data_table.csv: main wastewater dataset with weekly measurements and site metadata.
  - cases.csv: clinical testing data for the same period and sites.
- Key variables in data_table.csv:
  - Time and location: Week, Date, Site_Name.
  - Hydrology: Flow (m3 per day, population equivalent).
  - SARS-CoV-2 measurements: gc_100ml (N1), E_gene_100ml; Crass_gc_100; Crass_Recovery.
  - Water quality chemistry: NO3, NH4, PO4, pH, EC.
  - Public health context: Deaths, Deaths_100k, Daily_Cases_100k, Rolling_Sum_100k.
  - Population context: Population_Equivalent, Local_Authority_Population.
  - Data quality/flag: cov_class, cov_detect, E_class.
- Key variables in cases.csv:
  - Site_Name, Date, Local_Authority_Population, Daily_Cases, Cumulative_Cases, Rolling_Sum, Daily_Cases_100k, Rolling_Sum_100k, Week.
- Supplementary context describes how data were collected and processed (Section 3).

## Sampling and study design
- Six wastewater treatment plants (WWTPs) serving urban areas in Gwynedd, Cardiff, Liverpool, Manchester, the Wirral, and Wrexham; total population ~3 million PE.
- Sampling period: weekly grab samples from March–July 2020; Wirral site also collected as a 24-hour composite.
- Sampling window: weekday collections (08:00–09:00) to support temporal comparability.
- Treated effluent sampled periodically at the same times as influent.

## Laboratory methods and QA
- Wastewater processing:
  - Pasteurization (60°C, 90 min) for safety before analyses.
  - Concentration and nucleic acid extraction: centrifugation of influent; concentration to 500 µL; for effluent, tangential flow ultrafiltration followed by secondary concentration.
  - Internal control: murine norovirus (MNV) spiked into samples to monitor extraction and inhibition.
  - Nucleic acids extracted with NucliSENS MiniMag system; stored at -80°C; analyses performed in separate labs to minimize contamination risk.
- qPCR/qRT-PCR assays:
  - SARS-CoV-2 targets: N1 (and optionally E gene) using duplex/triplex qPCR/qRT-PCR.
  - CrAssphage used as a human fecal loading marker; quantified by singleplex qPCR.
  - Reactions run in duplicate; 5 µL of extracted RNA used per reaction; standards and negative controls included.
  - MNV recovery monitored; if recovery <1%, retesting with adjusted input, balancing sensitivity.
- Standards and assay details:
  - Serial dilutions spanning 10^5–10^0 genome copies used for quantification.
  - Primers/probes based on CDC and Corman et al. designs; detailed sequences and parameters provided.
  - Limit of detection (LoD) and limit of quantification (LoQ) previously established:
    - N1 LoD: 1.7 gc/µL; LoQ: 11.8 gc/µL.
    - E gene LoD: 3.8 gc/µL; LoQ: 25.1 gc/µL.
    - MNV LoD/LoQ: 3.1 gc/µL and 32.1 gc/µL respectively.
- Data quality assurance:
  - Duplicate analyses; use of controls to prevent/identify contamination.
  - Separate lab workflows to reduce cross-contamination risk.
  - CrAssphage data included to help normalize for human fecal loading and wastewater dilution effects.

## Data access, licensing and citation
- Data accessible via doi link: https://doi.org/10.5285/ce40e62a-21ae-45b9-ba5b-031639a504f7
- Licensed under the Open Government Licence (OGL).
- Required citation: Hillary et al. 2021, NERC Environmental Information Data Centre.

## Data integration and potential analyses for monitoring
- Combines environmental surveillance (wastewater SARS-CoV-2 RNA) with clinical indicators (daily cases, rolling sums, deaths) at the local authority level.
- Enables spatiotemporal analyses across six sites to:
  - Compare wastewater signal with clinical trends over time.
  - Explore associations between SARS-CoV-2 RNA concentrations and wastewater characteristics (flow, NO3/NH4/PO4, pH, EC).
  - Normalize SARS-CoV-2 signals using CrAssphage loading to account for population loading and dilution.
  - Support policy evaluation by linking environmental signals to public health outcomes.

## Limitations and considerations for analysts
- Sampling modality variability: one site used a 24-hour composite, others used grab samples; temporal representativeness may vary.
- Early-pandemic data: March–July 2020 period may reflect initial outbreak dynamics and testing practices.
- Analytical sensitivity: LoD/LoQ limits mean some low-concentration detections may be below quantification.
- Spatial scope: six sites across Wales and NW England; may limit generalizability to other regions or years.
- Data quality depends on accurate site/population metadata and correct linkage to local authority populations.

## Endnotes
- Data tables include both chemical and virological measurements alongside basic epidemiological context to support integrated environmental health monitoring and policy performance assessment.