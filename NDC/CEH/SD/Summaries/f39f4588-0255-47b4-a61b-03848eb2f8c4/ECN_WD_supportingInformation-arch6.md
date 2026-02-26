# Dataset Originator

## Overview
- 15-minute summaries from 10-second samplings collected by a logger, across ECN sites.
- Data include quality information and are available in formats from Moor House (WISKI) or Hydrolog formats.
- Site-specific quality codes and detailed quality metadata accompany the data.

## Data Providers and Aim
- ECN (UK Environmental Change Network) dataset, sponsored by a consortium of UK government departments and agencies.
- Partner organizations include: Agri-Food and Biosciences Institute; BBSRC; Natural Resources Wales; DEFRA; Environment Agency; Forestry Commission; Welsh Government; Natural England; NERC; Northern Ireland Environment Agency; Scottish Environment Protection Agency; Scottish Government; Scottish Natural Heritage.
- ECN requests acknowledgement of data use and one reprint of any publication citing the data.

## Protocol and Data Quality
- Protocol: streamWaterDischargeProtocol.pdf accompanies the dataset.
- Use accompanying quality information whenever using the data.
- Moor House - Upper Teesdale data uses Environment Agency loggers stored in WISKI format (Hydrolog format used prior to 2004); both formats include quality information (available for Moor House only).
- Quality codes and related explanations are provided in the accompanying materials.

## Data Structure
- Core fields: SITECODE, SDATE, SHOUR, SMINS, FIELDNAME, VALUE.
- SITECODE: ECN site identifier; SDATE: date; SHOUR: hour; SMINS: minute; FIELDNAME: variable measured; VALUE: measured value.

## Site Codes and Dataset Range
- T02 Glensaugh: 56° 54' 33.36" N, 2° 33' 12.14"W; 14-Oct-1993 to 26-Dec-2012.
- T04 Moor House - Upper Teesdale: 54° 41' 42.15" N, 2° 23' 16.26"W; 06-Oct-1992 to 24-Dec-2012.
- T07 Sourhope: 55° 29' 23.47" N, 2° 12' 43.32"W; 08-Dec-1993 to 26-Dec-2012.
- T08 Wytham: 51° 46' 52.86" N, 1° 20' 9.81"W; 09-Jun-1993 to 12-Dec-2012.
- T11 Y Wyddfa - Snowdon: 53° 4' 28.38" N, 4° 2' 0.64"W; 02-Jul-1997 to 27-Dec-2012.

## Field Names
- STAGE: Stage Height (m).
- DISCHARGE: Discharge (cumecs).
- HYCODE_ST: Hydrolog code for stage (0 = no problems).
- HYCODE_DI: Hydrolog code for discharge (0 = no problems; 3 = data suspect).
- WICODE_ST: WISKI code for stage.
- WICODE_DI: WISKI code for discharge (1 = good; 2 = estimated; 3 = missing; 4 = suspect; 5 = unchecked).

## Additional Quality Information
- Additional metadata provided in WDquality.csv.
- WDquality.csv structure:
  - FIELDNAME: variable related to the quality info.
  - FROM_DATE / TO_DATE: date range the quality info applies to.
  - DATETYPE: code indicating the time length to which the quality info relates (R = range; D = single date).
  - CONTINUING: Y/N flag for continuing issues.
  - SITECODE: ECN site related to the quality info.
  - DESCRIPTION: detailed quality information.

## Usage and Attribution
- Acknowledge ECN data usage to gauge dataset impact and value for environmental change research.
- Send one reprint of any publication that cites the ECN data.
- Data are intended to support analysis, combining datasets, and creating self-serve data products with appropriate quality controls.