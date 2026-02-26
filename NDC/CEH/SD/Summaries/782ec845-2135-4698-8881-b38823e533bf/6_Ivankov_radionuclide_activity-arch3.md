# Mapping the contamination of Ivankiv district territory with radionuclides Final report November 2013- September 2014 on the studies carried out by UIAR within the frameworks of contract No.2013-04 from 19/11/2013, 2014.

## Purpose and context
- Provides a dataset schema and variable definitions for soil sampling and radionuclide activity measurements used to map contamination in the Ivankiv district.
- Documents how composite soil samples are collected, measured, and reported to support environmental monitoring decisions.

## Dataset structure and key fields
- Sample identifiers and site identifiers accompany all measurements.
- Core sample details include Full_weight_kg (total weight of composite soil sample) and Sample_weight_kg (weight used for activity measurement).
- Field Notes describe sampling specifics (e.g., composite sample composed of 5 samples from a 37 mm corer down to ≥20 cm depth).

## Measured radionuclides and reporting units
- 137Cs_Bq_kg: activity concentration (Bq/kg) of cesium-137.
- 90Sr_Bq_kg: activity concentration (Bq/kg) of strontium-90.
- 40K_Bq_kg: activity concentration (Bq/kg) of potassium-40.
- 226Ra_Bq_kg and 232Th_Bq_kg: activity concentrations (Bq/kg) of radium-226 and thorium-232.
- 137Cs_kBq_m2 and 90Sr_kBq_m2: density of contamination (kBq/m²) for Cs-137 and Sr-90.
- Ratio_Cs:Sr:  Cs to Sr ratio (with 95% CI) to contextualize relative contamination.
- Relative_uncertainty_* fields: reported as percentages, indicating the 95% confidence interval uncertainty for each measurement.
- Fraction_90Sr_recovered: fraction of Sr-90 recovered (dimensionless).

## Data quality and non-detects
- Several measurements are reported as "< values," indicating results below the minimum detectable activity.
- Relative uncertainties are provided for several isotopes and for density measures, enabling uncertainty propagation in analyses.
- Some fields contain placeholders or blanks in Notes, indicating metadata gaps in places.

## Data handling and governance implications for monitoring frameworks
- Emphasizes the importance of metadata completeness (sampling methods, depth, composite construction) for traceability and reuse.
- Highlights the need to report and manage non-detects consistently (treating below-detection values).
- Underlines the necessity of documenting uncertainties (95% CI) to inform risk characterization and decision-making.
- Demonstrates the value of reporting both activity concentrations (Bq/kg) and surface densities (kBq/m²) for spatial mapping and risk assessment.
- Reflects a data sharing consideration: transparency of underlying data and accompanying metadata to support governance and public communication.

## Reference
- Kashparov, V. A., et al.: Mapping the contamination of Ivankiv district territory with radionuclides Final report November 2013- September 2014 on the studies carried out by UIAR within the frameworks of contract No.2013-04 from 19/11/2013, 2014.