# HEA/IHM data collection guide for NERC upload

## Overview
- Dataset comprises raw Household Economy Approach (HEA) data from 16 communities in Katakwi district and raw Individual Household Method (IHM) data from 42 households in Anyangabella and 51 households in Kaikamosing.
- Collected in December 2020; documents crop calendars for the Katakwi district.
- Purpose: to support vulnerability analysis and livelihood impact modelling to inform targeted policies for resilience at household and community levels.

## Methodology

- HEA approach
  - Delimit rural livelihood zones based on land use, climate, rainfall, markets, and other economic information.
  - Identify a reference year (representative but not exceptional conditions) with input from local informants.
  - Purposively sample locations to reflect variation within zones.
  - Conduct village interviews to classify wealth groups (e.g., very poor, poor, middle, better-off) and establish typical household incomes and expenditures for the reference year.
  - Repeat interviews across sites to build a baseline dataset for simulating shocks and assessing access to food and basic non-food needs by wealth group.

- IHM approach
  - Identify livelihood zones and survey sites; collect contextual data from focus groups (men and women in different economic activities).
  - Interview selected households using a semi-structured format to capture all relevant income sources and details (demography, assets, crops, livestock, employment, wild foods, non-market transfers, and other household characteristics such as gender of head and education).
  - Enter data into open-IHM software in the field; perform in-field checks for internal consistency and disparities; revisit households or amend datasets as needed.
  - Outputs support vulnerability analysis and policy development for resilience.

- Data collection and QA
  - Field operations conducted by local Ugandan partners; data collected in local language and translated into English by the data collectors.
  - Open-IHM software used for data entry and immediate quality checks; anomalies trigger follow-ups.
  - Data include descriptive and quantitative components linked to crop calendars and livelihood activities, enabling rapid analysis for decision-makers.

## Data contents

- The dataset includes multiple CSV files detailing crop calendars from two communities (Anyangabella and Kaikamosing) and associated variables:
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
- Each file provides detailed explanations of its content, origin, and collection timing.
- The data capture a typical agricultural year’s production timelines, with sections dedicated to crops, livestock, employment, transfers, and wild foods, across fishing and crop communities.
- A note: if a cell is empty, that indicates no data available for that value.

## Data governance and sharing

- Data collection and processing are designed to support vulnerability assessment and policy development, with an emphasis on data quality and consistency.
- Metadata and provenance are embedded in the dataset structure (e.g., Explanation fields within files describe data origins and collection details).
- The dataset reflects careful field QA, with open-IHM in-field checks and revisits to rectify anomalies.
- Collected in local language and translated to English to support broader use; published materials reference the EfD methodology resources for HEA and IHM.

## Data provenance and access

- Data originated from the EfD (Evidence for Development) framework and resources:
  - HEA methodology details: http://efd.org/methods/the-household-economy-approach-hea/
  - IHM methodology details: http://efd.org/methods/the-individual-household-method-ihm/
- The information here was prepared as part of a dataset submitted for NERC upload, with local Ugandan partners responsible for data collection and translation.

## Purpose and policy relevance

- Enables assessment of vulnerability across wealth groups and livelihood strategies.
- Supports livelihood impact modelling to inform targeted policy responses at the household and community levels.
- Facilitates rapid, decision-relevant analysis for resilience planning and resource allocation.

## Notes

- The dataset records quantitative information on crop and fishing production timelines throughout a typical agricultural year.
- The documentation emphasizes that data quality checks are performed in the field, and that detailed explanations accompany each data file to aid interpretation.