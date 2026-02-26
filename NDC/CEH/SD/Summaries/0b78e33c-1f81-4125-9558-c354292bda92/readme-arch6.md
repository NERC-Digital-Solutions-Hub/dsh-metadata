# Code for generating long-term equilibrium results for a range of parasite virulence and parasite evolutionary lag values, and dynamical results for specific parameter values

## Overview
- Supplementary code for the PNAS 2023 paper “Host-parasite coevolution and the stability of genetic kin recognition” (Scott, Grafen & West).
- Three MATLAB scripts included to generate data under different experimental setups.

## Scripts included
- Script_for_generating_parameter_sweep_data.m: generates long-term (equilibrium) results across a range of parasite virulence d and evolutionary lag lag; saves results in matrices.
- Script_for_generating_single_trial_data.m: generates over-time (dynamical) results for a specific set of parameter values.
- Script_for_generating_initial_genotype_frequencies.m: generates the initial genotype frequencies used to start each run.

## How they connect
- The parameter sweep script calls Script_for_generating_initial_genotype_frequencies.m to establish starting frequencies for each run.
- The single-trial script also calls Script_for_generating_initial_genotype_frequencies.m to initialize runs.
- Outputs:
  - Equilibrium data saved as matrices from the parameter sweep.
  - Time-series dynamical data from the single-trial runs.

## Data outputs and formats
- Equilibrium results: matrices.
- Dynamical results: time-series data for selected parameter values.
- Initial genotype frequencies: generated separately to seed runs.

## Usage notes
- To reproduce long-term equilibrium results: run Script_for_generating_parameter_sweep_data.m.
- To reproduce dynamical trajectories: run Script_for_generating_single_trial_data.m.
- Both rely on Script_for_generating_initial_genotype_frequencies.m for starting conditions.

## Reproducibility considerations
- MATLAB environment required; ensure appropriate version and file paths are configured.