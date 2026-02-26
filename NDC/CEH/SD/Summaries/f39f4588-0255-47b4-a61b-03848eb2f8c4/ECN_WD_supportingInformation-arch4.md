# Dataset Originator

- ECN Data Centre (http://data.ecn.ac.uk; ecn@ceh.ac.uk), Centre for Ecology and Hydrology
- Data Providers: UK Environmental Change Network (ECN) programme funded by a consortium of UK government departments and agencies (including AFBI, BBSRC, NRW, DSTL, DEFRA, Environment Agency, Forestry Commission, Welsh Government, Natural England, NERC, NI Environment Agency, SEPA, Scottish Government, Scottish Natural Heritage)
- Acknowledgement and citation: Please acknowledge use of data and send one reprint of any publication citing the data

## Purpose and context

- Provides 15-minute summaries from 10-second samplings from ECN site loggers
- Includes accompanying quality information to assess data suitability
- Moor House - Upper Teesdale data logged with Environment Agency tools (WISKI format; Hydrolog format prior to 2004) with embedded quality information
- Metadata and quality codes are documented in accompanying materials (WDquality.csv)

## Protocol and usage notes

- Data structure uses: SITECODE, SDATE, SHOUR, SMINS, FIELDNAME, VALUE
- Use accompanying quality information when analyzing data
- Quality codes and formats vary by site and logging system; explanations provided in the dataset notes

## Data structure and content

- SITECODE: Unique ECN site code
- SDATE: Date of data recording
- SHOUR: Hour of recording
- SMINS: Minute of recording
- FIELDNAME: Measured variable
- VALUE: Measured value

## Site Codes and coverage

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
- T11 Snowdon (Y Wyddfa)
  - Location: 53° 4' 28.38" N, 4° 2' 0.64" W
  - Date range: 02-Jul-1997 to 27-Dec-2012

## Fieldnames and measurements

- STAGE: Stage height (m)
- DISCHARGE: Discharge (cumecs)
- HYCODE_ST: Hydrolog code for stage (0 = no problems)
- HYCODE_DI: Hydrolog code for discharge (0 = no problems; 3 = data suspect)
- WICODE_ST: WISKI code for stage
- WICODE_DI: WISKI code for discharge (1 = good; 2 = estimated; 3 = missing; 4 = suspect; 5 = unchecked)

## Additional quality information

- WDquality.csv provides:
  - FIELDNAME: Variable quality info relates to
  - FROM_DATE / TO_DATE: Date range for the quality info
  - DATETYPE: Code indicating scope (range or single date)
  - CONTINUING: Whether the issue is ongoing (Y/N)
  - SITECODE: Applicable ECN site
  - DESCRIPTION: Detailed quality information

## Usage considerations for data leaders

- Data provenance and governance: Dataset originates from multiple ECN sites with defined QA/QC and multiple formats; ensure consistent metadata alignment and traceability
- Data availability and access barriers: Some formats (WISKI, Hydrolog) and site-specific quality codes may require careful interpretation
- Data quality and standards: Varying quality flags and incomplete metadata necessitate verification before integration into broader analyses
- Collaboration and attribution: Acknowledge ECN origin, include reprint requests for publications citing the data, and consider contributing to cross-site communities of practice to improve data coordination
- Data product readiness: Metadata, quality flags, and site-specific details support responsible data products, dashboards, and policy informatics with clear uncertainty handling