# WAG Protocol ANALYTICAL GUIDELINES FOR WATER SAMPLES Version 1.1 (previously AG Protocol, updated Jan 2001)

## Aim
- Provide guidelines for analysis of water samples from ECN terrestrial sites.
- Labs must operate analyses under controlled conditions and document methodologies, changes, and validation procedures.
- Annual review of procedures by Analytical Working Group with representatives from each laboratory.
- Establish detection limits and target performance for laboratories’ chosen methods.

## Scope and governance
- Laboratories manage their own resources but must adhere to standardized procedures and documentation.
- Metadata and methodology details should be recorded and maintained; summary information fed into the ECN database.
- Method changes are versioned with date stamps to track suitability for purpose.

## Approved techniques and reference techniques
- Tables of determinands with alternative approved techniques (superscripts refer to notes).
- Examples include pH, Conductivity, various ions (Na+, K+, Ca2+, Mg2+, NH4+, Cl-, NO3-, SO4 2-, PO4 3-), alkalinity, DOC, Total N.
- Preference for primary reference techniques (e.g., HMSO references) and notes on species quantified and detection limits.
- Guidance on when bracketed or alternative techniques may be suitable (with bias monitoring requirements).

## Data documentation and metadata
- Laboratory-method details kept by operators; summary information stored in the ECN meta database.
- Each determinand at each ECN site has a single data record linking site, core measurement, determinand, and date to indicate methodology and precision.
- Example provided for nitrate: method, sample types, typical concentrations, calibration range, reporting format, detection limit, and QC notes.

## Validation, accuracy, and precision
- Validation achieved through approved techniques, uniform detection limits, and internal QC; obligation to participate in interlaboratory analysis (e.g., AQUACHECK).
- Accuracy: closeness to true value; monitored via control samples and external schemes; all accuracy checks must be recorded.
- Precision: controlled via QC samples; data should not be submitted if QC indicates unacceptable performance.
- Example records illustrate how accuracy and interlaboratory comparisons are tracked.

## Quality control procedures
- Separate QC system for ECN participants; encouraged to maintain independent QC validation and join interlaboratory schemes.
- Opportunity to compute between-site correction factors; enables detection of rogue batches and long-term trends.
- Analysts manage QC provisions; annual preparation of concentrated QC solutions for cations and anions, with continuity checks across years.
- QE data transfer: QC data submitted to ECN CCU in a specified free-format, comma-separated dataset, aligned with sample data fields.

## Procedure for QC solution preparation and data transfer
- Detailed steps for preparing QC solutions (two concentrates, one for cations, one for anions), dilution, and matrix matching.
- QC samples analyzed in the same manner as other samples; new concentrate prepared annually; continuity checks performed.
- Data transfer format includes a structured set of fields (measurement code, site ID, QC sample code, preparation dates, analysis dates, pH, conductivity, all determinands, and quality codes).
- Example QC record provided (Moor House) to illustrate data submission format.

## Priority listing of determinands
- Establishes a hierarchy for limited sample volumes during low rainfall.
- 1 = pH and conductivity; 2 = cations (Ca2+, Mg2+, then K+, Na+) and anions (NO3-, SO4 2-, PO4 3-, Cl-); 3 = NH4+-N; 4 = Fe2+, Al3+; 5 = DOC; 6 = Total N and alkalinity; guides analytical options under constraints.

## Documentation of methodology changes
- Any changes to analysis are recorded with a date stamp; lab-specific details (maintenance, calibration, drift, training) are controlled at the laboratory level.
- Summary of changes documents suitability for purpose and provides a traceable history for datasets.

## Data management and stewardship implications
- Provides a robust metadata framework: per-d determinand methodology, lab-specific practices, calibration ranges, detection limits, and QC records.
- Supports data discoverability and interoperability by linking methodology to site, date, and determinand in a central database.
- Enables cross-lab comparability through reference techniques, standardized detection limits, and interlaboratory controls.
- Facilitates data quality assessment through documented accuracy/precision checks, corrective measures, and long-term QC trends.
- Requires ongoing governance: annual method reviews, versioning of protocols, and timely documentation of methodology updates and validation results.