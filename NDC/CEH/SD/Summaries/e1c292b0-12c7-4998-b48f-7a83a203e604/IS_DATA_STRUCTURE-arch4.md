# UK Environmental Change Network (http://www.ecn.ac.uk) Spittle Bugs (IS)

## Overview
- Dataset: Spittle Bug (IS) data from the UK Environmental Change Network (ECN).
- Originator: ECN Data Centre; ECN measurements protocol.
- Owners: ECN programme sponsored by a consortium of UK government departments/agencies (e.g., DEFRA, Natural England, NERC, Welsh Government, Scottish Government, etc.).
- Usage requests: Acknowledge data use and send one reprint of publications citing ECN data.
- Protocol reference: External protocol link provided for measurement methodology.

## Data Provenance and Governance
- ECN coordinates data collection and maintenance; data centre hosts core data.
- Sponsor consortium includes multiple public bodies with a stake in environmental change research.
- Data use is governed by protocol adherence and acknowledgement requirements; quality information accompanies data.

## Protocol and Data Collection Cadence
- Purpose: Estimate an index of nymph density for two spittle bug species (Neophilaenus lineatus and Philaenus spumaris) using sweep nets; also estimate colour morph proportions of adult P. spumaris.
- Frequency: Data recorded once per year.
- Quality: Use accompanying quality information; protocol designed to support standardized measurements.

## Data Structure and Metadata
- Core data organization:
  - Nymph data: 12 tables (one per site) named D1ISN_xxx (site code xxx) in Oracle.
  - Adult data: 12 tables (one per site) named D1ISA_xxx (site code xxx) in Oracle.
- Key fields (common structure):
  - SITECODE, LCODE, SDATE (sampling date), FIELDNAME, VALUE.
  - For nymphs: ISN_SPEC indicates species (P or N); FIELDNAME describes measurements per quadrat; VALUE contains counts.
  - For adults: ISA_MORPH indicates adult colour morph; FIELDNAME and VALUE capture morph-related data; Q1–Q8 provide quality codes per entry.
- Metadata guidance: Core metadata tables referenced; site-specific data capture includes quality codes and morph descriptors.

## Site Coverage and Time Span
- 12 ECN sites (codes T01–T12) with site names, coordinates, and date ranges:
  - T01 Drayton; 1993–2006
  - T02 Glensaugh; 1994–2012
  - T03 Hillsborough; 1993–2011
  - T04 Moor House - Upper Teesdale; 1993–2012
  - T05 North Wyke; 1993–2012
  - T06 Rothamsted; 1993–2011
  - T07 Sourhope; 1994–2012
  - T08 Wytham; 1993–2012
  - T09 Alice Holt; 1994–2007
  - T10 Porton Down; 1994–2012
  - T11 Y Wyddfa - Snowdon; 1998–2012
  - T12 Cairngorms; 1999–2012
- Site-specific coordinates provided for contextual metadata and spatial analyses.

## Data Quality and Morphology
- Nymphs: 40 quadrats per site (counts per quadrat) plus additional fields for random throw checks and summary statistics:
  - NSPITCHK (random throw), MEANNYM (mean nymph count), NMAL/NFEM (males/females morph counts).
- Adult Colour Morphs: Codes for morphs (e.g., ALB, FLA, GIB, LAT, LCE, LOP, MAR, POP, PRA, QUA, TRI, TYP, UUU).
- Quality Codes:
  - Standard ECN codes 100–232, 237–239, 501–511, 513, 999 reflect data quality issues (e.g., no information, sample loss, contamination, non-standard sampling, equipment issues, etc.).
  - 999 denotes accompanying quality text for unusual events not covered by codes.
- Data quality is assessed via Q1–Q8 fields associated with measurements.

## Access, Attribution and Collaboration
- Access requires adherence to ECN protocol and proper attribution.
- Data use is expected to include acknowledgement and sharing of publications referencing ECN data.
- The dataset emphasizes coordination across sites and alignment with ECN quality and metadata standards to support discoverability and reuse.

## Practical Takeaways for Data Leaders
- Treat ECN Spittle Bugs data as a time-series, multi-site dataset with standardized offers for nymph counts and adult morph data stored in site-specific Oracle tables.
- Ensure robust metadata governance by cataloging SITE CODE, SITE NAME, LOCATION, and DATE RANGE alongside per-entry QUALITY codes (Q1–Q8) and morph specifications.
- Leverage the protocol reference and accompanying quality information to validate data before use; be mindful of annual collection cadence and potential gaps in site-year coverage.
- Address data discoverability by maintaining a catalog entry that links D1ISN_xxx and D1ISA_xxx tables to site metadata, FIELDNAME mappings, and morph codes.
- Foster cross-site coordination to minimize data duplication of effort and to strengthen the data community around ECN spittle bug monitoring.
- Plan for data access constraints (e.g., permissions and repository access to Oracle) and ensure clear attribution when integrating ECN data into analyses and reports.