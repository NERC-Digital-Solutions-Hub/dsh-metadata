# UK Environmental Change Network (ECN) precipitation chemistry data: 1992-2012

## Overview
- Dataset from the ECN Data Centre (Centre for Ecology and Hydrology) documenting precipitation chemistry across ECN sites (1992–2012).
- Data providers are the UK Environmental Change Network programme, sponsored by a consortium of UK government departments and agencies.
- Use of the data should be acknowledged; authors should send one reprint of any publication citing the data.
- Supporting documentation and accompanying quality information are provided, including the ECN_PC2.csv file and a DOI for the main dataset documentation.

## Provenance and Access
- Dataset originator: ECN Data Centre, CEH.
- Data providers: ECN programme funded by multiple UK government and agency partners (list includes Defra, Natural England, NERC, SEPA, etc.).
- Acknowledgement and reprint request: ECN asks users to acknowledge data usage and to provide one reprint of publications citing ECN data.
- Access to data is supported by accompanying documentation (ECN precipitation chemistry data: 1992–2012) and the additional ECN_PC2.csv file.

## Protocol and Quality Assurance
- Protocol: Bulk collectors measure precipitation chemistry; samples collected weekly.
- Quality control: A standard QC solution is sent to laboratories analyzing ECN water samples and is analyzed alongside field samples; QC data are included with the dataset.
- Users must refer to the accompanying quality information when utilizing the data.

## Data Structure and Content
- Core data structure: 
  - SITECODE: Unique ECN site code
  - SDATE: Sampling date
  - FIELDNAME: Measured variable
  - VALUE: Measured value
  - VOLUME: Volume of sample collected
- Site Codes: 12 ECN sites (e.g., T01 Drayton, T02 Glensaugh, T03 Hillsborough, T04 Moor House–Upper Teesdale, T05 North Wyke, T06 Rothamsted, T07 Sourhope, T08 Wytham, T09 Alice Holt, T10 Porton Down, T11 Snowdon, T12 Cairngorms) with coordinates and dataset date ranges (1992–2012, with varying end dates per site).
- Fieldnames: Includes key chemistry parameters and related measurements, such as ALKY (alkalinity), CALCIUM, CHLORIDE, COLOUR, CONDY (conductivity), DOC (dissolved organic carbon), IRON, MAGNESIUM, NH4N, NO3N, pH, PHAQCS/PHACQU (pH readings from Aquacheck system), PO4P, POTASSIUM, SO4S, SODIUM, TOTALN, TOTALP, and VOLUME; plus quality code fields Q1–Q6.
- Quality codes: Quality indicators (100–199 range, plus additional codes) used by ECN site managers to flag data quality issues (e.g., 100 No information available, 101 No sample/readings, 501–510 laboratory-related issues, 999 Unusual event with accompanying text). A full list and descriptions are provided in the dataset documentation.

## Site and Measurement Details
- Site metadata includes site name, geographic coordinates, and the time span of available data for each site.
- Measurements cover multiple chemical species in precipitation and related parameters (e.g., alkalinity, major ions, conductivity, and pH measurements from different methods).

## Additional Documentation and Links
- Supporting documentation: ECN precipitation chemistry data documentation (1992–2012) with DOI: 10.5285/0cd4abd2-1bc9-48bc-b5c2-cebdeaa23ceb.
- Additional analytical information is provided in ECN_PC2.csv, detailing timing and laboratory metadata (e.g., FROMDATE/FROMHOUR/FROMMINUTE, SDATE/SHOUR/SMINS, LAB_NID, PHDATE/PHHOUR/PHMINS, FILTDATE, COMPDATE).

## Data Use and Stewardship
- Data stewardship emphasis includes ensuring metadata completeness, metadata standardization, and linkage of QC information to data values.
- Users are encouraged to create appropriate datasets, respect sharing quality indicators, and reference the ECN data consistently.
- The dataset supports research on environmental change and is intended to be discoverable and usable by researchers, with clear provenance and quality flags.

## Data Stewardship Considerations
- Ensure timely data ingestion from site coordinators and consistent application of ECN quality codes.
- Maintain alignment of site metadata (site codes, coordinates, date ranges) across data products.
- Preserve associated QC data and quality narratives to support data usability.
- Facilitate proper acknowledgment and data sharing acknowledgments in user outputs.