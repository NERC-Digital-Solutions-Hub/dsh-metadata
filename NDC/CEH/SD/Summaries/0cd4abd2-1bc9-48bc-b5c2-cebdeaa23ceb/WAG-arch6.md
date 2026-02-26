# ANALYTICAL GUIDELINES FOR WATER SAMPLES Version 1.1 (previously AG Protocol, updated Jan 2001)

## Overview
- Guidelines for analysis of water samples from ECN terrestrial sites.
- Labs are responsible for controlled analyses and must document methodology, changes, and validation procedures.
- Annual review by an Analytical Working Group; methods include defined detection limits as targets.

## Governance and responsibilities
- Each laboratory manages its own resources while adhering to standardized guidelines.
- Documentation of significant methodological changes and validation procedures is required.
- Data and methodology details are recorded for the ECN database and are subject to a stamped versioning process when changes occur.

## Approved and reference techniques
- Determinands and corresponding approved techniques (examples):
  - pH, Conductivity
  - Cations: Na+, K+, Ca2+, Mg2+
  - Anions: Cl−, NO3−, SO4 2−, PO4 3−
  - NH4+ N, Al3+, Fe2+
  - DOC (Total Organic Carbon)
  - Total N, Alkalinity
- Techniques include FES/AAS, ICP/OES, IC, Col- (colorimetric) methods, and others; notes indicate when species-specific quantification is direct or indirect.
- Reference techniques are specified with standardized descriptions, detection limits, and species of interest.
- Laboratories must report data against the specified fractions; if alternative techniques are used, bias must be checked via monitoring of both methods.

## Priority listing of determinands (sample-volume management)
- In low rainfall periods, a priority order guides analytical options:
  1. pH and conductivity
  2. Cations (Ca2+, Mg2+ first; then K+, Na+)
  3. Anions (NO3−, SO4 2−; then PO4 3−, Cl−)
  4. NH4+ N
  5. DOC
  6. Total N and alkalinity
  7. Cations requiring acidified portions (Fe2+, Al3+)
- Refer to the Initial Water Handling Protocol for sample handling, filtration, pH, and acidification.

## Data and metadata management
- Method details are kept by each laboratory; a summary is provided to the ECN database.
- Data records: one per determinand per ECN site, linking site, core measurement, determinand, date, methodology, and precision.
- Example data record (nitrate) illustrates fields such as site, determinand, method, sample types, calibration range, volume for analysis, detection limit, and QC measures.

## Validation, accuracy, and precision
- Validation through approved techniques, standardized detection limits, and internal QC.
- Participation in interlaboratory schemes (e.g., AQUACHECK) to assess accuracy.
- Two main quality measures: accuracy (closeness to true value; cross-lab agreement) and precision (repeatability across batches).
- Accuracy records include element, fraction, date, method, laboratory, interlaboratory scheme, mean, result, and corrective actions if needed.

## Quality control procedures
- ECN-specific QC system: labs continue independent QC validation and may join accredited interlaboratory exchanges.
- Potential to compute between-site correction factors; monitor for rogue batches and long-term analytical trends.
- Preparation and use of QC solutions (two concentrates for cation and anion analyses) distributed annually to sites; dilution and preparation steps outlined.
- QC data submission: free-form, comma-separated data records submitted to the ECN CCU; fields include preparation dates, analysis dates, pH measurements, conductivity, alkalinity, major ions, DOC, Total N, and quality codes.
- Example QC record provided (Moor House) with fields for measurement code, site, QC sample code, preparation dates, analysis dates, results for multiple determinands, and quality codes.

## Data transfer and documentation format
- QC data must be formatted consistently with water-sample data records; includes both anion and cation results per batch.
- Data fields specify measurement codes, site IDs, QC codes, preparation dates, analysis dates, individual determinand results, and quality indicators.
- Notes cover handling when pH and conductivity are measured locally versus at the analytical lab (date fields may be repeated).

## Recordkeeping and change management
- Laboratories must maintain detailed methodological records for operators.
- Any methodological changes generate new dated records in a meta-database.
- Data ranges and detection limits are standardized to ensure comparability across sites and over time.

## Example and notes
- The document includes an accuracy-record example and guidance on the data reporting format, including field specifications and quality codes.
- For pH measurements in low ionic strength waters, use methods capable of quantifying such solutions with proper reference electrodes.