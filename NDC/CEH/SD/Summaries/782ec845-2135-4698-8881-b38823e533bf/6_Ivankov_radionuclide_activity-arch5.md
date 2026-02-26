# Mapping the contamination of Ivankiv district territory with radionuclides Final report November 2013- September 2014 on the studies carried out by UIAR within the frameworks of contract No.2013-04 from 19/11/2013, 2014.

## Overview
- A radionuclide contamination dataset focusing on Ivankiv district, presenting soil sample measurements and contamination densities.
- Data cover sample weights, activity concentrations for key radionuclides, uncertainties, and Cs:Sr ratio.
- Includes detection limits (values shown as “<” indicate below minimum detectable activity) and 95% confidence interval information for uncertainties.

## Data structure and content
- Full_weight_kg: total weight of soil samples; Note: composite sample formed from 5 samples by 37 mm corer to depth of at least 20 cm.
- Sample_weight_kg: weight of the sample used for activity measurement.
- 137Cs_Bq_kg, 90Sr_Bq_kg, 40K_Bq_kg, 226Ra_Bq_kg, 232Th_Bq_kg: activity concentration per kilogram.
- 137Cs_kBq_m2, 90Sr_kBq_m2: density of contamination per square metre.
- Relative_uncertainty_137Cs_%, Relative_uncertainty_90Sr_recovery_%, Relative_uncertainty_90Sr_%, Relative_uncertainty_40K_%, Relative_uncertainty_226Ra_%, Relative_uncertainty_232Th_%: relative uncertainties with 95% confidence interval where available.
- Ratio_Cs:Sr: Cs to Sr ratio (95% confidence interval provided in the heading, but value is n/a in the data).
- Fraction_90Sr_recovered: fraction of strontium-90 recovered (n/a in the notes).
- Notes and Explanations: metadata fields describing site identifier and measurement context; some notes indicate below-MDA values or are left blank.
- Data provenance: references to final report and study team.

## Metadata and provenance
- Source reference: Kashparov et al., Mapping the contamination of Ivankiv district territory with radionuclides. Final report November 2013 - September 2014 (UIAR, contract No.2013-04, from 19/11/2013, 2014).
- Dataset assembled to capture sampling design (composite soil samples), measurement context, and quantitative radionuclide indicators for environmental monitoring.

## Data quality, standards, and limitations
- Includes detection limits and explicit notes for values below MDAs.
- Uncertainty is documented with 95% confidence intervals for several radionuclides, supporting risk and trend assessment.
- Some fields have missing or non-applicable values (noted as n/a); metadata fields (explanation, units, notes) vary in completeness.
- Overall, data governance should focus on harmonizing field names, units, and the interpretation of below-MDA values for interoperability.

## Data governance and sharing considerations for Data Stewards
- Metadata completeness: ensure clear explanations, consistent units (Bq/kg, kBq/m2, percent), and explicit notes on MDAs.
- Standardization: align field names across systems to enable interoperability with other radionuclide or environmental datasets.
- Data availability and updates: establish mechanisms to publish to portals and catalog datasets; plan for periodic updates and versioning; document any embargo or sharing restrictions.
- Documentation: link dataset records to the original reference report and sampling methodology (composite sampling, depth, corer size).
- Data quality checks: implement checks for below-MDA indicators, uncertainty reporting, and Cs:Sr ratio interpretation.

## Practical implications for archiving and reuse
- Ensure dataset is discoverable through metadata describing purpose, sampling design, radionuclides measured, units, and uncertainty.
- Provide clear guidance on handling below-MDA values and how uncertainties were calculated.
- Maintain traceability to the main report and the field collection protocol to support reproducibility and secondary analyses.

## Challenges to anticipate (per Data Steward considerations)
- Incomplete user needs or unclear use cases for some radionuclide metrics.
- Timeliness of data acquisition and integration from multiple systems.
- Heterogeneous formats across historical datasets and potential non-interoperable structures.
- Managing large, multi-parameter datasets with detailed uncertainty information.

## Recommended actions for data stewardship
- Create a standardized metadata template capturing: dataset purpose, sampling design, site identifiers, variable definitions, units, MDAs, uncertainties, and data provenance.
- Harmonize field names and unit conventions; explicitly document any deviations from standard terminology.
- Implement data quality rules for censored data (values below MDA) and ensure uncertainty fields are populated where applicable.
- Publish to appropriate data portals with proper dataset-level documentation, linking to the referenced final report.
- Establish a maintenance plan for updates and revisions, including versioning and clear embargo/sharing policies.