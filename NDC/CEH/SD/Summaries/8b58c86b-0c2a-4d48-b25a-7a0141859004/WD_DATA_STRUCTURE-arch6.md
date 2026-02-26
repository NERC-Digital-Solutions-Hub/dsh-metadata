# Dataset Originator

- ECN Data Centre (http://data.ecn.ac.uk - ecn@ceh.ac.uk), Centre for Ecology and Hydrology

## Overview and purpose

- The UK Environmental Change Network (ECN) dataset supports understanding environmental change by providing standardized, comparable data across multiple sites.
- Data providers are a consortium of UK government departments and agencies funding site monitoring or network coordination.
- ECN asks users to acknowledge data usage and to send one reprint of any publication citing the data.

## Data providers and sponsors

- Agri-Food and Biosciences Research Council (BBSRC)
- Biotechnology and Biological Sciences Research Council (BBSRC)
- Cyfoeth Naturiol Cymru - Natural Resources Wales
- Defence Science & Technology Laboratory
- Department for Environment, Food and Rural Affairs (Defra)
- Environment Agency
- Forestry Commission
- Llywodraeth Cymru - Welsh Government
- Natural England
- Natural Environment Research Council (NERC)
- Northern Ireland Environment Agency
- Scottish Environment Protection Agency
- Scottish Government
- Scottish Natural Heritage

## Protocol, data quality, and comparability

- ECN operates standard operating procedures to ensure data comparability across sites; reference WD.pdf for data collection explanations.
- Data are 15-minute summaries derived from 10-second logger samplings.
- Quality information accompanies the data; quality codes are provided for stage and discharge data.
- Moor House - Upper Teesdale uses an Environment Agency logger and records in WISKI format (Hydrolog format used before 2004); both formats include quality indicators.
- Explanations for quality codes are available in the accompanying documentation.

## Data structure and download format

- Dataset fields for download:
  - SITECODE: Unique ECN site code
  - SDATE: Date of recording
  - SHOUR: Hour of recording
  - SMINS: Minute of recording
  - FIELDNAME: Variable measured
  - VALUE: Measured value

## Supporting documentation

- ECN_WD_qtext.csv: Text provided by site managers explaining circumstances affecting data quality.
  - Fields include SITECODE, FIELDNAME, FROM_DATE, TO_DATE, DATETYPE, CONTINUING, DESCRIPTION

## Site codes and location information

- T02 – Glensaugh: 56° 54' 33.36" N, 2° 33' 12.14"W
- T04 – Moor House - Upper Teesdale: 54° 41' 42.15" N, 2° 23' 16.26"W
- T07 – Sourhope: 55° 29' 23.47" N, 2° 12' 43.32"W
- T08 – Wytham: 51° 46' 52.86" N, 1° 20' 9.81"W
- T11 – Snowdon (Y Wyddfa): 53° 4' 28.38" N, 4° 2' 0.64"W
- Additional site information is available at the ECN catalogue: https://catalogue.ceh.ac.uk/id/813712d4-d162-4edeaff8-cf1c337bdc27

## Variables and measurement details

- STAGE: Stage Height (units: m)
- DISCHARGE: Discharge (units: cumecs)
- HYCODE_ST / HYCODE_DI: Hydrologic data quality codes for stage and discharge (e.g., 0 = no problems, 3 = data suspect, 4 = data unchecked)
- WICODE_ST / WICODE_DI: WISKI quality codes (e.g., 1 = good within rating, 2 = estimated within rating)
- These codes help assess data reliability and guide data cleaning and interpretation

## Attribution and further information

- Acknowledge the use of ECN data in publications and contact ECN for reprint submissions.
- For more information about ECN sites and data, consult the ECN site catalogue and accompanying documentation.