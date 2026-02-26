# ChemPop_FISHWIMSStats_DETERMINAND_README.txt

- Purpose and scope
  - Statistics for chemical determinands derived for chemical determinand locations selected by minimised distance and maximum data along the river network from NFPD fish sites.
  - Statistics cover the antecedent period immediately prior to the biota (fish) survey date, set to 12 months for fish.
  - Data derived from 41 chemical determinands from the Environment Agency Water Quality Data Archive (1960–2017).

- Authors
  - Dr Rachel Ainsworth (r.ainsworth@hull.ac.uk) and Dr Virginie Keller (vke@ceh.ac.uk).

- Dataset structure
  - Directory contains regional folders (Anglian, North East, North West, Midlands, Southern, South West, Thames).
  - Each region contains files named Region_FISHWIMSStats_DET.csv (one per chemical determinand).
  - File contents are aligned via Fish_SiteID with related DataTable, Hydrology, and chemical determinand files.
  - Note: Some sites with sensitive data were omitted due to licensing restrictions.

- Data provenance
  - Source: Environment Agency Water Quality Data Archive (Beta), covering 41 determinands and data from 1960–2017.

- Methodology: data collection and matching
  - Fish sites filtered to those with 12 or more surveys over the period.
  - Fish data uploaded in ArcGIS; nearest three chemical determinand sites identified using Arc Toolbox Near Table Generator.
  - Determinand sites must have at least 25 samples; suitability also assessed based on river order, proximity to fish site, and time-frame overlap (allowing a 2-year window).
  - Extracted data from EA Water Quality data portal for the 41 chemicals; supporting documentation lists chemicals.

- Processing and statistics
  - Antecedent period: 12 months prior to fish survey date; data aggregated temporally.
  - Maximum concentration threshold (for metals) set at 10 mg/L; values above discarded from statistics.
  - Handling for values below LOQ (Limit of Quantification) considered via three options:
    - LOQ1: set to LOQ
    - LOQ2: set to 0
    - LOQ3: set to LOQ/2
  - Calculated per fish site: min, max, median, mean, standard deviation.
  - Additional metrics: total samples, number below LOQ, number above LOQ.

- Software and quality assurance
  - Tools: ArcGIS (v10.7+ or Pro) and Python 3 (modules: math, pandas, numpy, itertools, datetime, dateutil, os, time, shutil).
  - QA: chemical matching verified by Monika Jurgens.

- Data fields and structure
  - Each regional CSV contains 18 variables; key fields include:
    - Fish_SiteID, Fish_SurveyDate, W1_SMPT_REF
    - WQ_Min_LOQ1/2/3, WQ_Max_LOQ1/2/3, WQ_Median_LOQ1/2/3, WQ_Mean_LOQ1/2/3, WQ_STD_LOQ1/2/3
    - WQ_Count, WQ_COUNT_L_LOQ, WQ_COUNT_G_LOQ
  - Missing data coded as NA.
  - DET_CODE, DET_DESC, DET_Label, Max_Concentration provided for each chemical in the Supporting Documentation.
  - Max_Concentration thresholds filter out implausible values from statistics.

- Limitations and licensing
  - Water quality data from some monitoring sites cannot be included due to licensing restrictions.
  - Dataset uses Environment Agency Water Quality Archive data; © EA. All rights reserved.