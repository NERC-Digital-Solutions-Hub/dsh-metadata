# UK Environmental Change Network (http://www.ecn.ac.uk) Spittle Bugs (IS)

- Overview
  - A long-term ECN dataset focused on spittle bugs, specifically nymph density of Philaenus spumaris and Neophilaenus lineatus, and adult colour morph proportions of P. spumaris.
  - Data collected annually across multiple sites (12 ECN sites) with standardized measurement protocols.
  - Data are intended to support monitoring of environmental change and policy-relevant environmental health indicators, with quality information accompanying uses.

- Data provenance and governance
  - Dataset Originator: ECN Data Centre, Centre for Ecology and Hydrology (CEH) – data portal at http://data.ecn.ac.uk.
  - Dataset Owners: UK Environmental Change Network programme, sponsored by a consortium of UK government departments and agencies.
  - Sponsoring organisations include: AFBI, BBSRC, NRW, DSTL, DEFRA, Environment Agency, Forestry Commission, Welsh Government, Natural England, NERC, NIEA, SEPA, Scottish Government, SNH.
  - Acknowledgement and citation: Users are asked to acknowledge ECN data usage and to send one reprint of any publication citing ECN data.

- Protocol and data collection
  - Protocol aims: estimate an index of nymph density via sweep nets and estimate adult colour morph proportions for P. spumaris; data are recorded once per year.
  - Data should be used with accompanying quality information.
  - Protocol reference: ECN terrestrial measurements for spittle bugs (IS).

- Data structure and variables
  - Core data organization
    - Nymph data: stored in 12 tables named D1ISN_xxx (one per site). Key fields include SITECODE, LCODE, SDATE, ISN_SPEC (P or N), FIELDNAME, VALUE, plus quality fields Q1–Q8.
    - Adult data: stored in 12 tables named D1ISA_xxx (one per site). Key fields include SITECODE, LCODE, SDATE, ISA_MORPH (adult colour morph), plus VALUE and quality fields Q1–Q8.
  - Field definitions (highlights)
    - SITECODE: site identifier; required.
    - LCODE: location code; required.
    - SDATE: sampling date; required (dd-mmm-yyyy).
    - ISN_SPEC: nymph species code: P = Philaenus spumaris, N = Neophilaenus lineatus.
    - ISA_MORPH: adult colour morph code (see morphs list).
    - FIELDNAME: describes data field (e.g., quadrat counts).
    - VALUE: numeric measurements (counts, means, etc.), with appropriate numeric type.
    - Q1–Q8: quality codes corresponding to associated quality assessments.
  - Morphology codes (adult spittle bug morphs)
    - ALB, FLA, GIB, LAT, LCE, LOP, MAR, POP, PRA, QUA, TRI, TYP, UUU (Undeciphered).
  - Quality codes (ECN standard set)
    - Range includes codes 100–241, 501–..., plus 999 for unlisted/explicit notes.
    - Examples: 100 = No information available; 101 = No sample/reading taken; 203 = No flow observed; 999 = unusual event text description; and many others capturing sampling, preservation, and field conditions.
  - Data storage and portals
    - Core metadata and datasets are organized for site-based storage and are intended to be uploaded to appropriate ECN data portals.
  
- Sites and temporal coverage
  - 12 ECN sites with official site codes and names:
    - T01: Drayton (1993–2006 data range)
    - T02: Glensaugh (1994–2012)
    - T03: Hillsborough (1993–2011)
    - T04: Moor House - Upper Teesdale (1993–2012)
    - T05: North Wyke (1993–2012)
    - T06: Rothamsted (1993–2011)
    - T07: Sourhope (1994–2012)
    - T08: Wytham (1993–2012)
    - T09: Alice Holt (1994–2007)
    - T10: Porton Down (1994–2012)
    - T11: Y Wyddfa - Snowdon (1998–2012)
    - T12: Cairngorms (1999–2012)
  - Each site has its own coordinate location and date range in the dataset.

- Usage notes for analysts
  - The dataset is designed for standardised, reproducible monitoring analyses across sites and years.
  - Data quality is integral; users must consult the accompanying quality information and ECN quality codes when interpreting results.
  - Core dataset handling includes ensuring datasets are stored and accessible through appropriate ECN data portals.
  - When combining this dataset with others, analysts should consider data provenance, site comparability, and quality codes to maintain temporal and spatial consistency.

- Particular challenges and opportunities
  - Challenge: increasing the value of dataset by integrating with other relevant environmental data to avoid single-use outcomes.
  - Challenge: enabling access to underlying data used to produce final outputs, promoting transparency and reuse.