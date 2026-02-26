# Diatom silica oxygen isotope and n-alkanoic acid hydrogen isotope composition of sediments from Lake Suigetsu, Japan (22,000 to 10,000 cal BP) SUPPORTING DOCUMENTATION

## Overview
- Dataset provides δ18O of bulk diatom silica and δ2H of C16, C18, C28 and C30 n-alkanoic acids from Lake Suigetsu sediments.
- Approximately centennial resolution (about 100-year intervals), spanning 22,040 cal BP to 9,980 cal BP (n = 120 subsamples).
- Includes mass-normalised total lipid extract and concentrations of key n-alkanoic acid homologues.
- Purpose: infer changes to the East Asian Winter Monsoon and East Asian Summer Monsoon during Glacial Termination I.

## Core materials and chronology
- Subsamples from Lake Suigetsu SG12 core, collected at the lake center (coordinates provided).
- Chronology tied to SG06 via visible marker layers; SG06 model uses >800 radiocarbon dates, varve counts, tephra tie points; all ages on the IntCal20 timescale.
- Sample depth range 1274.8–2119.4 cm corresponds to 9980 ± 30 cal BP to 22,040 ± 38 cal BP.
- LL-channel sampling yields contiguous blocks containing 100 SG06_2012 years of sedimentation; core expansion corrected using event-layer depth comparisons.

## Sampling and preparation
- Each subsample split into two halves for δ18Odiatom and δ2Hbiomarker analyses.
- δ18Odiatom preparation includes disaggregation in H2O2, multiple heavy liquid density separations, organic and carbonate removal, and purity checks.
- Al2O3 quantified by XRF; SEM used to identify Al-bearing contamination. Samples with Al2O3 > 4.2% were adjusted or removed due to contamination.
- Mass-balancing corrections applied to δ18Odiatom to account for contamination; uncertainty from mass-balance assessed with 10,000 Monte Carlo replicates (1σ ≈ ±0.36 ‰).
- Final δ18Odiatom dataset: 113 datapoints retained (5 excluded for contamination, 2 too small for accurate δ18O).

## δ18Odiatom analysis
- Fluorination-based oxygen isotope analysis performed after sample pre-treatment.
- Standards and inter-laboratory calibrations used to place data on the VSMOW scale with reported external errors (1σ): δ18O_BFC ≈ ±0.13 ‰; δ18O_diatom ≈ ±0.33 ‰.
- Corrections described for contamination and scale normalization.

## δ2Hbiomarker analysis
- BECS protocol followed for extraction and derivatisation:
  - Total lipid extract (TLE) via accelerated solvent extraction.
  - TLE separated into neutral and acidic fractions; acids derivatised to form FAMEs.
  - Concentrations of C16, C18, C28 and C30 n-alkanoic acids quantified by GC-FID; concentrations normalised to dry sediment mass.
  - Compound-specific δ2H determined by GC-IRMS; measurements calibrated to a reference H2 gas and in-house standard calibrated to Indiana n-alkane mix.
- Methylation corrections applied to convert FAME δ2H values back to original n-alkanoic acid values.
- Phthalate interferences encountered; flow redirected during IRMS to avoid contamination; some subsamples required extended corrections.
- Reliability criteria: δ2H values with uncorrected 1σ uncertainty > ±10 ‰ were excluded; overall, data exhibited good internal consistency (comparison between C28 and C30 values supported reliability).
- Final δ2H datasets (per homologue) after filtering:
  - C16: 95 datapoints
  - C18: 86 datapoints
  - C28: 112 datapoints
  - C30: 108 datapoints
- Instrument precision for δ2H reported as ±2.53 ‰ (based on standards).

## Data structure and units
- Two CSV files provided:
  - lakesuigetsu_glacialtermination1_isotopes_results.csv
    - Contains sample number, lower and upper age (IntCal20 cal BP), corrected δ18Odiatom with error, corrected δ2H values for C16, C18, C28, C30 with errors, and age-model metadata.
  - lakesuigetsu_glacialtermination1_concentrations_results.csv
    - Contains sample number, lower and upper age (IntCal20 cal BP), mass-normalised total lipid extract, and mass-normalised concentrations of C16, C18, C28, C30 n-alkanoic acids (all normalised to dry sediment mass).

## Data quality, limitations, and notes
- δ18Odiatom: 113 of 120 samples used after excluding contamination-prone samples; remaining 7 excluded for data quality reasons (high Al contamination or insufficient mass).
- δ2H: reliability varies by homologue due to baseline issues and concentrations; final counts per homologue are 95 (C16), 86 (C18), 112 (C28), 108 (C30).
- Data are aligned to IntCal20 timescale and SG06/SG12 age models, enabling cross-proxy comparisons.
- Corrections applied for contamination (mass-balance for δ18Odiatom) and methylation (δ2H of FAMEs), with explicit uncertainty estimates.

## References
- Key methodological and chronostratigraphic sources, including contamination correction, diatom isotope methods, BECS protocols, and Lake Suigetsu chronologies (e.g., Bronk Ramsey et al., 2020; Chapligin et al., 2011; Leng & Sloane, 2008; Brewer et al., 2008; Nakagawa et al., 2012; Schlolaut et al., 2018; McLean et al., 2018; Staff et al., 2011).

## Potential uses for analysts
- Correlate δ18Odiatom with other climate proxies to reconstruct monsoon dynamics during Glacial Termination I.
- Use δ2H of n-alkanoic acids as a complementary hydroclimate proxy, including cross-comparison across C16, C18, C28, and C30 chains.
- Integrate these records with the SG06/SG12 chronology on the IntCal20 timescale to model timing and pacing of monsoon changes.
- Leverage concentration data (TLE and specific n-alkanoic acids) to assess organic matter inputs and lipid productivity concurrent with isotopic signals.
- Assess uncertainties and data gaps due to contamination corrections and measurement limitations when building multi-proxy climate reconstructions.