# Dataset Originator E CN Data Centre (http://data.ecn.ac.uk - ecn@ceh.ac.uk), Centre for Ecology and Hydrology

## Overview
- ECN dataset description from the UK Environmental Change Network, sponsored by multiple government departments and agencies.
- Data cover environmental monitoring across ECN sites; datasets require acknowledgement and may include publications or reprints.

## Governance and Providers
- Data Providers: ECN programme funded by a consortium of UK government departments and agencies (e.g., BBSRC, Defra, Environment Agency, Natural England, NERC, Scottish Government, Welsh Government, etc.).
- Acknowledgement: Users must acknowledge the use of ECN data and provide a reprint of any publication citing ECN data.
- Protocols: ECN maintains standard operating procedures to ensure data comparability across sites (refer to accompanying pc.pdf for collection methods).
- Data sharing and updates: Sharing limitations respected; systems in place to manage updates.

## Protocols and Quality Assurance
- Weekly sampling via bulk collectors; precipitation chemistry measured with standard QA processes.
- Routine quality control: laboratories analyze a quality control solution alongside field samples; QC data accompany the dataset.
- Users should apply accompanying quality information when using the data.

## Data Structure and Metadata
- Data Download fields:
  - SITECODE: Unique site code
  - SDATE: Sampling date
  - FIELDNAME: Variable measured
  - VALUE: Measured value
- Supporting Documentation:
  - ECN_PC2.csv: Lab analysis metadata (e.g., deployment dates, sampling times, lab identifiers, and analysis times)
  - ECN_PC_qtext.csv: Quality text describing quality issues (linked via quality codes; code '999' for unusual events)
  - ECN_QC1.csv and ECN_QC2.csv: Quality control data and additional lab analysis details
- Site Codes (Explanatory Information): T01–T12 with site names and precise coordinates (e.g., Drayton, Glensaugh, Hillsborough, Moor House, etc.). Full site list available via ECN catalogue link.
- Variable Data (FIELDNAME): Wide range of chemical and physical parameters, each with description and units, such as:
  - Alkalinity (ALKY), Calcium (CALCIUM), Chloride (CHLORIDE), Conductivity (CONDY), Dissolved organic carbon (DOC)
  - Major ions: NH4-N, NO3-N, K, Na, Ca, Mg, SO4-S, PO4-P, etc.
  - pH and related QA metrics (PH, PHAQCS, PHAQCU)
  - Sample volume (VOLUME) and related indicators
- Quality Codes (Q Codes): A standardized list (100–199, 501–507, 999, etc.) indicating data issues such as no information, sample loss, contamination, equipment failure, etc. A separate “quality text” (ECN_PC_qtext.csv) provides additional context for codes.

## Quality Assurance and Checks
- ECN_PC_chemistry-QC.csv: Post-hoc screening of ECN PC measurements, including comparisons of measured vs theoretical conductivity and ion balance checks.
- Conductivity checks:
  - COND_RATIO_OK: 1 if measured/theoretical conductivity ratio is within 0.8–1.2; 0 otherwise.
  - ION_DIFF_OK: 1 if anion-cation difference is within ±10 µeq L−1; 0 otherwise.
  - PO4_OK: 1 if PO4^3− is ≤ 5 µeq L−1 or measurement not provided; 0 if >5 or suspected contamination.
  - OVERALL_CHECK_OK: 1 if PO4_OK = 1 and (COND_RATIO_OK = 1 or ION_DIFF_OK = 1); 0 otherwise.
- Recommendation: Use only samples with OVERALL_CHECK_OK = 1 for temporal trend analyses and mean concentration/flux calculations.
- Low-concentration sensitivity: Ratios are especially sensitive at low solute concentrations; alternative checks use absolute anion/cation differences when conductivity data are missing.

## Access and Use
- Data are organized with site and sampling metadata to enable cross-site comparability.
- Users should consult the accompanying documentation and QC files to properly interpret data quality, and apply quality codes/text where relevant.

## Challenges for Data Stewards (Particular Challenges)
- Incomplete picture of user needs and priorities.
- Timely acquisition of data from diverse sources.
- Getting data creators to meet standards and provide metadata.
- Handling multiple systems and formats, including non-interoperable ones.
- Managing and transferring large datasets.
- Dealing with outdated databases requiring bespoke solutions.

## Practical Takeaways for Data Stewardship
- Maintain and publish clear governance, update protocols, and ensure data producers follow metadata standards.
- Preserve and link quality control data, site metadata, and QCff notes to datasets.
- Implement workflow to capture acknowledgements and track publications citing ECN data.
- Use standardized quality codes and QC explanations to support reliable downstream analyses.
- Provide guidance and tooling to data creators on formats, metadata, and QA requirements.