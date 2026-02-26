# Experimental Design

## Overview
- Cross-sectional, interviewer-administered survey to assess potential exposure to antibiotic-resistant bacteria from livestock, poultry, and the environment.
- Also assesses human and poultry antibiotic use.
- Settings: rural households and rural poultry farms (broiler farms) in Mirzapur, Tangail district; urban food markets in Dhaka, Bangladesh.

## Study design and sampling
- Participants selected to represent different exposure levels:
  - Rural villages, low exposure: households without domestic poultry (n=20)
  - Rural villages, high exposure: households owning domestic poultry (n=20)
  - Rural poultry farms, low exposure: non-poultry farm workers (n=40)
  - Rural poultry farms, high exposure: poultry farm workers (n=40)
  - Urban markets, low exposure: fruit and vegetable sellers (n=40)
  - Urban markets, high exposure: live poultry sellers and slaughterers (n=40)
- Rural households: 20 villages; within each village, one poultry-owning and one non-poultry-owning household (total n=40).
- Farms: 40 broiler farms; one farm worker per farm (n=40).
- Baseline low-exposure adults: healthy adults from the same villages as farm workers (n=40).

## Data collection methods
- Trained icddr,b researchers conducted surveys in Bangla; responses recorded on paper and translated to English for data entry.
- Phase 1 data collection: February–April 2017; Phase 2: August–October 2017.

## Ethics and consent
- Written informed consent obtained from all participants with right to withdraw.
- Ethical approvals: International Centre for Diarrhoeal Disease Research, Bangladesh (PR16071) and Loughborough University (R17-P037).

## Data quality control
- Data translated to English and entered into Excel.
- Random checks against original data sheets by an independent researcher.
- Frequency checks to identify and correct out-of-range or erroneous values.

## Data structure
- Three CSV data files:
  - ruralhouseholdsurvey.csv
  - poultryfarmsurvey.csv
  - urbanmarketsurvey.csv
- Blank cells indicate no data recorded.
- Supporting data-structure documentation (column headings) available as:
  - Ruralsurveydatastructure.rtf
  - Farmsurveydatastructure.rtf
  - Marketsurveydatastructure.rtf

## GIS relevance and considerations
- Data are suitable for map-based analyses once locations (geocoded households, farms, and markets) are available.
- Requires harmonization across datasets with different resolutions and careful handling of privacy and missing data.
- Provenance and QA steps (translation, data-entry checks) support reliable geospatial data preparation.