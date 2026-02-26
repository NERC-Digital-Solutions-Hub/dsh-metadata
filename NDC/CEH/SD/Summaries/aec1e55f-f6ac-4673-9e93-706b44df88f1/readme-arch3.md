# Supplemental code for "Multiple social encounters can eliminate Crozier's paradox and stabilise genetic kin recognition" (Scott, Grafen & West; Nature Communications; 2022)

- Overview
  - This document provides MATLAB code to accompany the Nature Communications paper, enabling data generation and simulation across three modeling approaches of kin recognition under selection.
  - All code targets MATLAB R2019a.

- Components and purpose
  - Generate_data_for_island_model_weak_selection
    - Generates data for the weak-selection mathematical island-model variant described in the study.
  - Generate_data_for_agent_based_simulation
    - Generates data for the agent-based simulation model, which captures stronger selection pressures and finite population dynamics.
  - Generate_data_for_balancing_selection_finite_pop
    - Generates data for the variant of the agent-based model with no tag mutation, used to examine balancing selection via tag fixation times.

- How the code supports the study
  - Provides data generation pipelines for comparing different selection regimes (weak vs. strong) and population structures (island model vs. finite populations).
  - Includes the no-tag-mutation scenario to investigate balancing selection dynamics through fixation timing.
  - Intended to facilitate replication of analyses and exploration of model assumptions in the paper.