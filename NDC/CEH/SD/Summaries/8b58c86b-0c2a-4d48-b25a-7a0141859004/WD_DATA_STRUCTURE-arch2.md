# Dataset Originator

- ECN Data Centre (http://data.ecn.ac.uk - ecn@ceh.ac.uk), Centre for Ecology and Hydrology

## Overview

- Data providers: The UK Environmental Change Network (ECN) programme funded by a consortium of UK government departments and agencies (list includes DEFRA, Environment Agency, Natural England, NERC, SNPs, Welsh Government, etc.).
- Purpose: Understand causes and consequences of environmental change; fund site monitoring or network coordination.
- Usage acknowledgement: Users should acknowledge data and send one reprint of any publication citing ECN data.

## Data Provenance and Access

- Protocols: ECN has standard operating procedures to ensure data comparability across sites; WD.pdf explains data collection methods.
- Data quality: Users must apply accompanying quality information; quality codes available in dataset (see notes below).
- Moor House - Upper Teesdale: Uses Environment Agency logger; data recorded in WISKI format (Hydrolog format used prior to 2004); quality codes available for this site.
- Data availability: Data are stored and uploaded to appropriate portals; underlying data are intended to be accessible to others.

## Data Structure and Variables

- Sampling: 15-minute summaries from 10-second samplings.
- Main variables (FIELDNAME):
  - STAGE: Stage Height (m)
  - DISCHARGE: Discharge (cumecs)
- Quality indicators:
  - HYCODE_ST: Hydrolog code for stage (0 no problems; 3 data suspect; 4 data unchecked)
  - HYCODE_DI: Hydrolog code for discharge (0 no problems; 3 data suspect; 4 data unchecked)
  - WICODE_ST: Wiski code for stage
  - WICODE_DI: Wiski code for discharge (1 good within rating; 2 estimated within rating)
- QUALITY and context: Use accompanying quality information when using data.

## Data Download and Format

- Data fields for download:
  - SITECODE: Unique ECN site code
  - SDATE: Date of recording
  - SHOUR: Hour of recording
  - SMINS: Minute of recording
  - FIELDNAME: Variable measured
  - VALUE: Measured value
- Supporting documentation: ECN_WD_qtext.csv contains site-specific quality notes attached by site managers (viewable via quality information).

## Site Codes and Locations

- T02 Glensaugh — 56° 54' 33.36" N 2° 33' 12.14"W
- T04 Moor House - Upper Teesdale — 54° 41' 42.15" N 2° 23' 16.26"W
- T07 Sourhope — 55° 29' 23.47" N 2° 12' 43.32"W
- T08 Wytham — 51° 46' 52.86" N 1° 20' 9.81"W
- T11 Y Wyddfa - Snowdon — 53° 4' 28.38" N 4° 2' 0.64"W
- Additional information on ECN sites available at the CEH catalogue link provided.

## Variable Details

- STAGE: Stage Height (m)
- DISCHARGE: Discharge (cumecs)

## Explanatory and Supporting Information

- ECN_WD_qtext.csv: Site managers’ notes on quality affecting data; fields include SITECODE, FIELDNAME, FROM_DATE, TO_DATE, DATETYPE, CONTINUING, DESCRIPTION.
- Additional information: Explanatory information provides variable definitions and quality code explanations.

## Usage Considerations and Challenges

- Data standardization: Ensuring data are comparable across sites via standard protocols and quality codes.
- Data value and accessibility: Increasing the value of monitoring datasets by combining with other data; enabling access to underlying data used to produce outputs.