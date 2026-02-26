# Dataset Originator

## Overview
- 15-minute summaries derived from 10-second samplings collected by loggers.
- Includes accompanying quality information; Moor House – Upper Teesdale data stored in WISKI format (Hydrolog format used prior to 2004) with quality codes available.
- An accompanying quality file (WDquality.csv) provides detailed quality flags for variables.
- A protocol document (streamWaterDischargeProtocol.pdf) explains data collection and processing.

## Data provenance and providers
- Originator: ECN Data Centre (http://data.ecn.ac.uk; ecn@ceh.ac.uk), Centre for Ecology and Hydrology.
- Data Providers: UK Environmental Change Network (ECN) programme funded by a consortium of UK government departments and agencies, including:
  - Agri-Food and Biosciences Institute
  - Biotechnology and Biological Sciences Research Council
  - Cyfoeth Naturiol Cymru – Natural Resources Wales
  - Defence Science & Technology Laboratory
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
- Usage acknowledgement: Please acknowledge data use and send one reprint of any publication citing these data.

## Data structure
- Core time-series fields: SITECODE, SDATE (date), SHOUR (hour), SMINS (minute), FIELDNAME (variable measured), VALUE (measured value).
- Site codes:
  - T02 Glensaugh (56°54'33.36"N, 2°33'12.14"W); date range 14-Oct-1993 to 26-Dec-2012.
  - T04 Moor House – Upper Teesdale (54°41'42.15"N, 2°23'16.26"W); 06-Oct-1992 to 24-Dec-2012.
  - T07 Sourhope (55°29'23.47"N, 2°12'43.32"W); 08-Dec-1993 to 26-Dec-2012.
  - T08 Wytham (51°46'52.86"N, 1°20'9.81"W); 09-Jun-1993 to 12-Dec-2012.
  - T11 Yn Wyddfa – Snowdon (53°4'28.38"N, 4°2'0.64"W); 02-Jul-1997 to 27-Dec-2012.
- Variables and units:
  - STAGE: Stage Height (meters)
  - DISCHARGE: Discharge (cumecs)
- Quality indicators:
  - HYCODE_ST, HYCODE_DI: Hydrolog code for stage/discharge (e.g., 0 = no problems; 3 = data suspect for DI).
  - WICODE_ST, WICODE_DI: WISKI codes for quality of stage/discharge (e.g., 1 = good; 2 = estimated; 3 = missing; 4 = suspect; 5 = unchecked).
- Notes: In Moor House data, quality information is available; additional quality codes are provided in accompanying files.

## Quality information and data integrity
- WDquality.csv provides detailed quality information per FIELDNAME, date ranges, and SITECODE, including:
  - FROM_DATE, TO_DATE
  - DATETYPE (length of time quality applies to)
  - CONTINUING (Y/N)
  - SITECODE and DESCRIPTION (quality notes)
- Important to consult quality metadata when analyzing or mapping data to ensure accurate interpretation.

## GIS and data use notes
- Data are suitable for map-based visualization and temporal analysis across multiple ECN sites.
- Spatial integration possible via site coordinates and SITECODE associations; combine with time stamps (SDATE, SHOUR, SMINS) for animated or time-enabled maps.
- Data quality flags should drive filtering, uncertainty assessment, or styling (e.g., highlighting suspect or estimated values).

## Access and protocol
- Data hosted by ECN Data Centre (URL above).
- Please refer to streamWaterDischargeProtocol.pdf for collection and processing details.