# UK Environmental Change Network (http://www.ecn.ac.uk) Spittle Bugs (IS)

## Overview
- Dataset from the UK Environmental Change Network (ECN) focusing on spittle bugs.
- Measures: annual nymph density for two species (Neophilaenus lineatus and Philaenus spumaris) and adult colour morph proportions for P. spumaris.
- Data Centre: ECN Data Centre; dataset owners include a consortium of UK government departments/agencies.
- Usage policy: acknowledge data use and provide one reprint of any publication citing the data; follow the accompanying quality information and the protocol reference.

## Data Scope and Protocol
- Purpose: estimates an index of nymph density and adult colour morph proportions; data are collected once per year.
- Protocol reference: linked measurement protocol for terrestrial ecologies.
- Quality: analysis should be guided by accompanying quality information; outputs may be updated as data quality is assessed.

## Data Structure and Storage
- Core storage: data stored in Oracle database with site-specific tables.
- Nymph data: 12 tables named D1ISN_xxx (one per site; xxx = site code). Key fields include SITECODE, LCODE, SDATE, ISN_SPEC, FIELDNAME, VALUE, plus quality-related fields.
- Adult data: 12 tables named D1ISA_xxx (one per site). Key fields include SITECODE, LCODE, SDATE, ISA_MORPH, FIELDNAME, VALUE, plus quality-related fields.
- Metadata: core metadata tables exist; refer to accompanying metadata documentation for full structure.

## Site Coverage
- Site codes T01–T12 with corresponding site names and date ranges:
  - T01 Drayton
  - T02 Glensaugh
  - T03 Hillsborough
  - T04 Moor House - Upper Teesdale
  - T05 North Wyke
  - T06 Rothamsted
  - T07 Sourhope
  - T08 Wytham
  - T09 Alice Holt
  - T10 Porton Down
  - T11 Y Wyddfa - Snowdon
  - T12 Cairngorms
- Each site includes location/coordinates and a dataset date range (varies by site, generally 1993–2012).

## Data Fields and Coding
- FieldNames:
  - Nymph data: 1–40 quadrats (counts per quadrat) plus additional fields for sets of quadrats, random throw metrics (NSPITCHK, MEANNYM), sex/morph counts (NMAL, NFEM), and quality fields (Q1–Q8).
  - Adult data: Fieldname mappings for quadrats and morph data, with ISA_MORPH for adult colour morph codes.
- Quadrats: detailed counts for up to 40 quadrats per sampling event.
- Adult colour morphs: codes (ALB, FLA, GIB, LAT, LCE, LOP, MAR, POP, PRA, QUA, TRI, TYP, UUU) with corresponding descriptions.
- Quality fields: Q1–Q8 accompany field values to capture data quality indicators.

## Quality Codes
- Standard ECN quality codes cover data loss, missing samples, partial loss, contamination, environmental/operational factors, and other data quality issues.
- Key examples: 100–No information available; 101–No sample taken; 102–Sample lost; plus many codes related to debris, sampling disturbances, equipment problems, and non-standard sampling.
- 999 indicates an unusual event requiring accompanying text in quality notes.
- Quality codes are assigned by ECN site managers; multiple codes may apply; detailed quality text is available in dataset quality information.

## Data Use and Outputs
- Outputs can include time-series of nymph density by species and adult morph proportions, across sites and years.
- Users should apply the quality codes and accompanying quality notes to assess data reliability.
- Data can be used to support environmental change research and related ecological analyses; outputs should be appropriately documented and cited.

## Access and Compliance
- Data access in an Oracle database format (site-specific tables).
- Researchers should acknowledge ECN data use and share a reprint of publications citing the data.
- Protocols and quality documentation should be consulted to ensure proper data interpretation and handling of non-standard or low-quality data.

## Practical Considerations for Data Support
- Integration: combine Nymph (D1ISN_xxx) and Adult (D1ISA_xxx) data across sites/years using SITECODE, LCODE, SDATE, and FIELDNAME/VALUE mappings.
- Data quality: filter or weight analyses by quality codes; account for non-standard sampling dates (quality flag 237/223-related indicators and others as described in quality documentation).
- Gaps and patchiness: expect variable data availability by site and year; plan analyses with attention to date ranges and site coverage.
- Documentation: ensure usage references protocol URL and metadata documentation for full field definitions and schema details.