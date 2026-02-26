# Dataset Originator ECN Data Centre (http://data.ecn.ac.uk - ecn@ceh.ac.uk), Centre for Ecology and Hydrology.

- A dataset describing Macrolepidoptera (moth) monitoring across ECN sites, using standard light-trap protocols.
- Data are produced by the ECN Data Centre and compiled with partner organisations supporting environmental-change research.

## Overview and purpose for GIS users

- Provides time-stamped, site-based moth catch data suitable for map-based visualisations of spatial and temporal patterns of moth activity and quality.
- Designed for integration with GIS workflows to explore spatial distributions, trends, and potential environmental drivers.

## Dataset provenance and ownership

- Originator: ECN Data Centre.
- Owners: UK Environmental Change Network (ECN) programme, funded by a consortium of UK government departments and agencies.
- Partner organisations include: Agri-Food and Biosciences Institute; BBSRC; Natural Resources Wales; Defence Science & Technology Laboratory; DEFRA; Environment Agency; Forestry Commission; Welsh Government; Natural England; NERC; SEPA; Scottish Government; Scottish Natural Heritage.
- ECN requests acknowledgement of data use and a reprint of publications citing the data.

## Protocol and data collection

- Protocol: Standard operating procedures to ensure comparability across sites; methodology aligns with Rothamsted Insect Survey (RIS) practices.
- Sampling: Macrolepidoptera identified using standard light-trap methods; data recorded nightly.
- Quality guidance: Use accompanying quality information when using the data (supplementary files).

## Data structure and download format

- Each data row includes:
  - SITECODE: Unique ECN Site code (e.g., T01–T12).
  - LCODE: Location ID (unique within site).
  - FROMDATE: Start date traps were set.
  - SDATE: Sampling date.
  - SPERIOD_D: Period over which traps were open (days).
  - YEAR: Year of sampling.
  - WEEK: Week number.
  - FIELDNAME: Variable being measured (e.g., quality codes Q1–Q8 or species codes).
  - VALUE: Measured value.
- Supporting documentation:
  - ECN_IM2.csv: Period over which moth traps were set (days); includes SITECODE, LCODE, FROMDATE, SDATE, SPERIOD_D, YEAR, WEEK.
  - ECN_IM_qtext.csv: Quality-text notes and codes assigned by site managers; can accompany data where quality text is used (code 999 indicates an unusual event; full text in this file).
- Site coordinates and locations are described for each site code (examples below).

## Site codes and locations (Explanatory Information)

- T01 Drayton: 52°11'37.95"N, 1°45'51.95"W
- T02 Glensaugh: 56°54'33.36"N, 2°33'12.14"W
- T03 Hillsborough: 54°27'12.24"N, 6°4'41.26"W
- T04 Moor House - Upper Teesdale: 54°41'42.15"N, 2°23'16.26"W
- T05 North Wyke: 50°46'54.96"N, 3°55'4.10"W
- T06 Rothamsted: 51°48'12.33"N, 0°22'21.66"W
- T07 Sourhope: 55°29'23.47"N, 2°12'43.32"W
- T08 Wytham: 51°46'52.86"N, 1°20'9.81"W
- T09 Alice Holt: 51° 9'16.46"N, 0°51'47.58"W
- T10 Porton Down: 51° 7'37.83"N, 1°38'23.46"W
- T12 Cairngorms: 57° 6'58.84"N, 3°49'46.98"W
- Note: Site codes are listed with corresponding locations; further site information is available in the accompanying catalogue link.

## Variables and measurement details

- FIELDNAME entries cover:
  - Quality codes (Q1–Q8; multiple fields) and Common Name placeholders.
  - Numerous species codes mapping to moth species (e.g., 100, 101, 102, etc. with associated common names).
- The dataset includes a comprehensive species code list (hundreds of entries) mapping numeric codes to scientific names and common names for Macrolepidoptera.
- The mapping is extensive; GIS work typically involves joining FIELDNAME (species or quality code) to the corresponding label from the provided reference.

## Data quality and interpretation

- Site managers assign quality codes to indicate data quality factors; codes are drawn from a standard list, with 999 used to flag unusual events requiring text notes.
- Quality and text notes are provided in the ECN_IM_qtext.csv file and linked to observations in ECN_IM2.csv data.
- Users should consult the quality codes and accompanying text to assess data reliability, sampling conditions, and any site-specific disturbances.

## Usage guidance for GIS applications

- Data are site-level, time-stamped observations with location coordinates, suitable for map-based visualization of moth distribution, phenology, and site comparisons.
- Important to integrate:
  - The trap period data from ECN_IM2.csv (SPERIOD_D) to understand sampling coverage.
  - The quality notes from ECN_IM_qtext.csv for contextual interpretation of specific observations.
- Large and complex species lists exist; consider linking FIELDNAME to a master species catalogue to ensure consistent labeling across datasets and visualizations.

## Access, attribution, and citations

- Acknowledge ECN data usage in any outputs.
- Provide one reprint of any publication citing the data.
- ECN and partner organisations are the data custodians; dataset should be used in line with their protocols and quality guidelines.

## Notes and special cases

- The dataset includes notes on certain species codes:
  - 3392: Mesapamea secalis/didyma (species pair that cannot be separated without dissection; females cannot be easily distinguished in some cases).
  - 3394: Amphipyra berbera berbera can appear as 2507 in past data; treated as the same subspecies in current conventions.
- Users should be aware of these interpretation nuances when aggregating or mapping species data.