# FISHWIMSStats_DETERMINAND_readme.txt

- This readme documents the FishWIMS statistical dataset derived from English rivers, combining fish survey data with chemical determinand data from the Environment Agency Water Quality Archive (Beta) and other sources.
- Title/scope: Fish abundance, habitat, water quality, flow and climate in English Rivers from 1975-2017; statistics are calculated for the antecedent 12-month period prior to each fish survey.

## Authors and Date
- Authors: 
  - Rachel Ainsworth, University of Hull
  - Virginie Keller, UK Centre for Ecology & Hydrology
- Date of data collection: 2021-01 to 2022-05-27
- Geographic location: England
- Funding: NERC Chempop grant NE/S000100/2

## Sharing, Access, and Licensing
- Data license: Environment Agency water quality data from the Water Quality Archive (Beta); © Environment Agency. Some determinand data cannot be included due to licensing restrictions.
- Public access: Data available at https://environment.data.gov.uk/water-quality/view/landing
- Data provenance: Fish_SiteID in the dataset corresponds to Fish_SiteID in related fish datasets, hydrology data, and chemical determinand files.
- Derived from: No; data are originally sourced from EA Water Quality data and related fish data.
- Citation: Ainsworth et al. (2024) Fish abundance, habitat, water quality, flow and climate data from English rivers, 1975-2017. NERC EDS Environmental Information Data Centre. DOI provided.
- Note on licensing: Some sites with sensitive data omitted from the final dataset due to licensing restrictions.

## Data and File Structure
- File(s): Region_FishWIMSStats_DET.csv for each region (RR*), containing statistics per chemical determinand label (DET_Label).
- Data relationships: Fish_SiteID links to Fish_SiteID in the DataTable, Hydrology, and chemical determinand files.
- Versioning: No multiple versions of the dataset; no updates recorded in this readme.
- Region-specific organization: Each regional folder contains one file per chemical (Region_FISHWIMSStats_DET.csv).

## Methodology (Data Collection and Generation)
- Site matching:
  - Use Arc Toolbox Near Table Generator to identify the three nearest chemical determinand sites for each fish site.
  - Manual validation against predefined criteria (e.g., site should have at least 25 samples; proximity to sewage treatment works; river order compatibility; time-frame overlap within a 2-year allowance).
- Data extraction:
  - Extract data from the EA Water Quality data portal for a defined list of 41 chemicals (see Supporting Documentation).
- Temporal scope:
  - Statistics calculated for the 12-month period immediately before the fish survey date; temporally aggregated.

## Data Processing and Quality Assurance
- Handling of high concentrations:
  - For certain determinands (notably metals), a maximum threshold of 10 mg/L is applied; values above threshold are discarded.
- Handling of values below LoQ (limit of quantification):
  - Three approaches considered: LoQ, 0, LoQ/2 (LoQ1/LoQ2/LoQ3).
- Calculated statistics per fish site:
  - Min, max, median, mean, standard deviation
  - Additional counts: total samples, samples below LoQ, samples above LoQ
- Software/tools:
  - ArcGIS (10.7+ or Pro) for site matching
  - Python 3 with math, pandas, numpy, itertools, datetime, dateutil, os, time, shutil
- QA procedures:
  - Subset chemical matching checked by Monika Jurgens
- Personnel involved:
  - Monika Jurgens, Rachel Ainsworth, Virginie Keller, Nuria BachellerJareno

## Data Specification and Metadata
- File content: Each regional file contains data for one chemical, named Region_FISHWIMSStats_DET.csv
- Variables: 18 per file
  - Key fields include:
    - Fish_SiteID: unique fish site code (Chempop project)
    - Fish_SurveyDate: date of fish survey (dd/mm/yyyy)
    - W1_SMPT_REF: chemical determinand sampling point reference
    - WQ_Min_LOQ1/2/3, WQ_Max_LOQ1/2/3, WQ_Median_LOQ1/2/3, WQ_Mean_LOQ1/2/3, WQ_STD_LOQ1/2/3
    - WQ_Count: total chemical samples for anteceding period
    - WQ_COUNT_L_LOQ: samples below LOQ
    - WQ_COUNT_G_LOQ: samples above LOQ
- Missing data: Codes not specified in the readme
- Abbreviations: Chemicals listed in Supporting Documentation; DET_CODE, DET_DESC, DET_Label, and Max_Concentration provided per determinand
- Determinands: DET_CODE (unique code), DET_DESC (description), DET_Label (short label for file naming), Max_Concentration (plausible maximum; values above are discarded)

## Data Standards, Calibration, and Quality Standards
- Data sources: Environment Agency water quality data (Water Quality Archive, Beta)
- Calibration/standards: Not applicable (n/a)
- Max concentration rules: Applied per determinand to constrain statistics
- Versioning/updates: Not indicated; no versioned updates described

## Special Considerations for Data Stewards
- Licensing restrictions impact data completeness; be aware of withheld data due to licensing
- Cross-dataset linkage relies on Fish_SiteID alignment across fish, hydrology, and chemical datasets
- Documentation and supporting materials (Supporting Documentation) needed to interpret the 41-chemical list and MAX_CONCENTRATION values
- Sensitive data handling: Some sites omitted; ensure appropriate access controls and licensing verification when redistributing

## Contact and Governance
- Primary contacts: Rachel Ainsworth (University of Hull) and Virginie Keller (UK CEH)
- Data use and citation should align with the provided DOI and dataset citation
- Governance considerations: data sharing governed by Environment Agency licensing; ensure compliance when sharing subsets or derived products