# ECN Spittle Bug Data: Nymph Density and Adult Colour Morphs (ECN_ISN.csv and ECN_ISA.csv)

## Overview
- Describes ECN dataset for spittle bugs, focusing on nymph density (Neophilaenus lineatus and Philaenus spumaris) and adult colour morph proportions of P. spumaris.
- Data are collected annually using a standard protocol to allow cross-site comparability.
- Data are available in two main download files: ECN_ISN.csv (nymph data) and ECN_ISA.csv (adult morph data).
- Supporting quality metadata are provided in ECN_ISN_qtext.csv and ECN_ISA_qtext.csv, with a special quality code 999 for unusual events.
- Site and location metadata are provided, including site codes, location coordinates, and a mapping of variable names to measured components.

## Dataset Origin and Ownership
- Originator: ECN Data Centre (Centre for Ecology and Hydrology) – dataset hosting and management.
- Owners: The UK Environmental Change Network (ECN) programme, funded by a consortium of UK government departments and agencies.
- Acknowledgement: Users are asked to acknowledge ECN data in publications and to send one reprint of any publication citing ECN data.

## Protocol and Quality Assurance
- ECN maintains standard operating procedures to ensure data comparability across sites.
- Data are collected annually with a defined protocol for the measurement of nymph density and adult morph data.
- Quality information accompanies the data to document factors affecting data quality; unusual events are described in the quality text files (code 999).

## Data Download and File Structure
- Nymph data file: ECN_ISN.csv
  - Columns: SITECODE (site code), LCODE (location within site), SDATE (sampling date), ISN_SPEC (nymph species code: P = Philaenus spumaris, N = Neophilaenus lineatus), FIELDNAME (variable measured), VALUE (measured value), plus quality fields Q1–Q8.
- Adult data file: ECN_ISA.csv
  - Columns: SITECODE, LCODE, SDATE, ISA_MORPH (adult colour morph code), FIELDNAME, VALUE, plus quality fields Q1–Q8.
- Quality text files: ECN_ISN_qtext.csv and ECN_ISA_qtext.csv
  - Provide narrative explanations for quality codes and any ongoing quality issues.
- Quality codes: A standard list of codes (e.g., 100–, 999 for unusual events) with descriptive explanations.
- Site codes: T01–T12 with site names and precise coordinates (latitude/longitude).

## Site Codes and Variables
- Site codes (T01–T12) correspond to named ECN sites (e.g., Drayton, Glensaugh, Hillsborough, etc.) with precise geographic coordinates provided.
- Fieldname definitions for nymph data cover counts across up to 40 spittle quadrats (1–40) and related metrics (e.g., NSPITCHK, MEANNYM, NMAL, NFEM, NTOT) and quality indicators (Q1–Q8).
- Adult colour morphs are recorded using morph codes (ALB, FLA, GIB, LAT, LCE, LOP, MAR, POP, PRA, QUA, TRI, TYP, UUU) with corresponding descriptive names.

## Usage Notes for Analysts
- The protocol targets an index of nymph density via sweep nets and reports the proportion of adult colour morphs for Philaenus spumaris.
- Data are recorded per site, location, and sampling date, enabling temporal trend analysis and spatial comparisons.
- Always consult accompanying quality information to interpret data reliability, including instances of quality code 999 for unusual events.
- The data structure supports integration with other ECN datasets and external environmental datasets to broaden analysis beyond single-use datasets.

## Data Access and Documentation
- Primary data downloads: ECN_ISN.csv and ECN_ISA.csv
- Supporting quality documentation: ECN_ISN_qtext.csv and ECN_ISA_qtext.csv
- Additional site information and variable definitions are accessible via ECN site catalogues and explanatory tables.
- For further information on ECN sites, refer to the ECN site catalog and Explanatory Information within the dataset description.

## Attribution and Contact
- Acknowledge ECN data use in publications; provide one reprint to ECN.
- For further information or access, contact ECN Data Centre (ecn@ceh.ac.uk) and visit the ECN data portal and ECN catalogue resources.