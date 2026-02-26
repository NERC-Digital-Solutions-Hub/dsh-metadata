# A large-scale field experiment to quantify the impacts of neonicotinoid (NNI) seed dressings on honeybees in the UK, Germany and Hungary

## Overview
- Large-scale field study across the UK, Germany, and Hungary to quantify effects of neonicotinoid seed dressings on honeybees.
- Target compounds: Thiamethoxam (TMX) and Clothianidin (CLO).
- Objective includes determining concentrations in hive products: nectar, honey, pollen, and wax.
- Analytical workflow employs LC-MS/MS with isotope-labelled internal standards; method validated for sensitivity and reliability.
- Key performance metrics: LOD ~0.4 ng/g and LOQ ~0.6 ng/g; expanded uncertainty ~40%; recoveries ~83–92% depending on matrix.
- Ensures data traceability, quality control, and cross-site methodological consistency to support robust comparisons across countries.

## Analytical workflow by matrix
- Nectar and honey
  - Sample prep: 0.1 g, spike with labelled internal standards (TMX-D4, CLO-D3, QMX).
  - Extraction: 2 mL of 50:50 methanol:water, vortex, centrifuge.
  - Workflow: take 1 mL aqueous layer, adjust with water, mix, and proceed to cleanup.
  - Cleanup: Oasis HLB SPE cartridge (60 mg, 3 mL), conditioned with methanol then water; dried under vacuum; hexane added and dried; eluted with 6 mL acetonitrile.
  - Final prep: dry extracts, re-dissolve in 1 mL mobile phase (95% A, 5% B), inject.
- Pollen and wax
  - Sample prep: 0.1 g, spike with labelled internal standards (TMX-D4, CLO-D3, QMX).
  - Extraction: 1 mL of 80:20 hexane:isopropanol, brief vortex, heat bath at 45°C for 15 minutes with mixing.
  - Additions: 1.8 mL of 50:50 methanol:water, vortex; centrifuge; take 1 mL aqueous layer.
  - Cleanup: Oasis HLB SPE cartridge as above; elute with acetonitrile; dry and re-dissolve in mobile phase as above.

## Chromatography and mass spectrometry (LC-MS/MS)
- Instrumentation: Liquid chromatography coupled to a triple quadrupole mass spectrometer (Thermo TSQ) with ESI in positive mode.
- Column: Phenomenex Synergi Fusion (2.5 µm, 50 mm × 2 mm ID).
- Mobile phase: A = water with 0.1% acetic acid; B = methanol with 0.1% acetic acid.
- Gradient: 95% A to 50% B over 15 min, then to 100% B, then return to starting conditions.
- Detection: SRM with two characteristic fragments for each analyte; data processed with Xcalibur software.
- Parameters optimized for robust quantification and confirmation of analyte identity.

## Quantification and calibration
- Quantification strategy: use response factors relative to internal standards; construct calibration curves with 1/X weighting.
- Calibration metrics: at least 5 standards; linearity with R² > 0.99 between ND (not detected) and 2.5 ng/mL.
- Quality checks: injections of standards and blanks to ensure linearity and stability.

## Method performance
- Linearity: demonstrated across the calibration range with high correlation.
- Sensitivity: LOD 0.4 ng/g and LOQ 0.6 ng/g for the full procedure.
- Uncertainty: expanded uncertainty of 40% (based on Nordtest framework for measurement uncertainty).
- Recoveries: nectar/honey TMX-D4 ~91.3% ± 7.2; CLO-D3 ~89.7% ± 7.2; pollen TMX-D4 ~83.5% ± 8.2; CLO-D3 ~82% ± 10.1.

## Quality control and assurance
- Systematic QC measures:
  - Blanks: solvent blanks and matrix-matched blanks to monitor contamination/carryover for each batch (≤16 real samples per batch).
  - Mobile phase blanks injected every four samples to guard against carryover.
  - In-house QC: matrix-free honey/pollen/wax spiked with TMX and CLO from a different source.
  - Traceable external standards: NIST-certified CLO and TMX standards analyzed periodically.
  - Blind analysis: samples analyzed without treatment labels; identities confirmed by comparing MRM transition ratios against pure standards.
- Data integrity: double-checks on analyte identities and quantification to ensure reliability of results.

## Data governance and data-leader considerations
- Emphasis for Data Leaders on:
  - Standardization across sites to enable cross-country comparisons (consistent sample handling, extraction, cleanup, LC-MS/MS settings, and data processing).
  - Detailed metadata capture (matrices, extraction conditions, instrument parameters, calibration ranges, QC results, and internal standards used).
  - Traceability and documentation of QA/QC procedures, including LOD/LOQ, recoveries, and uncertainty calculations.
  - Blinding procedures to minimize bias and ensure objective data interpretation.
  - Regular cross-site calibration checks and verification against certified references to maintain data quality and comparability.
  - Data lifecycle considerations: storage of raw and processed data, versioning of methods, and clear audit trails for reproducibility.

## References
- Nordtest 537: Handbook for calculation of measurement uncertainty in environmental laboratories.
- Additional method-specific references include internal standards (TMX-D4, CLO-D3, QMX) and instrument-specific calibration and quality practices.