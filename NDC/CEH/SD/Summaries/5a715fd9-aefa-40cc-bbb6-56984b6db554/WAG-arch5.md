# ANALYTICAL GUIDELINES FOR WATER SAMPLES Version 1.1 (previously AG Protocol, updated Jan 2001)

## Aim
- Provide guidelines for analysis of water samples from ECN terrestrial sites.
- Laboratories must conduct analyses under controlled conditions and document methodologies, significant changes, and validation procedures.
- Annual revision of procedures by an Analytical Working Group representing participating laboratories.
- Methods include defined detection limits and approved techniques for each determinand.

## Approved techniques and reference techniques
- Table of determinations with alternative approved techniques for each determinand (superscripts link to notes).
- Methods cover pH, conductivity, major ions (Na, K, Ca, Mg, Fe, Al), ammonium, Cl, NO3, SO4, alkalinity, PO4, DOC, Total N, etc.
- Notes clarify that some techniques quantify a related fraction or require comparative tests; pH and conductivity have additional Handling Protocol references.
- Reference techniques provide primary standards (e.g., HMSO publications, specific ion chromatography, AAS, IC, colorimetric methods).
- Laboratories must report data for the specified fraction and monitor alternate techniques to avoid bias if a different method is used.
- Uniform detection limits are defined to guide inter-lab comparisons; operational ranges may differ between laboratories.

## Providing details of methodology
- Laboratories keep full methodological details for operators; ECN database stores summary method information per determinand/site.
- Meta-database record includes site, core measurement, determinand, date, methodology in operation, and precision.
- Example format shown for nitrate (method, sample types, concentration ranges, calibration, QC measures).
- When methodology changes, a new dated record is added; laboratories control instrument maintenance, calibration, drift, and staff training.

## Validation
- Data validation relies on approved techniques, uniform detection limits, and internal quality control; participation in interlaboratory schemes (e.g., AQUACHECK) is required.
- Two main quality measures: accuracy and precision.

### Accuracy
- Measures closeness to true value and agreement across the analytical community.
- Achieved via control sample schemes; record all accuracy checks and any corrective procedures.
- Example accuracy record demonstrates percent relative error and corrective actions if needed.
- All accuracy results relevant to ECN samples must be reported to the ECN Database Manager in machine-readable form.

### Precision
- Controlled through synthetic QC solutions to detect batch bias; QC data reported to Site Managers with results.
- Laboratories should validate batches independently and may participate in accredited interlaboratory exchanges.

## Quality Control Procedures for ECN
- A separate ECN QC system exists; laboratories supplement with independent QC validation.
- Allows computation of between-site correction factors and detection of rogue batches/trends over time.
- Merlewood provides two concentrated QC solutions (cation and anion) distributed to site managers annually; used to monitor batch performance.
- QC solutions are analyzed in the same manner as samples; continuity checked by comparing previous and new QC solutions.
- QC data submission to ECN CCU uses the same data format as samples, with dates adjusted for QC preparation dates instead of sampling dates.

## Data Transfer and QC data format
- QC data must be submitted in a machine-readable, comma-separated format, aligned with the sample data structure.
- Data record fields include: measurement code (QC), Site ID, QC sample code, QC preparation dates, analysis dates, pH (un-stirred and stirred), conductivity, alkalinity, major ions (Na, K, Ca, Mg, Fe, Al), anions and cations (NO3-N, NH4-N, Cl, SO4-S, PO4-P), DOC, Total N, and a quality code.
- Quality fields may follow with 3-figure codes indicating data quality status.
- If sites perform pH/conductivity locally, separate QC preparation dates may be needed; otherwise repeat preparation dates for both sets.
- Example provided for Moor House QC record.

## Priority listing of determinands (sample volume constraints)
- In low rainfall periods, sample volumes are limited; priorities guide analytical options:
  1) pH and conductivity
  2) Cations (Ca2+, Mg2+ first; then K+, Na)
  3) Anions (NO3-, SO4 2-, then PO4 3-, Cl-)
  4) NH4+-N
  5) DOC
  6) Fe2+ and Al3+ (separate acidified portions)
  7) Total N and alkalinity
- Refer to Initial Water Handling Protocol for sample solution handling, filtration, pH, and acidification details.

## Documentation and data provenance
- Details on methodology, changes, validation, and QC are designed to create a traceable data lineage.
- Records enable assessment of data suitability for purpose and detect drift or biases over time.

## Example and governance notes
- Example accuracy record illustrates how results and corrective actions are documented.
- The protocol supports interlaboratory comparability, data quality assurance, and standardized reporting.
- Authorship and governance: coordinated by ECN and Analytical Working Group; ongoing adherence and updates with methodological changes.