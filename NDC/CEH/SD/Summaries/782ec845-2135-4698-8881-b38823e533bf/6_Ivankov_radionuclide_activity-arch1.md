# Mapping the contamination of Ivankiv district territory with radionuclides

## Overview
- Dataset describing radionuclide contamination measurements in Ivankiv district soils.
- Includes composite sampling details, weights, activity concentrations (Bq/kg), contamination densities (kBq/m2), uncertainties, Sr recovery, and Cs:Sr ratio.
- Based on a final report by Kashparov et al. (2013–2014) surveying contamination within UIAR efforts.

## Data elements and definitions
- Full_weight_kg: Total weight of soil samples (composite sample). Notes: 5 samples by a 37 mm corer to at least 20 cm depth.
- Sample_weight_kg: Weight of the sample used for activity measurement.
- 137Cs_Bq_kg: Activity concentration of Cs-137 (Bq/kg).
- Relative_uncertainty_137Cs_%: Relative uncertainty of 137Cs determination (95% CI).
- Fraction_90Sr_recovered: Fraction of Sr-90 recovered during processing.
- Relative_uncertainty_90Sr_recovery_%: Relative uncertainty of Sr-90 recovery (95% CI).
- 90Sr_Bq_kg: Activity concentration of Sr-90 (Bq/kg). Note: "<" values indicate below minimum detectable activity.
- Relative_uncertainty_90Sr_%: Relative uncertainty of Sr-90 determination (95% CI).
- 40K_Bq_kg: Activity concentration of K-40 (Bq/kg). Note: "<" values indicate below MD A.
- Relative_uncertainty_40K_%: Relative uncertainty of K-40 determination (95% CI).
- 226Ra_Bq_kg: Activity concentration of Ra-226 (Bq/kg). Includes 95% confidence interval context.
- Relative_uncertainty_226Ra_%: Relative uncertainty of Ra-226 determination (95% CI).
- 232Th_Bq_kg: Activity concentration of Th-232 (Bq/kg). Includes 95% confidence interval context; "<" indicates below MD A.
- Relative_uncertainty_232Th_%: Relative uncertainty of Th-232 determination (95% CI).
- 137Cs_kBq_m2: Density of Cs-137 contamination (kBq/m2).
- Relative_uncertainty_137Cs_kBq_m2_%: Relative uncertainty of Cs-137 density (95% CI).
- 90Sr_kBq_m2: Density of Sr-90 contamination (kBq/m2). Note: "<" values indicate below MD A.
- Relative_uncertainty_90Sr_kBq_m2_%: Relative uncertainty of Sr-90 density (95% CI).
- Ratio_Cs:Sr: Cs to Sr ratio with 95% confidence interval (unit: n/a).

## Sampling and measurement context
- Composite sampling approach: five 37 mm cores combined to form a single sample, depth ≥ 20 cm.
- Units: weights in kilograms; activities in Bq/kg; densities in kBq/m2.
- Minimum detectable activity (MDA) applies to values marked as "<".

## Data quality, uncertainty, and interpretation
- Uncertainties reported at 95% confidence intervals for all applicable measurements.
- Some measurements below MD A require treatment as censored data in analyses.
- Sr recovery fraction affects interpretation of Sr-90 related values.
- Cs:Sr ratio provides a normalized contamination indicator across sites.

## Provenance and reference
- Source: Kashparov, V. A., et al. Mapping the contamination of Ivankiv district territory with radionuclides. Final report November 2013–September 2014 (UIAR, contract No. 2013-04).

## Implications for analysis and modeling (analysts perspective)
- Enables spatial mapping of multiple radionuclides using both per-mass and per-area metrics.
- Facilitates cross-nuclide comparisons and ratio analyses (e.g., Cs:Sr) to infer contamination patterns.
- Analysts should handle MDAs appropriately, propagate measurement uncertainties, and account for Sr recovery when modeling Sr-90 data.
- Data integration may require harmonizing site identifiers and addressing potential gaps or non-standardized metadata.