# Python code for building and training a generative adversarial network for demographic inferences from genomic data

## Overview
- A collection of Python-based scripts to implement and train a Generative Adversarial Network (GAN) for demographic inferences from genomic data.
- Tuned for Anopheles mosquito genomes but adaptable to other species.
- Implements a GAN approach where the discriminator is a permutation-invariant CNN and the generator is a coalescent simulator.
- Inputs can be simulated data (msprime) or real genomes (VCF, converted to HDF5); outputs include text files and plots of inferred demographic histories and summary statistics.

## Input and Output
- Input formats and command-line usage:
  - Example: python3 pg_gan.py -m ${DEMO} -p ${PARAM} -n {SAMPLE_SIZE} -d ${H5} > ${OUTPUT}
  - DEMO: demographic history in msprime syntax; PARAM: neural network and demographic model parameters; SAMPLE_SIZE: number of observed genomes; H5: HDF5 file for VCF data; OUTPUT: prefix for all outputs.
- Output formats:
  - Text files and PNG plots showing parameter estimates, distributions of summary statistics, and diagnostic metrics.

## Model and Implementation
- Model description:
  - GAN-based algorithm combining realistic data generation with an explicit evolutionary model.
  - Discriminator: permutation-invariant CNN that classifies genotype matrices as real vs. synthetic.
  - Generator: coalescent simulator generating genotype data from a parameterized demographic history.
  - Training uses simulated annealing for parameter updates and standard gradient descent for the discriminator.
- Implementation details:
  - Codebase includes Python, R, and Bash scripts.
  - Runs via terminal with environments configured (activation command provided).
  - Outputs include text and plot files for estimated parameters.
- Environment and dependencies:
  - Deep learning components rely on tf/keras ecosystems.
  - Environments: tfenv_2.13 (for pg_gan.py and related scripts) and pg-gan_env.yml (for summary statistics and utilities).
  - README.md contains further run instructions.

## Data and Quality Control
- Data collection:
  - Input data can be simulated (msprime) or real (VCF converted to H5); conversion scripts are provided.
  - Required Python libraries are sourced from conda-forge.
  - Genomes available from public resources (e.g., MalariaGEN) for real data.
- Quality control:
  - Code validated through simulations with known outputs.
  - Accuracy metrics align with previously reported results in the referenced literature.

## File Structure and Contents
- Main folder contains:
  - ABC_reject_analysis.R, param_set.py, ss_helpers.py, deme_draw.py, pg_gan.py, summary_stats_multi.py, demographic_selection_oop.py, summary_stats.py, discriminator.py, README.md, real_data_random.py, util.py, generator.py, simulation.py, vcf2hdf5.py, global_vars.py
  - Additional subfolders:
    - environments: tfenv_2.13_requirements.txt, pg-gan_env.yml
    - prep_data: prep_samples.py, prep_vcf.sh
    - sps: engines.py, genomes.py, models.py, utils.py, genetic_maps.py, HomSap.py, species.py
    - supp: pg_gan_mosquito_schem.png (architecture diagram), ss_multi_readme.png (example outputs)
- 3.3.x sections provide detailed model code and output file descriptions:
  - 3.1.1 Model code: collection of Python, R, and Bash scripts
  - 3.1.2 Output files: .txt and .png formats
  - 3.2 File list and 3.3 File contents: detailed inventories of the code and data artifacts

## Model development and usage
- Model development:
  - Based on a previously described parametric GAN framework linking realistic data generation with explicit evolutionary models.
  - Discriminator architecture is a permutation-invariant CNN; generator uses a coalescent simulator to produce genotype data under a parameterized demographic history.
- Usage and execution:
  - Environments can be activated in a terminal (example provided for path-based activation).
  - Documentation and run guidelines are included in README.md.
- Input data collection and preparation:
  - Libraries sourced from conda-forge; genome data sources noted (e.g., MalariaGEN).
  - Data format conversion utilities included to support VCF-to-HDF5 workflow.

## GIS relevance and practical notes for GIS Specialists
- The workflow outputs demographic histories and distributions of summary statistics, which can inform spatial population analyses and map-based interpretations of demographic events.
- Although designed for genomic data, the approach can be adapted to model and visualize population structure and demographic change across geographic regions.
- Data handling supports mixing simulated and real genomic data, with clear input/output schemas and reproducible pipelines suitable for integration with geospatial data products.
- The repository provides ready-to-use data processing, quality checks, and visualization outputs (plots) that can feed into map-based storytelling and policy-relevant GIS analyses.

## References
- Wang, Z., Wang, J., Kourakos, M., Hoang, N., Lee, H.H., Mathieson, I. and Mathieson, S. (2021), Automatic inference of demographic parameters using generative adversarial networks. Mol Ecol Resour, 21: 2689-2705. https://doi.org/10.1111/1755-0998.13386