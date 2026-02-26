# Butterfly Protocol

## Overview
- Dataset created by the ECN Data Centre (Centre for Ecology and Hydrology) and distributed by the UK’s ECN program.
- Data providers include a consortium of UK government departments and agencies funding site monitoring and network coordination (e.g., DEFRA, Natural England, Natural Resources Wales, Scottish Government, SEPA, etc.).
- Purpose: monitor butterfly populations to understand environmental change, inform policy, and support monitoring decisions.
- Originator contact: ecn@ceh.ac.uk; data portal: http://data.ecn.ac.uk.

## Data use, acknowledgement, and sharing
- Users are asked to acknowledge the ECN data when using the datasets.
- Request to send one reprint of any publication that cites the use of ECN data.
- Data quality and metadata are central; users should consult accompanying quality information and the butterfly protocol for proper usage.

## Protocol (butterfly monitoring methodology)
- Butterflys are recorded on transects divided into up to 15 sections per site.
- Methodology follows the national Butterfly Monitoring Scheme (Biological Records Centre, CEH).
- Transect is walked weekly from 1 April to 29 September each year.
- Observers record butterflies flying within or passing through an imaginary 5m x 5m x 5m box in front of the observer.
- Conditions: temperature between 13-17°C and at least 60% sunshine.
- Quality information accompanying data should be used to assess suitability and applicability.

## Data structure
- SITECODE: Unique ECN site code.
- LCODE: Location ID.
- SDATE: Date of observation.
- SECTION: Transect section ID.
- FIELDNAME: Species code (numerical).
- VALUE: Measured value (count or other variable).

## Site Codes (ECN sites)
- T01 Drayton (52°11'38"N, 1°45'52"W); 14-Apr-1993 to 19-Dec-2012.
- T02 Glensaugh (56°54'33"N, 2°33'12"W); 14-Oct-1993 to 26-Dec-2012.
- T03 Hillsborough (54°27'12"N, 6°4'41"W); 02-Feb-1994 to 27-Dec-2012.
- T04 Moor House - Upper Teesdale (54°41'42"N, 2°23'16"W); 06-Oct-1992 to 24-Dec-2012.
- T05 North Wyke (50°46'55"N, 3°55'4"W); 29-Sep-1993 to 26-Dec-2012.
- T06 Rothamsted (51°48'12"N, 0°22'22"W); 02-Feb-1994 to 12-Dec-2012.
- T07 Sourhope (55°29'23"N, 2°12'43"W); 08-Dec-1993 to 26-Dec-2012.
- T08 Wytham (51°46'53"N, 1°20'10"W); 09-Jun-1993 to 12-Dec-2012.
- T09 Alice Holt (51°9'16"N, 0°51'48"W); 27-Apr-1994 to 12-Dec-2012.
- T10 Porton Down (51°7'38"N, 1°38'23"W); 17-Jan-1996 to 26-Jan-2000.
- T11 Y Wyddfa - Snowdon (53°4'28"N, 4°2'0"W); 02-Jul-1997 to 27-Dec-2012.
- T12 Cairngorms (57°6'59"N, 3°49'47"W); 06-Oct-1999 to 26-Dec-2012.

## Species list
- Extensive list of butterfly species with numeric codes mapped to Latin and common names (e.g., 2 = Aglais urticae - Small tortoiseshell; 4 = Anthocharis cardamines - Orange tip; 10 = Aporia crataegi - Black-veined white; 20 = Aricia agestis - Brown argus; 29 = Coenonympha pamphilus - Small heath; 54 = Gonepteryx rhamni - Brimstone; 75 = Maniola jurtina - Meadow brown; 90 = Papilio machaon - Swallowtail; 120 = Thymelicus sylvestris - Small skipper; 122 = Vanessa atalanta - Red admiral; 123 = Cynthia cardui - Painted lady; etc.). The list provides numerous additional codes for regional species.
- Note: The document includes a long mapping table; users should refer to the full list for precise coding.

## Additional information
- Additional dataset details stored in accompanying file ECN_IB2.csv, including:
  - SITECODE, LCODE, SDATE, SHOUR, SMINS, RECORDER, RECCODE, TEMP, SUNPERC, WSPEEDB, WEEK.
- This file supplements the main data with sampling timing, weather, and recorder information.

## Quality information
- Quality metadata stored in accompanying file ECN_IB_qtext.csv, including:
  - LCODE, SITECODE, FIELDNAME, FROM_DATE, TO_DATE, DATETYPE, CONTINUING, DESCRIPTION.
- Provides detailed quality notes to assess data confidence, consistency, and applicability over time and space.

## Data governance and accessibility (context for monitoring frameworks)
- Data sharing and governance considerations include:
  - Clear data provenance (originator and providers) and contact information.
  - Requirements to acknowledge data use and provide publications reprints.
  - Availability of accompanying quality and metadata documents to support data interpretation and reuse.
- Core monitoring outputs are produced as structured data (coded fields, transect-based counts) suitable for integration into environmental health dashboards, trend analyses, and policy evaluations.
- The protocol emphasizes standardized methodology, metadata richness, and data quality documentation to support transparency and comparability across sites and years.