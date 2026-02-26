# WAG Protocol

## Overview
- Provides guidelines for analysis of water samples from ECN terrestrial sites.
- Laboratories must conduct analyses under controlled conditions and document methodology, significant methodological changes, and validation procedures.
- Analytical procedures are reviewed annually by an Analytical Working Group with representatives from each laboratory.

## Data governance and metadata
- Laboratories should retain detailed methodology and provide summary information for the ECN database.
- For each determinand at each ECN site, a single data record should exist in the meta database, linking by site, core measurement, determinand, and date to indicate the active methodology and its precision.
- Records capture the rationale for changes and indicate suitability for the data’s intended use.

## Methodology documentation and versioning
- Any methodological change earns a new database record with a date stamp.
- Laboratories control instrument maintenance, calibration, drift, and staff training; changes are documented and assessed for data suitability.
- A separate, documented procedure exists for inter-site and within-site method comparisons to maintain consistency.

## Data quality and validation
- Accuracy and precision are the two core quality measures.
- Accuracy is assessed via participation in external controls (e.g., AQUACHECK) and recorded alongside results, including any corrective actions.
- Precision is monitored using quality control (QC) samples; unacceptable QC results prevent data submission.
- Interlaboratory comparisons and ongoing QC help identify trends and ensure long-term data reliability; corrective actions and data corrections are documented.

## Standard methods and comparability
- A list of approved techniques and reference techniques governs determinations; laboratories may use alternatives but must monitor for bias and report the fraction measured.
- For reporting, data should reflect the specified fraction (e.g., NO3- as nitrate) unless bias checks show equivalence between methods; labs must monitor alternative techniques to confirm absence of bias.

## Data transfer and metadata schema
- Method details are kept at the laboratory and summarized for the ECN database; includes basis of method, sample types, typical concentrations, calibration ranges, and detection limits.
- Documentation supports cross-site comparisons by standardizing reporting formats and definitions.
- Laboratories must report data on the specified fraction and provide method details and detection limits to enable proper interpretation.

## Priority data handling and sample management
- When sample volumes are limited, a priority sequence guides analytical options:
  - 1) pH and conductivity
  - 2) Cations (Ca2+, Mg2+, then K+, Na+) and anions (NO3-, SO4 2-, PO4 3-, Cl-)
  - 3) NH4+-N
  - 4) Metals requiring special handling (e.g., Fe2+, Al3+)
  - 5) DOC
  - 6) Total N and alkalinity
- Guidance references the Initial Water Handling Protocol for sample handling, filtration, pH adjustment, and acidification.

## Practical actions for Data Stewards
- Ensure datasets include comprehensive metadata: method name, reference technique, detection limits, calibration ranges, sample types, and date stamps for changes.
- Verify documentation of methodology updates and ensure linkage to data records in the ECN meta database.
- Confirm participation in interlaboratory checks (e.g., AQUACHECK) and ensure accuracy/precision results are stored with data.
- Manage QC data: require lab-submitted QC results, and maintain the QC data in a standardized transfer format.
- Monitor data lineage and provide traceability from raw data through analysis to final reported values, including any corrective actions.

## Appendix: QC data transfer format (highlights)
- QC data are transferred as free-format, comma-separated records per batch, containing fields such as:
  - Measurement code (QC)
  - Site ID, local QC sample code, preparation dates, analysis dates
  - pH (AQC Unstirred and Stirred), Conductivity, Alkalinity, major ions (Na, K, Ca, Mg, Fe, Al, Cl, NO3-N, NH4-N, PO4-P, SO4-S), DOC, Total N
  - Quality codes and any subsequent quality indicators
- Example records illustrate the exact field order and the need to include preparation/analysis dates and quality codes.

## Endnotes
- An example of a Moor House QC record demonstrates the data format and the inclusion of accuracy checks and quality codes for traceability.