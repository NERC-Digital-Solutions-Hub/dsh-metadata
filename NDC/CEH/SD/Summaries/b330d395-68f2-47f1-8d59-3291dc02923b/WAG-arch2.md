# WAG Protocol

- Purpose: Analytical guidelines for analyzing water samples from ECN terrestrial sites, with labs responsible for controlled analyses, documentation of methodology, method changes, validation procedures, and annual reviews by an Analytical Working Group.

- Scope of work: Defines approved and reference techniques for determinands, reporting formats, detection limits, and quality control to ensure consistent long-term environmental monitoring data.

- Roles and responsibilities:
  - Laboratories manage analytical resources under controlled conditions.
  - Document methodologies, significant method changes, and validation procedures.
  - Submit methodology summaries to the ECN meta-database; maintain records of instrument maintenance, calibration, drift, and staff training.
  - Participate in interlaboratory checks (e.g., AQUACHECK) and internal QC to demonstrate accuracy and precision.

- Approved and reference techniques:
  - Determinands include pH, conductivity, major cations (Na, K, Ca, Mg), trace/major elements (Fe, Al), nutrients (NH4-N, NO3-N, PO4-P, SO4-S), alkalinity, DOC, and Total N.
  - Methods span HMSO recommendations, AAS, ICP/OES, IC, colorimetric/indophenol methods, and Col (colorimetric) techniques; some methods quantify fractions rather than the exact species and may require comparative testing to monitor bias.
  - For pH and conductivity, refer to the Initial Water Handling Protocol; explicit limits and reporting standards are provided.

- Notes on methodology and data:
  - Laboratories must record method details for each determinand and each ECN site; data in the ECN database link site, determinand, date, and method.
  - An example is provided for nitrate using ion chromatography with specific sample types (rainwater, stream, soil solution) and calibration details.

- Priority listing of determinands (volume-limited scenarios):
  1. pH and conductivity
  2. Cations (Ca2+, Mg2+; then K+, Na+)
  3. Anions (NO3-, SO4 2-; then PO4 3-, Cl-)
  4. NH4+-N
  5. (DOC or total N, depending on interpretation) 
  6. Cations requiring separate acidified portion (Fe2+, Al3+)
  7. Total N, alkalinity
  - Follow the Initial Water Handling Protocol for sample handling, filtration, pH, and acidification.

- Providing details of methodology and data management:
  - Methodology details are stored locally, with summary metadata in the ECN meta-database.
  - Includes performance characteristics such as sample type, calibration range, detection limits, and data processing (e.g., regression corrections).

- Validation and quality assurance:
  - Two core measures: accuracy (closeness to true value and interlaboratory agreement via control schemes like AQUACHECK) and precision (repeatability via QC samples).
  - Laboratories should report accuracy checks and any corrective actions; maintain records of accuracy results to confirm conformity.
  - An accuracy record example demonstrates compare-and-correct processes across laboratories.

- Precision and quality control:
  - Use synthetic QC solutions to assess batch bias; report QC data with sample results to site managers.
  - A separate ECN QC system enables inter-site comparison, detection of rogue batches, and long-term analytical trends.
  - Annual preparation of concentrated QC solutions (one for cations, one for anions) at Merlewood; ongoing continuity checks across years.

- Data transfer and QC data format:
  - QC data must be submitted to the ECN CCU in a machine-readable, free-format dataset, with a single QC record per batch containing both anion and cation results.
  - The QC data record structure includes fields for measurement code, site, preparation dates, analysis dates, measurements (pH, conductivity, alkalinity, major ions, DOC, Total N), and quality codes.
  - An example Moor House QC record illustrates the required data layout and coding.

- Quality Control Procedures for the ECN Terrestrial Network:
  - A separate QC framework supplements internal QC and interlaboratory checks.
  - Enables computation of between-site correction factors and monitoring of data quality over time.
  - Encourages ongoing independent QC validation and participation in interlaboratory schemes.

- Practical notes:
  - If a site uses local analysis for pH and conductivity, QC preparation dates must reflect that; otherwise, a single QC solution may be used with repeated preparation dates.
  - Changes in methodology should trigger a new database entry with a date stamp to indicate when suitability for purpose was reassessed.

- Authorship and revision:
  - Principal author: A. P. Rowland (with contributions from C. Woods, M. Lane, and others); revised August 1998 (with references to earlier HMSO standards and methods).