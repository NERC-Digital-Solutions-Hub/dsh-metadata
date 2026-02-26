# Diatom silica oxygen isotope and n-alkanoic acid hydrogen isotope composition of sediments from Lake Suigetsu, Japan (22,000 to 10,000 cal BP) SUPPORTING DOCUMENTATION

## Overview and purpose
- Dataset provides δ18O of bulk diatom silica and δ2H of C16, C18, C28, and C30 n-alkanoic acids from Lake Suigetsu sediments.
- Approximately centennial resolution (∼100-year) covering 22,040 cal BP to 9,980 cal BP (n = 120).
- Includes mass-normalised total lipid extract and key n-alkanoic acid concentrations to help infer East Asian Monsoon changes during Glacial Termination I.

## Core materials and chronology
- Subsamples derived from Lake Suigetsu SG12 core (center of the lake; 35°35'08"N, 135°52'56"E).
- Chronology tied to SG06 via visible marker layers; SG06 chronology based on >800 radiocarbon dates, varve counts, tephra tie points; ages aligned to IntCal20.
- Subsamples collected from 1.2 cm LL-channels across 1274.8–2119.4 cm depth (9980 ± 30 cal BP to 22,040 ± 38 cal BP).
- Event layers removed during sampling to avoid bias; ages converted to IntCal20.

## Sampling, splitting, and preparation
- Each subsample split into two halves for δ18Odiatom and δ2Hbiomarker analyses.
- Surfaces for δ2Hbiomarker half scraped to remove contamination; all subsamples frozen and freeze-dried.

## δ18Odiatom analysis (diatom silica)
- Prepared by disaggregation in 30% H2O2, heavy liquid density separations (SPT) at 2.25, 2.20, 2.15 g cm−3; post-treatment with H2O2 and HCl to remove organics and carbonates.
- Purified diatom material subjected to fluorination (BrF5) with pre-fluorination steps; CO2 converted for isotope ratio mass spectrometry.
- Calibration and normalization:
  - δ18Odiatom calibrated to VSMOW using internal standards (BFC, in-house MCS) and inter-lab references.
  - External analytical error: ±0.13 ‰ for BFC; ±0.33 ‰ for diatom replicates.
- Al-bearing contamination identified in several samples by XRF/SEM; contamination-corrected via geochemical mass-balance (end-member approach) with Monte Carlo uncertainty (10,000 replicates; 1σ ≈ ±0.36 ‰).
- Outcome: 113 of 120 samples retained after excluding contaminated or too-small samples.
- Notes: mass-balance corrections rely on contamination end-members and an assumed pure diatom Al content (1.4% Al2O3).

## δ2H biostratigraphy (n-alkanoic acids)
- Protocol aligned with BECS standards: total lipid extraction (TLE), fractionation into neutral and acid fractions, derivatization of acids to FAMEs for GC-FID and GC-IRMS analyses.
- n-alkanoic acids analyzed: C16, C18, C28, C30; concentrations normalised to dry sediment mass.
- δ2H measurements:
  - Performed with GC-IRMS; similar injection strategy to GC-FID; phthalate peaks mitigated by redirecting flow.
  - Instrumental settings: furnace 1450 °C; interface 350 °C; duplicate measurements; delta values referenced to in-house standard calibrated to Indiana n-alkane mixture.
  - H3+ correction factors applied (range 4.24–4.57).
  - Methylation (exchangeable hydrogen removal) corrections applied to convert FAME δ2H to corresponding n-alkanoic acid δ2H values.
- Data quality and filtering:
  - Subsamples with elevated baselines or poor peak definition excluded; subsamples with low concentration excluded for certain homologues.
  - 95 datapoints for C16, 86 for C18, 112 for C28, 108 for C30 retained.
  - δ2H values with uncorrected 1σ uncertainty > ±10 ‰ were excluded; strong correlation observed between C28 and C30 values after exclusion of outliers (R2 = 0.71).
- Precision and corrections:
  - Reported δ2H values are corrected for methylation and methyl hydrogen contribution; expressed on VSMOW scale.

## Data structure, units, and accessibility
- Two CSV data files:
  - lakesuigetsu_glacialtermination1_isotopes_results.csv: δ18Odiatom and δ2H values (C16, C18, C28, C30) with associated age ranges and metadata.
  - lakesuigetsu_glacialtermination1_concentrations_results.csv: concentrations of mass-normalised total lipid extract and C16, C18, C28, C30 n-alkanoic acids.
- Key fields:
  - Sample Number; Lower Age (IntCal20 cal BP); Upper Age (IntCal20 cal BP).
  - Corrected δ18Odiatom and error; Corrected δ2H values for C16, C18, C28, C30 and their errors.
  - Concentration fields normalised to dry sediment mass (mg/g for TLE; µg/g for each n-alkanoic acid).
- Age model references included (SG06 and SG12 correlation models and event layers) to document chronological context.

## Data quality, limitations, and provenance
- Contamination controls and corrections explicitly documented; mass-balance approach used for Al-bearing contamination with quantified uncertainty.
- QA steps include microscopy checks, SEM/XRF assessment, and removal of contaminated samples.
- Some δ2H data affected by analytical limitations (baselines, low concentrations) and were excluded to preserve dataset reliability.
- All methods, calibrations, and corrections are detailed, with full references to the supporting methodological literature.

## References and methodological context
- Key methodological references for contamination corrections, fluorination, calibration, and isotope analyses are cited to support data integrity and reproducibility.