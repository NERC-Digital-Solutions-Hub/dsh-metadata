# ANALYTICAL GUIDELINES FOR WATER SAMPLES Version 1.1 (previously AG Protocol, updated Jan 2001)

- Purpose: Provide standardized guidelines for analyzing water samples from ECN terrestrial sites, with clear responsibilities, documented methodologies, and ongoing validation and review.
- Scope: Laboratories must conduct analyses under controlled conditions, document methodology and changes, and participate in validation procedures; annual review by an Analytical Working Group.

## Key aims for data handling and reporting (Data Support perspective)
- Ensure traceable, well-documented analytical methods and changes for ECN data records.
- Maintain metadata for each determinand-site-date record, including method, precision, and detection limits.
- Facilitate data quality through validated methods, consistent reporting, and interlaboratory comparisons.
- Provide end users with reliable data and clear information on how results were obtained and any limitations.

## Roles and responsibilities
- Laboratories: Manage analytical resources, apply controlled methods, and document significant methodological changes.
- Data management: Provide summary methodology information to ECN database; link data to site, core measurement, determinand, and date.
- Governance: Annual review of procedures by the Analytical Working Group.

## Approved and reference techniques
- Determinands and typical methods (examples):
  - pH and Conductivity
  - Major ions: Na+, K+, Ca2+, Mg2+, NH4+-N, Cl−, NO3−, SO4^2−, PO4^3−
  - Alkalinity and DOC
  - Total N
- Notes:
  - Some techniques quantify related fractions (e.g., not always the exact species); comparative tests may be used.
  - For pH and conductivity, refer to the Initial Water Handling Protocol.
  - Reference techniques provide primary standards for comparison; laboratories may adopt newer methods but should monitor for bias.

## Data reporting and methodology records
- Each laboratory should keep detailed methods for operators; provide summary information for the ECN database.
- Data records: one per determinand per ECN site, including methodology, sample type, typical concentrations, calibration ranges, measurement details, and QC measures.
- Example data record structure includes: substance, sample type, method, calibration range, detection limit, and reporting format.

## Validation and quality control
- Accuracy: Assessed by agreement with broader analytical community and participation in control sample schemes (e.g., AQUACHECK); results and any corrections must be recorded.
- Precision: Controlled via quality control samples; laboratories must report QC data with sample results and avoid submitting data if QC fails.
- Reporting: Accuracy and precision records should be submitted to the ECN Database Manager in machine-readable form.

## Quality Control Procedures for the ECN
- Separate QC system for ECN participants:
  - Encourages independent QC validation and interlaboratory comparisons.
  - Enables computation of between-site correction factors and detection of rogue batches or long-term trends.
- QC solids and data handling:
  - Two concentrated QC solutions (one for cations, one for anions) prepared annually; distributed to sites for the following year’s analysis.
  - QC data must be submitted in the same data format as sample results, with date fields adjusted for QC preparation and analysis dates.
- Procedure for QC preparation and analysis:
  - Prepare QC solutions from concentrated stocks; acidify aliquots as needed to match sample matrices.
  - Analyze cation solution for cations and DOC; anion solution for pH, conductivity, anions, NH4-N, Total N, Total P.
  - Submit QC results as a single batch record, including all determinands.
- Data transfer:
  - QC data are transferred to the ECN CCU in a free-format, comma-separated record with standardized fields (Measurement code, Site ID, QC sample code, preparation dates, analysis dates, determinand results, and quality codes).

## Data transfer and formatting details
- QC data format (example fields):
  - Measurement code, Site ID, Local QC sample code, QC preparation date, Date of pH measurement, Time, Preparation date for other determinands, Date analysis complete, pH (unstirred and stirred), Conductivity, Alkalinity, Na, K, Ca, Mg, Fe, Al, PO4-P, NO3-N, NH4-N, Cl, SO4-S, DOC, Total N, Quality code, etc.
- Quality codes and notes: Standardized quality fields follow as needed; provides a mechanism to flag data quality status.

## Documentation and governance
- Method changes are timestamped with database records to indicate updates.
- Labs control instrument maintenance, calibration, drift, and staff training; records ensure traceability and suitability of data for the study purpose.

## Practical implications for data users
- Data carry rich metadata: determinand, site, date, method, detection limit, calibration range, and QC status.
- Data users can assess data quality via documented accuracy and precision procedures and interlaboratory checks.
- Any methodological changes are traceable, enabling evaluation of data consistency over time.