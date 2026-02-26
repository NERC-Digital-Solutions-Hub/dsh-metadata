# Fish abundance, habitat, water quality, flow and climate in English Rivers from 1975-2017

## Overview
- Dataset describing fish abundance and associated environmental variables (habitat, water quality, flow, climate) in English rivers from 1975 to 2017.
- Focuses on extracting chemical statistics for chemical determinand locations chosen to minimize distance and maximize data coverage from NFPD fish sites; statistics pertain to the 12-month period immediately before each fish survey.

## Access, authors and funding
- Authors: Rachel Ainsworth (University of Hull) and Virginie Keller (UK CEH), with co-authors including researchers listed in the data citation.
- Date/scope: Data collection conducted between 2021-01 and 2022-05; geographic focus is England.
- Funding: NERC Chempop grant NE/S000100/2.
- Licensing and access:
  - Uses Environment Agency Water Quality Archive (Beta) data; some water quality determinand data cannot be included due to licensing restrictions.
  - Public data location: https://environment.data.gov.uk/water-quality/view/landing
  - Dataset citation: Ainsworth et al. (2024). Fish abundance, habitat, water quality, flow and climate data from English rivers, 1975-2017. NERC EDS Environmental Information Data Centre. DOI: https://doi.org/10.5285/b0afb78e-a0cb-4762-9220-659211ae3a5e

## Data content and structure
- File format: Region_FISHWIMSStats_DET.csv per region; one file per chemical determinand.
- Variables: 18 per file (example core fields include):
  - Fish_SiteID, Fish_SurveyDate, W1_SMPT_REF
  - Water quality summaries with three LOQ handling schemes:
    - WQ_Min_LOQ1/LOQ2/LOQ3, WQ_Max_LOQ1/LOQ2/LOQ3, WQ_Median_LOQ1/LOQ2/LOQ3, WQ_Mean_LOQ1/LOQ2/LOQ3, WQ_STD_LOQ1/LOQ2/LOQ3
  - WQ_Count, WQ_COUNT_L_LOQ, WQ_COUNT_G_LOQ
- Determinands: 41 chemicals (paired to determinand data via DET_CODE/DET_DESC/DET_Label and Max_Concentration). Full chemical listing available in supporting documentation.
- Data relationships: Fish_SiteID links to Fish_SiteID in fish DataTable, Hydrology and chemical determinand datasets.
- Data exclusions: Some sites with sensitive data omitted; some chemical data restricted by licensing.

## Methods and processing
- Site selection:
  - For each fish site, nearest three chemical determinand sites were identified using Arc Toolbox Near Table Generator.
  - Manual checks ensured suitability: same river or comparable order, temporal overlap with fish sampling (allowing a 2-year window), and reasonable distance.
- Data extraction:
  - Chemical data sourced from Environment Agency Water Quality data portal for a defined list of 41 chemicals.
- Temporal framing:
  - Statistics computed for the preceding 12-month period before the fish survey date.
- Data processing and calculations:
  - Aggregated data temporally after extraction.
  - For metals, a maximum threshold concentration of 10 mg/L was applied; values above thresholds were discarded.
  - Handling of values below the Limit of Quantification (LoQ) considered three approaches:
    - LoQ treated as LoQ
    - LoQ treated as 0
    - LoQ treated as LoQ/2
  - Statistics computed per fish site: minimum, maximum, median, mean, standard deviation, plus counts (total samples, samples below LoQ, samples above LoQ).
- Standards and QA:
  - ArcGIS (v10.7+ or Pro) used for site matching; Python 3 with math, pandas, numpy, itertools, datetime, dateutil, os, time, shutil for data extraction and statistics.
  - QA: chemical matching checked by Monika Jurgens.
  - Personnel involved: Monika Jurgens, Rachel Ainsworth, Virginie Keller, Nuria BachellerJareno.
- Data governance:
  - Metadata quality considerations addressed; some datasets required adding metadata or public-sharing constraints.
  - Datasets must meet openness and data management standards at source; licensing restrictions influence availability.

## Data structure and specifics
- Regional datasets:
  - Each region contains Region_FISHWIMSStats_DET.csv, with 18 variables describing the chemical statistics for each fish site and determinand.
- Determinant metadata:
  - DET_CODE, DET_DESC, DET_Label define each determinand; Max_Concentration provides plausible concentration bounds for filtering during statistics calculations.
- Data formats and codes:
  - LoQ handling codes and multiple LOQ options are embedded in the 18 variables, along with sample counts and quality indicators.

## Quality, limitations, and usage notes
- Limitations:
  - Some water quality data are not included due to licensing restrictions.
  - Omission of sensitive sites and potential gaps in metadata or access to certain datasets.
- Practical considerations:
  - Values below LoQ and the LOQ treatment method can influence statistics; users should be aware of how LOQ handling choices affect results.
  - Temporal and spatial matching criteria emphasize careful interpretation when linking fish data to chemical determinands.

## How this fits monitoring framework objectives
- Aligns with aims to identify environmental health measures for scrutinising and evaluating policy and informing future decisions.
- Demonstrates:
  - Stakeholder- and expert-informed measure selection and data verification.
  - Data discovery, metadata enhancement, and efforts to ensure data quality and openness at the source.
  - Data governance, dissemination of outputs, and stakeholder consultation.
  - Handling of data access barriers, licensing constraints, and the need for clear communication of complex statistical results.