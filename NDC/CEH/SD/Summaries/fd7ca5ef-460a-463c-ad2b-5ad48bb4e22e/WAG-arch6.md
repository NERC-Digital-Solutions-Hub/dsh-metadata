# WAG Protocol ANALYTICAL GUIDELINES FOR WATER SAMPLES Version 1.1 (previously AG Protocol, updated Jan 2001)

## Aim
- Provide guidelines for the analysis of water samples from ECN terrestrial sites.
- Laboratories manage their own resources but must conduct analyses under controlled conditions and document methodologies, changes, and validation procedures.
- Annual review by an Analytical Working Group.
- Define primary methods and target detection limits to ensure consistency.

## Approved techniques and reference methods
- Determinands and approved techniques include: pH, conductivity, Na, K, Ca, Mg, Fe, Al, NH4+-N, Cl-, NO3--N, SO4--S, HCO3-, PO4--P, DOC, Total N.
- Methods include traditional references (e.g., HMSO Blue Book) and alternatives (AAS, IC, ICP/OES, Col- methods) with notes on species quantified.
- Alternatives may be used but must be validated and monitored against reference techniques to avoid bias.
- For pH and conductivity, refer to the Initial Water Handling Protocol.
- Laboratories should report data for specified fractions (e.g., SO4 as SO4-S) and monitor alternative techniques for bias if used.

## Priority listing of determinands
- When sample volumes are limited, follow this order (1 = highest):
  1. pH, conductivity
  2. Anions: NO3-, SO4--S, then PO4--P, Cl-
  3. Cations: Ca2+, Mg2+, then K+, Na+
  4. NH4+-N
  5. DOC
  6. Cations requiring separate acidified portion: Fe2+, Al3+
  7. Total N, Alkalinity
- Refer to the Initial Water Handling Protocol for sample handling, filtration, pH, and acidification guidance.

## Providing details of methodology
- Laboratories keep detailed methods locally; a summary is stored in the ECN meta-database, linked by site, determinand, and date.
- Each data record includes substance, sample type, analytical basis, typical concentrations, calibration range, detection limit, and QC/accuracy measures.
- When methodology changes, a new record with a date stamp is created.
- Internal lab maintenance, calibration, drift, and training are managed by the laboratory.

## Validation: accuracy and precision
- Validation relies on approved techniques, uniform detection limits, and internal QC, plus regular interlaboratory checks (e.g., AQUACHECK).
- Accuracy measures closeness to true value; results and any correction procedures are recorded. Example provided shows a dissolved sulfate accuracy check with percent relative error and corrective actions if needed.
- Precision is controlled via synthetic QC solutions; QC data are reported to Site Managers and, where possible, interlaboratory schemes are used to assess performance.
- Laboratories should submit accuracy and precision data to ECN databases and participate in ongoing quality assessment.

## Quality Control (QC) procedures
- An ECN-specific QC system complements individual laboratory QC, enabling inter-site correction factors and long-term trend detection.
- Merlewood prepares two QC concentrates (cation and anion) annually; sites dilute and analyze QC solutions in the same way as samples.
- QC results are submitted in the same data format as samples, with preparation and analysis dates tracked for continuity.
- A dedicated example QC record (Moor House) illustrates data fields, units, and a quality code (Q) with subsequent quality codes as needed.

## Data transfer and metadata
- QC data are transferred to the ECN Central Control Unit (CCU) using a free-format, comma-separated dataset identical in structure to sample data, but with QC-specific date fields.
- Data fields cover measurement codes, site IDs, QC sample codes, preparation dates, analysis dates, pH (unstirred and stirred), conductivity, alkalinity, ions (Na, K, Ca, Mg, Fe, Al, PO4-P, NO3-N, NH4-N, Cl, SO4-S), DOC, Total N, plus a quality code.
- A standardized QC data record consolidates both anion and cation results per batch.
- An example Moor House QC record is provided to illustrate formatting and quality coding.

## Notes and recommendations
- Ensure data on the correct chemical fractions and monitor bias when alternative techniques are used.
- Maintain and reference method metadata for each ECN site and determinand to support data comparability.
- Regularly review methodology changes and validate new methods against reference techniques.

## Author and revision
- Documented by A.P. Rowland and colleagues; includes ongoing revision to maintain alignment with ECN requirements and interlaboratory quality standards.