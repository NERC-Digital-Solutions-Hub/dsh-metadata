# Dataset Originator E CN Data Centre (http://data.ecn.ac.uk - ecn@ceh.ac.uk), Centre for Ecology and Hydrology

## Overview
- The ECN dataset is maintained by the UK Environmental Change Network (ECN) and funded by a consortium of UK government departments and agencies.
- Organisations contributing to the ECN include Defra, Natural England, Environment Agency, Scottish and Welsh government bodies, and research councils.
- Users are requested to acknowledge ECN data and send one reprint of any publication citing the data.

## Protocol and Quality Assurance
- ECN operates with standard operating procedures to ensure data comparability across sites (refer to WD.pdf for collection methods).
- Data consist of 15-minute summaries derived from 10-second samplings recorded by a logger.
- Users must consult accompanying quality information when using the data.
- Moor House - Upper Teesdale uses an Environment Agency logger with WISKI format (formerly Hydrolog format before 2004); both formats include quality information, available in the dataset.
- Quality codes are provided to indicate data status and reliability (see Explanatory Information for details).

## Data Structure and Access
- Data Download fields:
  - SITECODE: Unique code for each ECN Site
  - SDATE: Date of recording
  - SHOUR: Hour of recording
  - SMINS: Minute of recording
  - FIELDNAME: Variable measured
  - VALUE: Measured value
- Supporting documentation:
  - ECN_WD_qtext.csv contains site-specific quality text explanations (SITECODE, FIELDNAME, FROM_DATE, TO_DATE, DATETYPE, CONTINUING, DESCRIPTION).
- Explanatory site codes and locations:
  - T02 Glensaugh (56° 54' 33.36" N, 2° 33' 12.14" W)
  - T04 Moor House - Upper Teesdale (54° 41' 42.15" N, 2° 23' 16.26" W)
  - T07 Sourhope (55° 29' 23.47" N, 2° 12' 43.32" W)
  - T08 Wytham (51° 46' 52.86" N, 1° 20' 9.81" W)
  - T11 Y Wyddfa - Snowdon (53° 4' 28.38" N, 4° 2' 0.64" W)
  - Additional information on ECN sites is available at the provided catalog link
    https://catalogue.ceh.ac.uk/id/813712d4-d162-4edeaff8-cf1c337bdc27
- Variables being measured (FIELDNAME) and units:
  - STAGE: Stage Height, meters (m)
  - DISCHARGE: Discharge, cubic meters per second (cumecs)
  - HYCODE_ST: Hydrologic code for stage (0 = no problems; 3 = data suspect; 4 = data unchecked)
  - HYCODE_DI: Hydrologic code for discharge (0 = no problems; 3 = data suspect; 4 = data unchecked)
  - WICODE_ST: WISKI code for stage
  - WICODE_DI: WISKI code for discharge (1 = good within rating; 2 = estimated within rating)

## Usage and Data Availability
- Data are designed for cross-site comparability and long-term environmental change analysis.
- The dataset includes metadata, site-specific notes, and quality indicators to aid interpretation and robust analysis.