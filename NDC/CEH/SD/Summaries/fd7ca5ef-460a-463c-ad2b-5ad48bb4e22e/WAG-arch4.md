# WAG Protocol

## Purpose and scope
- Analytical guidelines for water samples from ECN terrestrial sites.
- Laboratories are responsible for managed analyses under controlled conditions; must document methodology, changes, and validation procedures.
- Annual review of procedures by Analytical Working Group with representatives from each laboratory.

## Governance and responsibilities
- Laboratories conduct analyses under controlled conditions and document methodology, significant changes, and validation procedures.
- Analytical Working Group reviews procedures annually.
- Methods may be updated; laboratories must report changes and maintain records for traceability.

## Approved techniques and determinands
- Provides a set of approved techniques for key determinands (e.g., pH, conductivity, major ions, nutrients, DOC, total N).
- Alternative approved techniques listed; notes indicate suitability and when species-specific quantification may require additional testing.
- Reference techniques identified for comparison and assessment of new methodologies.
- Detection limits set as targets for each determinand and technique.

## Data requirements, metadata and reporting
- Details of analytical methods should be kept by the laboratory; summary information stored in the ECN database (one record per determinand per site).
- Meta database record includes site, core measurement, determinand, date, methodology, and precision.
- Any methodological change creates a new dated record; consistency and traceability are maintained.
- Laboratories must report data for the specified fraction (e.g., sulfate by IC) and monitor alternatives to confirm lack of bias if different techniques are used.

## Methodology documentation and data management
- Data records link to methodology and suitability for purpose.
- Reference to Initial Water Handling Protocol for sample handling, pH, and acidification guidance.
- Data standards and uniform detection limits facilitate cross-site comparability.

## Validation, accuracy and precision
- Validation achieved through approved techniques, uniform detection limits, and internal QC; participation in interlaboratory analyses (e.g., AQUACHECK).
- Accuracy: closeness to true value; assessed via control samples and inter-lab comparisons; corrective actions recorded.
- Precision: assessed using QC samples; results reported to site managers; rogue batches and trends monitored.

## Quality control procedures and interlaboratory comparisons
- Separate QC system for ECN participants; encourages internal QC validation and participation in external interlaboratory schemes.
- Possibility of calculating between-site correction factors if sites use consistent solutions and procedures.
- QC practice includes preparation of concentrated QC solutions for cations and anions, analysis of QC samples, and annual continuity checks.
- QC data must be submitted to the ECN Central Control Unit (CCU) in a machine-readable format, with detailed fields for dates, measurements, and quality codes.

## Data transfer, formatting and records
- QC data transfer fields cover preparation dates, analysis completion, and determinations for pH, conductivity, and all determinands (e.g., Na, Ca, NO3-N, NH4-N, DOC, Total N).
- Data records are comma-separated with defined field order; example provided for Moor House QC record.
- Quality codes (Q) and optional quality codes follow per-record.

## Priority handling when sample volume is limited
- A priority ordering guides data collection when rainfall is low and sample volumes are constrained:
  1) pH and conductivity
  2) Major cations (Ca2+, Mg2+) then K+, Na+
  3) Anions (NO3-, SO4 2-, PO4 3-, Cl-)
  4) NH4+ N
  5) DOC
  6) Total N, alkalinity
  7) Cations requiring separate acidified aliquots (Fe2+, Al3+)

## Practical implications for Data Leaders
- Establish and enforce standardized methodologies and metadata schemas across labs to ensure data comparability.
- Maintain a robust data lineage framework: method records, date-stamped changes, and linkage to the ECN meta-database.
- Mandate regular QA/QC participation (e.g., AQUACHECK) and transparent reporting of accuracy and precision metrics.
- Implement clear data transfer protocols and machine-readable formats to support seamless integration into the ECN database.
- Use the priority list to guide data collection strategies during low-volume periods, ensuring critical determinands are consistently captured.
- Facilitate collaboration across laboratories to develop corrective factors and detect analytical trends or rogue batches.