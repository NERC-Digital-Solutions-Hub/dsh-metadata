# ChemPop_FISHWIMSStats_DETERMINAND_README.txt

## Overview
- This readme documents statistics for chemical determinands associated with fish survey sites from the CHEMPOP project.
- Statistics cover 41 determinands and are derived for antecedent periods immediately prior to fish biota surveys.

## Data scope and selection
- Location selection is based on minimised river network distance from NFPD fish sites and data abundance along the river network.
- Antecedent period for fish surveys is 12 months.
- Data are extracted from the Environment Agency Water Quality Data Archive (1960–2017).

## Regional structure and file naming
- Regions: Anglian, North East, North West, Midlands, Southern, South West, and Thames.
- Each region contains one file per chemical determinand.
- File naming convention: Region_FISHWIMSStats_DET.csv.
- Within each regional file, the Fish_SiteID matches identifiers in DataTable, Hydrology, and chemical determinand files.

## Methodology (data collection and processing)
- Filter fish sites to those with 12 or more surveys within the time period.
- Upload fish data and relevant shapefiles to ArcGIS (v10.7+).
- Use Arc Toolbox Near Table Generator to identify the three nearest chemical determinand sites for each fish site.
- Manually validate nearest sites against criteria: river compatibility, sampling timeframe overlap (allowing up to a 2-year gap), and reasonable distance (exclude sites several kilometres away or on a different river).
- Extract EA Water Quality data for the selected sites and 41 chemicals.
- Compute statistics for the antecedent 12-month period prior to each fish survey date.
- Aggregate temporally for each site; apply a maximum concentration cap for some determinands (e.g., metals) at 10 mg/L by discarding values beyond the cap.
- Use three LOQ-handling approaches for values below LoQ:
  - LOQ, 0, and LOQ/2.
- Output statistics per fish site: minimum, maximum, median, mean, standard deviation.
- Additional variables: total sample count, number of samples below LOQ, number of samples above LOQ.

## Data fields and structure
- Each regional file contains 18 variables (columns).
- Key variables:
  - Fish_SiteID: unique fish site code.
  - Fish_SurveyDate: fish survey date (dd/mm/yyyy).
  - W1_SMPT_REF: chemical determinand sampling point reference.
  - WQ_Min_LOQ1/LOQ2/LOQ3: minimum values with LOQ handling variants.
  - WQ_Max_LOQ1/LOQ2/LOQ3: maximum values with LOQ handling variants.
  - WQ_Median_LOQ1/LOQ2/LOQ3: median values with LOQ handling variants.
  - WQ_Mean_LOQ1/LOQ2/LOQ3: mean values with LOQ handling variants.
  - WQ_STD_LOQ1/LOQ2/LOQ3: standard deviation with LOQ handling variants.
  - WQ_Count: total number of chemical samples in the antecedent period.
  - WQ_COUNT_L_LOQ: number below lower LOQ.
  - WQ_COUNT_G_LOQ: number above upper LOQ.
- LOQ handling variants are provided to support sensitivity analyses of lower-quantification-limit data.

## Data quality and QA
- QA on chemical matching performed by Monika Jurgens.
- Data missing codes: NA.
- The dataset includes a note that some water quality data cannot be published due to licensing restrictions.
- Maximum plausible concentrations (Max_Concentration) are enforced; values exceeding these are discarded from statistics.

## Provenance and licensing
- Source: Environment Agency Water Quality Data Archive (Beta).
- Copyright: Environment Agency; database rights reserved.
- Licensing restrictions prevent inclusion of certain water quality monitoring sites in the final dataset.

## GIS considerations and usage
- Data are designed for map-based GIS analyses, enabling spatial exploration of chemical determinand occurrences relative to fish sites.
- Fisher site IDs serve as keys for linking to other GIS layers (hydrology, river network, sewage treatment works).
- ArcGIS (10.7+ or Pro) is required, with Python 3 and libraries (math, pandas, numpy, itertools, datetime, dateutil, os, time, shutil) for data extraction and statistic calculations.
- Data packaging is region-based with region-specific determinand files, suitable for spatial joins and thematic mapping of determinand statistics.

## Additional notes and references
- The list of chemicals is available in the Supporting Documentation for this dataset.
- The dataset uses the Environment Agency water quality data from the Water Quality Archive (Beta).
- There is a note that some sites with sensitive data were omitted from the final dataset due to licensing restrictions.