# ChemPop_FISHWIMSStats_DETERMINAND_README.txt

## Overview
- Presents statistics for chemical determinands at fish survey sites, covering a 12-month antecedent period before each biota (fish) survey.
- Data are organized regionally and per chemical, intended to support environmental health monitoring and policy evaluation within the CHEMPOP project.

## DataScope and Determinands
- Time period: 1960–2017 chemical concentrations sourced from the Environment Agency Water Quality Data Archive.
- Chemical determinands: 41 determinands (coverage and specifics defined in supporting documentation).
- Spatial linkage: Selection based on minimised distance and maximum data along the river network from NFPD fish sites; nearest chemical determinand sites are matched to each fish site.
- Regional structure: Regions include Anglian, North East, North West, Midlands, Southern, South West, and Thames.
- Data omissions: Some sites with sensitive data omitted due to licensing restrictions.

## Data Structure and File Organization
- File organization: Each regional folder contains one file per chemical, named Region_FISHWIMSStats_DET.csv.
- File contents: Statistical summaries for each fish site and chemical within the region.
- File relationship: Fish_SiteID links to corresponding entries in DataTable, Hydrology, and chemical determinand files.

## Processing and Methodology
- Site selection and matching:
  - Used ArcGIS Near Table Generator to identify the three nearest chemical determinand sites for each fish site.
  - Manual checks against predefined criteria (e.g., river order compatibility, proximity, overlapping sampling periods within a 2-year allowance).
  - Chemical determinand sites must have been sampled at least 25 times.
- Data extraction:
  - Source data: EA Water Quality Data Portal (Water Quality Archive, Beta).
  - Extracted for the defined 41 chemicals and the chosen time window relative to each fish survey.
- Data aggregation and statistics:
  - Temporal aggregation to compute statistics for the anteceding period (12 months for fish).
  - For some metals, a maximum threshold concentration of 10 mg/L was applied; values above this threshold were discarded in statistics.
  - Handling values below the Limit of Quantification (LoQ): three LOQ treatment options considered (LoQ treated as LOQ, 0, or LOQ/2).
  - Calculated per fish site: minimum, maximum, median, mean, standard deviation; plus three supporting metrics: total samples, samples below LoQ, samples above LoQ.
- Software and tooling:
  - ArcGIS (10.7+ or Pro) for site matching; Python 3 for data extraction and statistics (modules: math, pandas, numpy, itertools, datetime, dateutil, os, time, shutil).

## Variables and Data Content
- Core variables (18 total per file) include:
  - Fish_SiteID, Fish_SurveyDate, W1_SMPT_REF (chemical sampling point reference)
  - WQ_Min_LOQ1/2/3, WQ_Max_LOQ1/2/3, WQ_Median_LOQ1/2/3, WQ_Mean_LOQ1/2/3, WQ_STD_LOQ1/2/3
  - WQ_Count (number of chemical samples in anteceding period)
  - WQ_COUNT_L_LOQ, WQ_COUNT_G_LOQ (counts below/above LOQ)
- Additional descriptive fields (per chemical) include:
  - DET_CODE, DET_DESC, DET_Label, Max_Concentration
- Data quality notes:
  - Values above the defined Max_Concentration are discarded from statistics.
  - Missing data coded as NA.
- Documentation and supporting data:
  - Full chemical list and determinand details provided in Supporting Documentation for the dataset.

## Quality Assurance and Governance
- QA activities:
  - Subset chemical matching and site alignment reviewed by a named QA contact (Monika Jurgens).
- Licensing and data use:
  - Data derived from Environment Agency Water Quality data; licensing restrictions limit inclusion of some sites.
  - Explicit notice that some water quality data cannot be published due to licensing constraints.
  Data use is governed by EA copyright and database rights.

## Practical Considerations for users (Authors of Monitoring Frameworks)
- Purpose alignment: The statistics provide site- and chemical-specific indicators of water quality conditions preceding fish surveys, enabling evaluation of environmental health and informing policy decisions.
- Interpretational notes:
  - The 12-month antecedent window ties chemical exposure indicators to biota outcomes.
  - LOQ handling choices affect metric values; users should consider the selected LoQ treatment when comparing chemicals or regions.
  - A maximum concentration cap (10 mg/L for metals) may discard extreme values; interpret results in light of this cap.
- Data access and limitations:
  - Regional files and per-chemical statistics are available, but some data remain restricted due to licensing, limiting full data transparency.
  - Data provenance and processing steps are documented to support reproducibility and governance considerations.