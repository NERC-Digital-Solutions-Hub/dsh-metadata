# WAG Protocol

- Purpose and scope
  - Analytical guidelines for analyzing water samples from ECN terrestrial sites.
  - Laboratories manage their own resources but must conduct analyses under controlled conditions and document methodology, changes, and validation procedures.
  - Annual review of procedures by an Analytical Working Group with representatives from each laboratory.

- Approved techniques and flexibility
  - Table of approved techniques for determinands (e.g., pH, conductivity, major ions, DOC, Total N, etc.) with alternative methods noted.
  - Some techniques quantify indirect species; when necessary, laboratories should monitor alternative methods to confirm bias absence.
  - For pH and conductivity, reference to the Initial Water Handling Protocol; detection limits set as targets.
  - Priority on reporting the fraction specified (e.g., SO4 2- by IC) and assessing bias if alternate fractions are used.

- Determinands priority (guidance for limited sample volumes)
  - 1: pH and conductivity (highest priority)
  - 2: Anions (NO3-, SO4 2-, then PO4 3-, Cl-)
  - 3: Cations (Ca2+, Mg2+, then K+, Na+)
  - 4: NH4+ N
  - 5: DOC
  - 6: Fe2+, Al3+
  - 7: Total N, alkalinity

- Data management and methodology records
  - Laboratories keep detailed methodological information; ECN database stores metadata for each determinand-site-date, indicating methodology and precision.
  - Meta record example includes substance, sample types, typical concentrations, calibration range, measurement method, results format, detection limit, and QC measures.
  - Any change to details results in a new database record with a date stamp.
  - Instrument maintenance, calibration, drift, and staff training are controlled by the laboratory.
  - Aim to provide a record of changes and assess suitability for the data’s purpose.

- Validation, accuracy, and precision
  - Validation via approved techniques, uniform detection limits, and internal QC; regular interlaboratory analyses (e.g., AQUACHECK).
  - Accuracy: proximity to true value and agreement across laboratories; results reported to ECN Database Manager; example records show percentage relative error and corrective actions if needed.
  - Precision: use of synthetic QC solutions to assess batch bias; QC data reported to Site Managers with sample results; unacceptable QC results mean data are not submitted.

- Interlaboratory quality control and community practices
  - A separate QC system exists for ECN participants; ongoing independent QC validation encouraged; interlaboratory exchange schemes recommended.
  - Potential to compute between-site correction factors if sites use uniform solutions and procedures.
  - Aim to detect rogue batches and long-term analytical trends; managed by analysts.

- QC materials and data transfer
  - Two concentrated QC solutions prepared at Merlewood (one for cations, one for anions) distributed to site managers for use in subsequent analyses.
  - Annual renewal of QC concentrates; continuity checks by analyzing old and new solutions in parallel.
  - QC data submitted in the same format as sample data to the ECN CCU, with a unified data record structure for each batch.
  - Data record fields include measurement code, site, QC sample code, preparation and analysis dates, pH and conductivity metrics, major ion and nutrient results, DOC, Total N, and quality codes.

- Data format and records
  - QC data records are free-format, comma-separated, with a standardized sequence of variables; a single QC record per batch encompassing both anion and cation results.
  - Example provided (Moor House) illustrating fields such as preparation dates, measurement dates, pH, conductivity, determinand results, and quality codes.

- Change management and governance
  - Methodology changes are tracked via dated records in the ECN meta-database.
  - Laboratories hold control over their analytical processes, with governance and periodic review embedded in the protocol.

- Implications for data leadership
  - Establishes robust governance, metadata, and versioning for environmental water data.
  - Emphasizes standardization of methods, transparency of changes, and interlaboratory quality assurance.
  - Supports data usability across sites through uniform detection limits, documented methodologies, and QC-driven data quality.