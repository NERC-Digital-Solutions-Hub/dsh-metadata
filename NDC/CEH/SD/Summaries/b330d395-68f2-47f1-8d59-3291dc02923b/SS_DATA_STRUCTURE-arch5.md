# Dataset Originator ECN Data Centre (http://data.ecn.ac.uk - ecn@ceh.ac.uk), Centre for Ecology and Hydrology

## Overview
- The UK Environmental Change Network (ECN) data centre provides environmental monitoring datasets intended to support understanding environmental change.
- Datasets are produced by ECN programme owners funded by a consortium of UK government departments and agencies.
- Users are asked to acknowledge data use and to send one reprint of any publication citing ECN data, aiding demonstration of data value and impact.

## Data Governance & Ownership
- ECN has standard operating procedures to ensure data comparability across sites (protocols referenced by accompanying ss.pdf).
- Dataset is accompanied by extensive metadata and supporting documentation to facilitate consistent use and interpretation.
- Acknowledgement and citation requirements are formalized to track data usage and output.

## Protocols, Standards, and Quality Assurance
- Standardized data collection and handling procedures are in place to maintain comparability among sites.
- A quality control process includes a standard QC solution analyzed alongside field samples.

## Data Model, Content, and Metadata
- Data Download fields include:
  - SITECODE: unique ECN site code
  - SDATE: sampling date
  - RID: replicate ID
  - FIELDNAME: variable measured
  - VALUE: measured value
- Supporting documents explain lab analyses (ECN_SS2.csv) and other metadata schemas (ECN_SS_qtext.csv, ECN_QC1.csv, ECN_QC2.csv).
- Explanatory information lists variables (FIELDNAME) such as ALKY, ALUMINIUM, CALCIUM, CHLORIDE, DOC, CONDY, pH, NO3N, PO4P, etc., with units and descriptions.
- Quality Codes (Q1–Q5) provide structured data quality indicators; a special code 999 indicates an unusual event with accompanying text in ECN_SS_qtext.csv.
- Site and location details are provided for ECN sites T01–T12 with exact coordinates and site names (e.g., Drayton, Glensaugh, Hillsborough, Moor House, etc.). Full site catalog information is available via the provided catalogue link.

## Usage Notes and Data Integrity
- Suction samplers collect soil solution chemistry data on a Fortnight basis; samples may require sampler replacement, indicated by a new RID.
- If a sampling day yields insufficient material, samples may be bulked and indicated with RID codes XXS (shallow) or XXD (deep).
- A quality control solution is used as a lab check; QC data accompany the dataset and should be consulted during analysis.
- Quality information is essential for proper data use; use accompanying quality metadata when analyzing.

## Data Availability, Access, and Updates
- Data are organized with multiple supporting files (ECN_SS2.csv, ECN_SS_qtext.csv, ECN_QC1.csv, ECN_QC2.csv) to support interpretation and reuse.
- Procedures exist for updates and documentation of data processing, with an emphasis on maintaining cross-site comparability and traceability of changes.

## Documentation, Site Information, and Linkages
- Explanatory Information defines variable names and units (e.g., ALKY, ALUMINIUM, CHLORIDE, DOC, NH4N, NO3N, PO4P, POTASSIUM, SODIUM, TOTALN, TOTALP, etc.).
- Quality Codes section provides detailed definitions for common data quality issues (e.g., data loss, sample issues, lab problems, unusual events).
- The ECN provides site-specific metadata and coordinates for T01–T12 and directs users to the ECN site catalog for additional context.

## Publication and Acknowledgement
- Users are requested to acknowledge ECN data usage in publications.
- A reprint of any publication citing ECN data should be sent to ECN to help quantify data impact and justify ongoing value.