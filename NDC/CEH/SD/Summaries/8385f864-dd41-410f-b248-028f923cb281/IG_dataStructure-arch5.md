# Dataset Originator ECN Data Centre (http://data.ecn.ac.uk - ecn@ceh.ac.uk), Centre for Ecology and Hydrology

## Overview
- ECN dataset describing ground beetle (Carabidae) abundance collected with pitfall traps across 12 ECN sites (T01–T12) during May–October, with fortnightly sampling.
- Data are governed and released by the UK Environmental Change Network (ECN) consortium, funded by multiple government departments and agencies.
- Data usage requires acknowledging ECN and, where applicable, sending a reprint of publications citing ECN data.

## Data Ownership and Attribution
- Dataset Owners: UK Environmental Change Network programme, sponsored by a consortium of UK government departments and agencies (e.g., DEFRA, Natural England, NERC, etc.).
- Usage note: Acknowledge ECN data usage and provide one reprint of any publication citing the data.

## Protocol and Data Collection
- Standard operating procedures ensure comparability of data across sites.
- Focus: Monitor abundance of ground beetles (Carabidae) using pitfall traps.
- Sampling cadence: Fortnightly from May to October.
- Users should apply accompanying quality information when using the data.

## Data Structure and Download
- Core data fields for each observation:
  - SITECODE: Unique ECN site code
  - LCODE: Location ID (unique within site)
  - SDATE: Sampling date
  - TRAP: Trap number
  - FIELDNAME: Variable measured (see below)
  - VALUE: Measured value
  - TYPE: Additional information for certain species (e.g., Pterostichus madidus) such as gender and leg colour morphs
- A subset of records may include quality text for irregular events (see ECN_IG_qtext.csv).

## Supporting Documentation
- ECN_IG2.csv: Trap deployment details (SITECODE, LCODE, FROMDATE, SDATE)
- ECN_IG3.csv: Habitat information (SITECODE, LCODE, HABDESC)
- ECN_IG_qtext.csv: Quality text entries describing data quality issues or events; linked to quality codes (see ECN_ig_qtext.csv for details)
- Site Codes: Explanatory list of 12 ECN sites with site names and precise coordinates (T01–T12)
- Additional information on ECN sites is available at the ECN catalogue link provided in the document

## Site Codes (Explanatory Information)
- T01 Drayton (52°11'37.95"N, 1°45'51.95"W)
- T02 Glensaugh (56°54'33.36"N, 2°33'12.14"W)
- T03 Hillsborough (54°27'12.24"N, 6°4'41.26"W)
- T04 Moor House - Upper Teesdale (54°41'42.15"N, 2°23'16.26"W)
- T05 North Wyke (50°46'54.96"N, 3°55'4.10"W)
- T06 Rothamsted (51°48'12.33"N, 0°22'21.66"W)
- T07 Sourhope (55°29'23.47"N, 2°12'43.32"W)
- T08 Wytham (51°46'52.86"N, 1°20'9.81"W)
- T09 Alice Holt (51°9'16.46"N, 0°51'47.58"W)
- T10 Porton Down (51°7'37.83"N, 1°38'23.46"W)
- T11 Y Wyddfa - Snowdon (53°4'28.38"N, 4°2'0.64"W)
- T12 Cairngorms (57°6'58.84"N, 3°49'46.98"W)

## Field Names and Taxonomic Details
- FIELDNAME includes quality codes (Q1–Q8) and, for certain taxa, taxon-specific fields (e.g., 6453 codes for ground beetles).
- Taxonomic coding (6453 series) covers numerous genera and species (e.g., Cicindela, Carabus, Bembidion, Pterostichus, Abax, Harpalus, Amara, etc.), with entries indicating genus-level and species-level descriptions.
- Special codes:
  - 6453 2714 = Pterostichus madidus (species)
  - 6453 6453 etc. reflect genus and species designations across a wide range of Carabidae
- FIELDNAME may be blank to indicate whole-sample level metrics; TYPE provides additional detail for certain species (e.g., gender, leg colour morphs).
- Unidentified taxa: UU (Unidentified); XX indicates no ground beetles present.

## Quality and Metadata
- Quality Codes: A comprehensive list (100–513, plus 999) describes data quality and contextual factors (e.g., data lost, sampling issues, environmental disturbances, laboratory or field processing issues).
- Quality text: If a quality issue is not captured by existing codes, site managers can provide narrative text (linked via ECN_IG_qtext.csv).
- Quality-related flags cover a wide range of potential problems, including equipment failures, environmental impacts, sampling anomalies, and data validation concerns.

## Usage Considerations for Data Stewards
- Data should be stored and shared with consistent metadata to enable discoverability and reuse across ECN platforms.
- Documentation should accompany data uploads (protocols, site metadata, habitat information, and quality codes) to aid data users in interpretation.
- Maintain transparency about data availability and any embargoes or limitations affecting updates or access.
- Facilitate updates across sites and formats by adhering to standardized field names and taxonomic coding schemes.
- Where possible, document work performed on datasets (transformation, cleaning, and quality flagging) to support reproducibility.

## Endnotes and Access
- The document includes a link to the ECN site catalogue for additional site information.
- Users are encouraged to acknowledge ECN data usage and submit reprints of publications citing ECN data.