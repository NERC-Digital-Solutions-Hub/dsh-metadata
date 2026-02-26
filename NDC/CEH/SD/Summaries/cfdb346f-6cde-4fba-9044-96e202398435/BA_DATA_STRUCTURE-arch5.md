# UK Environmental Change Network (http://www.ecn.ac.uk) Bats (BA)

## Overview
- Dataset originator: ECN Data Centre; data stored in Oracle database with site-specific tables D1BA_xxx (observations), D2BA_xxx (survey details), and D3BA_xxx (habitat observations) for each site.
- Dataset owners: The UK Environmental Change Network (ECN) programme, sponsored by a consortium of UK government departments and agencies funding site monitoring or network coordination.
- Acknowledgement and publication reuse: ECN requests acknowledgement of data use and asks that researchers send one reprint of any publication citing the data.

## Data governance and access
- Ownership and governance under ECN program and sponsoring organisations.
- Reuse requirements: Acknowledge data usage; provide one reprint of any publication citing ECN data.
- Metadata and structure guidance: Core metadata tables exist; refer to the metadata documentation for full structure details.

## Data structure and schema
- Per-site data organization: Three domain tables per site (10 sites in total, one table per site per domain):
  - D1BA_xxx: Bat observations (species codes, counts, transect, location, and activity codes).
  - D2BA_xxx: Survey methodology and equipment details (bat detector type, protocol settings, reference checks, waveform/sonogram usage).
  - D3BA_xxx: Habitat observations along transects (up to three HAB fields, habitat codes, and related values).
- Naming convention: Tables are named D1BA_xxx, D2BA_xxx, and D3BA_xxx, where xxx is the site code (T01–T11 in this dataset).
- Site coverage: Ten site-specific tables per domain; site codes labeled T01–T11 with associated site information.
- Core metadata reference: For the overall metadata structure, see the dedicated metadata documentation.

## Site coverage and metadata
- Site codes and key details:
  - T01 Drayton – Location: 52°11'37.95"N, 1°45'51.95"W; Date range: 29-JUN-1993 to 05-SEP-2006
  - T02 Glensaugh – Location: 56°54'33.36"N, 2°33'12.14"W; Date range: 07-JUL-1994 to 30-AUG-2012
  - T03 Hillsborough – Location: 54°27'12.24"N, 6°04'41.26"W; Date range: 12-AUG-1994 to 05-SEP-2002
  - T04 Moor House - Upper Teesdale – Location: 54°41'42.15"N, 2°23'16.26"W; Date range: 16-JUN-1993 to 28-AUG-2012
  - T05 North Wyke – Location: 50°46'54.96"N, 3°55'4.10"W; Date range: 04-JUL-1993 to 30-AUG-2012
  - T07 Sourhope – Location: 55°29'23.47"N, 2°12'43.32"W; Date range: 12-JUL-1994 to 03-SEP-2012
  - T08 Wytham – Location: 51°46'52.86"N, 1°20'9.81"W; Date range: 05-JUL-1993 to 21-AUG-2012
  - T09 Alice Holt – Location: 51° 9'16.46"N, 0°51'47.58"W; Date range: 29-JUN-1994 to 05-SEP-2012
  - T10 Porton Down – Location: 51° 7'37.83"N, 1°38'23.46"W; Date range: 04-JUL-1994 to 03-SEP-2006
  - T11 Y Wyddfa - Snowdon – Location: 53° 4'28.38"N, 4° 2'0.64"W; Date range: 16-JUL-1996 to 31-AUG-2011
- Note: The document lists site coordinates and date ranges, reflecting the temporal coverage of bat observations at each site.

## Data content and coding schemes
- Bat species field (D1BA_xxx FIELDNAME and VALUE):
  - Field FIELDNAME holds species codes (e.g., Bb, Es, M, Ms, Mb, Md, Mm, Mw, Mn, Nl, Nn, Pp, Ppl, Ppg, P, Pa, Pg, Rf, Rh, UU, XX for no bats).
  - VALUE holds counts for observed species.
  - A compact species key maps codes to Latin and common names (e.g., Bb = Barbastella barbastellus, Pp = Pipistrellus, XX = No bats found).
- Habitat observations (D1BA_xxx HAB1/HAB2/HAB3 fields and values):
  - Up to three habitat types recorded per sighting (HAB1–HAB3).
  - HABn values reference habitat type codes 1–43, with detailed descriptions (e.g., hedgerows, treelines, stone walls, roads, streams, ponds, various woodland and grassland types, arable land, built land, etc.; 43 = Others).
  - The habitat descriptions cover a broad range of landscape features and land cover types.
- Habitat and site association:
  - D3BA_xxx captures habitat context alongside transect data, including the habitat codes linked to each bat sighting location.
- Survey methodology (D2BA_xxx):
  - Information about bat detector type, whether the detector was kept at 45Hz, frequency adjustments, reference comparisons, and whether sonogram analysis was used.
  - These fields help document the data collection protocol and quality considerations.
- Data quality and protocol notes:
  - Methodology: transects conducted four times per year within specified three-week windows; surveys not conducted in heavy rain or strong winds.
  - Limitations: The methodology provides a broad view and has limitations in linking precise population levels to environmental change; cross-reference with broader monitoring programs to mitigate.
  - Quality information: Researchers should consult accompanying quality metadata when using the data.

## Usage notes and metadata considerations
- Acknowledgement and reuse: ECN requests acknowledgement of data use and the submission of one reprint if the data are used in publications.
- Metadata documentation: The core metadata tables are referenced; users should consult the metadata documentation for the complete data structure and field definitions.
- Publishing mindset and data usability: Data stewardship guidance implies ensuring the data are documented and usable for discovery and reuse, with clear provenance, structure, and field mappings.