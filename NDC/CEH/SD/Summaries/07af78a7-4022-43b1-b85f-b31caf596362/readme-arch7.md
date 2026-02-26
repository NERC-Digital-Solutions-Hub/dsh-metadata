# Code for generating equilibrium genotype frequency values, and checking the analytical relatedness expression with simulation Supplementary code for Scott, West, Dewar and Wild (Evolution Letters, 2023). This repository contains all code associated with the paper "Is cooperation favoured by horizontal gene transfer?" Code is written for Matlab R2022a. I provide files for: -  Generating equilibrium genotype frequency values. This is provided in the "Script_to_generate_equilibrium_genotype_frequencies.m" script. -  Testing our relatedness expression with simulated data. This is provided in the "Comparison_of_simulated_and_expected_relatedness.m" script.

- What the repository contains
  - Matlab code designed to reproduce results from the Evolution Letters 2023 paper
  - Two main scripts:
    - Script_to_generate_equilibrium_genotype_frequencies.m: generates equilibrium genotype frequency values
    - Comparison_of_simulated_and_expected_relatedness.m: tests the relatedness expression against simulated data
  - Targeted for Matlab R2022a

- How the code is used
  - Reproduces the paper’s numerical results
  - Provides a workflow to generate genotype frequencies and to validate analytical relatedness with simulations

- Relevance to GIS specialists (data workflow perspective)
  - Demonstrates data generation, transformation, and validation steps that can inform GIS-like data pipelines
  - Outputs (genotype frequencies, relatedness results) could be integrated into data products or visualizations, enabling exploration of results across scenarios if spatial or scenario-based layers are added
  - Emphasizes reproducibility and testing through scripted workflows, aligning with data quality assurance practices in GIS analyses

- Practical notes
  - Environment: MATLAB
  - Scripts are named for straightforward execution and replication of the study’s methods and findings

- Context and provenance
  - Supplementary code for the paper “Is cooperation favoured by horizontal gene transfer?” by Scott, West, Dewar and Wild
  - Associated with Evolution Letters, 2023