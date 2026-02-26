# Python code for building and training a generative adversarial network for demographic inferences from genomic data

## Overview
- A GAN-based pipeline for inferring demographic history from genomic data, primarily tuned for Anopheles mosquitoes but adaptable to other species.
- Implements the pg_gan framework: a permutation-invariant CNN discriminator that distinguishes real vs. synthetic genotype data, and a generator that is a coalescent simulator producing data from parameterized demographic histories.
- Training uses simulations (msprime) and real genomes (VCF converted to h5); outputs include text files and plots of inferred demographic histories, summary statistics distributions, and diagnostic metrics.
- Largely Python-based (keras), with Bash and R utilities; developed by Pui Ching Siu under supervision of Matteo Fumagalli; references an initial framework by Sara Mathieson.
- Input data can be simulated or real; outputs are designed to be self-contained text and visualizations.

## Input
- Command-line usage example: python3 pg_gan.py -m ${DEMO} -p ${PARAM} -n {SAMPLE_SIZE} -d ${H5} > ${OUTPUT}, where:
  - DEMO: demographic history in msprime syntax
  - PARAM: parameter initializations for neural networks and demographic models
  - SAMPLE_SIZE: number of observed genomes
  - H5: h5 file containing VCF data
  - OUTPUT: prefix for all outputs

## Output
- Text files and plots illustrating:
  - Point estimates of parameters of interest
  - Distributions of summary statistics
- Outputs available in .txt and .png formats

## Model code
- Implemented as a collection of Python, R, and Bash scripts.
- Output files produced as .txt and .png.

## Folder structure
- Main folder includes: ABC_reject_analysis.R, param_set.py, ss_helpers.py, deme_draw.py, pg_gan.py, summary_stats_multi.py, demographic_selection_oop.py, summary_stats.py, discriminator.py, README.md, real_data_random.py, util.py, generator.py, simulation.py, vcf2hdf5.py, global_vars.py
- environments subfolder: pg-gan_env.yml, tfenv_2.13_requirements.txt
- prep_data subfolder: prep_samples.py, prep_vcf.sh
- sps subfolder: engines.py, genomes.py, models.py, utils.py, genetic_maps.py, HomSap.py, species.py
- supp subfolder: pg_gan_mosquito_schem.png, ss_multi_readme.png

## Model development and usage
- Model: GAN-based algorithm per a cited paper, combining realistic data generation with an explicit evolutionary model.
  - Discriminator: permutation-invariant CNN taking a genotype matrix to classify real vs. synthetic data.
  - Generator: coalescent simulator generating genotype data from a parameterized demographic history.
  - Training: simulated annealing for generator parameter updates; discriminator updated via standard neural-network gradient descent.
- Data formats: supports msprime-simulated data and real VCF data converted to h5.
- Environment: instructions to activate the terminal environment and run scripts provided in the repository.
- Outputs: text files and plots for estimated parameters.

## Input data collection
- Required libraries sourced from conda-forge and keras.io.
- Genomes from Anopheles mosquitoes can be obtained from MalariaGEN data resources (link provided in documentation).

## Quality control
- Code quality/accuracy checked via simulations with known outputs.
- Reported accuracy values align with prior publication on automatic demographic inference using GANs.

## References
- Wang, Z., Wang, J., Kourakos, M., Hoang, N., Lee, H.H., Mathieson, I. and Mathieson, S. (2021). Automatic inference of demographic parameters using generative adversarial networks. Mol Ecol Resour, 21: 2689-2705. https://doi.org/10.1111/1755-0998.13386