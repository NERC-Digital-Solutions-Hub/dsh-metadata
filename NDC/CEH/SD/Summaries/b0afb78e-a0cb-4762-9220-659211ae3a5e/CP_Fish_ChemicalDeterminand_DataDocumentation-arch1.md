# Fish abundance, habitat, water quality, flow and climate in English Rivers from 1975-2017

## Overview
- A dataset of statistical summaries linking fish survey data to nearby chemical determinands in English rivers, covering 1975–2017.
- Derived from Environment Agency water quality data (Water Quality Archive, Beta) and Fish data from the CHEMPop project.
- Authors: Rachel Ainsworth (University of Hull) and Virginie Keller (UK CEH), with coauthors; dataset citation provided with a DOI.

## Data sources, scope, and access
- Geographic focus: England.
- Time frame: Fish surveys with antecedent water quality data from the preceding 12 months.
- Data sources: 
  - Fish survey data (Fish_SiteID, Fish_SurveyDate, etc.).
  - Environmental Agency water quality data (Water Quality Archive) for selected chemical determinands.
- Licensing and access:
  - Data licensed by Environment Agency; some determinand data restricted by licensing and some sites omitted.
  - Public access via Environment Agency data portal: https://environment.data.gov.uk/water-quality/view/landing
  - Publication: Ainsworth et al. 2024; DOI: 10.5285/b0afb78e-a0cb-4762-9220-659211ae3a5e

## Data structure and content
- File structure:
  - Region_FISHWIMSStats_DET.csv for each region, containing one file per chemical determinand (Region_FISHWIMSStats_DET.csv).
  - Each file comprises 18 variables; the chemicals are listed in the supporting documentation.
- Key linking identifiers:
  - Fish_SiteID matches Fish_SiteID in related DataTable, Hydrology, and chemical determinand datasets.
- Variables (highlights):
  - Fish_SiteID, Fish_SurveyDate, W1_SMPT_REF (determinand sampling point reference).
  - Water quality statistics for the antecedent 12-month period:
    - WQ_Min_LOQ1/LOQ2/LOQ3, WQ_Max_LOQ1/LOQ2/LOQ3, WQ_Median_LOQ1/LOQ2/LOQ3, WQ_Mean_LOQ1/LOQ2/LOQ3, WQ_STD_LOQ1/LOQ2/LOQ3.
    - WQ_Count (number of chemical samples in antecedent period).
    - WQ_COUNT_L_LOQ, WQ_COUNT_G_LOQ (samples below/above LOQ).
  - Additional statistical descriptors:
    - Minimum, maximum, median, mean, standard deviation (derived from the antecedent period) for each determinand.
- Data processing specifics:
  - Determinand sites near each fish site selected with ArcGIS Near Table Generator (nearest three sites).
  - Selection criteria: site must have at least 25 samples; geographically on the same river system; time overlap with fish sampling within a 2-year window; distance considerations to avoid unsuitable matches.
  - Data extraction from EA Water Quality data portal for a defined list of 41 chemicals (see supporting documentation).
  - For some determinands (mainly metals), a maximum threshold concentration of 10 mg/L was applied; values above were discarded.
  - Handling of values below the limit of quantification (LoQ) considered three options (LoQ1, LoQ2, LoQ3) and reflected in the LOQ-specific columns.
  - Max concentration constraints per determinand applied during statistics calculation.
- Metadata and documentation:
  - Data authoring, QA, and processing notes available in the readme; supporting documentation lists the 41 chemicals and detailed determinand definitions (DET_CODE, DET_DESC, DET_Label, Max_Concentration).
  - Data provenance and versioning: no multiple versions reported; a single regional file per chemical.

## Methods and processing details
- Data collection and matching:
  - Use of Arc Toolbox Near Table Generator to identify nearest chemical determinand sites.
  - Manual screening of matches against predefined criteria (river order, time frame overlap, distance).
- Data extraction and aggregation:
  - Extract data for selected determinands from EA Water quality portal for the defined 12-month antecedent period.
  - Temporal aggregation performed for each fish site; statistics computed after aggregation.
- Statistical computations:
  - For each fish site: min, max, median, mean, standard deviation, plus counts of samples and LoQ-related counts.
  - Outlier handling via a maximum threshold (10 mg/L) for some metals; values above threshold removed from statistics.
- Tools and software:
  - ArcGIS (10.7+ or Pro) for site matching.
  - Python 3 with modules: math, pandas, numpy, itertools, datetime, dateutil, os, time, shutil for data extraction and statistics.
- Quality assurance:
  - Subset chemical matching checked by Monika Jurgens.

## Data quality, limitations, and considerations
- Licensing restrictions mean some water quality determinand data cannot be included; certain sites omitted for licensing reasons.
- The dataset covers only determinands and sites that meet the predefined matching criteria and licensing allowances.
- Handling of values below LoQ introduces three alternative representations; users should be aware when comparing LOQ scenarios.
- Spatial and temporal alignment relies on closest-site matching and a 12-month antecedent window; mismatches or gaps can affect representativeness at local scales.

## Practical usage and provenance
- The dataset enables analysis of correlations between fish abundance/habitat/climate variables and water quality determinands across English rivers, with explicit regional, temporal, and chemical stratifications.
- It is intended to support statistical modelling, pattern discovery, and impact assessment for river ecosystems within the CHEMPop context.
- Primary citation: Ainsworth et al. (2024) Fish abundance, habitat, water quality, flow and climate data from English rivers, 1975-2017. NERC EDS Environmental Information Data Centre. DOI: https://doi.org/10.5285/b0afb78e-a0cb-4762-9220-659211ae3a5e

## Key notes for analysts
- Focus on region-specific DET.csv files to explore chemical-specific relationships with fish site data.
- Leverage the LOQ handling columns (LOQ1/LOQ2/LOQ3) to assess sensitivity to LoQ treatment.
- Use Fish_SiteID as the primary key to merge with other datasets in the CHEMPop project for integrated analyses.
- Consider licensing-restricted data when interpreting regional or site-level results; some sites and determinands are intentionally omitted.