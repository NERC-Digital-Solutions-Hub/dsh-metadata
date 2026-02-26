# Diatom silica oxygen isotope and n-alkanoic acid hydrogen isotope composition of sediments from Lake Suigetsu, Japan (22,000 to 10,000 cal BP) SUPPORTING DOCUMENTATION

## Overview
- Provides stable oxygen isotope composition of bulk diatom silica (δ18Odiatom) and compound-specific stable hydrogen isotope composition of C16, C18, C28, and C30 n-alkanoic acids (δ2H) from Lake Suigetsu sediment cores.
- Approximately centennial resolution (~100 years) from 22,040 cal BP to 9,980 cal BP (n = 120 samples).
- Includes mass-normalised total lipid extract (TLE) and key n-alkanoic acid concentrations.
- Data intended to infer changes to the East Asian Winter Monsoon and East Asian Summer Monsoon during Glacial Termination I.
- Core site: SG12 core, Lake Suigetsu (center of lake; ~35°35'08"N, 135°52'56"E). Chronology tied to SG06 via marker layers; IntCal20 timescale used for ages.

## Core Materials
- Subsamples from SG12 core, cross-cut along its length, with ages 1274.8–2119.4 cm depth corresponding to 9,980 ± 30 cal BP to 22,040 ± 38 cal BP.
- Chronology linked to SG06 (Radiocarbon dating >800 dates for past ~50 ka, varve counts, tephra ties) and aligned to IntCal20.
- Sampling approach: 1.2 cm-wide LL-channels yielding contiguous subsamples, each representing ~100 SG06_2012 years of sedimentation; event layers (floods, turbidites, tephra) removed prior to processing to prevent skewing.
- Each subsample split in half for δ18Odiatom and δ2Hbiomarker analyses; outer surfaces cleaned to minimize contamination; samples frozen and freeze-dried.

## δ18Odiatom Analysis
- Preparation: disaggregate in 30% H2O2; three heavy liquid density separations (SPT at 2.25, 2.20, 2.15 g/cm3) to isolate diatoms; re-treat with 30% H2O2 at 70°C for one week; remove carbonates with 5% HCl; filter through 80 µm mesh; assess visually with light microscopy; quantify Al2O3 via XRF.
- Contamination handling: SEM used to identify Al-bearing contamination; samples with Al2O3 > 4.2% (n=3) subjected to an additional density separation; mass-balance corrections applied for Al contamination (assuming pure diatom Al content of 1.4%); uncertainty from mass-balance estimated with Monte Carlo (10,000 runs).
- Purification and analysis: purified diatom material (6–7 mg) fluorinated with BrF5 to release structural oxygen; CO2 converted and measured by isotope ratio mass spectrometry; external standards used for calibration; results normalised to VSMOW; typical external errors: ~0.13‰ (BFC) to ~0.33‰ (replicates).
- Data handling: 113 of 120 samples retained after excluding contaminated or too-small samples; mass-balance correction applied to δ18Odiatom values.

## δ2Hbiomarker Analysis
- Preparation: total lipid extract (TLE) collected via accelerated solvent extraction; neutral and acid fractions separated; acid fraction derivatised to form fatty acid methyl esters (FAMEs) for analysis.
- Concentrations: C16, C18, C28, C30 n-alkanoic acids quantified by GC-FID with calibrated external standards; concentrations normalised to dry sediment mass.
- Hydrogen isotopes: δ2H of C16, C18, C28, C30 expressed as FAMEs measured by GC-IRMS; phthalate interferences mitigated by flow redirection during analysis; methylation corrections applied to convert FAME δ2H to n-alkanoic acid δ2H using BECS-based methodology and established mass-balance approaches.
- Quality control: samples with elevated baselines or low concentrations excluded from final dataset; final datapoints: 95 (C16), 86 (C18), 112 (C28), 108 (C30); precision: ~±2.53‰ (based on standards); H3+ correction factors 4.24–4.57.
- Data handling: duplicate measurements per sample; methylation-corrected δ2H values reported on the VSMOW scale; outliers removed using 1σ uncertainty criteria and cross-homologue comparisons (e.g., C28 vs C30 correlations).

## Data Structure, Nature and Units
- Two CSV files:
  - lakesuigetsu_glacialtermination1_isotopes_results.csv
    - Contains corrected δ18Odiatom and δ2H values for C16, C18, C28, C30 (with errors) and associated ages (lower/upper) in IntCal20 cal BP.
    - Metadata includes age-model references (SG06 SG12 correlations, event layers, and age models).
  - lakesuigetsu_glacialtermination1_concentrations_results.csv
    - Contains concentrations of mass-normalised total lipid extract and mass-normalised C16, C18, C28, C30 n-alkanoic acids (µg/g or mg/g, normalised to dry sediment mass) with associated ages.
- Age scale: IntCal20 cal BP; SG06 and SG12 correlation models referenced for each sample’s age range.

## Data Quality, Corrections and Limitations
- Corrections applied:
  - Mass-balance correction for Al-bearing contamination in δ18Odiatom samples; end-member values and assumptions (diatom Al content) used with Monte Carlo uncertainty estimation.
  - Methylation corrections and mass-balance scheme to translate FAME δ2H values to native n-alkanoic acid δ2H values.
  - Calibration to VSMOW scale with standard references and internal quality checks.
- Data coverage and omissions:
  - 7 samples removed from δ18Odiatom dataset due to contamination or insufficient mass; 113 usable δ18Odiatom datapoints from 120 subsamples.
  - δ2H datapoints filtered for reliability; some subsamples with raised baselines or low concentrations excluded, resulting in 95–112 datapoints across homologues.
- Uncertainties:
  - Analytical and correction-related uncertainties quantified (1σ ranges for δ18Odiatom around ±0.36‰ after mass balance; δ18O external error ~0.13–0.33‰; δ2H precision ~±2.53‰ for FAME measurements).
- Limitations:
  - Contamination challenges with Al-bearing material requiring corrective modelling; some internal contamination may persist despite cleaning.
  - Subsample mass limitations affected δ18Odiatom measurements for a subset of samples.

## GIS-Related Considerations and Use
- Time-resolved isotopic data (δ18Odiatom and δ2H of major n-alkanoic acids) and lipid concentrations can be integrated into GIS-based climate reconstructions and monsoon-forcing maps by:
  - Linking sample ages to a uniform chronology (IntCal20) for spatio-temporal visualization.
  - Mapping proxy values against time to visualize monsoon intensity changes across the Glacial Termination I interval.
  - Combining with other lake-core or regional paleoclimate datasets to build multi-proxy GIS layers for policy and public-facing climate visualization.
- Data structure supports programmatic access:
  - Two CSV files containing isotopic time series and corresponding lipid concentrations, with explicit age bounds and model references for alignment in GIS work.

## References
- Includes methodological and reference works underpinning extraction, purification, calibration, contamination correction, and isotopic interpretation (e.g., Brewer et al. 2008; Bronk Ramsey et al. 2020; Chapligin et al. 2011; Leng & Sloane 2008; Chivall et al. 2012; Clayton & Mayeda 1963; Coplen et al. 1983; Hut 1987).