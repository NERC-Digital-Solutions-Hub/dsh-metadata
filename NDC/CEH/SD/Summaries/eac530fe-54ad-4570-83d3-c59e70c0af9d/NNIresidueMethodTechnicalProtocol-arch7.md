A large-scale field experiment to quantify the impacts of neonicotinoid (NNI) seed dressings on honeybees in the UK, Germany and Hungary

## Objective and study scope
- Large-scale field experiment across the UK, Germany and Hungary to quantify the impacts of neonicotinoid seed dressings on honeybees.
- Focus on measuring neonicotinoid concentrations in key insect pollinator hive products: nectar, honey, pollen and wax.

## Data collection and sample types
- Matrix types: nectar, honey, pollen, and wax samples collected for analysis.
- Sample preparation:
  - Nectar/honey: 0.1 g wet samples spiked with labelled internal standards (Thiamethoxam-D4, Clothianidin-D3, QMX); extraction with 50:50 methanol–water; centrifugation; cleanup.
  - Pollen/wax: 0.1 g wet samples spiked with labelled internal standards; extraction with hexane/isopropanol; heating and vortexing; addition of methanol–water; centrifugation; cleanup.
- Cleanup and concentration:
  - Oasis HLB cartridges used for solid-phase extraction (SPE).
  - Elution with acetonitrile; evaporation to dryness; re-dissolution in mobile phase.

## Analytical method (LC-MS/MS)
- Instrumentation: LC-MS/MS with a triple quadrupole system (Thermo TSQ) with ESI; data processing with Xcalibur.
- Chromatography: Phenomenex Synergi Fusion column; gradient of water with 0.1% acetic acid (A) and methanol with 0.1% acetic acid (B); detailed gradient program.
- Detection: Single reaction monitoring (SRM) in positive ESI mode; two characteristic fragments per compound for quantification.
- Parameters: optimized spray voltage, temperatures, and gas settings; internal standards used for quantification.

## Calibration, quantification, and linearity
- Quantification approach: internal standards (deuterated analogues) for TMX and CLO; response factors calculated relative to internal standards.
- Calibration: linear calibration with 1/x weighting; at least 5 standards; R² > 0.99.
- Quantification range: linear from non-detect (ND) to 2.5 ng/mL.

## Performance metrics and validation
- Limits of detection/quantification:
  - LOD: 0.4 ng/g for the entire procedure.
  - LOQ: 0.6 ng/g.
  - Expanded uncertainty (method): 40%.
- Recoveries:
  - Nectar/honey: TMX 91.3% ± 7.2; CLO 89.7% ± 7.2.
  - Pollen: TMX 83.5% ± 8.2; CLO 82% ± 10.1.
- Batch processing: analyses batch contains up to 16 real samples.
- Quality control and assurance:
  - Regular blanks (solvent, matrix-matched), mobile phase blanks every ~4 samples to check carryover.
  - In-house QC material prepared from neonicotinoid-free honey/pollen/wax spiked with known TMX and CLO, with different material origin than calibration standards.
  - Traceable NIST-certified standards analyzed periodically (every 8–10 samples) to monitor retention times and instrument sensitivity.
  - Blind analysis: samples analyzed without treatment labels; double-checking identifications and quantifications via MRM transitions.
  
## Data handling, documentation, and provenance
- Documentation of methodology and performance metrics (LOD/LOQ, recoveries, calibration details, QC procedures).
- Traceability ensured through internal standards, matrix blanks, blank injections, and certified reference materials where available.
- Referenced methodology and uncertainty framework: Nordtest TR537 for measurement uncertainty calculation.

## Relevance for GIS specialists and data products
- Spatial and temporal context: field sites across three countries enable GIS-based exposure mapping and cross-site comparison.
- Potential data products: georeferenced concentrations of TMX and CLO in hive products, with associated uncertainty and QC flags.
- Data integration considerations:
  - Alignment of sample metadata (location, date, matrix type, treatment status) with analytical results.
  - Standardized metadata to support cross-lab comparability and reproducibility.
  - Handling of detection limits and non-detects in spatial analyses.
  - Documentation of uncertainty (expanded 40%) for risk mapping and policy-oriented visuals.

## Key considerations and caveats for GIS workflows
- Data quality: robust QA/QC chain, blind analysis, and frequent calibrations are essential for reliable spatial analyses.
- Data gaps: potential variability in samples across sites; ensure clear metadata about sampling coverage and resolutions.
- Uncertainty: incorporate LOD/LOQ and expanded uncertainty into spatial risk assessments and visualization.

## References
- Magnussen B., Näykki T., Hovind H., Krysell M. 2012. Nordtest report 537. Handbook for calculation of measurement uncertainty in environmental laboratories. Nordic Innovation.