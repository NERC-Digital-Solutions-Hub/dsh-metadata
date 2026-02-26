# Dataset Originator ECN Data Centre (http://data.ecn.ac.uk - ecn@ceh.ac.uk), Centre for Ecology and Hydrology.

## Overview
- Description: Dataset documenting Macrolepidoptera observations from the UK Environmental Change Network (ECN) using standard light trap protocols.
- Methodology: Based on Rothamsted Insect Survey procedures; data collected nightly.
- Purpose: Facilitate data discovery, cleaning, and analysis to support environmental change research.
- Acknowledgement: Users are asked to acknowledge ECN data use and to send one reprint of any publication citing the data.

## Data structure
- Core fields:
  - SITECODE: Site identifier code
  - LCODE: Location code (always 1 in this dataset, as there is one moth trap per site)
  - SDATE: Sampling date (dd-mmm-yyyy)
  - FIELDNAME: Either a quality code or a species code
  - VALUE: If FIELDNAME is a quality code, stores the quality description; if FIELDNAME is a species code, stores the observed count
- Notes:
  - Data are structured to support self-serve analysis via standard summaries, tables, and quality flags
  - Supplemental quality information should be used when analyzing data

## Site information
- Observed sites (T01–T10, T12; T11 not listed)
  - T01: Drayton (52°11'37.95"N, 1°45'51.95"W) — Date range 02-Jan-1993 to 26-Dec-2012
  - T02: Glensaugh (56°54'33.36"N, 2°33'12.14"W) — 23-Mar-1994 to 09-Dec-2012
  - T03: Hillsborough (54°27'12.24"N, 6°4'41.26"W) — 14-Feb-1993 to 23-Nov-2012
  - T04: Moor House - Upper Teesdale (54°41'42.15"N, 2°23'16.26"W) — 01-Jan-1993 to 17-Nov-2012
  - T05: North Wyke (50°46'54.96"N, 3°55'4.10"W) — 10-Dec-1992 to 21-Dec-2012
  - T06: Rothamsted (51°48'12.33"N, 0°22'21.66"W) — 24-Feb-1992 to 17-Dec-2012
  - T07: Sourhope (55°29'23.47"N, 2°12'43.32"W) — 14-Jan-1993 to 19-Dec-2012
  - T08: Wytham (51°46'52.86"N, 1°20'9.81"W) — 22-Oct-1992 to 17-Dec-2012
  - T09: Alice Holt (51°09'16.46"N, 0°51'47.58"W) — 10-Nov-1992 to 04-Dec-2012
  - T10: Porton Down (51°07'37.83"N, 1°38'23.46"W) — 01-Mar-1994 to 24-Oct-2012
  - T12: Cairngorms (57°06'58.84"N, 3°49'46.98"W) — 01-Jan-2001 to 31-Dec-2012
- Additional site information available at ECN catalog page

## Quality and species coding
- Quality codes (Table 3a; linked to Table 4 quality codes)
  - Q1–Q8: Standard ECN quality indicators
  - 999: Textual quality note for unusual events outside standard codes
- Species codes (Table 3b; extensive mapping)
  - Hundreds of codes map to Latin names and common names of moth species (macro and micro/more cryptic taxa)
  - Examples include common moths and a wide range of macro- and micro-lepidoptera with both typical and melanic forms
  - Codes are numeric (e.g., 100 for Alder Kitten, 1001 for Rush Veneer, etc.) with many entries for both typical and variant forms
- Purpose of codes
  - Facilitate standardized counting and species-level analyses across sites and years
  - Allow easy filtering by species, groupings, or quality flags

## Usage and data quality
- Data usage guidance
  - Use accompanying quality information to interpret observations and absences
  - Acknowledge dataset origin in any outputs
- Supplemental files
  - ECN_IM2.csv: Contains information about the period (number of days) traps were set (e.g., PERIOD = 1 for daily empties)
  - ECN_IM_qtext.csv: Contains additional quality notes and explanations for unusual observations or omissions

## Access and documentation
- Primary data source and contact
  - ECN Data Centre (http://data.ecn.ac.uk)
- Additional resources
  - Supplemental quality information files described above
  - ECN site metadata and further information available through the ECN catalog page linked in the dataset notes