# UK Environmental Change Network (http://www.ecn.ac.uk) Spittle Bugs (IS)

## Aim and scope
- Purpose: monitor environmental health indicators by estimating an index of nymph density for two spittle bug species (Neophilaenus lineatus and Philaenus spumaris) and, for P. spumaris adults, the proportion of colour morphs.
- Data are recorded annually to inform understanding of environmental change impacts and support policy-relevant monitoring decisions.

## Data provenance and governance
- Dataset Originator: ECN Data Centre; Dataset Owners: The UK Environmental Change Network programme funded by a consortium of UK government departments/agencies.
- Sponsor organizations include: Agri-Food and Biosciences Institute, BBSRC, Natural Resources Wales, Defence Science & Technology Laboratory, Defra, Environment Agency, Forestry Commission, Welsh Government, Natural England, NERC, SEPA, Scottish Government, and others.
- Usage and acknowledgment: ECN requests acknowledgement of data use and a reprint of any publication citing the data.
- Protocol reference: ECN measurements for terrestrial spittle bugs (protocol link provided).
- Data handling: accompanying quality information should be used; data governance and open data sharing considerations apply; metadata and data-sharing processes are highlighted.

## Data structure and content

### Core data design
- Site-specific data are stored in site-based tables:
  - Nymph data: D1ISN_xxx (one table per site)
  - Adult data: D1ISA_xxx (one table per site)
- Common field schema across core data:
  - SITECODE, LCODE: site and location codes
  - SDATE: sampling date (dd-mmm-yyyy)
  - ISN_SPEC: species code (P = Philaenus spumaris, N = Neophilaenus lineatus)
  - FIELDNAME: metadata field name
  - VALUE: corresponding value (numeric or coded per metadata type)
  - Quality fields: Q1–Q8 paired with codes indicating data quality
- Adult data additionally includes: ISA_MORPH (adult colour morph)

### Field names and morphology
- Colour morphs (adult): ALB, FLA, GIB, LAT, LCE, LOP, MAR, POP, PRA, QUA, TRI, TYP, UUU
- Morph naming denotes distinct adult colour forms; “NN” fields capture counts for morph-related analyses.

### Data coverage by site
- 12 ECN sites (T01–T12) with explicit site names and date ranges:
  - T01: Drayton (52°11'37.95"N, 1°45'51.95"W) — 1993–2006
  - T02: Glensaugh (56°54'33.36"N, 2°33'12.14"W) — 1994–2012
  - T03: Hillsborough (54°27'12.24"N, 6°4'41.26"W) — 1993–2011
  - T04: Moor House – Upper Teesdale (54°41'42.15"N, 2°23'16.26"W) — 1993–2012
  - T05: North Wyke (50°46'54.96"N, 3°55'4.10"W) — 1993–2012
  - T06: Rothamsted (51°48'12.33"N, 0°22'21.66"W) — 1993–2011
  - T07: Sourhope (55°29'23.47"N, 2°12'43.32"W) — 1994–2012
  - T08: Wytham (51°46'52.86"N, 1°20'9.81"W) — 1993–2012
  - T09: Alice Holt (51°9'16.46"N, 0°51'47.58"W) — 1994–2007
  - T10: Porton Down (51°7'37.83"N, 1°38'23.46"W) — 1994–2012
  - T11: Y Wyddfa – Snowdon (53°4'28.38"N, 4°2'0.64"W) — 1998–2012
  - T12: Cairngorms (57°6'58.84"N, 3°49'46.98"W) — 1999–2012

### Metadata and data quality
- Quality codes: Standard ECN codes covering data loss, sampling issues, processing problems, and similar quality concerns (e.g., 100–513, 999 for unusual events). Full code list is provided within the dataset’s quality metadata.
- Quality codes are attached to data records (Q1–Q8) and, when applicable, a free-text quality note is included (code 999).

## Measurement specifics and data usage
- Nymph data: annually collected via sweep nets; records include counts per quadrat across 40 quadrats and related sampling metrics (e.g., NSPITCHK, MEANNYM, NMAL/NFEM for morphs and random throws).
- Adult colour morph data: morphology counts captured alongside sampling, with morph codes listed above.
- Data are stored in Oracle databases; site and field metadata accompany values to support interpretation and verification.
- Users are advised to consult accompanying quality information to assess data suitability for monitoring analyses.

## Practical considerations for monitoring framework authors
- This dataset exemplifies a clear monitoring workflow: standardized annual sampling, site-level metadata, structured data tables, and explicit quality codes for transparency.
- It demonstrates governance requirements for data sharing, acknowledgement, and publication, illustrating how monitoring outputs can be made policy-relevant while maintaining data provenance.
- The combination of nymphal indices and adult morph analyses provides a multifaceted view of population status, enabling trend analysis and environmental-change inference across multiple sites.
- The presence of extensive site metadata, protocol references, and data-availability notes aligns with best practices in documenting monitoring frameworks for reproducibility and governance.