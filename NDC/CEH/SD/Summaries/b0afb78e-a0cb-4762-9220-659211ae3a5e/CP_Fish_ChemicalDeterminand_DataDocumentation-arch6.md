# Fish abundance, habitat, water quality, flow and climate in English Rivers from 1975-2017

## General overview
- Dataset of extracted chemical statistics for chemical determinand sites selected by proximity to NFPD fish sites in England.
- Statistics calculated for the 12-month antecedent period immediately prior to each fish survey date.
- Collaboration between University of Hull (Rachel Ainsworth) and UK CEH (Virginie Keller); funded by NERC Chempop (NE/S000100/2).
- Based on Environment Agency Water Quality Archive (Beta); some sites excluded due to licensing restrictions.

## Data provenance and access
- Geographic focus: England; data collection period for the study-era inferred from metadata: 2021/01 to 2022/05.
- Public link: https://environment.data.gov.uk/water-quality/view/landing
- Data citation: Ainsworth et al. (2024). Fish abundance, habitat, water quality, flow and climate data from English rivers, 1975-2017. NERC EDS Environmental Information Data Centre. DOI: 10.5285/b0afb78e-a0cb-4762-9220-659211ae3a5e
- Licensing: Environment Agency water quality data; some determinands/sites restricted by licensing; all rights reserved.

## Data structure and files
- File organization: Each region folder contains one file per chemical, named Region_FISHWIMSStats_DET.csv.
- Relationship key: Fish_SiteID matches Fish_SiteID in Fish DataTable, Hydrology, and chemical determinand files.
- Variables per file: 18 core fields plus derived statistics (see list below).
- Missing data: Some sites omitted due to licensing; list of chemicals available in supporting documentation.
- Chemicals: 41 determinands selected; details provided in supporting materials (DET_CODE, DET_DESC, DET_Label, Max_Concentration).

## Data content and variable details
- Key identifiers:
  - Fish_SiteID: unique fish site code
  - Fish_SurveyDate: date of fish survey (dd/mm/yyyy)
  - W1_SMPT_REF: reference for chemical sampling point
- Water quality covariates (LOQ handling options):
  - WQ_Min_LOQ1/2/3, WQ_Max_LOQ1/2/3, WQ_Median_LOQ1/2/3, WQ_Mean_LOQ1/2/3, WQ_STD_LOQ1/2/3
  - WQ_Count: number of chemical samples in anteceding period
  - WQ_COUNT_L_LOQ: samples below lower LOQ
  - WQ_COUNT_G_LOQ: samples above upper LOQ
- Determinand metadata (per chemical):
  - DET_CODE, DET_DESC, DET_Label, Max_Concentration
  - Values greater than Max_Concentration discarded from statistics
- Regional scope: 18 variables per file; number of rows varies by region

## Methods and processing
- Site matching:
  - Near Table Generator in ArcGIS to identify the three nearest chemical determinand sites per fish site
  - Manual checks against criteria: sampling frequency (≥25 samples), river type compatibility, proximity, and time-frame overlap (2-year allowance)
- Data extraction:
  - Extract EA Water Quality data for selected determinands/sites
- Temporal aggregation:
  - Statistics computed for the 12-month antecedent period before each fish survey
- Statistical outputs:
  - For each site: minimum, maximum, median, mean, standard deviation
  - Additional counts: total samples, samples below LOQ, samples above LOQ
- Data processing rules:
  - Metals: a maximum threshold concentration of 10 mg/l applied
  - Handling below LOQ values (three approaches): LOQ (LoQ1), 0 (LoQ2), LoQ/2 (LoQ3)
- Tools and software:
  - ArcGIS (10.7+ or Pro) for site matching
  - Python 3 with modules: math, pandas, numpy, itertools, datetime, dateutil, os, time, shutil
- Quality assurance:
  - Subset chemical matching checked by Monika Jurgens
- Contributors:
  - Monika Jurgens, Rachel Ainsworth, Virginie Keller, Nuria BachellerJareno

## Data quality, limitations, and considerations
- Accessibility limitations:
  - Some water quality determinand data excluded due to licensing restrictions
- LOQ handling:
  - Choice of LOQ treatment can influence statistics; three options are provided to accommodate analysis needs
- Data completeness:
  - Some sites with sensitive data omitted; outputs reflect available, licensed data

## Usage, licensing, and citation
- Licensing: Environment Agency water quality data; © EA; restricted data from certain sites
- Access: Public dataset via Environment Agency data portal; supporting documentation for chemical list
- Citation: As above; dataset DOI provided; appropriate acknowledgment of data sources and funding

## Related data and references
- DET codes and chemical details linked to the CHEMPOP project structure
- Cross-links: Fish_SiteID aligns with Fish Datatable, Site Variable tables, and Hydrology data
- Supporting documentation contains the complete list of chemicals and selection criteria