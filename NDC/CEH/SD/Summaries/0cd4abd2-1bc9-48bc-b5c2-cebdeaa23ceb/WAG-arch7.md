# ANALYTICAL GUIDELINES FOR WATER SAMPLES Version 1.1 (previously AG Protocol, updated Jan 2001)

## Overview
- Guidelines for analyzing water samples from ECN terrestrial sites.
- Laboratories are responsible for controlled analyses and must document methodology, changes, and validation procedures.
- Procedures reviewed annually by an Analytical Working Group.
- Approved techniques and reference methods provided; detection limits set as targets.
- Emphasis on data provenance, metadata, and consistency across sites for GIS-based mapping.

## Methodology and Determinands
- Determinands covered include pH, conductivity, major cations (Na, K, Ca, Mg), trace elements (Fe, Al), nitrogen forms (NH4-N, Total N), anions (Cl, NO3-N, SO4-S, PO4-P), alkalinity, DOC, and others.
- Each determinand has a set of approved alternatives; reference techniques are listed (e.g., AAS, IC, ICP/OES, colorimetry).
- Some determinations are reported in specific fractions (e.g., NO3-N, SO4-S) and/or require specific preparation (acidified samples, blanks).
- For pH and conductivity, additional guidance appears in the Initial Water Handling Protocol.
- Laboratories may use alternative techniques but must monitor for bias against ECN reference values if different fractionations are used.

## Data Provenance, Metadata, and Data Structure
- For ECN database purposes: one data record per determinand per site, linked to site, core measurement, determinand, and date.
- Each record includes methodology details and precision, enabling traceability and reproducibility in GIS analyses.
- Changes in methodology are timestamped with new database records to preserve a complete history.
- Documentation supports data quality assessments and potential cross-site corrections.

## Measurement Details, Ranges, and Units
- Results are reported with standardized units (e.g., mg/L, µS/cm, mg/L as certain species, CaCO3 for alkalinity).
- Fractions and species of interest specified (e.g., NO3-N vs NO3, SO4-S vs SO4).
- Typical concentrations, calibration ranges, and detection limits are defined within method records.
- When detection limits are near analytical range, laboratories should assess data suitability or re-analyse with appropriate ranges.

## Validation, Accuracy, and Precision
- Validation relies on: approved techniques, uniform detection limits, and internal QC; participation in interlaboratory schemes (e.g., AQUACHECK).
- Accuracy: closeness to true value and agreement across laboratories; results tracked over time, with corrective actions if biases are detected.
- Precision: assessed via synthetic QC solutions; batches flagged if QC values indicate unacceptable performance.
- Sites may compute between-site correction factors under a centralized QC framework.

## Quality Control (QC) and Interlaboratory Comparison
- A dedicated QC system supports site-level and cross-site data quality checks.
- Routine interlaboratory comparisons are encouraged but not a fixed requirement; independent QC validation is supported.
- QC procedures include preparing concentrated QC solutions (two sets for cations and anions), periodic continuity checks, and documenting QC results.
- QC data are transferred to the ECN Central Coordinating Unit (CCU) in a specified free-format, comma-separated dataset, with fields for preparation dates, analysis dates, measurement results, and quality codes.
- The protocol enables detection of rogue batches and long-term analytical trends.

## Data Transfer, Metadata, and QC Data Format
- QC data must be submitted in a standardized format with precise fields (site ID, preparation dates, analysis dates, measured values for each determinand, and quality codes).
- A single QC data record covers both anion and cation results per batch.
- Example records and field layouts are provided to ensure consistency across sites and over time.

## Practical Implications for GIS Data Products
- Data fed into GIS should carry rich metadata: determinand, date, site, measurement method, detection limits, units, and fraction specification.
- Data quality flags (from accuracy, precision, and QC results) are essential for reliable thematic mapping and trend analyses.
- The ability to compute site-to-site correction factors requires consistent methodology records and historical QC data.
- Changes in analytical methods must be tracked to avoid misinterpretation when visualizing time-series data.
- Users should be aware of potential biases when alternative techniques are used and rely on documented bias checks.

## Example and Records
- Example accuracy record demonstrates reporting format and bias assessment mechanisms (e.g., SO4 2- measured by ion chromatography; documentation of mean, mean error, and corrective measures).
- Example QC record (Moor House) outlines the structure of a complete QC submission, including dates, results, and quality codes.

## Authors and Revision
- Key contacts: A.P. Rowland, C. Woods, M. Lane.
- Version history and revisions are captured with each methodology change to ensure traceability in the ECN database.