# Supporting documentation for 14-Animal_Feed_Gamma_Spectrometry.csv

## Overview
- Metadata description for the 14-Animal_Feed_Gamma_Spectrometry.csv dataset.
- Captures sample metadata (Animal, Location, Feeding) and radionuclide activity concentrations in total diet on a dry mass basis.
- Radionuclides included: Ra-226, Cs-137, Ra-228, and K-40, with associated uncertainties and detection limits.
- Notes specify equilibrium relationships with decay products and conventions for missing values (e.g., below detection limits).

## Data model and core fields
- Core metadata fields
  - Animal: General type of animal; Units and Notes not applicable (n/a).
  - Location: Name of sample collection location; Units not applicable (n/a).
  - Feeding: Description of the feeding regime; Units not applicable (n/a).
- Radionuclide fields (per isotope, with explanations and notes)
  - Ra-226_Bq/kg_dm
    - Description: Activity concentration of Ra-226 in total diet on a dry mass basis.
    - Units: Bq per kg dry mass.
    - Notes: In equilibrium with Pb-214 and Bi-214.
  - Unc_Ra-226_Bq/kg_dm
    - Description: Uncertainty (quadratic propagation) of Ra-226 activity concentration.
    - Notes: In equilibrium with Pb-214 and Bi-214.
  - Detection_Limit_Ra-226_Bq/kg_dm
    - Description: Detection limit for Ra-226 in the total diet on a dry mass basis.
    - Notes: In equilibrium with Pb-214 and Bi-214.
- Cs-137 fields
  - Cs-137_Bq/kg_dm
    - Description: Activity concentration of Cs-137 in total diet on a dry mass basis.
    - Notes: Where blank, concentration was below the detection limit.
  - Unc_Cs-137_Bq/kg_dm
    - Description: Uncertainty (quadratic propagation) of Cs-137 concentration.
    - Notes: Where blank, concentration was below the detection limit.
  - Detection_Limit_Cs-137_Bq/kg_dm
    - Description: Detection limit for Cs-137 in the total diet on a dry mass basis.
    - Notes: Where blank, concentration was above the detection limit.
- Ra-228 fields
  - Ra-228_Bq/kg_dm
    - Description: Activity concentration of Ra-228 in total diet on a dry mass basis.
    - Notes: In equilibrium with Ac-228.
  - Unc_Ra-228_Bq/kg_dm
    - Description: Uncertainty (quadratic propagation) of Ra-228 concentration.
    - Notes: In equilibrium with Ac-228.
  - Detection_Limit_Ra-228_Bq/kg_dm
    - Description: Detection limit for Ra-228 in the total diet on a dry mass basis.
    - Notes: In equilibrium with Ac-228.
- K-40 fields
  - K-40_Bq/kg_dm
    - Description: Activity concentration of K-40 in total diet on a dry mass basis.
    - Notes: Where blank, concentration was below the detection limit.
  - Unc_K-40_Bq/kg_dm
    - Description: Uncertainty (quadratic propagation) of K-40 concentration.
    - Notes: Where blank, concentration was below the detection limit.
  - Detection_Limit_K-40_Bq/kg_dm
    - Description: Detection limit for K-40 in the total diet on a dry mass basis.
    - Notes: Where blank, concentration was above the detection limit.

## Measurement context and interpretation
- Units are consistently reported as Bq per kg dry mass (Bq/kg_dm).
- Equilibrium references:
  - Ra-226 is reported in equilibrium with Pb-214 and Bi-214.
  - Ra-228 is reported in equilibrium with Ac-228.
- Missing values (blanks) are defined as concentrations below the corresponding detection limits (for the listed fields).
- Detection limits are provided per radionuclide to inform on data sensitivity and reporting thresholds.
- Notes indicate data quality considerations, including equilibrium assumptions and handling of blanks.

## Data quality, standards, and governance considerations
- Metadata richness enables discoverability, provenance tracking, and appropriate interpretation (e.g., dry mass basis, equilibrium assumptions).
- Clear per-field explanations and notes support data consumers in understanding measurement context and limits.
- Potential consistency checks for cross-isotope metadata (e.g., ensuring equilibration assumptions align with associated isotopes) to maintain data integrity across the dataset.
- For Data Leaders: use this metadata to drive standardization across datasets, implement data validation rules (units, detection-limit handling, equilibrium notes), and plan for updates as detection capabilities or measurement protocols evolve.

## Usage implications for data strategy
- Supports risk assessment and regulatory reporting by providing concentration levels, uncertainties, and detection thresholds for key radionuclides in animal feed.
- Facilitates cross-dataset integration via standardized fields (Animal, Location, Feeding, isotope-specific concentrations and uncertainties).
- Encourages the establishment of data quality controls, metadata standards, and clear data ownership through well-documented field definitions and notes.