# WAG Protocol

- Aim and scope: Guidelines for analysis of water samples from ECN terrestrial sites. Laboratories must analyze under controlled conditions, document methodologies and changes, and participate in an annual review by an Analytical Working Group. Detection limits serve as targets for method performance.

- Roles and responsibilities (data governance perspective):
  - Laboratories manage analytical resources; ECN participants must follow standardized procedures.
  - Documentation of methodologies, significant changes, and validation procedures is required.
  - Methodology changes are tracked with date-stamped records; responsibility lies with the performing laboratory.
  - The Analytical Working Group provides governance and periodic review.

- Approved techniques and reference methods:
  - A range of determinations with multiple alternative techniques (pH, conductivity, major ions, metals, nutrients, alkalinity, DOC, total N, etc.).
  - For each determinand, there are primary reference techniques (e.g., HMSO references, AAS, IC, ICP/OES, Col- methods, Kjeldahl, etc.).
  - Laboratories should report data for the specified fraction (e.g., NO3-N, SO4-S) and monitor alternative techniques for bias.
  - Detection limits are defined and used to assess data suitability.

- Methodology documentation and metadata:
  - Labs keep detailed method information locally; ECN meta-database stores a per-determinand, per-site record linking methodology, precision, typical concentrations, calibration ranges, sample volumes, and reporting formats.
  - Each change to methodology creates a new dated record to indicate suitability for purpose and to track performance over time.

- Validation, accuracy, and precision:
  - Validation relies on uniform detection limits and internal QC; participation in interlaboratory analyses (e.g., AQUACHECK) is required.
  - Accuracy reflects agreement with the broader analytical community; all accuracy checks and corrections must be recorded.
  - An example accuracy record demonstrates reporting, method, lab, and corrective actions as applicable.

- Precision and quality control (QC):
  - QC uses synthetic solutions to assess batch bias; QC data are reported to Site Managers with results of each batch.
  - Participation in AQUACHECK and other interlaboratory schemes is encouraged; separate internal QC measures exist (e.g., CUSUM, AQUACHECK).
  - Consideration of between-site correction factors is possible to detect trends or rogue batches; QC solutions are prepared annually at a central site and used for the coming year.

- Data transfer and metadata standards:
  - QC data and sample results are transferred to the ECN Central Coordination Unit (CCU) in a consistent, machine-readable format (CSV-like).
  - A detailed field list governs the QC data record, including preparation dates, analysis dates, pH and conductivity measurements, concentrations for determinands, and quality codes.
  - A single QC record covers both anion and cation results; datasets may be consolidated but must preserve date-based context.

- Priority handling for limited sample volumes:
  - In low-volume periods, priority is set to ensure critical measurements are obtained in order: 1) pH and conductivity; 3) major cations (Ca2+, Mg2+, then K+, Na+) and anions (NO3-, SO4 2-, then PO4 3-, Cl-); 4) NH4+-N; 6) Fe2+, Al3+ (with separate acidified aliquots); 5) DOC; 7) Total N and alkalinity.

- Documentation of changes and data governance considerations:
  - Any methodological changes trigger database updates with date stamps, ensuring traceability.
  - Instrument maintenance, calibration, drift, and staff training are managed by the laboratory and influence data quality and interpretation.

- Example records and implications for stewardship:
  - Accuracy records (e.g., AQUACHECK comparisons) illustrate how results compare to reference values, enabling correction and bias assessment.
  - Example QC records (fields and format) demonstrate how data provenance, sample handling, and analytical performance are captured for auditability.

- Takeaways for Data Stewards:
  - Maintain and monitor metadata linking site, determinand, method, date, and performance metrics.
  - Ensure governance around method changes, validation procedures, and interlaboratory comparisons is enforced.
  - Uphold standardized data formats for both results and QC Records to enable reliable discovery, reuse, and long-term data quality across ECN sites.