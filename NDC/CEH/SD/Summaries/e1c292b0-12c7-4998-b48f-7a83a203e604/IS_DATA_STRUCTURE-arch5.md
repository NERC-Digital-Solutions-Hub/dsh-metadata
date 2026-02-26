# UK Environmental Change Network (http://www.ecn.ac.uk) Spittle Bugs (IS)

## Overview
- Originator: ECN Data Centre (http://data.ecn.ac.uk), Centre for Ecology and Hydrology; contact ecn@ceh.ac.uk
- Owners: UK Environmental Change Network programme; funded by a consortium of UK government departments/agencies across site monitoring and network coordination
- Use acknowledgement: ECN asks to acknowledge data use and to send one reprint of any publication citing the data

## Protocol and Data Collection
- Purpose: Estimate nymph density for two spittle bug species (Neophilaenus lineatus and Philaenus spumaris) and the colour morph proportions of adult P. spumaris
- Frequency: Data recorded once per year
- Metadata emphasis: Use accompanying quality information when using the data

## Data Structure and Storage
- Core storage: Oracle database
  - Nymph data: 12 tables D1ISN_xxx (one per site)
  - Adult data: 12 tables D1ISA_xxx (one per site)
- Site codes: T01–T12 (Drayton, Glensaugh, Hillsborough, Moor House Upper Teesdale, North Wyke, Rothamsted, Sourhope, Wytham, Alice Holt, Porton Down, Snowdon, Cairngorms)
- Key table fields (highlights):
  - Nymphs: SITECODE, LCODE, SDATE (sampling date), ISN_SPEC (species code), FIELDNAME, VALUE, plus quality codes Q1–Q8
  - Adults: SITECODE, LCODE, SDATE, ISA_MORPH (adult colour morph), FIELDNAME, VALUE, plus quality codes Q1–Q8
- Core metadata structure: Referenced in separate metadata documentation

## Site Information
- 12 sites with site names, precise coordinates, and dataset date ranges:
  - T01 Drayton (1993–2006)
  - T02 Glensaugh (1994–2012)
  - T03 Hillsborough (1993–2011)
  - T04 Moor House - Upper Teesdale (1993–2012)
  - T05 North Wyke (1993–2012)
  - T06 Rothamsted (1993–2011)
  - T07 Sourhope (1994–2012)
  - T08 Wytham (1993–2012)
  - T09 Alice Holt (1994–2007)
  - T10 Porton Down (1994–2012)
  - T11 Y Wyddfa - Snowdon (1998–2012)
  - T12 Cairngorms (1999–2012)

## Data Content and Fields
- Nymph data fields: 40 quadrats (1–40) for counts; additional fields include NSPITCHK, MEANNYM, NMAL, NFEM; quality fields Q1–Q8
- Adult data fields: ISA_MORPH (colour morph), quadrat and sample fields, plus quality fields Q1–Q8
- Colour morphs (adult codes): ALB, FLA, GIB, LAT, LCE, LOP, MAR, POP, PRA, QUA, TRI, TYP, UUU
- Nymph species codes: P = Philaenus spumaris, N = Neophilaenus lineatus
- Field metadata: FIELDNAME definitions and value types are stored with supporting M_DESC and M_REFFIELD references

## Quality, Provenance, and Documentation
- Quality codes: ECN standard codes used to indicate data quality factors (e.g., 100 No information available, 101 No sample/reading, 201 Biting insects, 202 Failing light, etc.)
- Unusual events: Code 999 used when an event falls outside standard codes; accompanying text explains circumstances
- Site managers assign quality codes; quality text accompanying dataset provides additional context
- Publication and usage notes: Acknowledgement and data provenance are important; accompanying quality metadata should be consulted for data quality context

## Governance and Stewardship Considerations
- Data governance alignment: Large, multi-site dataset requiring consistent metadata standards across sites and time
- Data availability and updates: Mechanisms exist to document sharing limitations, embargo considerations, and updates; process for updating datasets is in place
- Data discovery: Datasets are catalogued and shared via ECN portals; metadata and structure support discoverability and reuse
- Documentation and reproducibility: Core metadata documentation and protocol references are provided to support correct interpretation and reuse

## Particular Challenges for Data Stewards
- Incomplete or evolving understanding of user needs across a multi-site network
- Timely receipt of data from diverse sites and creators
- Ensuring metadata and standardization across various systems and formats
- Managing large, longitudinal datasets and potentially bespoke interoperability solutions
- Handling older databases and adapting data for current standards and portals

## Contact and Access
- ECN Data Centre contact: ecn@ceh.ac.uk
- Data access and usage guidance are provided through ECN portals and accompanying metadata documentation
- Acknowledgement and reprint requests are part of dataset use requirements