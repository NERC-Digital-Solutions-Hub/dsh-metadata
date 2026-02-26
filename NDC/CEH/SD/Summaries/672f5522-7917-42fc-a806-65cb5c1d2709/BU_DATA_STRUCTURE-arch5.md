# UK Environmental Change Network Rabbits and Deer (BU) Dataset

## Overview
- Dataset from the UK Environmental Change Network (ECN), focusing on rabbits, deer, and related transect observations across multiple ECN sites.
- Purpose: provide relative abundance estimates (via dropping counts) and associated transect data to support environmental-change research.
- Data producers and owners: ECN Data Centre (Centre for Ecology and Hydrology) and ECN programme leadership; ECN sponsors include multiple UK government departments and agencies.
- Usage guidance: acknowledge data use and submit one reprint of any publication citing the dataset; use accompanying quality information when analyzing data.

## Dataset origin and ownership
- Dataset Originator: ECN Data Centre, Centre for Ecology and Hydrology (ECN data hub).
- Dataset Owners: The UK Environmental Change Network programme; funded by a consortium of UK government departments and agencies (e.g., AFBI, BBSRC, Natural England, DEFRA, Environment Agency, NE, NERC, Scottish Government, etc.).
- Acknowledgement and dissemination: Users should acknowledge use of ECN datasets and provide one reprint of publications citing the data.

## Protocol and methodology
- Measurement approach: dropping counts collected on transects twice yearly (late March and late September) as an index of relative abundance for rabbits and deer; Moor House data uses the same method to estimate grouse abundance.
- An explicit note: there are no practicable direct population size measurements; interpretation is via the dropping-count index.
- Metadata emphasis: users should consult accompanying quality information for proper data use.

## Data structure and schema
- Data are stored in Oracle databases, organized as nine site-specific tables for each data type:
  - D1BU_xxx: core observational data (one table per site).
  - D2BU_xxx: droppings data (one table per site).
  - D3BU_xxx: transect (transect section) data (one table per site).
- Key fields across tables:
  - SITECODE (site code), LCODE (location code), SDATE (sampling date), PLOTID (transect section), FIELDNAME (data field name), VALUE (measurement value).
  - D2BU includes CLEARDATE (date droppings cleared) and SURVEY (survey reference).
  - D3BU includes LENGTH (transect length) and HABDESC (habitat description); various fields are defined per site with appropriate data types.
- Core metadata: structure documented separately in ECN metadata documentation.

## Site coverage and date ranges
- Nine ECN sites included (site codes and names):
  - T01 – Drayton (Location: 52°11'37.95"N 1°45'51.95"W); date range in dataset: 01-APR-1993 to 11-OCT-2006.
  - T03 – Hillsborough (54°27'12.24"N 6°4'41.26"W); 07-JUN-1995 to 02-MAY-2012.
  - T04 – Moor House - Upper Teesdale (54°41'42.15"N 2°23'16.26"W); 14-MAY-1993 to 10-OCT-2012.
  - T05 – North Wyke (50°46'54.96"N 3°55'4.10"W); 23-MAR-1993 to 28-SEP-2012.
  - T06 – Rothamsted (51°48'12.33"N 0°22'21.66"W); 11-APR-1994 to 18-OCT-2010.
  - T07 – Sourhope (55°29'23.47"N 2°12'43.32"W); 12-MAY-1993 to 28-SEP-1993.
  - T08 – Wytham (51°46'52.86"N 1°20'9.81"W); 06-MAY-1993 to 01-OCT-2012.
  - T09 – Alice Holt (51° 9'16.46"N 0°51'47.58"W); 10-OCT-1994 to 10-NOV-2006.
  - T10 – Porton Down (51° 7'37.83"N 1°38'23.46"W); 22-APR-1994 to 17-APR-2012.

## Field definitions and data types
- Field names and data categories cover counts of deer (D), grouse (G), rabbits (R), and sheep (S), plus quality codes (Q1–Q8) for each observation.
- Quality codes: standard ECN quality codes are applied (e.g., 100, 101, 102, …, 513, 999). They indicate issues such as data loss, partial sample loss, debris in samples, equipment problems, non-standard sampling, and other conditions affecting data quality.
- 999 code: Unusual event requiring accompanying text in the quality metadata.

## Quality codes and data quality
- ECN quality codes provide a standardized mechanism to flag factors that may affect data quality.
- Codes are assigned by ECN site managers; multiple codes may be applied per observation as applicable.
- If an unusual event occurred not covered by standard codes, code 999 is used and detailed in accompanying quality text.
- Researchers should consult the quality metadata accompanying the dataset to interpret observations and filter data accordingly.

## Data access, usage notes, and documentation
- Data are stored in an Oracle database accessible through ECN data channels.
- Users are encouraged to consult the accompanying quality information and the core metadata documentation for proper interpretation and use.
- Documentation references include the protocol for terrestrial measurements (http://www.ecn.ac.uk/measurements/terrestrial/b/bu) and the ECN metadata documentation.
- Contact: ECN Data Centre (ecn@ceh.ac.uk); ECN website: http://www.ecn.ac.uk.

## Documentation and provenance
- Core metadata and detailed schema documentation exist beyond this summary; users should refer to the ECN metadata documentation for exact field definitions, reference tables (e.g., M_DESC, M_REFFIELD), and data type specifics.
- The dataset emphasizes traceability of data provenance, site-specific data handling, and the need to document data processing steps.