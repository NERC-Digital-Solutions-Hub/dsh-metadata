# TREE_Northumbria_Gamma_Water

## Overview
- Metadata schema for UKCEH radiochemistry sample analyses (gamma/water context).
- Captures sample identifiers, description, site, mass, decay date reference, and radionuclide activity concentrations.
- Focuses on two radionuclides: Potassium-40 (K-40) and Cesium-137 (Cs-137), including measurement uncertainties and detection limits.
- Includes markers for censored data (< MDA) and general notes for context.

## Key Data Fields and Meanings
- CEH_Sample_Identifier: UKCEH radiochemistry laboratory unique sample identifier.
- CEH_Sample_Description: Description of the UKCEH sample.
- Site: Sampling site.
- Mass_of_Sample_Analysed_g: Mass of the sample analysed, in grams.
- Sampling_Date_Used_As_Decay_Date: Date the sample was taken and used as the decay date.
- K-40_Bq_per_kg_FM: Activity concentration of K-40 in Bq per kg fresh mass at the day of sampling.
- Counting_Error_K-40_Bq_per_kg_FM: Two-sigma counting error for K-40 in Bq per kg fresh mass.
- K-40_<: Indicator that the K-40 value is given as a "<" (below detection).
- MDA_K-40_Bq_per_kg_FM: Minimum Detectable Activity for K-40 in Bq per kg fresh mass.
- Cs-137_Bq_per_kg_FM: Activity concentration of Cs-137 in Bq per kg fresh mass at the day of sampling.
- Counting_Error_Cs-137_Bq_per_kg_FM: Two-sigma counting error for Cs-137 in Bq per kg fresh mass.
- Cs-137_<: Indicator that the Cs-137 value is given as a "<" (below detection).
- MDA_Cs-137_Bq_per_kg_FM: Minimum Detectable Activity for Cs-137 in Bq per kg fresh mass.
- General_Notes: General notes field for additional context.

## Measurement Details
- Units:
  - Bq per kg fresh mass (Bq/kg FM) for both K-40 and Cs-137.
  - Mass is recorded in grams (g).
  - "FM" denotes fresh mass.
- Uncertainty:
  - Counting_Error fields represent two-sigma counting uncertainties.
- Detection limits:
  - MDA fields provide the minimum detectable activity for each nuclide.
  - "<" markers (K-40_<, Cs-137_<) indicate values below the MDA.

## Data Use and Interpretation
- Enables calculation of radionuclide concentrations by sample, site, and date with associated uncertainty.
- Facilitates handling of censored data where concentrations are reported as below detection limits.
- Supports comparisons across samples and sites, and potential correlations between K-40 and Cs-137 concentrations.
- Provides traceability via explicit sample identifiers, descriptions, and decay-date reference, aiding reproducibility and data provenance.

## Considerations for Analysts
- Pay attention to sample mass (g) and its impact on concentration calculations.
- Treat "<" values appropriately in analyses, using MDA columns for censored-data strategies.
- Use Counting_Error values to assess measurement precision in downstream statistical analyses.
- Leverage General_Notes for any site-specific or methodological context that may affect interpretation.