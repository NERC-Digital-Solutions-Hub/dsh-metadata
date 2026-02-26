# Multiple social encounters can eliminate Crozier's paradox and stabilise genetic kin recognition

## Overview
- Supplemental code for the Nature Communications 2022 paper by Scott, Grafen & West.
- Written for MATLAB R2019a.
- Provides data generation pipelines for three computational models related to the study:
  - A weak-selection mathematical island model.
  - An agent-based simulation model with stronger selection and finite populations.
  - A variant of the agent-based model without tag mutation to study balancing selection via tag fixation times.

## What the code does
- Generates data for the weak-selection island-model mathematical framework.
- Generates data for an agent-based simulation that captures stronger selection pressures and finite population effects.
- Generates data for a version of the agent-based model where tag mutation is disabled, enabling examination of balancing selection through tag fixation times.

## Scripts included
- Generate_data_for_island_model_weak_selection
- Generate_data_for_agent_based_simulation
- Generate_data_for_balancing_selection_finite_pop

## Environment and reproducibility
- MATLAB R2019a compatibility.
- Aims to reproduce data used in the study’s analyses and figures.

## Outputs and potential for visualization
- Produces data sets corresponding to different modeling approaches and scenarios.
- Data can underpin analyses and visualizations of kin recognition dynamics and social encounter effects, analogous to map-based data visualization workflows in GIS.

## Relevance to GIS specialists
- Illustrates data generation and integration across spatially-structured models, akin to assembling datasets from multiple sources and resolutions.
- Highlights data verification, cleaning/transformation needs, and handling of complex/pooled datasets—paralleling GIS data preparation challenges.
- Emphasizes reproducibility and the ability to explore parameter spaces, analogous to iterative GIS prototyping and stakeholder feedback.

## Practical considerations
- Large or complex simulation outputs require thoughtful data management and packaging.
- The no-mutation variant isolates balancing selection effects, useful for sensitivity analyses.
- Parameters governing selection strength, population structure, and tagging can be adjusted to explore different scenarios.