# Python code for building and training a generative adversarial network for demographic inferences from genomic data

## Overview
- A collection of Python-based scripts to implement and train a Generative Adversarial Network (GAN) for inferring demographic history from genomic data.
- Tuned for Anopheles mosquito genomes but adaptable to other species.
- Implements a GAN framework where:
  - The discriminator is a permutation-invariant CNN that distinguishes real vs synthetic genotype matrices.
  - The generator is a coalescent simulator that generates genotype data from a parametric demographic history.
  - Training uses simulated annealing to propose parameter updates; discriminator training uses standard gradient descent.
- Inputs can be simulated data (msprime) or real data (VCF, converted to h5); outputs include text results and plots of demographic histories and summary statistics.
- Implemented primarily in Python (Keras), with Bash and R components; authorship and supervision noted.

## Data inputs and formats
- Input types:
  - Demographic histories described in msprime syntax.
  - Parameter sets for neural networks and demographic models.
  - Observed genome sample size and an h5 file for VCF data.
- Usage example (command line):
  - python3 pg_gan.py -m ${DEMO} -p ${PARAM} -n {SAMPLE_SIZE} -d ${H5} > ${OUTPUT}
- Data formats:
  - Supports both simulated msprime data and real-world VCF data (converted to h5 as needed).
  - Outputs are text files and plots.

## Outputs and products
- Text outputs and PNG plots:
  - Point estimates of targeted demographic parameters.
  - Distributions of summary statistics.
  - Diagnostic plots and statistics to assess model fit and convergence.

## Model and approach
- Model description:
  - GAN-based algorithm described in a referenced paper, combining realistic data generation with explicit evolutionary modeling.
  - Discriminator: permutation-invariant CNN taking genotype matrices as input.
  - Generator: coalescent simulator generating data from a parametric demographic history.
  - Training: simulated annealing to explore parameter updates; discriminator trained via standard gradient descent.
- Data sources for training:
  - Simulations with msprime and real data via VCF→h5 conversions.
- Execution environment:
  - Commands to activate the appropriate Python environment (example provided).
- Outputs:
  - Text and plot-based results for demographic parameter estimates and summary statistic distributions.

## Data management and governance
- Folder structure (high level):
  - Main scripts (e.g., pg_gan.py, discriminator.py, generator.py, etc.).
  - Supporting utilities and demos (e.g., real_data_random.py, prep_data, sps, supp, README).
  - Environment definitions (environments folder with tfenv_2.13_requirements.txt and pg-gan_env.yml).
- Environment and dependencies:
  - Deep learning components rely on tf/Keras; other utilities span Python, R, and Bash.
  - Conda/virtual environment guidance and README for running code.
- Data provenance and lineage:
  - Supports both simulated and real data inputs; conversion utilities included to switch between formats (msprime, VCF, H5).

## Data availability and access
- Data sources:
  - Simulated data generated via msprime.
  - Real data via VCF files; genomes from Anopheles mosquitoes can be obtained from MalariaGEN (https://www.malariagen.net/data).
- Usage note:
  - The codebase invites citation as a condition of use.

## Quality control and validation
- Validation approach:
  - Quality tested through simulations with known outputs.
  - Accuracy metrics aligned with prior work in the domain.
- Reproducibility aids:
  - Environment files and example workflows provided to reproduce results.

## Reproducibility and collaboration
- How to run and reproduce:
  - Clear command-line examples, multiple scripts for data prep, model training, and analysis.
  - Separate environment files for deep learning and utility functions to enable reproducible setups.
- Collaboration and reuse:
  - The project is designed for researchers to adapt to other species or demographic scenarios.
  - Encourages citing the code when used.

## References
- Wang, Z., Wang, J., Kourakos, M., Hoang, N., Lee, H.H., Mathieson, I. and Mathieson, S. (2021). Automatic inference of demographic parameters using generative adversarial networks. Mol Ecol Resour, 21: 2689-2705. https://doi.org/10.1111/1755-0998.13386

## Practical considerations for Data Leaders
- Data system thinking:
  - The workflow integrates data generation, transformation, and modeling in a cohesive pipeline, enabling end-to-end reproducibility and traceability.
- User needs and co-ownership:
  - Outputs include demographic estimates and summary statistics that can inform policy or research discussions; the modular structure supports collaboration with data partners.
- Data discovery and access:
  - Supports both simulated data and real genomic data (VCF), facilitating exploration of methods before applying to proprietary datasets.
- Data quality and standards:
  - Uses standardized formats (msprime, VCF, h5) and documented preprocessing steps; quality checks validate model outputs against known benchmarks.
- Collaboration and community:
  - Provides environment configurations and scripts to ease sharing and adaptation with the broader genomics and population genetics communities.