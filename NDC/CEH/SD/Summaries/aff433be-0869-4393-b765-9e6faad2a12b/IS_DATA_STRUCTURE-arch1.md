# Dataset Originator ECN Data Centre (http://data.ecn.ac.uk - ecn@ceh.ac.uk), Centre for Ecology and Hydrology

## Overview
- The ECN Data Centre hosts a dataset from the UK Environmental Change Network (ECN) program, funded and coordinated by a consortium of UK government departments and agencies.
- Aims to understand environmental change by collecting standardized data across multiple sites.
- This dataset focuses on spittle bug populations, specifically nymph density and adult colour morphs, collected annually.

## Data and Files
- Data downloads include:
  - ECN_ISN.csv: nymph data
  - ECN_ISA.csv: adult data
- Supporting quality information:
  - ECN_ISN_qtext.csv (quality text for nymph data)
  - ECN_ISA_qtext.csv (quality text for adult data)
- Data fields in ECN_ISN.csv:
  - SITECODE, LCODE, SDATE, ISN_SPEC (P = Philaenus spumaris, N = Neophilaenus lineatus), FIELDNAME (variable measured), VALUE (measurement)
- Data fields in ECN_ISA.csv:
  - SITECODE, LCODE, SDATE, ISA_MORPH (adult colour morph), FIELDNAME, VALUE
- Quality codes are provided alongside quality text to indicate data reliability and context.

## Site and Variables
- Explanatory information for Site Codes:
  - T01 to T12 with specific site names (e.g., Drayton, Glensaugh, Hillsborough, etc.) and their geographic coordinates.
- Field names (FIELDNAME) details:
  - For nymphs: numbers of spittles in quadrats 1–40, plus metrics like NSPITCHK (random throw exercise) and MEANNYM (mean nymphs in random throw), NMAL (male counts per morph), NFEM (female counts per morph), NTOT (total adults per morph), and quality codes Q1–Q8.
  - For adults: similarly includes morph counts by morph code and related quality fields.
- Adult colour morphs (ISA_MORPH codes):
  - ALB, FLA, GIB, LAT, LCE, LOP, MAR, POP, PRA, QUA, TRI, TYP, UUU with corresponding descriptions (e.g., Albomaculata, Flavicollis, etc.).
- Quality codes (Q1–Q8 and 999 for unusual events) cover issues such as sample loss, equipment action, environmental disturbances, and data edits.

## Protocol and Usage
- ECN has standard operating procedures to ensure data comparability across sites (refer to accompanying is.pdf for collection methods).
- Usage notes:
  - The protocol is designed to estimate an index of nymph density via sweep nets (per quadrat) and to estimate adult colour morph proportions.
  - Data are recorded once per year.
  - Users should consult the accompanying quality information before analysis.

## Data Quality and Metadata
- Site managers assign quality codes from a standard list; exceptional cases documented as quality code 999 with accompanying text in ECN_ISN_qtext.csv and ECN_ISA_qtext.csv.
- The dataset includes extensive explanatory information for site identifiers and measured variables to support correct interpretation and reproducibility.

## Access, Acknowledgement, and Citations
- The dataset owners request acknowledgement of data use in publications and ask for one reprint of any publication citing the data.
- Data provenance and metadata are designed to be discoverable and usable, with links to broader ECN site information and data catalogues.

## Supporting Documentation and Access Notes
- Supporting documentation provides definitions for quality codes and context for quality text entries.
- Explanatory site information links are provided to view full site details and coordinates.

## Contacts and Ownership
- Dataset Originator: ECN Data Centre, Centre for Ecology and Hydrology
- Dataset Owners: UK ECN sponsors including DEFRA, Natural England, Natural Resources Wales, Scottish Environment Protection Agency, and others as listed in the document.