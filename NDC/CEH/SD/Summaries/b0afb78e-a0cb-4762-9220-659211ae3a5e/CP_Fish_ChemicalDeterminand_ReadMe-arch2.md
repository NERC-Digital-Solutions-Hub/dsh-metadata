# ChemPop_FISHWIMSStats_DETERMINAND_README.txt

## Aim and scope
- Presents statistics for chemical determinands at fish survey sites, enabling environmental health monitoring and policy performance assessment.
- Data cover 41 chemical determinands derived from the Environment Agency Water Quality Archive (1960–2017).
- Statistics are calculated for the 12 months immediately prior to each fish survey date.

## Dataset description
- Directory contains extracted chemical determinand statistics for sites selected by minimised distance and maximum data along the river network from NFPD fish sites.
- For each region, statistics are stored in a file per chemical named Region_FISHWIMSStats_DET.csv.
- Regions include Anglian, North East, North West, Midlands, Southern, South West, and Thames.
- Fish_SiteID in these files matches IDs in related DataTable, Hydrology, and chemical determinand files.
- Some sites with sensitive data were omitted due to licensing restrictions.
- No multiple versions of the dataset; no updated files listed.

## File structure and contents
- Each regional folder contains a single file per chemical with the naming convention Region_FISHWIMSStats_DET.csv.
- File contains 18 variables (columns), including:
  - Fish_SiteID, Fish_SurveyDate, W1_SMPT_REF
  - Water quality moment statistics for 3 LOQ treatments: WQ_Min_LOQ1/2/3, WQ_Max_LOQ1/2/3, WQ_Median_LOQ1/2/3, WQ_Mean_LOQ1/2/3, WQ_STD_LOQ1/2/3
  - WQ_Count, WQ_COUNT_L_LOQ, WQ_COUNT_G_LOQ
  - DET_CODE, DET_DESC, DET_Label, Max_Concentration (per determinand)
- Values below the LOQ and handling of LOQ values are captured through three LOQ treatment options.
- Missing data coded as NA.
- The dataset also notes the maximum plausible concentration (Max_Concentration) for each determinand; values above this are discarded from statistics.

## Determinand data and filtering
- 41 determinands were sourced from EA Water Quality data for the defined period.
- Determinand data are filtered by:
  - Nearest three determinand sites to each fish site (via ArcGIS Near Table Generator).
  - Chemical sites must have at least 25 samples.
  - Temporal overlap: fish sampling dates must overlap with determinand sampling within a 2-year allowance.
  - River topology and proximity criteria to ensure suitable comparability (e.g., same river order, reasonable distance).

## Methodology and processing
- Data extraction: EA Water Quality data portal for selected determinands and sites.
- Spatial matching: ArcGIS (v10.7 or later) used to map fish sites to nearby determinand sites; Python used for data extraction and statistics (modules: math, pandas, numpy, itertools, datetime, dateutil, os, time, shutil).
- Time window: statistics calculated for the 12 months preceding the fish survey date.
- Temporal aggregation: data aggregated within the defined period.
- Handling below-LoQ values: three approaches considered (LoQ treated as LOQ, as 0, or as LOQ/2) and applied to compute statistics.
- Statistical outputs per site: minimum, maximum, median, mean, standard deviation; plus total samples, samples below LOQ, and samples above LOQ.
- Maximum concentration threshold: for some determinands (notably metals), a 10 mg/L threshold was applied; values above are discarded.
- Quality assurance: chemical site matching checked by Monika Jurgens.

## Software and QA notes
- Software: ArcGIS (10.7+ or Pro) and Python with specified libraries.
- QA: dedicated verification of chemical matching by a named reviewer.

## Data provenance and licensing
- Data derived from the UK Environment Agency Water Quality Archive (Beta).
- Copyright and database rights held by Environment Agency; all rights reserved.
- Some water quality data from certain sites cannot be included in the final dataset due to licensing restrictions.