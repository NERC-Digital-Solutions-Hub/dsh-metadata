# UK Environmental Change Network (http://www.ecn.ac.uk) Spittle Bugs (IS) Dataset

- Purpose and what is measured
  - Annual measurement of nymph density for two spittle bug species: Philaenus spumaris and Neophilaenus lineatus.
  - Proportions of colour morphs of adult Philaenus spumaris.
  - Data collected using sweep nets to estimate an index of nymph density; adults’ colour morphs recorded for P. spumaris.

- Data provenance and governance
  - Dataset Originator: ECN Data Centre, Centre for Ecology and Hydrology.
  - Dataset Owners: UK Environmental Change Network (ECN) programme; funded by a consortium of UK government departments and agencies.
  - Acknowledgement and data citation: ECN requests acknowledgement in publications and one reprint of any publication citing the dataset.
  - Protocol reference: Provided at http://www.ecn.ac.uk/measurements/terrestrial/i/is

- Data collection and frequency
  - Data are recorded once per year.
  - Protocol aims to estimate an index of nymph density and adult colour morph proportions.

- Data structure and storage
  - Core data stored in Oracle database.
  - Nymph data: 12 tables (D1ISN_xxx) — one per site.
    - Core fields include SITECODE, LCODE, SDATE, ISN_SPEC (P = Philaenus spumaris; N = Neophilaenus lineatus), FIELDNAME, VALUE, plus quality fields.
  - Adult data: 12 tables (D1ISA_xxx) — one per site.
    - Core fields include SITECODE, LCODE, SDATE, ISA_MORPH (adult colour morph), FIELDNAME, VALUE, plus quality fields.
  - Field naming and metadata: Structure references M_DESC and M_REFFIELD for descriptions and references; metadata documentation exists for core metadata tables.
  - Quality and auxiliary fields: Q1–Q8 (each with quality code and value). Additional fields NSPITCHK, MEANNYM, NMAL, NFEM capture processing and morph-related metrics.

- Site coverage and temporal span
  - 12 sites across the UK with site codes T01–T12.
  - Site details (name and approximate location) and date ranges:
    - T01 Drayton – 1993–2006
    - T02 Glensaugh – 1994–2012
    - T03 Hillsborough – 1993–2011
    - T04 Moor House - Upper Teesdale – 1993–2012
    - T05 North Wyke – 1993–2012
    - T06 Rothamsted – 1993–2011
    - T07 Sourhope – 1994–2012
    - T08 Wytham – 1993–2012
    - T09 Alice Holt – 1994–2007
    - T10 Porton Down – 1994–2012
    - T11 Y Wyddfa - Snowdon – 1998–2012
    - T12 Cairngorms – 1999–2012
  - Each site includes a precise location coordinate pair (latitude and longitude) and the dataset’s temporal range per site.

- Field definitions and data content
  - Nymph quadrats: fields describe counts of spittle nymphs in quadrats 1–40 (and extended quadrat descriptions up to 39–40 in the data schema).
  - Additional fields:
    - NSPITCHK: spittle count for random throw exercise (two values)
    - MEANNYM: mean nymph count for random throw exercise (two values)
    - NMAL/NFEM: counts of male/female morphs (two values each)
  - Adult colour morphs (ISA_MORPH codes): ALB, FLA, GIB, LAT, LCE, LOP, MAR, POP, PRA, QUA, TRI, TYP, UUU.
  - Quality codes: ECN standard codes (e.g., 100, 101, 102, …, 999) indicating data quality factors; 999 indicates unusual events requiring a quality text explanation.

- Data usage guidance for GIS work
  - Use site location (coordinates) and sampling dates to map spatial-temporal patterns of nymph density indices and morph distributions.
  - Leverage quadrat-level data to create fine-grained spatial visuals within each site (where available).
  - Incorporate the accompanying quality information to assess data reliability and filter/weight analyses accordingly.
  - Cross-walk fieldnames (FIELDNAME and VALUE) to interpret measured variables, including morph counts and quality metrics.

- Access, references, and metadata
  - Protocol and data access references are provided via ECN websites:
    - Protocol: http://www.ecn.ac.uk/measurements/terrestrial/i/is
    - ECN Data Centre: http://data.ecn.ac.uk
  - Metadata documentation exists for core metadata tables to support data integration and interoperability.