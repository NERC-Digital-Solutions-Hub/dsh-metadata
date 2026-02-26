# WAG Protocol

## Overview
- Analytical guidelines for water samples from ECN terrestrial sites.
- Labs are responsible for controlled analyses, documentation of methodology and changes, and validation procedures.
- Analytical procedures reviewed annually by an Analytical Working Group.
- Detection limits serve as targets and guidance for method selection.

## Scope and Governance
- Applicable to ECN laboratories; annual review by an Analytical Working Group with representatives from each lab.
- Laboratories must document methodology changes and validation procedures.
- Results should be comparable across sites through standardized methods and reporting.

## Approved Techniques and Determinands
- pH and conductivity (with specified references) and a suite of ions and constituents.
- Examples of determinands: Na+, K+, Ca2+, Mg2+, Fe2+, Al3+, NH4+-N, Cl-, NO3--N, SO42-, HCO3-, PO4 3-, DOC, Total N, alkalinity.
- Multiple approved techniques are listed; some are reference methods. Techniques may quantify related species; comparative tests recommended when non-targeted fractions are used.
- Laboratories should report data for the specified fraction and monitor alternative methods to check for bias.

## Reference Techniques and Bias Checks
- Reference methods provided for comparison as new analytical technologies emerge.
- If alternatives are used, laboratories must monitor dual techniques to assess potential bias.
- Reporting includes the specific fraction measured and the reference technique.

## Data Quality, Detection Limits, and Ranges
- Uniform detection limits and accuracy/precision emphasis.
- If results approach the detection limit, consider re-analysis with a lower analytical range.
- Defined limits help ensure uniformity across laboratories.

## Priority Determinands (Volume-Limited Scenarios)
- When sample volumes are restricted, follow a priority order:
  1) pH and conductivity
  2) Cations (Ca2+, Mg2+; then K+, Na+) and anions (NO3-, SO4 2-, then PO4 3-, Cl-)
  3) NH4+-N
  4) Transition metals requiring separate aliquots (Fe2+, Al3+)
  5) DOC
  6) Total N and alkalinity
- Refer to the Initial Water Handling Protocol for sample handling specifics.

## Methodology Documentation and Meta-Database
- Laboratories keep detailed method records locally; a summary is stored in the ECN meta-database.
- Each determinand-site-date combination has a data record detailing methodology, accuracy, calibration, and typical concentrations.
- Example format provided (nitrate) to illustrate data capture and provenance.

## Validation: Accuracy and Precision
- Validation via accuracy (closeness to true value) and precision (repeatability).
- Participation in interlaboratory checks (e.g., AQUACHECK) encouraged.
- Accuracy records include element, fraction, lab, method, date, results, mean, and percentage relative error, with corrective notes when applicable.

## Quality Control Procedures
- Separate ECN QC system in addition to site-specific QC.
- Labs should pursue independent QC validation and interlaboratory exchanges.
- Potential to compute between-site correction factors if solutions and procedures align.
- Annual QC solution distribution (two concentrated QC solutions for cations and anions), with end-of-year preparation and continuity checks.
- QC data must be submitted in the ECN data framework, aligned with sample data records.

## Data Transfer and Metadata Format
- QC data submitted to the ECN CCU in the same structure as water samples, with adjusted date fields.
- Data record structure includes: measurement code, site ID, QC sample code, preparation dates, analysis dates, pH (unstoned and stirred), conductivity, alkalinity, and concentrations for determinands (Na, K, Ca, Mg, Fe, Al, PO4-P, NO3-N, NH4-N, Cl, SO4-S, DOC, Total N), followed by quality codes.
- Includes a Quality code field for additional flags as needed.

## Example Records
- Example Moor House QC record demonstrates the format and fields for documenting QC results, dates, measured values, and quality status.

## GIS-Specific Implications
- Ensures cross-site data comparability through standardized methods, detection limits, and QA/QC practices.
- Metadata captures method, calibration ranges, fractions measured, detection limits, units, and quality codes, enabling reliable spatial analyses.
- Data in a centralized ECN meta-database with traceable methodology supports consistent map-based visualization of water chemistry across sites.
- Priority handling guidance informs where data gaps may occur in volume-limited field campaigns, affecting spatial interpolation and risk assessments.