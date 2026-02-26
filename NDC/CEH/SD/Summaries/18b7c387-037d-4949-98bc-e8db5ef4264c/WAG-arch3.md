# WAG Protocol

## Aim
- Provide guidelines for the analysis of water samples from ECN terrestrial sites.
- Ensure laboratories operate under controlled conditions with documented methodologies, method changes, and validation procedures.
- Annual review of procedures by an Analytical Working Group with representatives from each laboratory.

## Governance, roles and data stewardship
- Participating laboratories manage analytical resources; one lab’s methodology may be used, but all analyses must be documented.
- A meta-database for ECN stores summary information about methodologies, sites, determinands, dates, and precision to indicate suitability and enable data interpretation.
- Laboratories are responsible for instrument maintenance, calibration, drift, and staff training; methodology changes are version-stamped in the database.
- Emphasis on data sharing of underlying data and clear presentation of findings; outputs should be traceable to the original methodologies.

## Approved and reference techniques
- For each determinand, there are approved techniques and alternative methods; the document lists multiple options (e.g., pH, conductivity, various ion analyses) and indicates when alternatives are suitable.
- Reference techniques (primary methods) are provided as benchmark standards, with explicit notes on detection limits and measurement approaches.
- Some methods quantify related species rather than the exact target; comparative testing may be required to ensure consistency.

## Priority listing of determinands
- When sample volumes are limited, a priority order guides analytical options:
  1) pH and conductivity
  2) Cations: Ca2+, Mg2+, then K+, Na+
  3) Anions: NO3-, SO4 2-, then PO4 3-, Cl-
  4) NH4+-N
  6) Fe2+, Al3+
  5) DOC
  7) Total N and alkalinity
- Refer to the Initial Water Handling Protocol for sample handling, filtration, pH adjustment, and acidification.

## Providing details of methodology
- Each laboratory keeps detailed method documents locally; a concise summary is stored in the ECN database, linked to site, determinand, and date.
- The database entry includes substance, matrix, method, typical concentrations, calibration ranges, sample volumes, detection limits, and QC notes.
- A sample format is provided (nitrate example) to illustrate how methodology and performance characteristics are recorded.

## Validation, accuracy and precision
- Validation hinges on using approved techniques, uniform detection limits, and internal QC; regular interlaboratory comparisons (e.g., AQUACHECK) are required.
- Accuracy: assesses closeness to the true value and consistency across the analytical community; results and any corrective actions are recorded and reported to the ECN database.
- Precision: ensured via synthetic QC solutions; QC data are reported with each batch; analyses should be halted if QC indicates unacceptable performance.
- Laboratories may implement their own QC schemes and interlaboratory checks to monitor long-term trends and detect rogue batches.

## Data transfer, records and governance
- Data quality rests on accuracy and precision; methodologies and data are accessible for interpretation and auditing.
- Any methodological changes are stamped with dates; updates are reflected in the ECN database to maintain data lineage.
- QC data and batch information are transferred to the ECN CCU in machine-readable form, with consistent formatting and a single QC record per batch.

## Quality control procedures for the ECN Terrestrial Network
- A dedicated QC framework complements internal QC, including:
  - Preparation of two QC solutions (for cations and anions) distributed to sites.
  - Analysis of QC solutions in the same manner as samples.
  - Annual renewal of QC concentrates with continuity checks across years.
  - QC data incorporated into the same data records as samples; a detailed data transfer format governs submission.

## Example data and records
- Example Moor House QC record demonstrates the structure of QC data, including:
  - Measurement code, site ID, preparation dates, analysis dates, pH, Conductivity, determinand concentrations, and quality codes.
- The format is free-form, comma-separated, and designed to be machine-readable for integration with the ECN database.

## Notes and cautions
- For pH and conductivity, follow the Initial Water Handling Protocol.
- If laboratories choose techniques that quantify related fractions rather than the exact species, they should monitor alternative methods to confirm bias absence.
- Changes in methodology should be recorded with date stamps and linked to data to ensure traceability and assess suitability for the intended analyses.