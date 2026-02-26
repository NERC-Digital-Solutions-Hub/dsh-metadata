# Elemental and isotopic data of a series of timed exchange experiments between clay, mineral water and seawater NERC Grant NE/T007214/1

## Overview
- Presents elemental (Sr, Mg, Ca) and isotopic (Sr and Mg) data from a series of timed exchange experiments involving clay, mineral water, and seawater.
- Documents measurement methods, calibration standards, and uncertainty assessments to support data reliability and potential reuse in environmental health monitoring.

## Data types and measurement methods
- Elemental data
  - Elements: Strontium (Sr), Magnesium (Mg), Calcium (Ca)
  - Method: ICP-OES (Agilent 5100)
  - Matrix-matched standards used for calibration spanning sample concentration ranges
  - External standards:
    - SPS-SW2 and SLRS-6 for water-based matrices (within ±5% of certified values)
    - SPS-SW2, SLRS-6, and a 3.2 BCR-2 standard for ammonium chloride matrix (within ±10% of certified values)
- Strontium isotope data (87Sr/86Sr and d88/86Sr)
  - Method: MC-ICP-MS Thermo Neptune Plus
  - Technique: Forced Mass Bias Zr-dope EEN
  - Uncertainty assessment: Monte-Carlo simulation with 1000 iterations using mean internal precision (2SE) to propagate errors
  - Reference materials and values: IAPSO Standard seawater (0.709186 ± 0.000008, 2SD, n=9)
  - Reported total errors derived from simulated isotope-ratio distributions
- Magnesium isotope data (d26/24Mg and d25/24Mg)
  - Method: MC-ICP-MS Thermo Neptune Plus
  - Technique: Sample-Standard-Bracketing
  - Uncertainty assessment: Two standard deviations from at least three repeat analyses
  - Standards: Repeat analyses of IAPSO seawater and Cam1; results compared to published values
  - Reported values (examples):
    - d26/24Mg: −0.79 ± 0.07 (2SD, n=5)
    - d25/24Mg: −2.59 ± 0.12 (2SD, n=3)
    - Additional Mg isotopic values: −0.41 ± 0.05 (2SD, n=5) and −1.33 ± 0.09 (2SD, n=3)

## Uncertainty, QA/QC, and data integrity
- Uncertainty propagation
  - Sr isotopes: Monte-Carlo approach with 1000 random sets per variable to estimate true sample ratios and total errors
  - Mg isotopes: multiple repeat analyses underpin two-standard-deviation uncertainty estimates
- Quality assurance
  - Use of matrix-matched external standards to ensure accuracy across different sample matrices
  - Replicate analyses and reporting of 2SD to convey precision
  - Calibration against certified reference materials (SPS-SW2, SLRS-6, BCR-2) to validate measurements
- Data interpretation
  - Clear documentation of analytical uncertainty supports robust comparison across samples and potential integration into broader monitoring datasets

## Data handling and governance (as described)
- Explicit metadata and procedural detail provided for each measurement type (instruments, standards, matrices, and corrective approaches)
- Emphasis on transparency of QA/QC practices and uncertainty analyses to enable reproducibility
- The document focuses on data generation and uncertainty assessment; it does not specify data-sharing policies, but metadata richness and reference materials support potential future sharing and verification

## Implications for environmental monitoring frameworks
- Demonstrates rigorous QA/QC and uncertainty quantification essential for monitoring datasets used in policy evaluation and decision-making
- Highlights the importance of:
  - Matrix-specific calibration and validation with appropriate standards
  - Robust uncertainty propagation (e.g., Monte Carlo for isotopic data)
  - Replication and standardization across laboratories to ensure data comparability
- Provides a model for integrating elemental and isotopic measurements with quantified uncertainties to inform environmental health assessments and monitoring strategies

## Key references and standards used
- Standards and reference materials:
  - SPS-SW2
  - SLRS-6
  - BCR-2
  - IAPSO Standard seawater
- Instrumentation:
  - ICP-OES (Agilent 5100)
  - MC-ICP-MS (Thermo Neptune Plus)
- Analytical approaches:
  - Matrix-matched calibration
  - Bracketing technique for Mg isotopes
  - Monte-Carlo error propagation for Sr isotopes