# UK Environmental Change Network (ECN) soil solution chemistry data: 1992-2012

## Overview
- Dataset originator: ECN Data Centre (Centre for Ecology & Hydrology)
- Data providers: UK ECN programme, funded by a consortium of UK government departments/agencies
- Purpose: provide soil solution chemistry data across ECN sites to support environmental change research; encourage acknowledgement of data use and sharing of publications that cite the data
- Timespan and scope: soil solution chemistry data from 12 ECN sites, with measurements spanning 1992–2012

## Data structure and content
- Core data model: SITECODE (site ID), SDATE (sample date), RID (replicate ID), FIELDNAME (variable measured), VALUE (measured value)
- Site metadata: 12 ECN sites (T01–T12) with site name, coordinates, and dataset date ranges
  - Examples: Drayton (T01), Glensaugh (T02), Hillsborough (T03), Moor House - Upper Teesdale (T04), North Wyke (T05), Rothamsted (T06), Sourhope (T07), Wytham (T08), Alice Holt (T09), Porton Down (T10), Snowdon/Y Wyddfa (T11), Cairngorms (T12)
- Fieldnames and units: broad suite of soil chemistry and water-quality variables, including
  - Alkalinity, Aluminium, Calcium, Chloride, Colour (absorbance), Conductivity, Dissolved Organic Carbon, Iron, Magnesium, Ammonium, Nitrate-Nitrogen, pH, Aquacheck pH (stirred and unstirred), Phosphate, Potassium, Sulphate, Sodium, Total Nitrogen, Total Phosphorus, Vacuum, Volume
  - Q1–Q5 quality code fields
- Additional analytical information: ECN_SS2.csv provides timing and laboratory-related details
  - Fields include lab ID, measurement dates/times for pH, filtration, and analysis completion
- Quality codes: standardized ECN quality codes (e.g., 100, 101, 102, …, 999 for unusual events) used by site managers to flag data quality issues; a quality text description accompanies 999 cases
- Supporting documentation: external resources and a DOI link for further details
- Data quality and usage guidance: use accompanying quality information when using data; a standard QC solution is analyzed alongside field samples

## Protocol and data collection notes
- Sampling protocol: suction samplers measure soil solution chemistry; samples collected fortnightly
- Replicate handling: sampler replacements indicated by a new RID
- Bulk sampling: when insufficient sample is collected, days can be bulked with RID values XXS (shallow) or XXD (deep)
- Quality control: standard QC solution analyzed with field samples; QC data available with dataset
- Data interpretation: ensure to review quality information accompanying the dataset for proper interpretation

## Data quality and curation considerations
- Quality management: site managers assign a set of ECN quality codes to reflect potential data issues; codes cover sample loss, equipment problems, weather impacts, laboratory issues, etc.
- Unusual events: code 999 is used when an unusual event occurs; related explanatory text is available in the accompanying quality information
- Practical data use: combine ECN data with ECN_SS2 timing data for accurate temporal alignment; consider site-specific gaps or quality flags when analyzing trends

## Access, usage, and citation guidance
- Acknowledgement: users are asked to acknowledge the use of ECN data in publications
- Publication sharing: send one reprint of any publication that cites ECN data
- Supporting materials: reference the accompanying documentation (ECN soil solution chemistry data: 1992-2012) and the ECN_SS2.csv file for detailed measurement timing
- Citation pathway: dataset and its supporting docs can be accessed via the provided links and DOI

## Practical guidance for Data Support
- How to use the dataset effectively
  - Merge core data (SITECODE, SDATE, RID, FIELDNAME, VALUE) across sites for comparative analyses
  - Integrate ECN_SS2 timing data to align pH measurements and sample processing with sampling events
  - Use site metadata (coordinates, date ranges) to filter and stratify analyses by location and period
  - Apply QC flags from Q1–Q5 and consult 999 text descriptions for data caveats
- Data cleaning and preparation steps
  - Normalize units where needed (as fieldnames include various units)
  - Resolve replicate IDs and handle bulked samples (XXS/XXD) appropriately
  - Exclude or separately flag data points with unfavorable quality codes for sensitive analyses
- Considerations for reporting and reuse
  - Clearly cite ECN data and include the DOI when referring to the dataset
  - Provide the reprint reference when possible for traceability
  - Acknowledge that data are from 12 ECN sites and span 1992–2012 with potential gaps and quality-related flags