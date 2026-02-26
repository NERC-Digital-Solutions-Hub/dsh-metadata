# ChemPop_FISHWIMSStats_DETERMINAND_README.txt

## General Information
- WP/task: Statistics for chemical determinands
- Dataset description: Extracted chemical determinand statistics for locations selected by minimised distance and maximum data along the river network from NFPD fish sites; statistics cover the antecedent period immediately before the biota survey date, set to 12 months for fish.
- Authors: Dr Rachel Ainsworth (r.ainsworth@hull.ac.uk) and Dr Virginie Keller (vke@ceh.ac.uk)

## File Structure and Naming
- Each regional folder contains one file per chemical, named as: Region_FISHWIMSStats_DET.csv
- Regions: Anglian, North East, North West, Midlands, Southern, South West, Thames
- File contains data for each chemical determinand per region
- Relationship: Fish_SiteID in these files matches Fish_SiteID in DataTable, Hydrology, and chemical determinand files
- Missing data due to licensing restrictions: Some sites with sensitive data omitted from final dataset
- Versioning: No multiple versions

## Provenance
- Data source: Chemical concentrations of 41 determinands (1960–2017) extracted from the Environment Agency Water Quality Data Archive
- Source URL: https://environment.data.gov.uk/water-quality/view/landing
- Data used: Water quality data from EA Water Quality Archive (Beta)

## Methodological Information
- Site selection and matching:
  - Filter fish sites to those with 12+ surveys
  - Use ArcGIS (v10.7+) with Near Table Generator to identify nearest three chemical determinand sites to each fish site
  - Chemical determinand sites must have been sampled at least 25 times
  - Consider proximity to sewage treatment works and river hierarchy; exclude unsuitable river relationships
  - Time frame overlap: acceptable if fish survey dates fall within a 2-year window with corresponding chemical sampling
- Data extraction:
  - Extract data for a defined list of 41 chemicals from EA Water Quality data portal
- Data processing:
  - Statistics calculated for the preceding period immediately prior to fish survey date; 12 months for fish surveys
  - Temporal aggregation performed after extraction
  - Threshold handling: for metals, a maximum concentration threshold of 10 mg/L applied; values above threshold discarded
  - LoQ handling (three options considered): LoQ treated as LOQ, 0, or LOQ/2
  - Output statistics per fish site: minimum, maximum, median, mean, standard deviation; plus total samples, samples below LoQ, samples above LoQ
- Software and tools:
  - ArcGIS (v10.7+ or Pro)
  - Python 3 with modules: math, pandas, numpy, itertools, datetime, dateutil, os, time, shutil
- Quality assurance:
  - Subset chemical matching checked by Monika Jurgens

## Data-Specific Information
- File content:
  - Each regional DET file contains 18 variables
  - Key variables:
    - Fish_SiteID, Fish_SurveyDate, W1_SMPT_REF
    - WQ_Min_LOQ1/2/3, WQ_Max_LOQ1/2/3, WQ_Median_LOQ1/2/3, WQ_Mean_LOQ1/2/3, WQ_STD_LOQ1/2/3
    - WQ_Count, WQ_COUNT_L_LOQ, WQ_COUNT_G_LOQ
- Data details:
  - Number of rows/columns varies by chemical/regional combination
  - Data missing coded as NA
  - The DET_Code, DET_Desc, DET_Label, and Max_Concentration are provided per chemical; values above Max_Concentration are discarded from statistics
- Practical note:
  - Some water quality data cannot be included in the final dataset due to licensing restrictions
  - Data are governed under EA copyright and database rights

## Data Quality and Limitations
- Missing data and licensing restrictions lead to omissions of certain sites
- LoQ handling options indicate sensitivity to values below detection limits; the final approach to LoQ handling should be documented in supporting materials
- Only 12-month antecedent window; may affect comparability across sites with uneven sampling
- Metals have a defined maximum threshold (10 mg/L) for inclusion in statistics

## Licensing and Usage Considerations
- Dataset uses Environment Agency water quality data (Water Quality Archive, Beta)
- Licensing restrictions limit inclusion of some sites and data in the published dataset
- Users should reference supporting documentation for the full list of chemicals and determinands and any site-specific licensing notes