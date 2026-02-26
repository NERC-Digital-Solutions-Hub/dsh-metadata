# UK Environmental Change Network (http://www.ecn.ac.uk) Ground Predators (IG)

## Overview

- Dataset originator: ECN Data Centre, Centre for Ecology and Hydrology.
- Dataset owners: The UK Environmental Change Network (ECN) programme, sponsored by a consortium of UK government departments and agencies.
- Acknowledgement and use: ECN requests acknowledgement of data use and one reprint of any publication citing the data.
- Protocol reference: http://www.ecn.ac.uk/measurements/terrestrial/i/ig
- Purpose: Monitor abundance of ground predators (Carabidae) using pitfall traps; data recorded fortnightly from May to October; accompanying quality information should be used when analyzing the data.

## Protocol and Sampling Design

- Sampling method: Pitfall traps to monitor ground predator abundance.
- Temporal coverage: Fortnightly data collection between May and October.
- Quality information: Each dataset includes accompanying quality information; use these quality codes to assess data reliability and context.

## Data Organization and Storage

- Core data storage: Oracle database with 12 site-specific tables for each data type.
  - D1IG_xxx: Site data tables (one per site; xxx is the site code).
  - D2IG_xxx: Traps set/collection timing tables (one per site).
  - D3IG_xxx: Habitat information tables (one per site).
- Table structure (highlights):
  - Common fields across D1IG_xxx and D2IG_xxx: SITECODE, LCODE, SDATE (sampling date), FROMDATE (date traps were set), etc.
  - D1IG_xxx: Includes SITE, LOCATION, SDATE, VALUE, and related metadata fields.
  - D2IG_xxx: Includes FROMDATE (set date) and SDATE (collection date).
  - D3IG_xxx: Includes HABDESC (habitat description) and LCODE.
- Metadata: Core metadata tables exist with additional documentation (refer to the metadata documentation for full structure).

## Site Details

- There are 12 sites (T01–T12) with names, coordinates, and dataset date ranges:
  - T01 Drayton — location: 52°11'37.95"N 1°45'51.95"W — date range: 12-MAY-1993 to 28-OCT-2009.
  - T02 Glensaugh — 56°54'33.36"N 2°33'12.14"W — 27-MAY-1994 to 31-OCT-2012.
  - T03 Hillsborough — 54°27'12.24"N 6°4'41.26"W — 14-MAY-1993 to 31-OCT-2012.
  - T04 Moor House - Upper Teesdale — 54°41'42.15"N 2°23'16.26"W — 20-MAY-1993 to 17-OCT-2012.
  - T05 North Wyke — 50°46'54.96"N 3°55'4.10"W — 05-MAY-1993 to 30-NOV-2010.
  - T06 Rothamsted — 51°48'12.33"N 0°22'21.66"W — 28-JUL-1992 to 03-NOV-2009.
  - T07 Sourhope — 55°29'23.47"N 2°12'43.32"W — 25-MAY-1994 to 14-NOV-2012.
  - T08 Wytham — 51°46'52.86"N 1°20'9.81"W — 26-MAY-1993 to 31-OCT-2012.
  - T09 Alice Holt — 51° 9'16.46"N 0°51'47.58"W — 18-MAY-1994 to 31-OCT-2012.
  - T10 Porton Down — 51° 7'37.83"N 1°38'23.46"W — 24-MAY-1994 to 31-OCT-2012.
  - T11 Y Wyddfa - Snowdon — 53° 4'28.38"N 4° 2'0.64"W — 19-MAY-1999 to 28-NOV-2012.
  - T12 Cairngorms — 57° 6'58.84"N 3°49'46.98"W — 23-JUN-1999 to 14-NOV-2012.

## Data Fields and Taxonomy

- Field names (in data tables) can contain either species codes or quality codes.
- Fieldname examples:
  - Q1–Q8: Quality codes (descriptions provided in the Quality Codes section).
  - VALUE: Numerical measurement (integer/decimal).
  - SITECODE, LCODE: Site and location codes.
  - SDATE: Sampling date.
  - FROMDATE: Date traps were set (D2IG tables).
  - HABDESC: Habitat description (D3IG tables).
- Field naming and data types are designed to support multi-site, multi-site-habitat, and time-series analyses.

## Species Codes and Taxonomic Coverage

- Species Codes: Extensive mapping linking codes to beetle taxa (Carabidae) with genus and species levels.
- Example structure:
  - Codes correlate to Latin names and taxonomic ranks (GENUS, SPECIES).
  - The dataset includes hierarchical mappings (e.g., genus-level tokens and species-level tokens) for many taxa across numerous genera and species.
- The taxonomy cover includes numerous genera and species (e.g., Bembidion, Harpalus, Amara, Carabus, Drypta, etc.), with many entries showing both genus-level and species-level classifications.
- A dedicated “Species Codes” section provides the full mappings used in the dataset.

## Quality Codes and Data Integrity

- ECN quality codes are assigned by site managers to indicate factors affecting data quality (e.g., equipment issues, environmental disturbances, sampling anomalies).
- Standard codes include numeric values with descriptive text (e.g., 100 No information available; 101 No sample/reading taken; …; 999 Unusual event with accompanying quality text).
- Quality information can be extensive and may be accompanied by textual notes for unusual events not covered by standard codes.
- Quality codes help data stewards assess data reliability, understand context, and apply appropriate filtering or weighting in analyses.

## Data Use, Governance, and Documentation

- Data governance: The ECN program emphasizes appropriate data governance, metadata, and standardization across sites and datasets.
- Documentation: Core metadata tables exist; researchers should refer to the accompanying metadata documentation for full schema details.
- Data sharing and updates: The data are organized to support updating and dissemination through relevant ECN portals; data creators/sharers should be guided toward standards for metadata, format, and quality information.
- Protocol and acknowledgement: When using the data, acknowledge ECN usage and, if possible, provide a reprint of publications citing the data.

## Protocol Reference

- I/IG measurement protocol and measurement specifics are available at: http://www.ecn.ac.uk/measurements/terrestrial/i/ig

## Summary for Data Stewards

- The UK Environmental Change Network Ground Predators (IG) dataset is a multi-site, longitudinal dataset of ground beetle abundance collected via pitfall traps, spanning 12 ECN sites with detailed site, trap, and habitat data stored in an Oracle-based multi-table schema (D1IG_xxx, D2IG_xxx, D3IG_xxx).
- Data are organized to support cross-site comparisons and long-term analyses, with comprehensive taxonomy mappings (Species Codes) and quality flags (Quality Codes) to document data reliability and context.
- Governance considerations include clear data origin, ownership, acknowledgement requirements, protocol references, and metadata availability to enable discovery, reuse, and appropriate data sharing and updates.
- For data access and use, refer to the ECN data centre and accompanying metadata documentation; ensure quality codes are consulted to assess data suitability for analysis.