# Host-parasite coevolution and the stability of genetic kin recognition

## Overview
- This repository provides supplementary code for the PNAS 2023 paper by Scott, Grafen & West.
- Purpose: generate data for parasite–host coevolution studies, including long-term equilibrium results across parameter ranges and dynamical, time-series results for specific parameter sets.
- Outputs are designed as matrices and time-series that can be analyzed and visualized.

## Scripts and what they do
- Script_for_generating_parameter_sweep_data.m
  - Generates long-term (equilibrium) results for a range of parasite virulence values (d) and evolutionary lag values (lag).
  - Saves results in matrices for further analysis.
- Script_for_generating_single_trial_data.m
  - Generates over-time (dynamical) results for a specific set of parameter values.
- Script_for_generating_initial_genotype_frequencies.m
  - Generates the initial genotype frequencies used to start each run.
  - Called by both of the above scripts to initialize simulations.

## How to use and data flow
- Running the parameter sweep script produces equilibrium data matrices, suitable for comparative analyses across parameter combinations.
- Running the single-trial script produces time-series data for detailed dynamical examination.
- Both scripts rely on the initial genotype frequencies script to establish starting conditions, ensuring consistency across runs.

## Outputs and potential uses
- Equilibrium matrices (from parameter sweeps).
- Time-series data (dynamical results for selected parameters).
- Initial genotype frequency configurations (reused across runs).
- Outputs are ready for subsequent analysis and visualization, such as plotting results or creating data products for exploration.