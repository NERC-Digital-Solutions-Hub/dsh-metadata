# Fish abundance, habitat, water quality, flow and climate in English Rivers from 1975-2017

## General Information
- This dataset contains extracted chemical statistics for chemical determinand locations selected by minimised distance and maximum data along the network from NFPD fish sites.
- Determinands are calculated for the antecending period immediately prior to the biota (fish) survey date, set to 12 months for fish.
- Geographic scope: England; data collection period stated as 2021/01 to 2022/05/27.
- Authors: Rachel Ainsworth (University of Hull) and Virginie Keller (UK CEH).
- Funding: NERC Chempop grant NE/S000100/2.
- Data collection date range and geographic context indicate integration of fish survey data with nearby chemical determinands.

## Data & File Overview
- File structure: Each regional folder contains one file per chemical, named Region_FISHWIMSStats_DET.csv (18 variables per file; 41 chemicals total referenced in supporting documentation).
- Relationship: Fish_SiteID links to Fish_SiteID in the DataTable, Hydrology, and chemical determinand files.
- Access: Uses Environment Agency Water Quality Archive (Beta); some water quality determinand data cannot be included due to licensing restrictions; publicly accessible at https://environment.data.gov.uk/water-quality/view/landing.
- Data provenance: No data derived from other sources; citation provided for the dataset (Ainsworth et al., 2024) with DOI: https://doi.org/10.5285/b0afb78e-a0cb-4762-9220-659211ae3a5e
- Supporting data: List of chemicals available in the Supporting Documentation.

## Methodological Information
- Data selection and matching:
  - Arc Toolbox Near Table Generator used to identify the nearest three chemical determinand sites for each fish site.
  - Determinand sites were manually checked against predetermined criteria (river, order, proximity to sewage treatment works, and temporal overlap) and required at least 25 samples.
  - Chemical determinand sites must have temporal overlap with fish sampling dates within a 2-year allowance.
- Data extraction:
  - Chemical data extracted from the EA Water quality data portal for a defined list of 41 chemicals (as described in supporting docs).
- Data processing:
  - Statistics calculated for the 12-month period immediately preceding the fish survey date.
  - Temporal aggregation of data; for some determinands (notably metals), a maximum threshold concentration of 10 mg/L was applied; values above this threshold were discarded.
  - Values below the Limit of Quantification (LoQ) are handled with three options (LoQ1, LoQ2, LoQ3) across all statistics (min, max, median, mean, std dev) and associated counts.
- Tools and software:
  - ArcGIS (Version 10.7 or later or Pro) for site matching.
  - Python 3 with modules: math, pandas, numpy, itertools, datetime, dateutil, os, time, shutil for data extraction and statistics.
- Quality assurance:
  - Chemical matching validated by Monika Jurgens.
- Personnel:
  - Monika Jurgens, Rachel Ainsworth, Virginie Keller, Nuria BachellerJareno.

## Data-Specific Information
- File contents:
  - Each regional file contains 18 variables describing statistics for each fish site and determinand.
  - Key variables include:
    - Fish_SiteID
    - Fish_SurveyDate
    - W1_SMPT_REF
    - WQ_Min_LOQ1/LOQ2/LOQ3
    - WQ_Max_LOQ1/LOQ2/LOQ3
    - WQ_Median_LOQ1/LOQ2/LOQ3
    - WQ_Mean_LOQ1/LOQ2/LOQ3
    - WQ_STD_LOQ1/LOQ2/LOQ3
    - WQ_Count
    - WQ_COUNT_L_LOQ
    - WQ_COUNT_G_LOQ
- Determinand metadata:
  - DET_CODE: unique determinand code used in WIMS
  - DET_DESC: brief determinand description
  - DET_Label: succinct determinand label for CHEMPOP file naming
  - Max_Concentration: maximum plausible concentration within the project unit; values above are discarded from statistics
- Data constraints:
  - Some site data excluded due to licensing restrictions.
  - The dataset explicitly documents the maximum concentration handling and LOQ treatment to standardise outputs.

## Access, Licensing & Citations
- Licensing: Environment Agency water quality data from the Water Quality Archive (Beta). All rights reserved; some data restricted due to licensing.
- Public portal: https://environment.data.gov.uk/water-quality/view/landing
- Citation: Ainsworth, R.F.; Keller, V.; Bachiller- Jareno, N.; Jürgens, M. D.; Eastman, M.; Sadykova, D; Rizzo, C.; Scarlett, P.; Peirson, G.; Eley, F.; Antoniou, V.; Cowx, I.G.; Johnson, A.C.; Nunn, A. D. (2024). Fish abundance, habitat, water quality, flow and climate data from English rivers,1975-2017. NERC EDS Environmental Information Data Centre. https://doi.org/10.5285/b0afb78e-a0cb-4762-9220-659211ae3a5e

## Additional Notes for Analysts Monitoring the Environment
- The dataset exemplifies standardised data integration across ecological (fish) and chemical water quality indicators to assess environmental health over time.
- Challenges include enhancing data value through integration with additional datasets and ensuring broad access to underlying data while navigating licensing constraints.
- The approach supports transparent, comparable outputs (min, max, mean, median, std, and sample counts) aligned with monitoring and policy performance evaluation.