# Dataset Originator

- The ECN Data Centre (Centre for Ecology and Hydrology) is the dataset originator, hosting 15-minute environmental discharge/ stage data derived from 10-second samplings.
- Data are provided by the UK Environmental Change Network (ECN) programme, funded by a consortium of UK government departments and agencies (including Agri-Food and Biosciences Institute, DEFRA, Environment Agency, Natural England, Scottish Environment Protection Agency, Welsh Government, and others).
- ECN requests acknowledgment of data use and one reprint of any publication citing the data.

## Purpose and Scope

- The dataset is intended to monitor environmental change by delivering consistent, quality-assured data suitable for assessing environmental health and policy performance over time.
- Data are presented in standard formats (reports, maps, charts) and are suitable for integration with other data sources to increase analytical value.

## Data Content and Structure

- Data are 15-minute summaries derived from 10-second sampling, with accompanying quality information.
- Moor House - Upper Teesdale uses an Environment Agency logger; data formats include WISKI (and previously Hydrolog) with embedded quality codes.
- Core data fields:
  - SITECODE: Unique ECN site code
  - SDATE: Date of recording
  - SHOUR: Hour of recording
  - SMINS: Minute of recording
  - FIELDNAME: Variable measured (e.g., STAGE, DISCHARGE)
  - VALUE: Measured value
- Primary measured variables:
  - STAGE: Stage height (m)
  - DISCHARGE: Discharge (cumecs)
- Quality coding:
  - HYCODE_ST / HYCODE_DI: Hydrolog codes (e.g., 0 = no problems; 3 = data suspect)
  - WICODE_ST / WICODE_DI: Wiski codes (e.g., 1 = good, within rating; 2 = estimated; 3 = missing; 4 = suspect; 5 = unchecked)
- Additional quality information is provided in WDquality.csv, describing quality issues by field, date range, site, and descriptive notes.

## Site Coverage and Metadata

- Sites included (with codes, names, coordinates, and data ranges):
  - T02 — Glensaugh: 56° 54' 33.36" N, 2° 33' 12.14" W; data 14-Oct-1993 to 26-Dec-2012
  - T04 — Moor House - Upper Teesdale: 54° 41' 42.15" N, 2° 23' 16.26" W; data 06-Oct-1992 to 24-Dec-2012
  - T07 — Sourhope: 55° 29' 23.47" N, 2° 12' 43.32" W; data 08-Dec-1993 to 26-Dec-2012
  - T08 — Wytham: 51° 46' 52.86" N, 1° 20' 9.81" W; data 09-Jun-1993 to 12-Dec-2012
  - T11 — Y Wyddfa - Snowdon: 53° 4' 28.38" N, 4° 2' 0.64" W; data 02-Jul-1997 to 27-Dec-2012

## Data Protocols and Quality Assurance

- Reference protocol: streamWaterDischargeProtocol.pdf accompanying this document.
- Quality information to consult alongside data:
  - Use the accompanying quality information to understand data validity and limitations.
  - The dataset includes multiple quality codes across both stage and discharge measurements, with site- and date-specific quality notes in WDquality.csv.

## Data Use, Access, and Management

- Data are designed for transparent verification and reuse in monitoring and research on environmental change.
- Acknowledgment of data use is requested, along with sharing one reprint of any publication citing the dataset.
- Outputs may be stored/uploaded to appropriate data portals and presented in standard formats (reports, maps, charts) to support policy evaluation and environmental health assessments.