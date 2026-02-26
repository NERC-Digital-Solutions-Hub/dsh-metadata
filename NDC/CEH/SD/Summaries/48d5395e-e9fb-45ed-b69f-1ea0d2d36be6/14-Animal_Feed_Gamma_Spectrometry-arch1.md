# Supporting documentation for 14-Animal_Feed_Gamma_Spectrometry.csv

## Overview
- Provides metadata and variable definitions for measurements of radionuclide activity in total animal diet on a dry mass basis.
- Focuses on gamma spectrometry data for Ra-226, Cs-137, Ra-228, and K-40, with associated uncertainties and detection limits.
- Includes sample metadata: Animal, Location, and Feeding regime.

## Key variables and measurements
- Animal: General type of animal.
- Location: Location where the sample was collected.
- Feeding: Description of the feeding regime.
- Ra-226_Bq/kg_dm: Activity concentration of Ra-226 in total diet (Bq per kg dry mass).
- Unc_Ra-226_Bq/kg_dm: Uncertainty of Ra-226 concentration (quadratic propagation).
- Detection_Limit_Ra-226_Bq/kg_dm: Detection limit for Ra-226 (dry mass basis).
- Cs-137_Bq/kg_dm: Activity concentration of Cs-137 (Bq/kg dry mass).
- Unc_Cs-137_Bq/kg_dm: Uncertainty of Cs-137 concentration.
- Detection_Limit_Cs-137_Bq/kg_dm: Detection limit for Cs-137.
- Ra-228_Bq/kg_dm: Activity concentration of Ra-228 (Bq/kg dry mass).
- Unc_Ra-228_Bq/kg_dm: Uncertainty of Ra-228 concentration.
- Detection_Limit_Ra-228_Bq/kg_dm: Detection limit for Ra-228.
- K-40_Bq/kg_dm: Activity concentration of K-40 (Bq/kg dry mass).
- Unc_K-40_Bq/kg_dm: Uncertainty of K-40 concentration.
- Detection_Limit_K-40_Bq/kg_dm: Detection limit for K-40.
- Notes about equilibrium: Ra-226 is in equilibrium with Pb-214 and Bi-214; Ra-228 is in equilibrium with Ac-228. When blanks appear, the concentration is below the detection limit.
- Units basis: All concentrations are on a dry mass basis (Bq/kg_dry).

## Measurement details and interpretation
- Detection limits indicate censoring: blank entries mean concentrations were below detection limits.
- Equilibrium references inform interpretation of Ra-226 and Ra-228 values with their daughter isotopes.
- The dataset uses a total diet approach (as opposed to individual components).

## Data quality and challenges
- Uncertainties are provided, enabling propagation in analyses.
- Detection limits vary by radionuclide and sample, creating left-censoring in the data.
- Information is limited to the provided fields; missing metadata beyond those columns may affect cross-study comparability.
- Data are organized around a dry-mass basis to ensure comparability across samples.

## Analytical considerations and use cases
- Correlation and modeling:
  - Explore relationships between radionuclide concentrations and factors such as animal type, location, and feeding regime.
  - Build predictive models for radionuclide concentrations using Animal, Location, and Feeding as predictors.
- Handling censored data:
  - Treat below-detection-limit values as left-censored; apply appropriate statistical methods or imputation strategies.
  - Incorporate Unc_ fields to quantify measurement uncertainty in analyses.
- Uncertainty propagation:
  - Use Unc_Ra-226_Bq/kg_dm, Unc_Cs-137_Bq/kg_dm, Unc_Ra-228_Bq/kg_dm, and Unc_K-40_Bq/kg_dm for robust uncertainty analysis.
- Data governance and reproducibility:
  - Track data sources and maintain metadata provenance to support discovery and reuse.
  - Ensure consistent units (Bq/kg_dry) and explicit handling of blanks in reports and models.

## Practical notes for analysts
- Be mindful of equilibrium assumptions when interpreting Ra-226 and Ra-228 values.
- Use detection limits to interpret whether non-detect values reflect true absence or limits of measurement capability.
- When aggregating across animals or locations, document how censored data are treated and how uncertainties are propagated.