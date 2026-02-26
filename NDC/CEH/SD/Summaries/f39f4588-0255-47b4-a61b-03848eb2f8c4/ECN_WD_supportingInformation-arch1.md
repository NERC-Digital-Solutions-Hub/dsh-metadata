# Dataset Originator

- Originator: ECN Data Centre (http://data.ecn.ac.uk, ecn@ceh.ac.uk), Centre for Ecology and Hydrology
- Data providers: UK Environmental Change Network (ECN) programme funded by a consortium of UK government departments and agencies, contributing to site monitoring or network co-ordination
  - Agri-Food and Biosciences Institute
  - Biotechnology and Biological Sciences Research Council
  - Cyfoeth Naturiol Cymru – Natural Resources Wales
  - Defence Science and Technology Laboratory
  - Department for Environment, Food and Rural Affairs
  - Environment Agency
  - Forestry Commission
  - Llywodraeth Cymru – Welsh Government
  - Natural England
  - Natural Environment Research Council
  - Northern Ireland Environment Agency
  - Scottish Environment Protection Agency
  - Scottish Government
  - Scottish Natural Heritage
- Acknowledgement and publication whenever using these data
  - Please acknowledge the use of ECN datasets
  - Send one reprint of any publication citing the data

## Protocol and data notes

- See streamWaterDischargeProtocol.pdf accompanying this document
- Data are 15-minute summaries derived from 10-second logger samplings
- Use the accompanying quality information when analysing the data
- Moor House – Upper Teesdale data are recorded with an Environment Agency logger
  - Environment Agency uses the WISKI format for these data; Hydrolog format was used prior to 2004
  - Both formats include quality information, available in this dataset for Moor House
  - Explanations for quality codes are provided below

## Data structure

- SITECODE, Description: Unique ECN site code
- SDATE, Description: Date of data recording
- SHOUR, Description: Hour of data recording
- SMINS, Description: Minute of data recording
- FIELDNAME, Description: Measured variable
- VALUE, Description: Measured value

## Site Codes (sites and ranges)

- T02, Glensaugh
  - Location: 56° 54' 33.36" N, 2° 33' 12.14" W
  - Date range: 14-Oct-1993 to 26-Dec-2012
- T04, Moor House – Upper Teesdale
  - Location: 54° 41' 42.15" N, 2° 23' 16.26" W
  - Date range: 06-Oct-1992 to 24-Dec-2012
- T07, Sourhope
  - Location: 55° 29' 23.47" N, 2° 12' 43.32" W
  - Date range: 08-Dec-1993 to 26-Dec-2012
- T08, Wytham
  - Location: 51° 46' 52.86" N, 1° 20' 9.81" W
  - Date range: 09-Jun-1993 to 12-Dec-2012
- T11, Y Wyddfa – Snowdon
  - Location: 53° 4' 28.38" N, 4° 2' 0.64" W
  - Date range: 02-Jul-1997 to 27-Dec-2012

## Fieldnames and meanings

- STAGE: Stage Height (units: m)
- DISCHARGE: Discharge (units: cumecs)
- HYCODE_ST: Hydrolog code for stage (0 = no problems)
- HYCODE_DI: Hydrolog code for discharge (0 = no problems; 3 = data suspect)
- WICODE_ST: WISKI code for stage
- WICODE_DI: WISKI code for discharge (1 = good within rating; 2 = estimated within rating; 3 = missing; 4 = suspect within rating; 5 = unchecked within rating)

## Additional quality information

- An accompanying document WDquality.csv provides quality details
  - Fields include: FIELDNAME, FROM_DATE, TO_DATE, DATETYPE, CONTINUING, SITECODE, DESCRIPTION
  - DATATYPE indicators explain the applicability of quality issues (range vs. single date)
  - CONTINUING flags whether an issue is ongoing
  - QUALITY information is linked to specific SITECODE and FIELDNAME combinations

## Usage considerations for analysts

- Data quality and formatting depend on the included quality information and formats (WISKI/Hydrolog) noted per site
- When combining datasets, account for site-specific date ranges and quality flags
- Reference the accompanying protocol and quality documents for correct interpretation of codes and data handling
- Properly acknowledge ECN data and consider sharing reuse results via reprints to support dataset value demonstration