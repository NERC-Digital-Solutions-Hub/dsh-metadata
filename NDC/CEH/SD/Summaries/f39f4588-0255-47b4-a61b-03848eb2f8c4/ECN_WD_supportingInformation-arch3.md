# Dataset Originator ECN Data Centre (http://data.ecn.ac.uk - ecn@ceh.ac.uk), Centre for Ecology and Hydrology

## Overview
- ECN (Environmental Change Network) dataset consisting of environmental water data from multiple UK sites.
- Data are 15-minute summaries derived from 10-second logger samplings.
- Focus on stream water discharge and related stage height, with accompanying quality information.
- Moor House - Upper Teesdale uses a different logging format (WISKI) with historical Hydrolog format data; both formats include quality codes.

## Data Originators and Providers
- Originator: ECN Data Centre.
- Data Providers: UK ECN programme funded by a consortium of government departments and agencies, including DEFRA, Environment Agency, Natural England, Natural Resources Wales, and others.
- Acknowledgement: Users should acknowledge ECN data use and provide one reprint of any publication citing the data.

## Protocol and Quality Information
- Protocol referenced: streamWaterDischargeProtocol.pdf (accompanying document).
- Quality information: Use the accompanying quality information when using the data; quality codes are provided for both stage and discharge.
- Data formats: WISKI format (for Moor House) and Hydrolog format (historical); both include quality information.

## Data Structure
- Records are organized with:
  - SITECODE: ECN site identifier
  - SDATE: Date of data recording
  - SHOUR: Hour of recording
  - SMINS: Minute of recording
  - FIELDNAME: Variable measured (e.g., STAGE or DISCHARGE)
  - VALUE: Measured value

## Site Codes and Coverage
- T02 Glensaugh: 14-Oct-1993 to 26-Dec-2012
- T04 Moor House - Upper Teesdale: 06-Oct-1992 to 24-Dec-2012
- T07 Sourhope: 08-Dec-1993 to 26-Dec-2012
- T08 Wytham: 09-Jun-1993 to 12-Dec-2012
- T11 Snowdon (Y Wyddfa): 02-Jul-1997 to 27-Dec-2012

## Field Names and Variables
- STAGE: Stage height (units: meters)
- DISCHARGE: Discharge (units: cumecs)
- HYCODE_ST / HYCODE_DI: Hydrologic codes for stage and discharge (e.g., 0 = no problems; 3 = data suspect)
- WICODE_ST / WICODE_DI: WISKI quality codes for stage and discharge (e.g., 1 = good; 2 = estimated; 3 = missing; 4 = suspect; 5 = unchecked)

## Additional Quality Information
- WDquality.csv provides metadata on quality issues:
  - FIELDNAME: Variable the quality info relates to
  - FROM_DATE / TO_DATE: Date range of the quality issue
  - DATETYPE: Code indicating whether issue applies to a range (R) or a single date (D)
  - CONTINUING: Whether the issue is ongoing (Y/N)
  - SITECODE: Site the issue relates to
  - DESCRIPTION: Detailed quality information

## Use, Access, and Governance Considerations
- Emphasizes data cleaning, transformation, analysis, and clear presentation of findings (reports, charts, dashboards).
- Encourages sharing of underlying data and implementation of data governance processes.
- Highlights practical barriers common to monitoring frameworks:
  - Data availability and data of sufficient quality
  - Access delays and organizational data silos
  - Requirements to publicly share datasets
  - Keeping data up to date and ensuring adequate metadata
  - The effort required to transform data into usable formats
  - Communicating complex findings clearly
  - Establishing data governance for storage, sharing, and updates