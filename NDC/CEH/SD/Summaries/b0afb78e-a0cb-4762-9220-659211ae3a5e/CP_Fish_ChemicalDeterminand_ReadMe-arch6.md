# ChemPop_FISHWIMSStats_DETERMINAND_README.txt

## Overview
- Provides extracted chemical determinand statistics for locations selected by proximity and data availability to NFPD fish sites.
- Statistics cover the antecedent period immediately before the biota (fish) survey date, set to 12 months for fish.
- Authors: Dr. Rachel Ainsworth and Dr. Virginie Keller (2023).

## Data scope and objective
- Objective: support analysis of chemical determinands around fish sites by linking fish survey data with nearby chemical data.
- 41 chemical determinands are included, sourced from the Environment Agency Water Quality Data Archive.
- Timeframe: chemical data spanning 1960–2017, with statistics calculated for the 12-month period preceding each fish survey.

## Data organization and files
- Regional structure: folders for Anglian, North East, North West, Midlands, Southern, South West, and Thames.
- Each region contains one file per chemical, named Region_FISHWIMSStats_DET.csv.
- File contents are linked via Fish_SiteID (matches other data tables, including Hydrology and chemical determinand files).
- Note: some sites with sensitive data are omitted due to licensing restrictions. No multiple versions of the dataset exist.

## Provenance
- Data derived from the UK Environment Agency Water Quality Data Archive (Beta) and linked to fish survey sites via river network proximity.
- The file arrangement includes 41 determinands and supporting metadata documented separately.

## Methods: data collection and selection
- Data sources:
  - Fish survey data filtered to sites with 12 or more surveys over the study period.
  - Chemical data matched to fish sites using ArcGIS Near Table Generator to identify the three nearest chemical determinand sites.
- Selection criteria for chemical determinand sites:
  - Must have been sampled at least 25 times.
  - River catchment compatibility (order comparisons) and proximity considered.
  - Time-frame overlap with fish sampling (allowing a two-year window); distance to fish site considered.
- Data extraction: EA Water Quality data portal for the selected sites and 41 chemicals (as documented in supporting materials).

## Processing and calculations
- Timeframe: statistics calculated for the 12 months immediately before the fish survey date.
- Aggregation: data aggregated temporally after extraction.
- Thresholds: for some determinands (e.g., metals) a maximum threshold of 10 mg/L applied; values above are discarded.
- Handling values below LoQ (limit of quantification):
  - Three approaches considered: LOQ, 0, LOQ/2.
  - The dataset reports multiple LOQ handling variants for each statistic (min, max, median, mean, std) and counts.
- Statistics computed per fish site and determinand:
  - Basic statistics: minimum, maximum, median, mean, standard deviation.
  - Counts: total samples, samples below LOQ, samples above LOQ.

## Software and technical details
- GIS and data tools: ArcGIS (Version 10.7 or later; ArcGIS Pro supported).
- Scripting: Python 3 (modules include math, pandas, numpy, itertools, datetime, dateutil, os, time, shutil).
- QA steps: subset chemical matching validated by Monika Jurgens.

## Data structure and variables
- Each regional file contains 18 variables, with a consistent set across chemicals.
- Key columns (examples):
  - Fish_SiteID: unique fish site code (CHEMPoP project)
  - Fish_SurveyDate: date of fish survey
  - W1_SMPT_REF: chemical determinand sampling point reference
  - LOQ-adjusted statistics: WQ_Min_LOQ1/2/3, WQ_Max_LOQ1/2/3, WQ_Median_LOQ1/2/3, WQ_Mean_LOQ1/2/3, WQ_STD_LOQ1/2/3
  - WQ_Count: number of chemical samples in the anteceding period
  - WQ_COUNT_L_LOQ: number of samples below LOQ
  - WQ_COUNT_G_LOQ: number of samples above LOQ
- Additional metadata per chemical:
  - DET_CODE: determinand code in WIMS
  - DET_DESC: determinand description
  - DET_Label: short label used in file naming
  - Max_Concentration: plausible maximum concentration; values above discarded in statistics
- Missing data: NA

## Data licensing and access notes
- Water quality data from the Environment Agency is used under copyright and licensing restrictions.
- Some water quality data cannot be included in the final published dataset due to licensing restrictions.
- Separate supporting documentation provides the full list of chemicals and related determinand metadata.

## Usage notes and caveats
- Outputs are regionally organized and linked to specific fish sites via Fish_SiteID, enabling cross-reference with hydrology and other datasets.
- Users should account for LOQ handling choices when analyzing the statistics, as three LOQ options are present in the data structure.
- Be mindful of licensing restrictions that may limit data availability for certain sites or determinands.