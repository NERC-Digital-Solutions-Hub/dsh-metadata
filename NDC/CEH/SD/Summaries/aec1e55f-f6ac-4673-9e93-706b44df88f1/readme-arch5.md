# Supplemental code for "Multiple social encounters can eliminate Crozier's paradox and stabilise genetic kin recognition" (Scott, Grafen & West; Nature Communications; 2022)

## Overview
- Provides MATLAB R2019a supplemental code accompanying the paper.
- Three data-generation paths are included:
  - Weak-selection island model data (Generate_data_for_island_model_weak_selection)
  - Agent-based simulation data with stronger selection and finite populations (Generate_data_for_agent_based_simulation)
  - Balancing selection data without tag mutation (Generate_data_for_balancing_selection_finite_pop)

## Data Assets Generated
- Datasets produced for the weak-selection island model.
- Datasets produced for the agent-based simulation model under stronger selection with finite population dynamics.
- Datasets produced for the agent-based simulation variant where there is no tag mutation, used to examine balancing selection via tag fixation times.

## Data Provenance and Metadata
- Code is organized into clearly named scripts corresponding to each modeling scenario.
- MATLAB version compatibility specified (R2019a) to ensure reproducibility across environments.
- Script names indicate their specific data-generation purpose within the study.

## Data Quality and Validation
- The document outlines the data-generation tools but does not detail validation procedures; as data stewards, consider implementing and documenting checks to ensure outputs are consistent with model specifications and parameter regimes.

## Access, Sharing, and Documentation
- Supplementary code intended to accompany the Nature Communications article; users should reference these scripts when inspecting or reusing generated data.
- Clear linkage between code and the corresponding modeling components described in the paper.

## Technical Details and Dependencies
- MATLAB environment required: MATLAB R2019a.
- Three dedicated scripts:
  - Generate_data_for_island_model_weak_selection
  - Generate_data_for_agent_based_simulation
  - Generate_data_for_balancing_selection_finite_pop

## Reproducibility and Maintenance
- Centralizes data-generation workflows in labeled scripts, facilitating reproducibility of results.
- Long-term maintenance considerations for data stewards:
  - Version control of scripts and any parameter files
  - Documentation of input parameters, random seeds, and computational resources
  - Clear license and citation information for reuse

## Potential Challenges and Considerations
- Computational demands may be significant due to agent-based simulations with finite populations and multiple models.
- Ensuring compatibility if MATLAB updates alter behavior or functions used in the scripts.
- Aligning outputs with manuscript figures and tables for traceability.