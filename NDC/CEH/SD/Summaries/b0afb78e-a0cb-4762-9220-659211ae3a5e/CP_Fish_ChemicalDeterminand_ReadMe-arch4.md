# This ChemPop_FISHWIMSStats_DETERMINAND_README.txt file was generated on 2023-0114 by Dr Rachel Ainsworth and Dr Virginie Keller

## Overview
- WP/task: Statistics for chemical determinands
- Dataset describes extracted chemical determinand statistics for locations selected by minimised river-network distance and data density from NFPD fish sites; statistics cover the 12 months preceding each biota (fish) survey date.
- Authors: Rachel Ainsworth (r.ainsworth@hull.ac.uk) and Virginie Keller (vke@ceh.ac.uk)

## Data contents and structure
- File organization: Each regional folder contains one file per chemical, named Region_FISHWIMSStats_DET.csv; Regions include Anglian, North East, North West, Midlands, Southern, South West and Thames.
- Data linkage: Fish_SiteID in these files matches Fish_SiteID in related DataTable, Hydrology, and chemical determinand files.
- Regional scope: 41 determinands sourced from Environment Agency water quality data (1960–2017).
- Missing data: Some sites with sensitive data omitted due to licensing restrictions.
- Variables: Each file contains 18 variables (e.g., Fish_SiteID, Fish_SurveyDate, W1_SMPT_REF, a full set of LOQ-related metrics, WQ_Count, WQ_COUNT_L_LOQ, WQ_COUNT_G_LOQ, etc.).
- Key determinand metadata included per chemical: DET_CODE, DET_DESC, DET_Label, Max_Concentration (used to discard implausible values).

## Provenance and data sources
- Data provenance: Chemical concentrations for 41 determinands drawn from the Environment Agency Water Quality Data Archive (Beta) and used to generate statistics prior to fish surveys.

## Data selection and site matching methodology
- Site filtering: Included fish sites with 12+ surveys within the relevant period.
- Spatial linkage: Used ArcGIS to identify the three nearest chemical determinand sites to each fish site; manual verification against predefined criteria.
- Temporal alignment: Chemical data must have overlap with fish sampling dates (allowing up to 2 years); the antecedent period is 12 months prior to fish surveys.
- River-network considerations: The nearest determinand site must be on the same or appropriately related river order; otherwise unsuitable.
- Sample sufficiency: Determinand sites must have at least 25 samples to be considered.
- Data extraction: Chemical determinand data for the defined 41 chemicals extracted from the EA Water Quality data portal.

## Data processing and calculations
- Temporal aggregation: Statistics calculated for the preceding 12-month window, then aggregated per fish site.
- Statistical outputs per site: minimum, maximum, median, mean, standard deviation; plus total samples, and counts of samples below/above LOQ.
- LOQ handling: Three options considered for values below LOQ:
  - LOQ1: set to LOQ
  - LOQ2: set to 0
  - LOQ3: set to LOQ/2
- Thresholding: For some determinands (notably metals), a maximum threshold concentration of 10 mg/L applied; values above this were discarded.
- Software and tools: ArcGIS (Version 10.7+ or Pro) for site matching; Python 3 with modules including math, pandas, numpy, itertools, datetime, dateutil, os, time, shutil for data extraction and statistics.

## Quality assurance
- QA on chemical matching performed by Monika Jurgens.

## Data structure details
- File content: Each regional folder contains Region_FISHWIMSStats_DET.csv per chemical.
- Rows/columns: Varies by chemical and region; 18 variables per file.
- Variable descriptions emphasize water-quality covariates and LOQ handling:
  - WQ_Min_LOQ1/2/3, WQ_Max_LOQ1/2/3, WQ_Median_LOQ1/2/3, WQ_Mean_LOQ1/2/3, WQ_STD_LOQ1/2/3
  - WQ_Count, WQ_COUNT_L_LOQ, WQ_COUNT_G_LOQ
  - Fish_SiteID, Fish_SurveyDate, W1_SMPT_REF
- Data availability: Missing data coded as NA.
- Chemical metadata: DET_CODE, DET_DESC, DET_Label, Max_Concentration; Max_Concentration caps the plausible range and discards outliers beyond this threshold.
- Licensing note: Water quality data may be partially excluded due to licensing restrictions; dataset uses EA Water Quality Archive data rights.

## Licensing and access considerations
- Some water-quality data omitted due to licensing restrictions.
- Dataset uses Environment Agency Water Quality Archive (Beta); © EA; rights reserved.

## Implications for data leadership and governance
- Data lineage and discoverability: Clear linkage across fish sites and chemical determinand sites, with regionally organized per-chemical files and explicit metadata.
- Data quality and consistency: Explicit QA step for chemical matching; LOQ handling options documented; metal concentrations threshold applied.
- Data completeness and access: Licensing restrictions affect completeness; archiving uses a defined historical window (1960–2017) and a fixed 12-month antecedent period.
- Reproducibility considerations: Requires ArcGIS tooling and specified Python environment/modules; explicit processing steps facilitate replication of statistics per fish site.
- Data stewardship: Metadata-rich files and explicit Max_Concentration controls support data validity; cross-region standardization aids interoperability for broader analyses.