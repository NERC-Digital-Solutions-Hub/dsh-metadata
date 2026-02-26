# A large-scale field experiment to quantify the impacts of neonicotinoid (NNI) seed dressings on honeybees in the UK, Germany and Hungary

## Objective and scope
- Large-scale, multi-country field study (UK, Germany, Hungary) to quantify the impacts of neonicotinoid seed dressings on honeybees.
- Focus on determining concentrations of neonicotinoids in pollinator hive products (nectar, honey, wax, pollen) using LC-MS/MS.
- Emphasis on rigorous method development, validation, and quality control to ensure data reliability for comparative assessment across sites.

## Analytical method overview
- Target analytes: Thiamethoxam (TMX) and Clothianidin (CLO).
- Sample types and extraction:
  - Nectar and honey: homogenised, 0.1 g samples; spiked with labelled internal standards (TMX-D4, CLO-D3, QMX); extraction with 50:50 methanol:water; vortexing, centrifugation, and cleanup.
  - Pollen and wax: 0.1 g samples; extraction with 80:20 hexane:isopropanol; heating and vortexing; addition of 50:50 methanol:water; centrifugation and cleanup.
- Cleanup and concentration:
  - Oasis HLB SPE cartridges (60 mg, 3 mL) with conditioning, drying, hexane evaporation, and elution with 6 mL acetonitrile.
  - Evaporation to dryness and re-dissolution in 1 mL mobile phase (95% A / 5% B) for LC-MS/MS.
- Instrumentation and settings:
  - LC-MS/MS: Thermo TSQ Quantum Ultra TSQ with ESI, Xcalibur software.
  - Column: Phenomenex Synergi Fusion (2.5 µm, 50 mm × 2 mm ID).
  - Mobile phases: A = 0.1% acetic acid in water; B = 0.1% acetic acid in methanol; gradient from 95% A to 100% B and back.
  - MS/MS in SRM mode (positive ESI) with two characteristic fragments per compound.
  - Optimized: spray voltage ~3000 V, capillary ~300°C, collision gas Argon, desolvation gas nitrogen.
- Quantification and calibration:
  - Use response factors relative to deuterated internal standards.
  - Calibration with at least 5 standards; linearity assessed with 1/x weighting; R² > 0.99.
  - Quantification limits: linear range from ND to 2.5 ng/mL.
- Quality control and assurance:
  - QC samples: blanks (solvent and matrix-matched) to monitor contamination; mobile phase blanks every four injections to check carryover.
  - In-house QC materials: neonicotinoid-free honey, pollen, and wax spiked with known TMX and CLO amounts (origin different from calibration standards).
  - Traceable standards: periodic analysis of NIST-certified CLO and TMX standards.
  - Blinding: samples analysed blind to treatment; identities confirmed by comparing MRM transitions with pure standards.
  - Data integrity: identities confirmed by retention time and MRM transition ratios; double-checked results.
- Method performance and uncertainty:
  - LOD for the entire procedure: 0.4 ng/g; LOQ: 0.6 ng/g.
  - Expanded method uncertainty: 40% (based on Nordtest guidance).
  - Recoveries (current batch performance):
    - Nectar/honey: TMX 91.3% ± 7.2; CLO 89.7% ± 7.2.
    - Pollen: TMX 83.5% ± 8.2; CLO 82% ± 10.1.
- Data handling and analysis:
  - Peaks integrated with ICIS algorithm in Xcalibur for calibration and quantification.
  - Identities confirmed by comparing sample ratios of MRM transitions to those of standards.
  - Samples analysed in a blinded, quality-controlled workflow with routine checks for retention time drift and instrument sensitivity.
- Project governance:
  - Conducted under NERC Centre for Ecology and Hydrology project NEC05367.

## Data quality, provenance, and reproducibility implications
- Comprehensive QA/QC framework ensures traceability and contamination control across matrices and sites.
- Use of isotopically labelled internal standards enables accurate compensation for matrix effects and variable recoveries.
- Detailed methodological documentation (sample prep, LC-MS/MS conditions, calibration strategy) supports reproducibility and inter-lab comparability.
- Incorporation of blanks, matrix blanks, mobile phase blanks, and NIST standards strengthens data reliability and auditability.
- Quantification outcomes include explicit performance metrics (LOD/LOQ, recoveries, R²), enabling transparent uncertainty assessment.

## Key data-centric takeaways for data leaders
- End-to-end data lifecycle: from sample collection across multiple matrices to LC-MS/MS data processing, with rigorous QC and traceability at each step.
- Standardization across sites: consistent extraction, cleanup, and analytical protocols to enable cross-site comparisons.
- Metadata and provenance: explicit reporting of internal standards, calibration ranges, MRM transitions, and instrument settings to support re-analysis and validation.
- Uncertainty and quality metrics: documented measurement uncertainty (40%), LOD/LOQ, and recovery data to inform interpretation and policy decisions.
- Reproducibility and governance: blinded analyses, cross-checks, and alignment with recognized uncertainty standards (Nordtest) to support robust evidence for regulatory or environmental decision-making.