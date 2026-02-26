# HEA/IHM data collection guide for NERC upload

## Overview
- Dataset arising from HEA and IHM studies conducted in December 2020.
- Focus: crop calendars and related livelihood data for Katakwi district (16 communities) and two village-based household samples (Anyangabella: 42 households; Kaikamosing: 51 households).
- Collected to analyze vulnerability and support livelihood resilience policies at household and community levels.
- Data collected in local language and translated into English by the data collectors.

## Data provenance and collection context
- Geographic scope: Katakwi district; two village sites for IHM component.
- Timeframe: December 2020.
- Data collectors: local Ugandan partners; translations performed by collectors.
- Purpose: support vulnerability analysis, economic shock simulations, and targeted policy development.

## Methodology
- HEA (Household Economy Approach):
  - Demarcate rural livelihood zones using land use, climate, rainfall, markets, and other economic factors.
  - Identify a recent reference year and purposively select sample locations representing variation within zones.
  - Conduct village interviews to classify wealth groups and establish typical household incomes/expenditures for the reference year.
  - Repeat interviews across zones to build a baseline dataset for shock impact simulations.
- IHM (Individual Household Method):
  - Identify livelihood zones and select survey sites; collect contextual economic information via focus groups (including both women and men in different activities).
  - Interview selected households (semi-structured) covering demography, assets, crop/livestock production, employment, wild foods, transfers, and other relevant characteristics.
  - Data entered into Open-IHM software, checked for internal consistency, biological adequacy, and alignment with observed living conditions.
  - Revisit households or amend datasets as needed to address anomalies.

## Data structure and contents
- Dataset contains quantitative crop calendar information across a typical agricultural year.
- Files (examples and purposes):
  - Crop_Calendar_Fishing_Interview_details.csv
  - Crop_Calendar_Livestock_Interview_details.csv
  - Crop_Calendar_Livestock_Crops.csv
  - Crop_Calendar_Fishing_Crops.csv
  - Crop_Calendar_Fishing_LS.csv
  - Crop_Calendar_Livestock_LS.csv
  - Crop_Calendar_Fishing_EMP.csv
  - Crop_Calendar_Livestock_EMP.csv
  - Crop_Calendar_Fishing_TRANSFERS.csv
  - Crop_Calendar_Livestock_TRANSFERS.csv
  - Crop_Calendar_Fishing_WILD_FOODS.csv
  - Crop_Calendar_Livestock_WILD_FOODS.csv
- Each file describes data sources, who collected the data, and when; where relevant, it explains what types of crops, employment, transfers, and wild foods are captured and their seasonal proportions.
- Notation: missing cells indicate no data for that value.

## Data quality, validation, and governance
- Data capture and initial validation:
  - Field data entered into Open-IHM software with in-field checks for consistency and realism.
  - Cross-checks with contextual information from focus groups and observed living conditions.
  - Anomalies trigger revisits to households or dataset amendments.
- Documentation and metadata:
  - Metadata includes origins, data collectors, and collection dates.
  - Data are accompanied by explanations clarifying the source and scope of each file.
- Versioning and updates:
  - Data are designed to support ongoing analysis and potential updates as part of vulnerability modelling and policy development.

## Access, sharing, and usage considerations
- Intended for uploading to data portals (NERC-related) and for discoverability by researchers and practitioners.
- Data are household- and community-level; appropriate governance and ethical considerations should guide sharing and use.
- Users should consult the accompanying metadata to understand scope, sample sizes, and collection context.
- Cells may be empty where data did not exist for a given variable or site.

## Limitations and caveats for reuse
- IHM coverage is limited to two villages for the household component, with broader HEA data across 16 communities in Katakwi.
- Data collected in local language and translated; potential translation nuances should be considered in secondary analyses.
- Interoperability considerations due to multiple file types and formats; consistent interpretation relies on accompanying explanations within each file.