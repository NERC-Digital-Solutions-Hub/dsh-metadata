# Python code for building and training a generative adversarial network for demographic inferences from genomic data

## Overview
- A GAN-based workflow to infer demographic history from genomic data, tuned for Anopheles mosquitoes but adaptable to other species.
- Implements and trains a parametric GAN framework combining realistic data generation with evolutionary model interpretability.
- Discriminator: permutation-invariant CNN that distinguishes real vs synthetic genotype data.
- Generator: coalescent simulator producing genotype data from a parameterized demographic history.
- Training uses simulated annealing for parameter updates and standard gradient-based optimization for the discriminator.
- Input data can be simulated (msprime) or real genomes (VCF converted to H5); outputs include text results and plots of demographic parameters, summary statistics, and diagnostic metrics.

## Input data
- Command-line usage: python3 pg_gan.py -m ${DEMO} -p ${PARAM} -n {SAMPLE_SIZE} -d ${H5} > ${OUTPUT}
  - DEMO: demographic history in msprime syntax
  - PARAM: parameters for neural networks and demographic models
  - SAMPLE_SIZE: number of observed genomes
  - H5: h5 file for VCF data
  - OUTPUT: prefix for all outputs
- Data types supported:
  - Simulated msprime data (demographic histories)
  - Real genome data via VCF files (converted to h5)

## Output
- Text files and PNG plots illustrating:
  - Point estimates of parameters of interest
  - Distributions of summary statistics

## Model code and outputs
- Code sources: Python, R, and Bash scripts
- Output file formats: .txt and .png

## Folder structure
- Main folder contents include:
  - ABC_reject_analysis.R, param_set.py, ss_helpers.py, deme_draw.py, pg_gan.py, summary_stats_multi.py, demographic_selection_oop.py, summary_stats.py, discriminator.py, README.md, real_data_random.py, util.py, generator.py, simulation.py, vcf2hdf5.py, global_vars.py
- Environments (subfolder):
  - tfenv_2.13_requirements.txt
  - pg-gan_env.yml
- Data prep (subfolder):
  - prep_samples.py, prep_vcf.sh
- SPS (subfolder):
  - engines.py, genomes.py, models.py, utils.py, genetic_maps.py, HomSap.py, species.py
- SUPPORT (subfolder):
  - pg_gan_mosquito_schem.png, ss_multi_readme.png (output statistics example)

## Model development and usage
- Environments and dependencies:
  - tfenv_2.13 for deep learning tasks (pg_gan.py, demographic_selection_oop.py)
  - pg-gan_env.yml for summary statistics, ABC rejection analysis, and utilities
- Run instructions and further details provided in README.md

## Model
- GAN-based method described in a referenced paper: a parametric GAN that combines realistic data generation with explicit evolutionary modeling.
- Generator: coalescent simulator producing genotype data from demographic history parameters.
- Discriminator: permutation-invariant CNN taking genotype matrices and classifying real vs synthetic data.
- Training regime:
  - Generator updates via simulated annealing to improve discriminator confusion
  - Discriminator updates via gradient descent
- Data sources for training: msprime simulations and VCF-to-h5 conversions
- Output includes parameter estimates and diagnostic plots

## Input data collection
- Required libraries sourced from conda-forge and keras.io
- Genomic data sources:
  - Anopheles mosquito genomes available from MalariaGEN data repository

## Quality control
- Code quality validated with simulations of known outputs
- Accuracy metrics align with previously published results

## References
- Wang, Z., Wang, J., Kourakos, M., et al. (2021). Automatic inference of demographic parameters using generative adversarial networks. Mol Ecol Resour, 21: 2689-2705. https://doi.org/10.1111/1755-0998.13386

## Relevance to Monitoring Frameworks
- Data formats and provenance:
  - Uses standardized data formats (msprime, VCF, h5) and explicit demographic models, enabling traceability of inputs and outputs.
- Reproducibility and governance:
  - Comprehensive environment and dependency files (tfenv_2.13, pg-gan_env.yml) support reproducible analyses.
  - Clear documentation of model components, data collection, and processing steps enhances auditability.
- Data quality and interoperability:
  - Integrates simulated and real data workflows, with outputs that facilitate interpretation of demographic inferences and summary statistics.
- Data sharing and transparency:
  - Outputs (text and plots) provide transparent reporting of parameter estimates and diagnostics; reliance on source code and data formats promotes openness, though actual data sharing policies would depend on external data sources (e.g., MalariaGEN).