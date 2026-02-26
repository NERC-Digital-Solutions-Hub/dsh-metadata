# Dataset Originator

## Overview and Responsible Parties
- Data Centre: ECN Data Centre (http://data.ecn.ac.uk), ecn@ceh.ac.uk, Centre for Ecology and Hydrology.
- Data Providers: UK Environmental Change Network (ECN) programme; funded by a consortium of UK government departments and agencies (e.g., AFBI, BBSRC, NRW, Dstl, Defra, Environment Agency, Forestry Commission, Welsh Government, Natural England, NERC, NIEA, SEPA, Scottish Government, SNH).
- Purpose: Long-term environmental change data collection; sponsors contribute site monitoring or network coordination.
- Acknowledgement: Users should acknowledge ECN data usage and send one reprint of any publication citing ECN data.

## Protocol and Notes
- Protocol: Refer to streamWaterDischargeProtocol.pdf accompanying this document.
- Data characteristics:
  - 15-minute summaries derived from 10-second logger samplings.
  - Use accompanying quality information when using data.
  - Moor House – Upper Teesdale uses an Environment Agency logger; formats include WISKI (current) and Hydrolog (pre-2004). Quality information is available for Moor House within this dataset.
  - Quality codes are explained in the accompanying documentation.

## Data Structure and Metadata
- Core data fields:
  - SITECODE: Unique ECN Site code.
  - SDATE: Date of data recording.
  - SHOUR: Hour of data recording.
  - SMINS: Minute of data recording.
  - FIELDNAME: Variable measured.
  - VALUE: Measured value.

## Site Codes and Coverage
- T02 Glensaugh
  - Location: 56° 54' 33.36" N, 2° 33' 12.14" W
  - Date range: 14-Oct-1993 to 26-Dec-2012
- T04 Moor House - Upper Teesdale
  - Location: 54° 41' 42.15" N, 2° 23' 16.26" W
  - Date range: 06-Oct-1992 to 24-Dec-2012
- T07 Sourhope
  - Location: 55° 29' 23.47" N, 2° 12' 43.32" W
  - Date range: 08-Dec-1993 to 26-Dec-2012
- T08 Wytham
  - Location: 51° 46' 52.86" N, 1° 20' 9.81" W
  - Date range: 09-Jun-1993 to 12-Dec-2012
- T11 Y Wyddfa - Snowdon
  - Location: 53° 4' 28.38" N, 4° 2' 0.64" W
  - Date range: 02-Jul-1997 to 27-Dec-2012

## Fieldnames, Units, and Quality Codes
- STAGE
  - Description: Stage height
  - Units: m
- DISCHARGE
  - Description: Discharge
  - Units: cumecs
- HYCODE_ST
  - Description: Hydrolog code for stage
  - Examples: 0 = no problems
- HYCODE_DI
  - Description: Hydrolog code for discharge
  - Examples: 0 = no problems; 3 = data suspect
- WICODE_ST
  - Description: Wiski code for stage
- WICODE_DI
  - Description: Wiski code for discharge
  - Examples: 1 = good, within rating; 2 = estimated, within rating; 3 = missing; 4 = suspect, within rating; 5 = unchecked, within rating

## Additional Quality Information
- File: WDquality.csv
- Structure:
  - FIELDNAME: Variable to which quality info relates
  - FROM_DATE / TO_DATE: Date range the quality info applies to
  - DATETYPE: Code indicating time length of the quality info (R = range; D = single date)
  - CONTINUING: Y/N indicating if the issue is ongoing
  - SITECODE: ECN site the quality info relates to
  - DESCRIPTION: Detailed quality information

## Practical Implications for Data Stewards
- Data governance and provenance:
  - Ensure proper acknowledgement of ECN data usage and capture reprints as required.
  - Track data provenance across multiple logger formats (WISKI and Hydrolog) and ensure accompanying quality metadata is used.
- Data quality and interoperability:
  - Apply quality codes (HYCODE and WICODE) and consult WDquality.csv for context on data issues.
  - Handle site-specific metadata (site codes, coordinates, date ranges) to maintain accurate discovery and attribution.
- Data ingestion and updates:
  - Be aware of protocol documentation and ensure update mechanisms respect data availability, embargoes, and potential proprietary constraints.
  - Maintain consistent data structures (SITECODE, SDATE, SHOUR, SMINS, FIELDNAME, VALUE) across portals and catalogs.
- User needs alignment:
  - The dataset provides 15-minute summaries with higher-frequency metadata; data stewards should ensure users understand the time resolution and quality indicators for appropriate reuse.