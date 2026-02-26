# UK Environmental Change Network (http://www.ecn.ac.uk) Atmospheric Chemistry: Nitrogen Dioxide (AN)

## Overview
- Dataset from the UK Environmental Change Network (ECN) focusing on atmospheric NO2 measured with passive diffusion tubes.
- Dataset originator: ECN Data Centre (Centre for Ecology and Hydrology); Dataset owners: ECN programme funded by a consortium of UK government departments and agencies.
- Data usage request: Acknowledge use of datasets and send one reprint of any publication citing the data.
- Protocol reference provided via ECN measurements page.

## Provenance and governance
- Measurements conducted with passive diffusion tubes deployed over two-week periods; blanks are prepared and analyzed alongside experimental tubes as a quality check.
- Users must apply the accompanying quality information when using the data.
- ECN data management emphasizes data availability, disclosure risks, proprietary issues, embargoes, and updating mechanisms.
- Data sharing and catalogue: datasets uploaded to relevant portals and data holdings catalogued; work performed on datasets may be documented.

## Data content and structure
- Core data model:
  - Information stored in Oracle database, with one data table set per site:
    - D1AN_xxx: dataset identifiers and sample metadata
    - D2AN_xxx: sample measurements and deployment details
  - Common fields across tables include SITECODE, SDATE (sampling date), TUBEID (sample tube identifier, E = Experimental, B = Blank), FIELDNAME, VALUE, and associated metadata tables (e.g., M_DESC, M_REFFIELD).
- Site metadata:
  - 12 ECN sites (T01–T12) with site names, precise locations, and date ranges for data in the dataset:
    - T01 Drayton, T02 Glensaugh, T03 Hillsborough, T04 Moor House - Upper Teesdale, T05 North Wyke, T06 Rothamsted, T07 Sourhope, T08 Wytham, T09 Alice Holt, T10 Porton Down, T11 Snowdon, T12 Cairngorms
  - Date ranges spanning roughly 1993 to 2012 (varies by site).
- Metadata and field definitions:
  - Field names include WEIGHTNO2 (weight of NO2 on the mesh), NO2 (NO2 concentration in micrograms/m3), NO2PPB (NO2 concentration in ppb), TDIFF (exposure time in minutes), and Q1–Q8 quality codes.
  - Units: WEIGHTNO2 (micrograms), NO2 (micrograms/m3), NO2PPB (ppb), TDIFF (minutes), Q1–Q8 (integers for quality codes).
- Quality codes:
  - ECN standard quality codes used to indicate data quality factors (codes 100–187, plus 501–508, 513, and 999 for unusual events with accompanying text).
  - Examples include: 100 (no information; data lost), 101 (no sample/reading taken), 201 (biting insects affected sampling), 500s (laboratory-related issues), 999 (unusual event; see accompanying quality text).
  - A “quality text” field may accompany unusual or non-standard situations (code 999).
- Core metadata structure:
  - References to core metadata tables and definitions are noted (e.g., M_DESC, M_REFFIELD), with a directive to consult the accompanying metadata documentation for full structure.

## Metadata, quality and standards
- Quality assessment responsibility lies with ECN site managers, who assign multiple quality codes as applicable.
- If an unusual event occurs not covered by codes, a text description is attached (code 999) and quality text provides details.
- Quality codes help users understand data completeness, sampling issues, or laboratory problems affecting results.
- Data products come with accompanying quality information to aid data stewards in interpretation and reuse.

## Data access, sharing and updates
- Data are stored in Oracle databases and uploaded to relevant data portals for discovery.
- Data availability and limitations are important considerations for publishing and sharing; updates and versioning are implied but specifics are not detailed.
- Researchers are encouraged to acknowledge data use and provide a reprint of publications citing the data.

## Site metadata and time range
- Each site (T01–T12) has:
  - Site name and precise geographic coordinates
  - Date range of available data (varying by site; earliest around 1993, latest around 2012)
- This information supports discovery, provenance tracking, and longitudinal analyses across the network.

## Practical guidance for use (Data Stewards perspective)
- Ensure proper acknowledgment and citation when datasets are used; track downstream publications.
- Leverage the two-tier data structure (D1AN_xxx and D2AN_xxx) along with core metadata tables for data integration and governance.
- Use quality codes (Q1–Q8 and associated quality text) to assess data suitability for specific analyses, and pay special regard to code 999 for unusual events.
- Refer to accompanying quality information to interpret dataset limitations and to understand any non-standard events or instruments issues.
- Be mindful of site-specific date ranges and coordinate systems when compiling multi-site analyses.
- Maintain governance by recording data processing steps, documenting transformations, and ensuring changes are reflected in catalogues and portals.