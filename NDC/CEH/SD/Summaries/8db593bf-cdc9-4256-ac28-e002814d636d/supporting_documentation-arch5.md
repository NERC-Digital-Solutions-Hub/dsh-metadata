# Elemental and isotopic data of a series of timed exchange experiments between clay, mineral water and seawater NERC Grant NE/T007214/1

## Overview of the dataset
- Datasets cover elemental concentrations (Sr, Mg, Ca) and isotopic compositions from timed exchange experiments among clay, mineral water, and seawater.
- Elemental data were obtained by ICP-OES (Agilent 5100) at the University of Cambridge, using matrix-matched synthetic standards.
- Isotopic data include radiogenic 87Sr/86Sr and stable d88/86Sr, as well as magnesium isotopes (d26/24Mg, d25/24Mg) measured by MC-ICP-MS at Cambridge.
- Standard/reference materials used for quality control include SPS-SW2, SLRS-6 (water-based matrix), BCR-2 (SCO-013a), and LiBOx calibrations; IAPSO standard seawater used as a reference.
- Data presentation includes explicit method details, matrices, and calibration strategies, with associated uncertainties.

## Analytical methods, calibration, and standards
- Elemental measurements:
  - Technique: ICP-OES (Agilent 5100) with matrix-matched standards.
  - Standards: SPS-SW2, SLRS-6; additional standards including a 3.2 BCR-2 (SCO-013a) and LiBOx for matrix corrections.
  - Matrices: water-based and ammonium chloride-based matrices; external standards within specified accuracy.
- Sr isotopes and Sr-related isotopic ratios:
  - Technique: MC-ICP-MS (Thermo Neptune Plus) with Forced Mass Bias Zr-doped EEN.
  - Data treatment: Monte-Carlo simulation to propagate analytical uncertainties into total errors.
  - Reference materials and comparisons: IAPSO Standard seawater used in validation; multiple isotope ratio measurements per variable.
- Magnesium isotopes:
  - Technique: MC-ICP-MS (Thermo Neptune Plus) with Sample-Standard Bracketing.
  - QC: repeats of standards (IAPSO seawater, Cam1) to verify accuracy against published values.
- Data processing notes:
  - For isotopes, large numbers of random draws (n = 1000) based on mean internal precision (2SE) used to derive true sample isotope ratios and total errors.
  - Repeats and internal precision used to report two-standard-deviation (2SD) uncertainties.

## Data quality, uncertainties, and QA/QC
- External standard recoveries and accuracy:
  - Water-based matrix standards within ±5% of certified values.
  - Ammonium chloride-based matrix standards within ±10% of certified values.
- Isotope data uncertainty treatment:
  - Monte-Carlo approach with n = 1000 simulations to quantify total error due to analytical uncertainty.
  - Magnesium isotope measurements reported with 2SD uncertainties from multiple repeats.
- Reported representative results (examples):
  - Sr/Mg/Ca elemental data: values with specified uncertainties and calibration context (example ranges provided in text for standard reference materials).
  - 87Sr/86Sr and d88/86Sr: reported with total uncertainties derived from Monte-Carlo propagation.
  - Mg isotopes (d26/24Mg, d25/24Mg): reported with 2SD uncertainties across multiple repeats (n values vary by standard/case).

## Data provenance, documentation, and accessibility
- Source and location:
  - Analyses conducted at the University of Cambridge.
  - Instrumentation: ICP-OES for elemental data; MC-ICP-MS for Sr and Mg isotopes.
- Documentation included in the dataset:
  - Detailed methods, matrices, standards, calibration approaches, and uncertainty frameworks.
  - Repeats and standard comparisons explicitly described to support reproducibility.
- Data integration considerations:
  - Clear separation of data by measurement type (elemental vs isotopic) and by matrix.
  - Provenance tied to specific standards and reference materials used for QA/QC.

## Data governance, sharing, and metadata considerations for Data Stewards
- Metadata to capture:
  - Instrument model and tuning, method names (ICP-OES, MC-ICP-MS), and sample-bracketing or calibration strategy.
  - Matrix type for each measurement (water-based vs ammonium chloride-based).
  - Standards used (SPS-SW2, SLRS-6, BCR-2, LiBOx, IAPSO), and their certified values or references.
  - Uncertainty methodology (±5% or ±10% acceptance criteria for standards; Monte-Carlo details for isotope data; n values).
  - Replicate counts (n) and reporting of 2SD or other uncertainty metrics.
  - Any data transformations or normalization applied.
- Data quality and accessibility:
  - Ensure data are stored with links to the corresponding QA/QC materials and reference standards.
  - Maintain versioning and provenance trails for method updates or reprocessing.
  - Provide clear documentation on matrix effects and any corrections applied to account for matrix differences.
- Potential reuse considerations:
  - Matrix-specific calibration and standard selections may affect cross-study interoperability; include matrix metadata to enable correct cross-comparison.
  - Large datasets and multiple formats may require explicit data dictionaries to ensure interoperability and discoverability.

## Challenges and considerations for Data Stewards
- Incomplete picture of user needs and priorities may complicate data curation; align metadata with typical user queries (e.g., isotope ratios, standard corrections, matrix effects).
- Data transfer and interoperability across different matrices and standard materials (water-based vs ammonium chloride-based) require careful metadata and normalization rules.
- Handling and storing large numbers of derived errors (Monte-Carlo propagated uncertainties) and multiple repeats necessitate consistent data schemas and clear documentation.