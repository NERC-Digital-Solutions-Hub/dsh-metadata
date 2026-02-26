# Python code for building and training a generative adversarial network for demographic inferences from genomic data

## Overview
- Purpose: Implement and train a GAN-based framework to infer demographic histories from genomic data, tuned for Anopheles mosquitoes but adaptable to other species.
- Approach: Permutation-invariant CNN discriminator classifies real vs synthetic genotype matrices; generator is a coalescent simulator that models demographic history.
- Scope: Works with both simulated msprime data and real VCF data (converted to h5); outputs include demographic histories, summary statistics, and diagnostic plots.
- Lineage: Based on a previous framework (pg_gan) and developed by Pui Ching Siu under Matteo Fumagalli; initial framework by Sara Mathieson.
- Outputs: Text files and plots that present parameter estimates, distributions of summary statistics, and other diagnostics.

## How to run and what you get
- Execution example: python3 pg_gan.py -m ${DEMO} -p ${PARAM} -n {SAMPLE_SIZE} -d ${H5} > ${OUTPUT}
  - DEMO: demographic history in msprime syntax
  - PARAM: parameter initialisation for neural networks and demographic models
  - SAMPLE_SIZE: number of observed genomes
  - H5: compressed VCF data in h5 format
  - OUTPUT: prefix for all resulting files
- Outputs:
  - Text files and PNG plots
  - Point estimates of parameters of interest
  - Distributions of summary statistics

## Model architecture and learning
- Model type: Generative Adversarial Network (GAN) for demographic inference
- Discriminator: permutation-invariant CNN operating on genotype matrices to distinguish real vs synthetic data
- Generator: coalescent simulator generating genotype data from a parameterised demographic history
- Training: simulated annealing for proposing parameter updates; gradient-based optimization for the discriminator
- Data sources: simulations via msprime and VCF files converted to h5
- Environment activation: example command to activate the required environment is provided in the documentation

## Data collection, formatting, and quality control
- Input data collection:
  - Python libraries sourced from conda-forge and keras.io
  - Genomes for Anopheles mosquitoes available from MalariaGEN
- Quality control:
  - Methods tested via simulations with known outputs
  - Accuracy metrics aligned with prior work (reference to related study)

## File structure and environments
- Main folder contents: a set of Python, R, and Bash scripts (e.g., pg_gan.py, discriminator.py, generator.py, simulation.py, etc.)
- Environments:
  - tfenv_2.13_requirements.txt – for deep learning tasks (pg_gan.py, demographic_selection_oop.py)
  - pg-gan_env.yml – for summary statistics plots, ABC rejection analysis, and utilities
- Subfolders:
  - prep_data: sample and VCF preparation scripts
  - sps: core genome and model utility modules (engines.py, genomes.py, models.py, etc.)
  - supp: diagrams and example outputs
- Documentation: README.md provides additional run instructions

## Model development and usage details
- 4.1 Model:
  - GAN framework described in a referenced publication; generator uses coalescent simulations; discriminator is a permutation-invariant CNN
  - Training relies on msprime simulations and VCF-to-h5 conversions
  - Environment setup and activation instructions provided
- 4.2 Input data collection:
  - Dependencies from conda-forge and keras.io
  - Data sources include Anopheles genomes from MalariaGEN
- 4.3 Quality control:
  - Validation through simulations with known outputs; reported accuracy matches prior literature

## References
- Wang, Z., Wang, J., Kourakos, M., Hoang, N., Lee, H.H., Mathieson, I., and Mathieson, S. (2021). Automatic inference of demographic parameters using generative adversarial networks. Molecular Ecology Resources. https://doi.org/10.1111/1755-0998.13386