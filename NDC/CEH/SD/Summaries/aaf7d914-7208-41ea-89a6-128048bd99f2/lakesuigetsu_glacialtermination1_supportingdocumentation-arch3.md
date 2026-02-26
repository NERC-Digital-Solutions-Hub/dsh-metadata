# Diatom silica oxygen isotope and n-alkanoic acid hydrogen isotope composition of sediments from Lake Suigetsu, Japan (22,000 to 10,000 cal BP) SUPPORTING DOCUMENTATION

- Overview
  - Provides δ18O of bulk diatom silica and δ2H of C16, C18, C28, and C30 n-alkanoic acids from Lake Suigetsu sediments, 22,040 to 9,980 cal BP (n = 120) at ~centennial resolution.
  - Includes mass-normalised total lipid extract and key n-alkanoic acid concentrations.
  - Aimed at inferring East Asian Winter/Summer Monsoon changes during Glacial Termination I.
  - Data organized into two CSV files: isotopes results and concentrations results.

- Core Materials
  - Subsamples from Lake Suigetsu SG12 core (center of lake; coordinates provided).
  - Chronology tied to SG06 via visible markers; SG06 is based on >800 radiocarbon dates, varve counts, tephra tie points, on IntCal20 timescale.
  - Subsamples taken from 1.2 cm LL-channels across 1274.8–2119.4 cm depth (9980 ± 30 cal BP to 22,040 ± 38 cal BP); contiguous samples representing ~100 SG06_2012 years each.
  - Event layers (floods, turbidites, tephra) removed during sampling to avoid skew.
  - Each subsample split for δ18Odiatom and δ2Hbiomarker analyses; surfaces cleaned for contamination control; samples frozen and freeze-dried prior to analysis.

- δ18Odiatom Analysis
  - Sample preparation: disaggregate in 30% H2O2, three heavy-liquid density separations (SPT at 2.25, 2.20, 2.15 g cm-3), remove organics with H2O2, remove carbonates with HCl, filter to remove large sponge spicules.
  - Contamination assessment: %Al2O3 measured by XRF; SEM used to identify Al-bearing contamination in high-Al samples.
  - Contamination correction: samples with %Al2O3 > 4.2% excluded (n=3); remaining contamination corrected via mass-balance using end-member values and assuming diatom material Al/Si = 0.016; Monte Carlo (10,000) for uncertainty (1σ ~ ±0.36 ‰).
  - Final dataset: 113 datapoints retained (5 excluded for high Al, 2 too small for δ18O).
  - Diatom oxygen isotope measurement: fluorination (BrF5) after pre-fluorination steps; CO2 converted and measured relative to standard CO2; δ18O values normalised to VSMOW.
  - Standards and precision: BFC standard analysed with each batch; external errors: δ18O(BFC) ±0.13‰, diatom samples ±0.33‰.
  - Calibration: using in-house MCS standard; anchor to VSMOW scale; quality checks and cross-lab calibration referenced.

- δ2Hbiomarker Analysis
  - Lipid extraction: total lipid extract (TLE) via accelerated solvent extraction; fractionation into neutral and acid fractions; derivatization of acids to FAMEs using BF3 in methanol.
  - Concentration measurements: GC-FID on a Restek Rtx-1 column; external calibration with n-alkane mix; concentrations normalised to dry sediment mass.
  - Hydrogen isotope measurements: GC-IRMS with methylated FAMEs; corrections for methylation and H exchange (methyl hydrogen correction using reference standards and mass-balance approach).
  - Quality control and filtering: duplicates performed; phthalate interferences redirected flow to avoid affecting the IRMS signal; samples with high baselines or low concentrations removed or flagged (reliable δ2H values achieved for most, but some samples excluded; dataset contains 95 datapoints for C16, 86 for C18, 112 for C28, 108 for C30).
  - Precision: instrument precision for δ2H on in-house standard; H3+ correction factor applied (range 4.24–4.57).
  - Data corrections: methylation corrections applied to obtain δ2H values for n-alkanoic acids (vs. FAMEs); linear regression to convert to VSMOW; all values reported relative to VSMOW.

- Details of Data Structure, Nature, and Units
  - Two CSV files:
    - lakesuigetsu_glacialtermination1_isotopes_results.csv: isotopic results for δ18Odiatom and δ2H of C16, C18, C28, and C30 acids; columns include sample number, age (IntCal20 cal BP) for lower/upper bounds, corrected δ18Odiatom with errors, corrected δ2H for each acid with errors.
    - lakesuigetsu_glacialtermination1_concentrations_results.csv: concentrations of total lipid extract and C16, C18, C28, C30 n-alkanoic acids (mass-normalised to dry sediment), with age bounds and metadata.
  - Ages tied to SG06/SG12 correlation models and event-layer updates; ages on IntCal20 cal BP scale.
  - Units: δ values in ‰ relative to VSMOW; concentrations in mg/g (TLE) or µg/g (n-alkanoic acids).

- Data Processing and Quality Assurance
  - Event layers removed to prevent single-event material bias.
  - Contamination checks and corrections applied to δ18Odiatom; exclusion of samples with excessive Al contamination.
  - Baseline issues and low concentrations addressed in δ2H measurements; data filtered to ensure reliable values (outliers excluded based on uncertainty thresholds and cross-correlation of homologues).
  - Documentation of analytical procedures, standards, calibration, and corrections to enable reproducibility and governance.

- Governance, Openness, and Use in Monitoring Frameworks
  - Detailed methodological transparency supports data quality assessment and reproducibility, aligning with data governance and open-data expectations.
  - Metadata and data provenance are explicit (sample IDs, ages, processing steps, calibration standards, and correction methods).
  - Some data exclusions noted (Al contamination, small sample mass, measurement baselines) highlight practical data quality barriers common in environmental monitoring datasets.

- References
  - Includes methodological and analytical references for contamination correction, fluorination methods, isotopic measurement, calibration standards, and core chronology, providing traceability and context for the dataset.