# Dataset Originator ECN Data Centre (http://data.ecn.ac.uk - ecn@ceh.ac.uk), Centre for Ecology and Hydrology

- The ECN (UK Environmental Change Network) dataset is managed by the ECN Data Centre and is funded by a consortium of UK government departments and agencies.
- Users are asked to acknowledge use of ECN data and to send one reprint of any publication that cites the data.

## Overview for Data Stewards

- Purpose: Provide standardized, comparable environmental data across multiple ECN sites, focused on spittle bugs (nymphs and adult colour morphs) collected annually.
- Protocols: Standard operating procedures ensure data comparability across sites; accompanying documentation explains data collection procedures.
- Access: Data are available as downloadable CSV files; supporting quality information is included with the dataset.

## Data Files and Structure

- ECN_ISN.csv (nymph data)
  - Core fields: SITECODE, Description; LCODE, Description; SDATE, Description; ISN_SPEC (P = Philaenus spumaris, N = Neophilaenus lineatus); FIELDNAME, Description; VALUE, Description.
- ECN_ISA.csv (adult colour morph data)
  - Core fields: SITECODE, Description; LCODE, Description; SDATE, Description; ISA_MORPH (adult colour morph code); FIELDNAME, Description.
- Supporting quality documentation
  - ECN_ISN_qtext.csv and ECN_ISA_qtext.csv provide textual explanations for quality codes when needed.

## Quality and Metadata

- Quality codes: Site managers assign standard quality codes to indicate factors affecting data quality; codes are included with the data (Q1–Q8, plus additional Q codes).
- Unusual events: A quality code of 999 denotes an unusual event; accompanying text is available in the qtext files.
- Guidance: Use the accompanying quality information when using the data to assess reliability and context.

## Site and Variable Reference

- Explanatory Site Codes: T01–T12 with corresponding site names and exact location coordinates (e.g., T01 Drayton; T12 Cairngorms).
- Explanatory Variables (FIELDNAME)
  - For nymphs: fields correspond to counts per quadrat (e.g., spittle counts across quadrats 1–40, with additional metrics for random throw exercises and morph counts).
  - For adults: FIELDNAME corresponds to variables measured for adult morph assessments (e.g., counts by morph).
- Adult Colour Morphs: Code mappings include ALB, FLA, GIB, LAT, LCE, LOP, MAR, POP, PRA, QUA, TRI, TYP, UUU.

## Data Governance, Usage, and Updates

- Governance: ECN has standard operating procedures to maintain data comparability and quality across sites; dataset updates follow predefined procedures.
- Usage expectations: Researchers should acknowledge ECN data use and share a reprint of publications citing the data.
- Updates and maintenance: Quality codes and text provide ongoing context for data quality across time and site changes.

## Documentation and Support

- Supporting documentation files (ECN_ISN_qtext.csv, ECN_ISA_qtext.csv) provide context for quality codes and any unusual events documented by site managers.
- Additional information about ECN sites is available through the ECN catalogue link provided in the documentation.

## Contact and Dataset Ownership

- Dataset Originator: ECN Data Centre, Centre for Ecology and Hydrology.
- Dataset Owners: The ECN programme funded by a consortium of UK government departments and agencies (including Defra, Natural England, Environment Agency, and others listed in the document).
- Acknowledgement: Users should acknowledge the use of ECN data and provide a reprint of relevant publications.