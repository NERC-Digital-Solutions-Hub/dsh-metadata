# UK Environmental Change Network (http://www.ecn.ac.uk) Spittle Bugs (IS)

## Overview
- Dataset from the UK Environmental Change Network (ECN) focusing on spittle bugs.
- Captures nymph density (two species) and adult colour morph proportions (Philaenus spumaris) using sweep nets.
- Data collected annually across multiple ECN sites; intended for environmental change research and related analyses.
- Data usage should be acknowledged to ECN; request for one reprint of any publication citing ECN data.

## Data origin and ownership
- Originator: ECN Data Centre, Centre for Ecology and Hydrology.
- Owners: ECN programme funded by a consortium of UK government departments and agencies (including DEFRA, Natural England, Environment Agency, NERC, Scottish Government, Welsh Government, etc.).
- Protocol reference and quality metadata accompany the dataset.
- Data collection protocol designed to estimate nymph density index and adult colour morph proportions; annual records.

## Protocol and sampling design
- Focus: nymph density for two species (Neophilaenus lineatus, Philaenus spumaris) and colour morph proportions of adult P. spumaris.
- Sampling: data recorded once per year per site.
- Includes accompanying quality information to accompany data usage.

## Data structure and storage
- Core data are stored in an Oracle database, with separate tables for nymphs and adults across sites:
  - Nymph data: 12 tables named D1ISN_xxx (xxx = site code).
  - Adult data: 12 tables named D1ISA_xxx (xxx = site code).
- Common field structure (for both nymphs and adults):
  - SITECODE: site code.
  - LCODE: location code.
  - SDATE: sampling date (dd-mmm-yyyy).
  - VALUE: numeric measurement (varies by field).
  - FIELDNAME and FIELDNAME reference table: field definitions.
  - For nymphs: ISN_SPEC codes for species (P = Philaenus spumaris, N = Neophilaenus lineatus); additional fields for quadrats and quality codes (Q1–Q8 variants).
  - For adults: ISA_MORPH for adult colour morph (e.g., ALB, FLA, GIB, LAT, LCE, LOP, MAR, POP, PRA, QUA, TRI, TYP, UUU); FIELDNAME and VALUE definitions similar to nymphs.
- Metadata: core metadata tables exist (see metadata documentation); FIELDNAME and VALUE use predefined reference tables (M_DESC, M_REFFIELD, etc.).
- Quality fields: Q1–Q8 accompany each measurement, with quality codes defined separately.

## Site codes and date ranges
- 12 ECN sites (site code – site name – date range):
  - T01 – Drayton: 1993-2006
  - T02 – Glensaugh: 1994-2012
  - T03 – Hillsborough: 1993-2011
  - T04 – Moor House - Upper Teesdale: 1993-2012
  - T05 – North Wyke: 1993-2012
  - T06 – Rothamsted: 1993-2011
  - T07 – Sourhope: 1994-2012
  - T08 – Wytham: 1993-2012
  - T09 – Alice Holt: 1994-2007
  - T10 – Porton Down: 1994-2012
  - T11 – Snowdon (Y Wyddfa): 1998-2012
  - T12 – Cairngorms: 1999-2012
- Geographic coordinates are provided for each site in the dataset documentation.

## Data fields and structure (highlights)
- Nymph data fields:
  - Field counts per quadrat (1–40, with corresponding 1–2 indexing for certain fields), multiple quality indicators (Q1–Q8) per field.
  - NSPITCHK and MEANNYM fields for random throw exercises and mean nymphs, respectively.
  - NMAL/NFEM fields for male/female counts by morph where applicable.
- Adult data fields:
  - ISA_MORPH for adult colour morph (e.g., ALB, FLA, GIB, LAT, LCE, LOP, MAR, POP, PRA, QUA, TRI, TYP, UUU).
  - FIELDNAME and VALUE structure analogous to nymph data, supporting morph counts and quality indicators.
- Quality codes:
  - Standard ECN quality codes (100–191, 200–235, 237–241, 501–513) plus 999 for unusual circumstances text.
  - Examples: 100 = No information; 101 = No sample/reading; 200s cover various sampling/observational issues; 237–241 indicate approximations or confidence levels; 501–513 cover laboratory/sample-related notes.
- Data provenance and reuse:
  - Data are part of ECN’s long-term monitoring program, with expectations of data citation and sharing of derived datasets via metadata-enabled portals.

## Usage guidance and data quality
- Use accompanying quality information when analyzing data to account for potential data loss, sampling issues, or observational problems.
- The protocol emphasizes the importance of the annual index estimation and morph proportions, supported by quality codes to flag data reliability.
- Datasets are designed to be discoverable via ECN metadata portals; maintain traceability to data sources and site metadata.

## Acknowledgement and publication
- ECN requests acknowledgement of data use.
- Authors should send one reprint of any publication citing ECN data.