# HEA/IHM data collection guide for NERC upload

## Overview
- Dataset combines raw HEA data from 16 rural livelihood zones in Katakwi district and raw IHM data from Anyangabella (42 households) and Kaikamosing (51 households), collected in December 2020.
- Focuses on crop calendars and livelihoods for vulnerability analysis and policy guidance.

## Methodology

- HEA (Household Economy Approach)
  - Delineates rural livelihood zones based on land use, climate, rainfall, markets, and other economic factors.
  - Identifies a reference year with typical conditions in consultation with local informants.
  - Purposively samples locations to represent variation within zones.
  - Conducts village interviews with knowledgeable representatives to define wealth-group characteristics.
  - Conducts focus-group interviews across wealth groups to establish typical incomes and expenditures for the reference year.
  - Builds a baseline dataset to simulate impacts of shocks on access to food and basic needs.

- IHM (Individual Household Method)
  - Identifies livelihood zones and selects survey sites within zones; gathers contextual economic information via focus groups.
  - Interviews selected households to cover all relevant income sources and related details (demography, assets, production, employment, wild foods, non-market transfers).
  - Records characteristics such as gender of household head and education levels.
  - Data entered into open-IHM software; undergoes in-field checks for consistency and alignment with observed living conditions.
  - Anomalies trigger revisits and potential dataset amendments.

## Data content and scope
- Quantitative data on crop and fishing production timelines across a typical agricultural year.
- Two village datasets: Anyangabella (fishing community) and Kaikamosing (crop community).
- Data files cover:
  - Interview details (fishing and livestock)
  - Crops grown and their proportions
  - Livestock details
  - Employment types and proportions
  - Transfers and wild foods
- Cells may be empty where data are not available.

## Data files and structure
- Interrelated crop calendar files and accompanying metadata:
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
- Each file provides details on data origin, collectors, timing, and what the data represents; two datasets reflect fishing versus crop communities.

## Data quality and validation
- Data collection conducted in the local language and translated into English by the data collectors.
- Field use of open-IHM software enables real-time data checking and consistency checks.
- Anomalies prompt revisits and potential amendments to ensure data integrity.

## Purpose and usage
- Designed to support analysis of vulnerability levels and livelihood impact modelling.
- Aims to inform targeted policy and resilience-building measures at both household and community levels.

## Provenance and references
- Based on methods from the Evidence for Development (EfD) resources:
  - The Household Economy Approach (HEA)
  - The Individual Household Method (IHM)
- Data collected by local Ugandan partners; sources cited with EfD URLs (accessed 24/03/2021).