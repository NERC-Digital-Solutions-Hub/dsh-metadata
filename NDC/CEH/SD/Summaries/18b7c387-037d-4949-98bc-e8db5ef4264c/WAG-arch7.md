# ANALYTICAL GUIDELINES FOR WATER SAMPLES Version 1.1 (previously AG Protocol, updated Jan 2001)

- Aim and scope
  - Provide guidelines for analysis of water samples from ECN terrestrial sites.
  - Laboratories are responsible for resources and must conduct analyses under controlled conditions.
  - Require documentation of methodology, significant changes, and validation procedures.
  - Annual review by an Analytical Working Group representing participating laboratories.
  - Outline appropriate methods and establish target detection limits for each determinand.

- Approved techniques and reference methods
  - Deteminands include pH, conductivity, major cations (Na, K, Ca, Mg), major anions (NO3, SO4, PO4, Cl, HCO3), metals (Fe, Al), NH4-N, DOC, Total N, etc.
  - For each determinand, tables list alternative approved techniques and reference techniques (superscripts refer to notes).
  - Some techniques quantify related species rather than directly the target fraction; pH and conductivity reference to Initial Water Handling Protocol.
  - Laboratories should report data for the specified fraction; if a different but biased technique is used, monitor against bias by comparing alternative methods.
  - Operational analytical ranges vary by lab; near detection limits assess whether data are suitable or require re-analysis with a lower range.
  - Uniform guidelines are required across laboratories to enable comparability.

- Priority ordering when sample volumes are limited
  - 1 (highest): pH and conductivity
  - 2: Cations – Ca2+, Mg2+ (then K+, Na+)
  - 2: Anions – NO3−, SO42− (then PO4 3−, Cl−)
  - 4: NH4+ N
  - 6: DOC
  - 7: Total N, alkalinity
  - Follow the Initial Water Handling Protocol for sample handling, filtration, pH, and acidification guidance.

- Providing details of methodology and data recording
  - Each laboratory keeps detailed methods; ECN database stores summary method for each determinand per site.
  - Data structure: one data record per determinand per ECN site, including site, core measurement, determinand, date, methodology, and precision.
  - Example format provided for nitrate includes: sample type, volume, calibration range, measurement method, detected values, detection limit, and QC notes.
  - Changes to methods create new database records with date stamps; lab maintenance and staff training are controlled by the lab.

- Validation, accuracy, and precision
  - Validation achieved via approved techniques, uniform detection limits, and internal QC; regular participation in interlaboratory checks (e.g., AQUACHECK).
  - Accuracy: assesses closeness to true value, monitored through control samples and external schemes; require recording accuracy checks and any corrective actions.
  - Example accuracy record illustrates comparing measured vs mean values and reporting relative error with corrective actions if needed.

  - Precision: ensured with synthetic QC solutions; QC data must be reported with each result set; data should not be submitted if QC indicates unacceptable performance.

- Quality Control procedures for ECN terrestrial network
  - A distinct ECN QC system complements laboratory QC, encouraging independent validation and interlaboratory exchange.
  - Aim to enable between-site correction factors and detection of rogue batches or long-term trends.
  - Analysts manage QC with two concentrated QC solutions prepared at a central site (Merlewood) for cation and anion analyses.
  - Procedures cover preparation, dilution, analysis of QC samples, and continuity checks year-to-year.
  - QC data are transferred to the ECN Central Coordination Unit (CCU) in a standardized format as part of the dataset; includes batch-level QC results for both cationic and anionic determinations.
  - Example QC record (Moor House) demonstrates how QC fields are populated, including preparation dates, analysis dates, measured values, quality codes, and notes.

- Data transfer, formatting, and records
  - QC data must be submitted in the same format as water sample data, with adjusted date fields for QC preparation.
  - Data records are designed for machine readability (CSV-like format) and include a comprehensive set of fields for traceability and quality assessment.
  - The format supports both the primary determinant data and accompanying QC indicators to enable end-user assessment of data suitability.

- Practical implications for GIS-based data products
  - Each measurement is tied to detailed metadata: site, determinand, date, method, detection limit, precision, and QA/QC status.
  - Data provenance is explicit: methodology changes are versioned with date stamps; reference methods provide context for comparability.
  - Enables harmonized map-based data visualizations across ECN sites, with transparent uncertainty (detection limits, accuracy, precision) and QA status.
  - Supports data integration across laboratories by requiring cross-checks for bias and interlaboratory consistency (AQUACHECK).
  - Facilitates data quality flagging and filtering in GIS workflows to ensure reliable map outputs, trend analyses, and policy-relevant visuals.

- Author and revision note
  - Authoring context: A.P. Rowland et al.; revised August 6, 1998; updated January 2001 to Version 1.1.