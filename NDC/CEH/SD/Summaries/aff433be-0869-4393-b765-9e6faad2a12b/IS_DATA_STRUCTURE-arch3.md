# ECN Data Centre dataset for spittlebug nymph density and adult colour morphs

## Overview
- Describes ECN data on nymph density for two spittlebug species (Neophilaenus lineatus and Philaenus spumaris) and adult colour morph proportions for Philaenus spumaris.
- Data are recorded annually from ECN sites and are intended to support environmental health monitoring, policy scrutiny, and decision-making.

## Data origin and ownership
- Dataset Originator: ECN Data Centre, Centre for Ecology and Hydrology.
- Dataset Owners: UK government departments and agencies funding site monitoring or network coordination (e.g., AFBI, BBSRC, Natural Resources Wales, Defra, Environment Agency, Forestry Commission, etc.).
- Usage acknowledgment: ECN asks users to acknowledge data use and to send one reprint of any publication citing the data.

## Protocols and comparability
- ECN uses standard operating procedures to ensure data comparability across sites.
- Accompanying protocol is available (is.pdf) detailing data collection methods.
- The protocol is designed to estimate an index using sweep nets for nymphs and to determine adult morph proportions, with annual data collection.

## Data files and structure
- ECN_ISN.csv: Nymph data
  - Columns include SITECODE (site), LCODE (location within site), SDATE (sampling date), ISN_SPEC (P = Philaenus spumaris; N = Neophilaenus lineatus), FIELDNAME (variable measured), VALUE (measurement).
- ECN_ISA.csv: Adult colour morph data
  - Columns include SITECODE, LCODE, SDATE, ISA_MORPH (adult morph code), FIELDNAME.
- Supporting quality documentation: ECN_ISN_qtext.csv and ECN_ISA_qtext.csv (explanation for quality text tied to quality codes).
- Quality codes: Site managers assign quality codes from a standardized list; codes are included in data downloads with textual explanations in the qtext files.
- Quality codes also include a special code 999 for unusual events with accompanying text.

## Site and variable metadata
- Site Codes: T01 to T12 with corresponding site names and precise latitude/longitude coordinates (e.g., T01 Drayton, T12 Cairngorms).
- Variable codes (FIELDNAME) for nymph data include 1–40 representing counts in multiple quadrats, plus additional metrics like NSPITCHK (random throw exercise), MEANNYM (mean nymphs in quadrats for random throw), NMAL (males by morph), NFEM (females by morph), NTOT (total adults by morph), and quality fields Q1–Q8.
- Adult colour morphs: Codes for morphs (e.g., ALB = Albomaculata, FLA = Flavicollis, GIB = Gibba, LAT = Lateralis, LCE = Leucocephala, LOP = Leucophthalma, MAR = Marginella, POP = Populi, PRA = Praeusta, QUA = Quadrimaculata, TRI = Trilineata, TYP = Typica, UUU = Undeciphered).
- Quality codes: Extensive list (e.g., 100 = No information available; 101 = No sample taken; 200–513 various data issues; 999 = Unusual event) with corresponding descriptions in the documentation.

## Explanatory information and metadata
- Explanatory information for site codes and variables links site identifiers to names and exact locations.
- Fieldnames provide definitions for each measured variable (e.g., counts per quadrat, morph counts, and derived metrics).

## Data use and governance considerations
- Data quality: Quality codes and accompanying text explain factors affecting data quality; users should consult ECN_ISN_qtext.csv and ECN_ISA_qtext.csv for context.
- Data governance: Site managers assign quality codes; data may require transformation or cleaning to be analysis-ready.
- Data sharing: Public sharing of underlying data is a consideration; ensure appropriate governance and openness standards are followed.
- Data updates: Metadata and quality information are important for verifying data suitability and currency.

## How this supports monitoring frameworks
- Provides standardized, comparable ecological time-series data across multiple national sites.
- Facilitates evaluation of environmental change indicators relevant to policy monitoring, including species abundance and morphological variation.
- Supports transparency through explicit data quality metadata and documented collection protocols.

## Access and attribution
- Data are available as downloadable CSV files with accompanying quality metadata.
- Users are encouraged to acknowledge ECN data use and to share a reprint of publications citing the data.