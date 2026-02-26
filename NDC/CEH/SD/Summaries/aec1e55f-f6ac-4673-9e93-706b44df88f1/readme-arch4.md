# Multiple social encounters can eliminate Crozier's paradox and stabilise genetic kin recognition

## Overview
- Supplemental MATLAB code for a 2022 Nature Communications article by Scott, Grafen & West.
- Provides data generation for three modeling approaches related to genetic kin recognition and Crozier's paradox:
  - weak-selection island model
  - agent-based simulation with stronger selection and finite populations
  - agent-based scenario without tag mutation to study balancing selection via tag fixation times

## Data assets and pipelines
- Generate_data_for_island_model_weak_selection: creates data for the weak-selection mathematical model.
- Generate_data_for_agent_based_simulation: creates data for the agent-based model incorporating stronger selection and finite population effects.
- Generate_data_for_balancing_selection_finite_pop: creates data for the version without tag mutation, focusing on balancing selection through tag fixation times.
- All scripts are authored for MATLAB R2019a, ensuring a consistent computational environment.

## Data management and reproducibility
- Modular scripts with descriptive names that map directly to the modeled scenarios.
- Clearly delineated data generation tasks to support replication of results and further experimentation.
- Outputs are aligned with the study’s exploration of how multiple social encounters influence kin recognition stability under different selection regimes.

## Implications for Data Leaders
- Demonstrates the value of modular, scenario-specific data pipelines to support complex scientific inquiries.
- Highlights the importance of environment specification (MATLAB version) for reproducibility and future reuse.
- Illustrates how distinct modeling approaches (theoretical vs. agent-based) can be packaged as separate data products to enable comparative analysis and broader collaboration.

## Considerations and potential risks
- Dependence on a specific MATLAB release (R2019a) may affect future accessibility; plan for version control or containerization.
- Clear metadata and documentation are essential to ensure users understand model assumptions, parameters, and outputs across the three scripts.
- Coordinating data produced from different models requires careful data lineage and consistent interpretation guidelines to avoid misalignment in downstream analyses.