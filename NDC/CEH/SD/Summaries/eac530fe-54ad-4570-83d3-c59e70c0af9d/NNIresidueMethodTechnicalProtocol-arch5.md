# A large-scale field experiment to quantify the impacts of neonicotinoid (NNI) seed dressings on honeybees in the UK, Germany and Hungary

## Overview
- Objective: quantify neonicotinoid concentrations (Thiamethoxam and Clothianidin) in honeybee hive products (nectar, honey, pollen, wax) using LC-MS-MS.
- Study scope: UK, Germany, Hungary; method provides set performance metrics and quality controls.

## Analytical workflow and matrices
- Matrices and extraction:
  - Nectar and honey: 0.1 g; internal standards TMX-D4, CLO-D3, QMX; 50:50 methanol:water extraction; vortex, centrifuge; process aqueous layer.
  - Pollen and wax: 0.1 g; same internal standards; hexane:isopropanol 80:20 extraction; heat in water bath; add 50:50 methanol:water; vortex; centrifuge; process aqueous layer.
- Cleanup:
  - Oasis HLB SPE (60 mg, 3 mL); condition with methanol then water; dry, elute with 6 mL acetonitrile.
- Reconstitution and analysis:
  - Dry extracts, re-dissolve in 1 mL mobile phase (95% A, 5% B); inject into LC-MS-MS.

## Instrumentation and method parameters
- Instrumentation: LC-MS-MS with Thermo TSQ Quantum Ultra TSQ, ESI, Xcalibur software.
- Chromatography: Phenomenex Synergi Fusion column (2.5 µm, 50 mm × 2 mm); gradient of water with 0.1% acetic acid (A) and methanol with 0.1% acetic acid (B).
- Gradient and operation: starts 95% A / 5% B, ramps to 50% B in 15 min, to 100% B in 5 min, back to 5% B and hold.
- MS/MS: SRM in positive mode; monitoring two characteristic fragments per analyte for quantification; internal standards used for correction.
- Optimization: spray voltage 3000 V; other injection and MS parameters as detailed (e.g., temperatures, gas settings).

## Calibration, quantification, and performance
- Calibration: linear range from ND to 2.5 ng/mL using at least 5 standards; 1/X weighting; R^2 > 0.99.
- Linearity and quantification: established across procedures with internal standards; quantification based on response factors to deuterated internal standards.
- Method performance:
  - LOD: 0.4 ng/g; LOQ: 0.6 ng/g for the entire procedure.
  - Expanded method uncertainty: 40%.
  - Recoveries (overall procedure):
    - Nectar/Honey: TMX-D4 91.3% ± 7.2; CLO-D3 89.7% ± 7.2.
    - Pollen: TMX-D4 83.5% ± 8.2; CLO-D3 82% ± 10.1.

## Quality control and assurance
- Controls used: blank solvent, matrix blanks; mobile phase blanks every four samples to detect carryover.
- In-house QC: neonicotinoid-free honey, pollen, wax spiked with native TMX and CLO (from Sigma) to mirror sample analysis.
- Traceability: inclusion of a traceable NIST-certified standard (CLO and TMX) analyzed periodically (every 8–10 samples) to monitor retention times and instrument sensitivity.
- Verification: blind analysis of samples; confirmation by comparing MRM transition ratios to standards.

## Data stewardship and documentation implications
- Metadata to capture for datasets:
  - Sample type, matrix, extraction and cleanup procedures, solvents, SPE conditions, LC-MS-MS settings, gradient profile, column information.
  - Calibration curves, standards used, LOD/LOQ, linear range, recovery figures, internal standard details, QC results, blanks, and NIST standard runs.
  - Documentation confirming blind analysis, retention times, and transition ratio verifications.
- Data quality indicators to report:
  - Recovery rates by matrix and analyte, calibration performance (R^2), LOD/LOQ, expanded uncertainty, and QC outcomes.
- Provenance and traceability:
  - Link measurements to specific samples, batches, and instrument conditions; maintain records of QA steps and any deviations.

## Considerations and limitations for data users
- Matrix-dependent recoveries indicate variability across nectar/honey vs. pollen.
- Quantitative range is linear up to 2.5 ng/mL; extrapolations beyond require caution.
- Uncertainty is substantial (approx. 40%), emphasizing the need for robust QC data and transparent metadata.

## References
- Nordtest report 537. Handbook for calculation of measurement uncertainty in environmental laboratories. Nordic Innovation.