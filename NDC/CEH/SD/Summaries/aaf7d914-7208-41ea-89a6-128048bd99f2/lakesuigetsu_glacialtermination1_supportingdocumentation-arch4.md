# Diatom silica oxygen isotope and n-alkanoic acid hydrogen isotope composition of sediments from Lake Suigetsu, Japan (22,000 to 10,000 cal BP) SUPPORTING DOCUMENTATION

## Overview
- Dataset provides stable oxygen isotope composition (δ18O) of bulk diatom silica and compound-specific stable hydrogen isotope composition (δ2H) of C16, C18, C28, and C30 n-alkanoic acids from Lake Suigetsu sediments, at approximately centennial resolution (n = 120; 22,040 cal BP to 9,980 cal BP).
- Accompanied by mass-normalised concentrations of total lipid extract (TLE) and key n-alkanoic acid homologues.
- Objective: infer changes to the East Asian Winter Monsoon and East Asian Summer Monsoon during Glacial Termination I.
- Core materials: SG12 core from the lake centre; chronological control via SG06 chronology ( >800 radiocarbon dates for past ~50 ka, varve counts, tephra tie points) on IntCal20 timescale.
- Sampling details: subsamples from 1.2 cm LL-channels across 1274.8–2119.4 cm (9980 ± 30 to 22,040 ± 38 cal BP); each subsample split for δ18Odiatom (n=120) and δ2Hbiomarker (n=120); contamination minimised by surface cleaning and storage handling; samples frozen and freeze-dried.

## Data and Methods

### δ18Odiatom Analysis
- Preparation: disaggregation in 30% H2O2, three heavy liquid density separations (SPT) at 2.25, 2.20, and 2.15 g cm-3, followed by further H2O2/acid treatments to remove organics and carbonates; surface microbe checks and %Al2O3 quantified by XRF.
- Contamination handling: SEM used to identify Al-rich detrital contamination; samples with %Al2O3 > 4.2% (n=3) reprocessed; contamination-corrected δ18Odiatom applied via a mass-balance approach (end-member contamination values used); Monte Carlo propagation with 10,000 replicates to estimate 1σ uncertainty (mean ±0.36 ‰).
- Purified diatom material (6–7 mg) fluorinated to liberate structural oxygen, converted to CO2, and measured by IRMS; calibration anchored to in-house standards and widely referenced references; δ18Odiatom expressed on VSMOW scale with normalization.
- Final dataset includes 113 datapoints after removing contaminated or too-small samples.

### δ2Hbiomarker Analysis
- Extraction: total lipid extract (TLE) via Accelerated Solvent Extraction; separation into neutral and acid fractions; derivatization of acids to fatty acid methyl esters (FAMEs) with BF3/methanol.
- Concentrations: measured by GC-FID on a Restek Rtx-1 column; external calibrations with a mixture of n-alkanes; concentrations normalised to dry sediment mass.
- Isotopes: δ2H of C16, C18, C28, and C30 n-alkanoic acids measured by GC-IRMS; methylation corrections applied to convert FAME δ2H to n-alkanoic acid δ2H values; methanol-derived hydrogen δ2H contribution estimated via a mass-balance approach.
- Instrumentation: GC conditions matched to FID method; hydrogen isotope measurements referenced to an in-house standard calibrated to Indiana n-alkane mixture; H3+ correction factors ranged from 4.24 to 4.57.
- Data quality: duplicate measurements; reliable δ2H for all chain lengths not achieved in all subsamples due to baseline issues (raises in baselines affecting peak areas); 26 subsamples excluded on this basis; 9 subsamples affected by low concentrations.
- Final data: 95 datapoints for C16, 86 for C18, 112 for C28, 108 for C30 δ2H values (after quality control and outlier removal).

## Data Structure & Units

- Two CSV files:
  - lakesuigetsu_glacialtermination1_isotopes_results.csv
  - lakesuigetsu_glacialtermination1_concentrations_results.csv

- Isotopes file content:
  - Sample Number (A)
  - Lower Age (B): IntCal20 cal BP
  - Upper Age (C): IntCal20 cal BP
  - Corrected δ18Odiatom and error (D–E): ‰ VSMOW
  - Corrected δ2H for C16 (F–G), C18 (H–I), C28 (J–K), C30 (L–M) and associated errors: ‰ VSMOW
  - Data model references include SG06 SG12 correlations and event layer information

- Concentrations file content:
  - Sample Number (A)
  - Lower Age (B) and Upper Age (C): IntCal20 cal BP
  - Mass normalised total lipid extract (D): mg/g
  - Mass normalised C16 n-alkanoic acid (E): µg/g
  - Mass normalised C18 n-alkanoic acid (F): µg/g
  - Mass normalised C28 n-alkanoic acid (G): µg/g
  - Mass normalised C30 n-alkanoic acid (H): µg/g
  - All concentrations are normalised to dry sediment mass

## Data Quality, Uncertainties, and Limitations
- δ18Odiatom: contamination corrections applied with mass-balance; residual uncertainty from contamination modeled (1σ ≈ 0.36 ‰).
- δ2H: methylation corrections and methanol hydrogen corrections applied; baseline issues and low concentrations led to excluding some data; reliability thresholds applied (1σ uncertainty > ±10 ‰ removed); overall reliability supported by correlation between C28 and C30 values after outlier removal (R2 = 0.71).
- Sample reductions: 5 samples excluded due to high Al2O3 contamination; 2 samples too small for accurate δ18Odiatom determination.
- Data coverage spans 22,040 to 9,980 cal BP with centennial resolution across 120 subsamples, though not every subsample yields complete δ18O and δ2H data due to quality controls.

## Purpose, Usage, and Context
- The dataset is designed to support paleoenvironmental reconstruction of hydrological changes linked to East Asian monsoon variability during Glacial Termination I.
- The combination of diatom δ18O and n-alkanoic acid δ2H values, along with lipid concentrations, enables integrated interpretation of hydrological balance, monsoon dynamics, and sedimentary lipid biomarkers across the late glacial interval.
- Chronological framework relies on SG12 core correlation to SG06 with event-layer removals and IntCal20-based age models.

## References
- Methodological and chronology references detailing contamination corrections, normalization scales, calibration procedures, and baseline corrections (e.g., Brewer et al. 2008; Bronk Ramsey et al. 2020; Chapligin et al. 2011; Chivall et al. 2012; Clayton & Mayeda 1963; Coplen et al. 1983; Hut 1987; Leng & Sloane 2008; Mackay et al. 2011; McLean et al. 2018; Nakagawa et al. 2012; Schlolaut et al. 2018; Staff et al. 2011; Swann & Snelling 2023).