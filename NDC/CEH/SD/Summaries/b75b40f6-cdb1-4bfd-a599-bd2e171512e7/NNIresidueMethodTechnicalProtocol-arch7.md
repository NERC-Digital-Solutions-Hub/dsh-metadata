# A large-scale field experiment to quantify the impacts of neonicotinoid (NNI) seed dressings on honeybees in the UK, Germany and Hungary

- Purpose: quantify the impacts of neonicotinoid seed dressings on honeybees by measuring neonicotinoid concentrations in honeybee hive products (nectar, honey, wax, and pollen) across the UK, Germany and Hungary.
- Approach: standardized LC-MS/MS methodology with rigorous QA/QC to enable reliable concentration data and cross-location comparability.

## Methodology overview

- Target analytes: Thiamethoxam (TMX) and Clothianidin (CLO).
- Matrices analyzed: nectar/honey, pollen, and wax.
- Internal standards: labelled deuterated analogues (Thiamethoxam-D4, Clothianidin-D3, QMX).
- Analytical platform: liquid chromatography tandem mass spectrometry (LC-MS/MS) with an ion trap/quadrupole system; positive electrospray ionisation (ESI).

## Sample preparation and extraction

- Nectar and honey
  - Wet weight: 0.1 g.
  - Spike with internal standards.
  - Extraction solvent: 2 mL of methanol:water (50:50).
  - Processing: vortex, centrifuge, take 1 mL aqueous, add 4 mL water, mix.
- Pollen and wax
  - Wet weight: 0.1 g.
  - Spike with internal standards.
  - Extraction solvent: hexane:isopropanol (80:20).
  - Heat: water bath at 45°C for 15 minutes with occasional mixing.
  - Addition: 1.8 mL of methanol:water (50:50); vortex, centrifuge, collect 1 mL aqueous, add 4 mL water, mix.
- Cleanup
  - Solid-phase extraction (SPE) using Oasis HLB (60 mg, 3 mL).
  - Conditioning: methanol then water; drying under vacuum; hexane wash; final dryness.
  - Elution: 6 mL acetonitrile; dried (Turbovap) and reconstituted in 1 mL mobile phase.

## Instrumental analysis

- LC-MS/MS setup
  - Column: Phenomenex Synergi Fusion (2.5 μm, 50 mm × 2 mm ID).
  - Mobile phase: A = water with 0.1% acetic acid; B = methanol with 0.1% acetic acid.
  - Gradient: start 95% A / 5% B; ramp to 50% B over 15 min; to 100% B over 5 min; hold, then return to start.
  - Injection volume: 25 μL.
- MS/MS conditions
  - Mode: SRM with ESI positive.
  - Detection: two characteristic fragments per analyte for quantification.
  - Key parameters: optimized spray voltage, temperatures, collision gas, etc.
- Data handling
  - Quantification by comparing analyte responses to their internal standards.
  - Calibration: linear with 1/X weighting; at least 5 standards; linearity R² > 0.99.
  - Linear range: ND to 2.5 ng/mL.

## Calibration, quantification, and linearity

- Calibration strategy: response factor to native/internal standard pairs; use of internal standards for each matrix.
- Linearity: R² > 0.99 across the calibration range.
- Data quality: retention time and transition ratios checked against standards.

## Quality control and assurance

- Controls included in every batch (≤16 real samples per batch).
- Blanks: solvent blanks and matrix-matched blanks to monitor contamination.
- Mobile phase blanks injected every four samples to detect carryover.
- In-house QC samples: neonicotinoid-free honey, pollen, and wax spiked with TMX and CLO (different supplier than calibration standards).
- External reference: traceable NIST-certified standards for CLO and TMX analyzed periodically.
- Blind analysis: samples analyzed without knowledge of treatment status; confirmation by comparing transition ratios to pure standards.
- Reproducibility and identity: multiple checks for retention times, peak shapes, and MRM transitions.

## Performance metrics and uncertainty

- Limits of detection and quantification
  - LOD for entire procedure: 0.4 ng/g.
  - LOQ: 0.6 ng/g.
  - Expanded method uncertainty: ~40%.
- Recovery (method efficiency)
  - Nectar/honey: TMX-D4 ~91.3% ± 7.2%; CLO-D3 ~89.7% ± 7.2%.
  - Pollen: TMX-D4 ~83.5% ± 8.2%; CLO-D3 ~82% ± 10.1%.
- Calibration and accuracy
  - Calibration maintained with internal standards; normalised responses used for quantification.
- QA/QC cadence
  - Regular blank injections, indoor QC checks, and periodic external standard verifications to ensure reliability across batches.

## Data implications for geospatial analysis (GIS perspective)

- Spatial coverage: data derived from field sites across the UK, Germany, and Hungary enable cross-country spatial comparisons of neonicotinoid exposure in hive products.
- Data layers suitable for mapping
  - Concentration values by matrix (nectar/honey, pollen, wax).
  - Associated metadata: sampling location, date, and treatment context (NNI seed dressings).
  - QA/QC flags and uncertainty measures to accompany map visualisations.
- Data integration considerations
  - Harmonisation across matrices and sampling protocols.
  - Inclusion of detection limits and uncertainty in geospatial representations.
  - Linkage to environmental and exposure data for policy-relevant maps.

## Endnotes and provenance

- Project context: NEC05367, NERC Centre for Ecology and Hydrology.
- Validation and uncertainty framework draws on Nordtest (NT) guidance for measurement uncertainty in environmental laboratories.
- Data and methods designed to support robust, auditable concentration measurements suitable for integration into GIS-based analyses of exposure and risk.