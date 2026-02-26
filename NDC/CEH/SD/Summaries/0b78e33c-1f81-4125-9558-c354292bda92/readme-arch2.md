# Code for generating long-term equilibrium results for a range of parasite virulence and parasite evolutionary lag values, and dynamical results for specific parameter values

## Overview
- Supplementary code for the paper "Host-parasite coevolution and the stability of genetic kin recognition" (Scott, Grafen & West, PNAS 2023).
- Provides tools to explore how varying parasite virulence (d) and parasite evolutionary lag influence long-term equilibrium outcomes and time-series dynamics.
- Includes three scripts that work together to generate and initialize simulation runs.

## Scripts included
- Script_for_generating_parameter_sweep_data.m
  - Generates long-term (equilibrium) results across a range of d (parasite virulence) and lag values.
  - Saves results in matrices for efficient analysis and comparison.
- Script_for_generating_single_trial_data.m
  - Generates over-time (dynamical) results for a specific set of parameter values.
- Script_for_generating_initial_genotype_frequencies.m
  - Generates the initial genotype frequencies used to start each run.
  - Called by the other scripts to initialize simulations.

## Outputs and data handling
- Parameter sweep script outputs matrices containing equilibrium results across combinations of d and lag.
- Single-trial script outputs time-series data for chosen parameter values.
- All runs begin from initial genotype frequencies produced by the initial_genotype_frequencies script, ensuring standardized starting conditions.

## Reproducibility and provenance
- All functionality is organized within a repository of scripts designed for systematic parameter exploration.
- Standardized initialization (via initial genotype frequencies) supports consistent reproduction and comparative analysis.

## Relevance to environmental monitoring
- Demonstrates a structured approach to generating standardized long-term and dynamic results across parameter spaces, with clear data storage in matrices and defined starting conditions.
- Illustrates how complex dynamical outputs can be produced, stored, and traced back to initial conditions, aiding scrutiny and reuse of simulation data in environmental health modelling contexts.

## Considerations for Analysts
- Clarify parameter definitions and ranges (d and lag) when adapting the code for environmental applications.
- Ensure outputs are properly documented and stored in accessible formats to enable scrutiny over time.
- Maintain and reference the initial conditions generator to reproduce or compare alternative scenarios.