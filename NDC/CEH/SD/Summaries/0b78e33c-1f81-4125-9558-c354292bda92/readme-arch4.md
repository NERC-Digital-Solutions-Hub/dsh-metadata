# Code for generating long-term equilibrium results for a range of parasite virulence and parasite evolutionary lag values, and dynamical results for specific parameter values

## Purpose and context
- Provides supplementary MATLAB code for the PNAS 2023 paper “Host-parasite coevolution and the stability of genetic kin recognition” (Scott, Grafen & West).
- Contains three scripts designed to explore host–parasite coevolution across parameter spaces and over time.

## Scripts and roles
- Script_for_generating_parameter_sweep_data.m
  - Generates long-term (equilibrium) results over a range of parasite virulence (d) and evolutionary lag values.
  - Saves results in matrices for subsequent analysis.
- Script_for_generating_single_trial_data.m
  - Generates over-time (dynamical) results for a specific set of parameter values.
- Script_for_generating_initial_genotype_frequencies.m
  - Generates the initial genotype frequencies used to start each run.
  - Called by both the parameter sweep and single-trial scripts to ensure consistent starting conditions.

## Data products and outputs
- Equilibrium results: matrices capturing long-term outcomes across combinations of d and lag.
- Dynamical results: time-series data for a chosen parameter set.
- Initial conditions: genotype frequency profiles generated to initialize each run.

## Workflow and dependencies
- The parameter sweep and single-trial scripts depend on the initial genotype frequencies script.
- Clear, modular workflow enables reproducible exploration across parameter spaces.

## Data governance and reproducibility considerations
- Outputs are stored as structured matrices suitable for subsequent analysis and comparison.
- Centralized generation of initial conditions supports traceability and consistency across runs.
- Modular design facilitates auditing of parameter choices and starting states.

## Relevance for data leadership
- Demonstrates a parameter-driven experiment framework that supports scalable exploration of model behavior.
- Highlights important data workflows: reproducible initialization, systematic parameter sweeps, and time-series outputs.
- Emphasizes modular code organization and provenance of starting conditions for reliable analyses.