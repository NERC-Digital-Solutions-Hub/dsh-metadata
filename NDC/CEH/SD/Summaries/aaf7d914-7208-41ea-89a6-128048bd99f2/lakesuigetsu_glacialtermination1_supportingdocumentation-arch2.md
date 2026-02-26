# Diatom silica oxygen isotope and n-alkanoic acid hydrogen isotope composition of sediments from Lake Suigetsu, Japan (22,000 to 10,000 cal BP) SUPPORTING DOCUMENTATION

## Overview
- Dataset provides stable oxygen isotope composition (δ18O) of bulk diatom silica and compound-specific stable hydrogen isotope composition (δ2H) of C16, C18, C28, and C30 n-alkanoic acids (as FAMEs) from Lake Suigetsu sediments.
- Resolution: approximately centennial (100-year) from 22,040 cal BP to 9,980 cal BP (n = 120).
- Accompanying data: mass-normalised total lipid extract (TLE) and key n-alkanoic acid concentrations.
- Purpose: infer changes to the East Asian Winter Monsoon and East Asian Summer Monsoon during Glacial Termination I.
- Core and chronology: subsamples from Lake Suigetsu SG12 core; chronology linked to SG06 via visible marker layers; ages on IntCal20 timescale.
- Sample handling: event layers (floods, turbidites, tephra) removed prior to subsampling to prevent skewing of integrated signals.

## Core Materials and Chronology
- Core: SG12 from the centre of Lake Suigetsu (35°35'08"N, 135°52'56"E).
- Chronology: SG06 model with >800 radiocarbon dates for the past ~50 ka, tephra tie points, varve counts; all ages on IntCal20 timescale.
- Subsampling: 1.2 cm-wide LL-channels across depth 1274.8–2119.4 cm (9980 ± 30 cal BP to 22,040 ± 38 cal BP); each subsample contains 100 integrated SG06_2012 years.
- Handling corrections: linear correction for minimal core expansion during storage; event layers removed during sampling.

## δ18Odiatom Analysis
- Preparation: disaggregation in 30% H2O2; density separations with sodium polytungstate at 2.25, 2.20, and 2.15 g/cm3; oxidative cleaning and carbonate removal with H2O2 and HCl; large sponge spicules removed; surfaces checked by light microscopy.
- Contamination assessment: %Al2O3 measured by XRF; high Al contamination (>4.2% Al2O3) prompted additional cleaning via density separation; some contamination treated with mass-balance corrections; end-member contamination quantified for correction.
- Contamination correction: mass-balance approach using end-member values and a minimum Al2O3 for pure diatom material; Monte Carlo (10,000 replicates) to estimate uncertainty (1σ ≈ ±0.36 ‰).
- Purification: diatom material fluorinated (pre-fluorination and BrF5 fluorination) and CO2 liberated for isotopic analysis.
- Measurement: δ18Odiatom measured on a Thermo Finnigan MAT 253; scales anchored and normalized to VSMOW.
- Accuracy: external analytical error ~±0.33 ‰ (diatom samples) with corrected values.
- Data quality: 113 of 120 samples retained after removing contaminated or too-small samples.

## δ2Hbiomarker Analysis
- Extraction and fractionation: total lipid extract (TLE) obtained with accelerated solvent extraction; neutral and acid fractions separated; acid fraction derivatised to fatty acid methyl esters (FAMEs) with BF3 in methanol.
- Quantification: FAME concentrations (C16, C18, C28, C30) measured by GC-FID; external calibrations with n-alkane standards; concentrations normalised to dry sediment mass.
- Isotope measurements: δ2H of C16, C18, C28, C30 FAMEs measured by GC-IRMS; hydrogen isotopes corrected for methyl group hydrogens introduced during derivatisation.
- Calibration: δ2H values converted to VSMOW using in-house standard and Indiana n-alkane mixture; precision reported as ±2.53 ‰ (1σ) from standards.
- Quality control: duplicates as standard practice; phthalate interferences managed by diverting flow during IRMS analysis; some subsamples showed raised baselines or low concentrations.
- Data curation: reliable δ2H values obtained for C28 and C30 in many subsamples; C16 and C18 more affected by baseline and concentration issues.
- Data quality thresholds: δ2H values with uncorrected 1σ uncertainty > ±10 ‰ excluded; final counts: 95 datapoints (C16), 86 (C18), 112 (C28), 108 (C30).
- Corrections: methylation correction applied to account for exchangeable hydrogen; mass-balance approach also applied to correct for methyl-derived hydrogens.

## Data Structure and Access
- Two CSV files:
  - lakesuigetsu_glacialtermination1_isotopes_results.csv: contains sample number, age range (IntCal20 cal BP), corrected δ18Odiatom, corrected δ2H for C16, C18, C28, C30 with associated errors and information about age models.
  - lakesuigetsu_glacialtermination1_concentrations_results.csv: contains sample number, age range, and mass-normalised concentrations for TLE and C16, C18, C28, C30 n-alkanoic acids.
- Age model references included for every entry (SG06 and SG12 correlation models and event layers).

## Uncertainties, Limitations, and Quality Assurance
- Contamination corrective approach introduces ~±0.36 ‰ (1σ) uncertainty for δ18Odiatom due to Al-bearing detrital contamination.
- δ2H data affected by baseline noise and low concentrations; several subsamples excluded or limited in interpretation.
- Phthalate interferences required selective data exclusion or spectral flow adjustments.
- Overall data are calibrated to IntCal20 timescale and standard reference materials; explicit quality control steps documented.

## Practical Implications for Environmental Monitoring
- Provides century-scale isotopic and lipid biomarker records tied to East Asian monsoon dynamics during Glacial Termination I.
- Data are standardized, quality-controlled, and ready for integration with other environmental datasets to assess climate-health and policy performance implications over time.
- Methodological transparency (contamination corrections, calibration, and quality flags) supports reproducibility and cross-dataset comparisons.