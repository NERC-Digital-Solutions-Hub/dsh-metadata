# Python code for building and training a generative adversarial network for demographic inferences from genomic data

## Overview
- A collection of Python, R, and bash scripts to implement and train a Generative Adversarial Network (GAN) for demographic inferences from genomic data.
- Tuned for Anopheles mosquito genomes but adaptable to other species.
- Implements a GAN framework combining realistic data generation with explicit evolutionary modeling.
- Outputs include demographic history parameters, distributions of summary statistics, and diagnostic plots/text.
- Inputs can be simulated msprime data or real VCF data (converted to H5); supports both formats.

## How to run (input and output)
- Typical command:
  - python3 pg_gan.py -m ${DEMO} -p ${PARAM} -n {SAMPLE_SIZE} -d ${H5} > ${OUTPUT}
  - DEMO: demographic history in msprime syntax
  - PARAM: parameter initializations for neural networks and demographic models
  - SAMPLE_SIZE: number of observed genomes
  - H5: h5 file for VCF data
  - OUTPUT: prefix for all outputs
- Outputs:
  - Text files and PNG plots showing parameter estimates, distributions of summary statistics, and diagnostics.

## Model and methodology
- GAN-based model with:
  - Discriminator: permutation-invariant CNN that classifies genotype matrices (real vs. synthetic data).
  - Generator: coalescent simulator producing genotype data from a parameterized demographic history.
  - Training: simulated annealing updates to Generator parameters; standard gradient descent for the Discriminator.
- Data sources:
  - Simulations via msprime and VCFs converted to H5.
- Adaptability:
  - Core architecture described in the cited work, designed for interpretability alongside realistic data generation; adaptable to other species and demographic scenarios.

## Data inputs and data handling
- Required data formats:
  - Simulated msprime data or real VCF data (converted to H5).
- Data acquisition guidance:
  - Genomes (e.g., Anopheles) can be sourced from specified repositories; libraries and environments are defined to support running the code.
- Environment and tooling:
  - Deep learning components rely on specific Python environments; separate environment files exist to support various aspects of the workflow.

## Outputs and reporting
- Output formats:
  - .txt text files and .png plots for parameter estimates, summary statistics, and diagnostics.
- What is produced:
  - Point estimates for parameters of interest.
  - Distributions and summaries of demographic-related statistics.
  - Diagnostic metrics to assess model performance and fit.

## Model development and usage
- Model implementation:
  - Core scripts include pg_gan.py and related components; codebase is Python-heavy with supportive R and Bash scripts.
  - Environments and dependencies are organized to support both model execution and statistical plotting/analysis.
- Running and environment setup:
  - Documentation and README provide steps to activate the required environments and run the model.
  - Example commands illustrate how to initiate model runs and generate outputs.

## Input data collection and quality control
- Data collection notes:
  - Input data can be generated or sourced externally (msprime simulations or VCF data).
  - Input preparation and data conversion utilities are provided (e.g., for converting VCF to HDF5).
- Quality control:
  - Model validation performed with simulations where true outputs are known.
  - Reported accuracy aligns with expectations from the referenced literature.

## File structure and components
- Main folder contents include:
  - ABC_reject_analysis.R, param_set.py, ss_helpers.py, deme_draw.py, pg_gan.py, summary_stats_multi.py, demographic_selection_oop.py, summary_stats.py, discriminator.py, generator.py, simulation.py, vcf2hdf5.py, util.py, global_vars.py, README.md, real_data_random.py
- Subfolders:
  - environments: tfenv_2.13_requirements.txt, pg-gan_env.yml
  - prep_data: prep_samples.py, prep_vcf.sh
  - sps: engines.py, genomes.py, models.py, utils.py, genetic_maps.py, HomSap.py, species.py
  - supp: pg_gan_mosquito_schem.png (architecture diagram), ss_multi_readme.png (example outputs)
- Model and output specifics:
  - 3.3.1 Model code and 3.3.2 Output files detail the structure and contents
  - Model outputs are provided as .txt and .png
  - Environments outline dependencies for both deep learning and plotting/utility functions

## Practical relevance for environmental monitoring analysts
- Standardized, reproducible workflow to infer demographic histories from genomic data, enabling temporal environmental health assessments and policy performance reviews.
- Outputs in consistent formats (text and plots) facilitate reporting and comparison over time or across sites.
- Adaptable to different species and datasets, promoting broader applicability beyond a single organism.
- Encourages data stewardship by clearly organizing inputs, outputs, and environment configurations; citations required when using the code.

## Accessibility and citations
- The code requires citation as a condition of use.
- References to the foundational method and related validation can be found in the cited Mol Ecol Resour paper (Wang et al., 2021) and the associated DOI.