# Supporting documentation for 15-Animal_Feed_Stable.csv

## Overview
- Metadata and data dictionary for the 15-Animal_Feed_Stable.csv dataset.
- Documents sample metadata (animal type, location, feeding regime) and concentrations of various elements in the total diet on a dry mass basis.
- For each analyte, provides concentrations, uncertainties, and detection limits to support data cleaning, interpretation, and downstream analyses (e.g., correlations, models, exposure assessments).

## Data fields and definitions

- Core sample metadata
  - Animal: General type of animal. Location: Name of the location where the sample was collected. Feeding: Description of the feeding regimes.
  - These fields establish the context for each measurement (sample identity, provenance, and feeding conditions).

- Concentration fields (for each element)
  - Cs_mg/kg_dm, Sr_mg/kg_dm, K_mg/kg_dm, Na_mg/kg_dm, Ca_mg/kg_dm, Mg_mg/kg_dm, P_mg/kg_dm, Pb_mg/kg_dm, U_mg/kg_dm, Th_mg/kg_dm
  - Explanation: Concentration of the stable element in the total diet on a dry mass basis (mg per kg dry mass).
  - Units: mg per kg dry mass (mg/kg_dm).
  - Notes: If blank, the concentration is below the detection limit.

- Uncertainty fields (quadratic propagation)
  - Unc_Cs_mg/kg_dm, Unc_Sr_mg/kg_dm, Unc_K_mg/kg_dm, Unc_Na_mg/kg_dm, Unc_Ca_mg/kg_dm, Unc_Mg_mg/kg_dm, Unc_P_mg/kg_dm, Unc_Pb_mg/kg_dm, Unc_U_mg/kg_dm, Unc_Th_mg/kg_dm
  - Explanation: Uncertainty (quadratic propagation) of the respective element concentration in the total diet on a dry mass basis.
  - Units: mg per kg dry mass.
  - Notes: Where blank, the concentration was below the detection limit.

- Detection limit fields
  - Detection_Limit_Cs_mg/kg_dm, Detection_Limit_Sr_mg/kg_dm, Detection_Limit_K_mg/kg_dm, Detection_Limit_Na_mg/kg_dm, Detection_Limit_Ca_mg/kg_dm, Detection_Limit_Mg_mg/kg_dm, Detection_Limit_P_mg/kg_dm, Detection_Limit_Pb_mg/kg_dm, Detection_Limit_U_mg/kg_dm, Detection_Limit_Th_mg/kg_dm
  - Explanation: Detection limit of the stable element in the total diet on a dry mass basis.
  - Units: mg per kg dry mass.
  - Notes: Where blank, the concentration is above the detection limit.

## Data quality and interpretation considerations

- Handling of non-detects
  - Concentrations with no value indicate below detection limits.
  - Detection limits are provided per element to support censored-data handling during analysis.

- Uncertainty treatment
  - Unc_ fields quantify measurement uncertainty (quadratic propagation) to support error propagation in analyses and model fitting.

- Data consistency and cleaning notes
  - Most elements follow a consistent pattern (concentration, uncertainty, detection limit). Some Na-related fields show irregular naming in the source (potential formatting artefact) and may require careful harmonisation during data cleaning.
  - All element concentrations are on a dry-mass basis to enable comparability across samples and feeding regimes.

## Practical use for analysts

- Enables correlation analyses between diet composition (feeding regime) and element concentrations in the diet across locations and animal types.
- Supports uncertainty-aware modeling and exposure assessment on a dry-mass basis.
- Facilitates data provenance and reproducibility by clearly linking measurements to detection limits and associated uncertainties.
- Useful for data integration with other datasets by providing standardized units (mg/kg_dm) and explicit metadata (animal, location, feeding).

## End-to-end considerations

- The dataset is designed to support robust statistical analysis and modelling of dietary intake for animals, with explicit handling of non-detects and measurement uncertainty.
- Analysts should align field names and units, address any formatting irregularities (notably in Na, Pb, U fields), and consistently use detection limits to treat censored observations.