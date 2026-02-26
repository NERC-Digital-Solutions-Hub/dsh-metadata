# Python code for building and training a generative adversarial network for demographic inferences from genomic data

## Overview
- A collection of scripts to implement and train a GAN for demographic inferences from genomic data.
- Tuned for Anopheles mosquito genomes but adaptable to other species.
- Implements a parametric GAN framework combining realistic data generation with an explicit evolutionary model.
- Discriminator: permutation-invariant CNN; takes genotype matrices to distinguish real vs synthetic data.
- Generator: coalescent simulator producing genotype data from a parameterized demographic history.
- Training: simulated annealing for parameter updates; discriminator uses standard gradient descent.
- Input data can be simulated (msprime) or real (VCF converted to h5); outputs include demographic histories, summary statistics distributions, and diagnostic plots.

## Data inputs and formats
- Input types:
  - Simulated data: msprime files.
  - Real data: VCF files (converted to h5 for processing).
- Command-line usage example:
  - python3 pg_gan.py -m ${DEMO} -p ${PARAM} -n {SAMPLE_SIZE} -d ${H5} > ${OUTPUT}
  - DEMO: demographic history in msprime syntax.
  - PARAM: parameters for neural networks and demographic models.
  - SAMPLE_SIZE: number of observed genomes.
  - H5: compressed HDF5 file for VCF inputs.
  - OUTPUT: prefix for all output files.
- Outputs:
  - Text files and plots illustrating parameter estimates and distributions of summary statistics (in .txt and .png formats).
- Model and data formats:
  - Model code across Python, R, and Bash scripts.
  - Outputs in .txt and .png; environments manage dependencies for deep learning and utilities.

## Outputs
- Text-based parameter estimates and diagnostic metrics.
- Plots showing distributions of summary statistics and inferred demographic parameters.

## Data governance and stewardship considerations
- Citation requirement: As a condition of using the code, you must cite it (data provenance and attribution must be tracked).
- Data provenance:
  - Works with both simulated data (msprime) and real genomic data (VCF -> h5).
  - Real data usage should comply with data access, consent, and licensing terms (e.g., MalariaGEN data referenced as a source in the workflow).
- Metadata and standards:
  - Documentation includes a README and structured directory layout to support reproducibility and traceability.
  - Environments and dependencies are explicitly specified to support consistent re-use and auditing.
- Data sharing and updates:
  - The workflow integrates a pipeline that can handle updates to data representations (e.g., format conversions between msprime, VCF, and h5) and outputs.
  - Results include both parameter estimates and diagnostic plots, enabling audit and provenance checks.
- Compliance and privacy considerations:
  - When using real genomes, ensure adherence to data sharing, privacy, and ethical policies; the document notes data sources and formats, which implicates governance around access.

## Repository structure and environments
- Main folder contents include:
  - ABC_reject_analysis.R, param_set.py, ss_helpers.py, deme_draw.py, pg_gan.py, summary_stats_multi.py, summary_stats.py, discriminator.py, generator.py, simulation.py, vcf2hdf5.py, global_vars.py, README.md, real_data_random.py, util.py.
- Subfolders:
  - environments: tfenv_2.13_requirements.txt, pg-gan_env.yml (environments for running the code).
  - prep_data: prep_samples.py, prep_vcf.sh (data preparation scripts).
  - sps: engines.py, genomes.py, models.py, utils.py, genetic_maps.py, HomSap.py, species.py (supporting modules).
  - supp: pg_gan_mosquito_schem.png (architecture diagram), ss_multi_readme.png (example output statistics).
- Documentation and references:
  - README.md provides further run instructions and environment setup.
  - References include an external paper on GAN-based demographic inference.

## Usage and reproducibility
- Environment setup:
  - Two environment files support different aspects: tfenv_2.13_requirements.txt for deep learning tasks; pg-gan_env.yml for summary statistics and utilities.
- Activation example:
  - Activate the terminal environment before running (example commands provided in the documentation).
- Reproducibility:
  - Clear command-line inputs, explicit file formats, and dedicated environment files support reproducibility and auditing.

## Quality control and validation
- Validation approach:
  - Quality controlled by simulations with known outputs.
  - Accuracy values reported align with prior work (reference provided).
- Data integrity:
  - The pipeline supports both synthetic and real data inputs, with appropriate format conversions to ensure compatibility across stages.

## Key considerations for data stewards
- Manageable data formats and conversions:
  - Multiple formats (msprime, VCF, h5) require careful governance around conversion processes and metadata.
- Licensing and attribution:
  - Citation requirement enforces proper attribution and usage terms; ensure license compatibility for any real data used.
- Data provenance and auditability:
  - Comprehensive folder structure and README documentation support traceability of data, models, and results.
- Handling of large datasets:
  - Real genomic data can be large; governance should address storage, access controls, and transfer policies.

## References
- Wang, Z., Wang, J., Kourakos, M., Hoang, N., Lee, H.H., Mathieson, I. and Mathieson, S. (2021). Automatic inference of demographic parameters using generative adversarial networks. Mol Ecol Resour, 21: 2689-2705. https://doi.org/10.1111/1755-0998.13386