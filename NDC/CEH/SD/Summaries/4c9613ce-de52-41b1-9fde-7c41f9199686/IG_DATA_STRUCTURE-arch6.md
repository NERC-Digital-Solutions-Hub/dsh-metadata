# UK Environmental Change Network (http://www.ecn.ac.uk) Ground Predators (IG)

- Overview of the dataset
  - Ground predator abundance data collected using pitfall traps as part of the UK Environmental Change Network (ECN) Ground Predators (IG) protocol.
  - Data are collected fortnightly during May to October.
  - 12 site-specific data tables (D1IG_xxx) capture trap data; 12 tables (D2IG_xxx) capture trap-out dates; 12 tables (D3IG_xxx) capture habitat information.
  - Accompanying quality information must be consulted when using the data.

- Provenance and usage guidance
  - Originator: ECN Data Centre (Centre for Ecology and Hydrology).
  - Dataset owners: ECN programme, funded by a consortium of UK government departments and agencies.
  - Acknowledgement: Please acknowledge ECN data usage and send one reprint of any publication citing the data.

- Data structure and schema (high level)
  - Core data tables:
    - D1IG_xxx: Taxon abundance data per site (fields include SITECODE, LCODE, SDATE, TRAP, FIELDNAME, VALUE).
    - D2IG_xxx: Trap deployment and collection timing (FROMDATE, SDATE, etc.).
    - D3IG_xxx: Habitat information (HABDESC) per site.
  - Metadata references:
    - Core metadata tables described elsewhere; accompanying quality metadata is required for proper interpretation.
  - Site-specific organization: One table per site for each data type; site code xxx corresponds to a specific ECN site.

- Site coverage
  - T01 to T12 (12 sites) with names and date ranges:
    - T01 Drayton (1993-05 to 2009-10)
    - T02 Glensaugh (1994-05 to 2012-10)
    - T03 Hillsborough (1993-05 to 2012-10)
    - T04 Moor House - Upper Teesdale (1993-05 to 2012-10)
    - T05 North Wyke (1993-05 to 2010-11)
    - T06 Rothamsted (1992-07 to 2009-11)
    - T07 Sourhope (1994-05 to 2012-11)
    - T08 Wytham (1993-05 to 2012-10)
    - T09 Alice Holt (1994-05 to 2012-10)
    - T10 Porton Down (1994-05 to 2012-10)
    - T11 Y Wyddfa - Snowdon (1999-05 to 2012-11)
    - T12 Cairngorms (1999-06 to 2012-11)

- Data content and coding
  - Field naming and coding:
    - Field names (in D1IG_xxx) include SITECODE, LCODE, SDATE, TRAP, FIELDNAME, VALUE.
    - FIELDNAME holds either a species code or a quality code.
  - Taxonomic coding:
    - Species Codes provide Latin names and taxonomic rank (e.g., Cicindela, Cicindela campestris, Carabus species, Bembidion spp., Harpalus spp., etc.).
    - Genesus/species mappings and many hierarchical taxon entries across Carabidae and related groups.
    - Example structure shows genus-level entries and detailed species-level mappings for many taxa.
  - Quality coding:
    - Field Q1, Q2, Q3, Q4, Q5, Q6, Q7, Q8 each store a quality code (integer) describing data quality factors.
    - Quality codes come from a standard ECN list with common values (e.g., 100 No information available; 101 No sample/reading; 105 Snow in funnel; 201 Failing light; 501 Laboratory: No sample; 999 Unusual event with accompanying text).
    - An accompanying quality text describes unusual circumstances (code 999).

- Data usage and quality considerations
  - The ECN quality codes enable assessment of data suitability for analysis and help filter or annotate data with potential issues.
  - Fortnightly sampling windows and seasonal limitations (May–October) should be considered in analyses.
  - Users should consult the accompanying quality information for each dataset to interpret potential data limitations or anomalies.

- Access and integration for data support work
  - Data are stored in an Oracle database with site-specific tables; data integration involves joining D1IG_xxx, D2IG_xxx, and D3IG_xxx (by SITECODE, LCODE, and date fields) and applying quality codes.
  - Outputs can be transformed into dashboard-ready data products (e.g., site-by-time trends, habitat associations, taxon-specific abundance matrices) with self-serve capabilities.
  - When disseminating outputs, proper attribution to ECN and linkage to protocol and quality metadata is required.

- Practical notes for data product development
  - Build cross-site, time-series dashboards to compare ground predator abundance and habitat descriptions across sites.
  - Provide filters by site, date range, taxon (via FIELDNAME/species codes), and quality code (Q1–Q8).
  - Include a quality summary panel that highlights data with codes indicating potential issues (e.g., 100, 101, 999) and any accompanying free-text notes.
  - Ensure data products reference the ECN protocol for terrestrial ground predator monitoring and direct users to the data quality documentation.