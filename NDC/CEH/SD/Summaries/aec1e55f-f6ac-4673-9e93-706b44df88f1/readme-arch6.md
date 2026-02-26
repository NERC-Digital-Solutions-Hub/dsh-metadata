# Multiple social encounters can eliminate Crozier's paradox and stabilise genetic kin recognition

## Purpose and scope
- Supplemental code accompanying the Nature Communications (2022) paper by Scott, Grafen & West.
- Provides data generation workflows for three modelling approaches:
  - Weak-selection island model
  - Agent-based simulation with stronger selection and finite populations
  - Agent-based simulation without tag mutation to examine balancing selection via tag fixation times

## What the code generates
- Data for the weak-selection island model via Generate_data_for_island_model_weak_selection.
- Data for the agent-based simulation model that accounts for stronger selection and finite populations via Generate_data_for_agent_based_simulation.
- Data for the balancing-selection scenario with finite populations where there is no tag mutation, via Generate_data_for_balancing_selection_finite_pop (focusing on tag fixation times).

## Implementation details
- All code is written for MATLAB R2019a.
- Each data-generation script corresponds to a distinct modelling approach, enabling separate or combined analyses.

## Outputs and potential data products
- Generated datasets suitable for downstream analysis of selection regimes, kin recognition dynamics, and related evolutionary scenarios.
- Outputs likely support examination of patterns such as fixation times (in the balancing-selection scenario) and differences between weak and strong selection across population structures.

## Reproducibility and usage
- The scripts are designed to facilitate reproducible data generation for the three modelling frameworks.
- Users can run, modify, and extend parameter explorations to compare model predictions and derive insights for the study’s hypotheses.