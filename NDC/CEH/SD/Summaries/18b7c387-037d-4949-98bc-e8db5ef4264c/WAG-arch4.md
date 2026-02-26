# WAG Protocol

- Purpose: Provide guidelines for analysis of water samples from ECN terrestrial sites; laboratories manage analytical resources but must conduct analyses under controlled conditions, document methodology, changes, and validation procedures; annual review by Analytical Working Group; define target detection limits.

- Governance and responsibilities for data leaders:
  - Laboratories retain detailed methods; summary methodology is stored for the ECN database.
  - Each determinand has a data record in a meta database linking site, core measurement, determinand, and date to indicate methodology and precision.
  - Method changes require date-stamped records; site managers must document instrument maintenance, calibration, drift, and staff training.

- Approved and reference techniques:
  - Approved techniques are listed for each determinand (e.g., pH, conductivity, various cations/anions, DOC, Total N, etc.), with notes on species quantified and suitable alternatives.
  - Reference techniques provide primary methods for comparison and assessment of new methodologies; emphasis on consistency and comparability over time.

- Priority determinands (in case of low sample volumes):
  - 1) pH and conductivity
  - 2) Cations (Ca2+, Mg2+; then K+, Na+)
  - 3) Anions (NO3-, SO4 2-, then PO4 3-, Cl-)
  - 4) NH4+-N
  - 6) Cations requiring separate acidified portions (Fe2+, Al3+)
  - 5) DOC
  - 7) Total-N, alkalinity

- Providing details of methodology and data traceability:
  - Laboratories keep full method details locally; ECN database holds summarized metadata per determinand/site/date.
  - Example record (nitrate): includes site, determinand, sample types, volumes, calibration ranges, measurement technique, detection limit, precision, and interferences.
  - Reports should include fractionation, if specified (e.g., NO3- vs NO3-N), and monitoring for bias when alternative techniques are used.

- Validation, accuracy, and precision:
  - Validation achieved via approved techniques, uniform detection limits, and internal quality control; participation in interlaboratory schemes (e.g., AQUACHECK) recommended.
  - Accuracy measures agreement with wider analytical community; results recorded to confirm conformity and any corrections.
  - Example accuracy record illustrates percentage relative error and corrective actions if needed.

- Quality control (QC) and long-term data integrity:
  - Separate QC system for ECN participants using synthetic solutions; site managers may perform QC locally.
  - Between-site correction factors can be computed if sites use standardized solutions; helps detect rogue batches and trends.
  - QC data must be reported to ECN database in a predefined format; batch-level QC data include both anion and cation results.
  - Annual preparation of QC concentrate (two solutions) with continuity checks across years.

- Data transfer and formats:
  - QC data and sample results are transmitted in machine-readable, comma-separated format.
  - Data record fields cover measurement code, site ID, QC codes, preparation and analysis dates, pH measurements (two forms), conductivity, alkalinity, and all determinands (with units and precision).
  - Quality codes support additional fields if required; example provided for Moor House.

- Data quality culture and ongoing improvement:
  - Emphasis on documenting methodology changes, maintaining traceability, and using QC results to monitor performance.
  - Encourages ongoing internal QC validation and adoption of accredited interlaboratory exchanges to ensure data quality and comparability across the ECN network.

- Cross-cutting references for implementation:
  - Initial Water Handling Protocol referenced for sample handling specifics (filtration, pH, acidification).
  - Protocol supports ensuring data assets are fit for purpose, comparable across sites, and capable of supporting long-term ecological analyses.