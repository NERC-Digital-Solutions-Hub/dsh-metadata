# Butterfly Monitoring Dataset (ECN)

## Overview and purpose
- ECN Data Centre (Centre for Ecology and Hydrology) acts as the dataset originator.
- The UK Environmental Change Network (ECN) data provide long-term environmental monitoring data to understand environmental change.
- Collaboration among multiple government departments and agencies funds site monitoring and network coordination.
- Acknowledgement: Users must acknowledge data use and send one reprint of any publication citing ECN data.

## Data providers and sponsorship
- ECN is sponsored by a consortium including: Agri-Food and Biosciences Institute; BBSRC; Natural Resources Wales; DSTL; Defra; Environment Agency; Forestry Commission; Welsh Government; Natural England; NERC; Northern Ireland Environment Agency; Scottish Environment Protection Agency; Scottish Government; Scottish Natural Heritage.

## Protocol and data collection (butterfly monitoring)
- Protocol referenced by accompanying butterflyProtocol.pdf.
- Notes:
  - Butterfly species recorded on transects divided into up to 15 sections.
  - Method follows the national Butterfly Monitoring Scheme by the Biological Records Centre (CEH).
  - Transect walked weekly from 1 April to 29 September; observer records butterflies seen within a defined 5m x 5m x 5m imaginary box.
  - Temperature targeted between 13-17°C; sunshine of at least 60%.
  - Use of accompanying quality information when using the data.

## Data structure and schema
- Core data fields:
  - SITECODE: Unique ECN site code (references a site).
  - LCODE: Location ID.
  - SDATE: Date data was recorded.
  - SECTION: Transect section ID.
  - FIELDNAME: Species code (see species list).
  - VALUE: Measured value.
- Additional qualitative/auxiliary data are provided in separate files:
  - ECN_IB2.csv: Supplementary sampling details (site, location, date/time, recorder, temperature, sunshine, wind, week).
  - ECN_IB_qtext.csv: Quality information linked to locations and variables, with date ranges and descriptive notes.

## Site codes and data coverage
- 12 ECN sites (T01–T12) with corresponding site names, coordinates, and date ranges:
  - T01 Drayton; T02 Glensaugh; T03 Hillsborough; T04 Moor House - Upper Teesdale; T05 North Wyke; T06 Rothamsted; T07 Sourhope; T08 Wytham; T09 Alice Holt; T10 Porton Down; T11 Snowdon; T12 Cairngorms.
  - Date ranges vary from the early 1990s to around 2012, with specific start/end dates per site.
- Site coordinates and dataset date spans are provided to contextualize temporal coverage and geographic distribution.

## Species list and coding
- Comprehensive list of butterfly species coded with Latin and common names (e.g., 2 = Aglais urticae – Small tortoiseshell; 4 = Anthocharis cardamines – Orange tip; 10 = Aporia crataegi – Black-veined white; 12 = Argynnis aglaja – Dark green fritillary; 36 = Cupido minimus – Small blue; 90 = Papilio machaon – Swallowtail; etc.).
- Codes are used in FIELDNAME to denote species observations; extensive mapping provided to interpret data values.

## Additional information
- ECN_IB2.csv contains additional sampling metadata:
  - SITECODE, LCODE, SDATE, SHOUR, SMINS, RECORDER, RECCODE, TEMP, SUNPERC, WSPEEDB, WEEK, etc.
- ECN_IB_qtext.csv contains detailed quality notes:
  - Links quality descriptions to specific locations, variables, date ranges, and status (continuing or not).

## Quality and governance considerations for data stewards
- Quality information exists as a separate file (ECN_IB_qtext.csv) to document data quality issues, ranges, and timing.
- Data stewards should:
  - Ensure metadata completeness (site, location, date, temperature, light, wind, etc.) and consistency across datasets.
  - Respect data sharing limitations and document updates or embargoes as indicated by accompanying files.
  - Upload dataset updates to relevant portals and catalogue holdings when applicable.
  - Document processing steps (quality checks, cleaning, transformations) and any methodological deviations.

## Practical considerations and challenges for data stewardship
- Incomplete picture of user needs may require providing usable, well-documented datasets with clear metadata and quality notes.
- Timely access to data from multiple sites can be challenging; maintain coordination with data providers to minimize delays.
- Aligning data from diverse systems and formats (e.g., core data, supplementary files, quality metadata) to deliver an interoperable dataset.
- Handling large, multi-site datasets with long temporal coverage and extensive species lists.
- Ensuring metadata and quality information remains synchronized with data releases.

## End-user guidance and reuse
- Users should consult the main protocol (butterflyProtocol.pdf) for collection rules and quality expectations.
- Acknowledge ECN data use and supply a reprint of any publication citing the data.
- Before sharing or publishing, verify metadata completeness (SITECODE, LCODE, SDATE, SECTION, FIELDNAME, VALUE) and consult ECN_IB2.csv and ECN_IB_qtext.csv for context and quality constraints.