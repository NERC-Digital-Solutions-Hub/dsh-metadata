# Supporting documentation for 14-Animal_Feed_Gamma_Spectrometry.csv

## Overview
- Describes activity concentrations of radionuclides in the total diet on a dry mass basis, for various animals, locations, and feeding regimes.
- Rows include: Animal, Location, Feeding, and concentrations with uncertainties and detection limits for Ra-226, Cs-137, Ra-228, and K-40.
- Notes specify equilibrium with decay products (Pb-214, Bi-214, Ac-228) and how blanks are interpreted.

## Columns and Metadata

- Animal
  - Explanation: General type of animal
  - Units: n/a
  - Notes: n/a

- Location
  - Explanation: Location where the sample was collected
  - Units: n/a
  - Notes: n/a

- Feeding
  - Explanation: Description of the feeding regime
  - Units: n/a
  - Notes: n/a

- Ra-226_Bq/kg_dm
  - Explanation: Activity concentration of Ra-226 in the total diet on a dry mass basis
  - Units: Bq per kg dry mass
  - Notes: In equilibrium with Pb-214 and Bi-214; blank = below detection limit

- Unc_Ra-226_Bq/kg_dm
  - Explanation: Uncertainty (quadratic propagation) of Ra-226 concentration
  - Units: Bq per kg dry mass
  - Notes: In equilibrium with Pb-214 and Bi-214; blank = below detection limit

- Detection_Limit_Ra-226_Bq/kg_dm
  - Explanation: Detection limit for Ra-226
  - Units: Bq per kg dry mass
  - Notes: In equilibrium with Pb-214 and Bi-214; blank = concentration above detection limit (as described in the notes)

- Cs-137_Bq/kg_dm
  - Explanation: Activity concentration of Cs-137 in the total diet on a dry mass basis
  - Units: Bq per kg dry mass
  - Notes: Where blank, concentration below the detection limit

- Unc_Cs-137_Bq/kg_dm
  - Explanation: Uncertainty (quadratic propagation) of Cs-137 concentration
  - Units: Bq per kg dry mass
  - Notes: Where blank, concentration below the detection limit

- Detection_Limit_Cs-137_Bq/kg_dm
  - Explanation: Detection limit for Cs-137
  - Units: Bq per kg dry mass
  - Notes: Where blank, concentration above the detection limit

- Ra-228_Bq/kg_dm
  - Explanation: Activity concentration of Ra-228 in the total diet on a dry mass basis
  - Units: Bq per kg dry mass
  - Notes: In equilibrium with Ac-228; blank = below detection limit

- Unc_Ra-228_Bq/kg_dm
  - Explanation: Uncertainty (quadratic propagation) of Ra-228 concentration
  - Units: Bq per kg dry mass
  - Notes: In equilibrium with Ac-228; blank = below detection limit

- Detection_Limit_Ra-228_Bq/kg_dm
  - Explanation: Detection limit for Ra-228
  - Units: Bq per kg dry mass
  - Notes: In equilibrium with Ac-228; blank = concentration above detection limit

- K-40_Bq/kg_dm
  - Explanation: Activity concentration of K-40 in the total diet on a dry mass basis
  - Units: Bq per kg dry mass
  - Notes: Where blank, concentration below the detection limit

- Unc_K-40_Bq/kg_dm
  - Explanation: Uncertainty (quadratic propagation) of K-40 concentration
  - Units: Bq per kg dry mass
  - Notes: Where blank, concentration below the detection limit

- Detection_Limit_K-40_Bq/kg_dm
  - Explanation: Detection limit for K-40
  - Units: Bq per kg dry mass
  - Notes: Where blank, concentration above the detection limit

## Measurements, Uncertainty, and Detection Limits
- All nuclide concentrations are reported in Bq per kg dry mass (Bq/kg_dm).
- Uncertainties are provided as Unc_<nuclide>_Bq/kg_dm (quadratic propagation).
- Detection limits are provided per nuclide (Detection_Limit_<nuclide>_Bq/kg_dm).
- If a concentration or uncertainty is blank, it indicates the concentration is below the detection limit.
- Notes indicate isotopic equilibrium relationships (e.g., Ra-226 with Pb-214/Bi-214; Ra-228 with Ac-228) and guide interpretation.

## Data Quality and Interpretation Considerations
- Handling of censored data: blanks indicate below detection limits; appropriate methods should be used for censored values in analysis.
- Equilibrium context should be considered when comparing nuclide concentrations with related decay products.
- Some detection-limit notes may imply concentration status (e.g., blank = above detection limit in specific fields); align interpretation with the provided notes.

## Suggested Data Use and Products
- Build dashboards or pivot tables to compare nuclide concentrations across animals, locations, and feeding regimes.
- Create self-serve reports enabling end users to explore isotope-specific concentrations, uncertainties, and detection limits.
- Use the equilibrium notes to inform interpretation in exposure assessments and risk analyses.
- Link this dataset with related isotope data (Pb-214, Bi-214, Ac-228) where available to enhance context.

## Data Preparation and Processing Tips for Data Support
- Validate presence of Animal, Location, Feeding, and all nuclide-related columns.
- Treat blank concentration and uncertainty values as left-censored data at the corresponding detection limit.
- Preserve equilibrium context during analysis to ensure physically plausible interpretations.
- When visualizing, include error bars using Unc_<nuclide>_Bq/kg_dm and clearly denote censored values.