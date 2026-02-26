# Code for generating long-term equilibrium results for a range of parasite virulence and parasite evolutionary lag values, and dynamical results for specific parameter values

## Overview
- Supplementary code for the paper “Host-parasite coevolution and the stability of genetic kin recognition” (Scott, Grafen & West, PNAS 2023).
- Includes scripts to generate long-term equilibrium results and time-series dynamical results, used to explore parasite virulence and evolutionary lag.

## Contents of the repository
- Script_for_generating_parameter_sweep_data.m
  - Generates long-term equilibrium results across a range of d (parasite virulence) and lag values.
  - Saves results in matrices.
- Script_for_generating_single_trial_data.m
  - Generates over-time dynamical results for a specific set of parameter values.
- Script_for_generating_initial_genotype_frequencies.m
  - Generates the initial genotype frequencies used to start each run.

## How the scripts work together
- The parameter-sweep and single-trial scripts both rely on Script_for_generating_initial_genotype_frequencies.m to establish starting conditions for each run.
- The initial frequencies script is invoked as part of the workflow to ensure consistent initialization across simulations.

## Outputs and data management
- Results from parameter sweeps are saved as matrices.
- Time-series results are produced for chosen parameter values.
- Outputs enable analysis of equilibrium versus dynamical behavior under different virulence (d) and evolutionary lag scenarios.

## Reproducibility and provenance
- All analyses are implemented as MATLAB scripts, enabling reproducibility by re-running the code with the same parameter settings.
- Clear ordering: initial genotype frequencies → parameter sweep or single-trial data generation → stored results.

## Data governance considerations for Data Stewards
- Metadata to capture: definitions and units for d (parasite virulence) and lag, parameter ranges, and the exact parameter values used for single-trial runs.
- Provenance: record the sequence of script executions and any changes to initial conditions.
- Licensing and access: ensure clear licensing for the codebase and any generated results; document usage rights for third-party reuse.
- Storage and versioning: organize outputs (matrices and time-series data) with version control and consistent file naming to facilitate discovery and reuse.

## Practical notes for use
- Ensure MATLAB environment is available to run the three scripts.
- Verify parameter settings before running the parameter sweep to align with the study’s intended exploration space.
- Maintain a log of runs to support traceability from parameter choices to published results.