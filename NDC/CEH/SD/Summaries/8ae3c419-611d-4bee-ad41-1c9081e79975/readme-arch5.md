# Supplementary Information for EIDCHELP-82246, 'Python code to identify sources of chemical pollutants in waterways'

## Purpose and context
- Describes the repository accompanying the manuscript on apportioning sources of chemicals of emerging concern along an urban river using inverse modelling.
- Notes the repository is a snapshot of the live repository at https://github.com/kmch/SourceApp and relates to the published preprint and submission to Science of the Total Environment.
- Highlights the code’s aim: identify locations and concentrations of chemical sources by exploiting river topology and downstream mixing, building on prior convex‑optimization source apportionment work.

## Data types, units, and sources
- Chemical concentration data are recorded in ng/L.
- Inversion results were generated from data reported by Egli et al. (2023) and others.
- Data files and inputs include:
  - Data/ICL_London_Dataset2019-2021.csv (raw chemical dataset from Egli et al. 2022)
  - Data/LIDAR_Composite_10m_DTM_2022_521500_540000_151500_179500.tif (digital elevation model for drainage network)
  - Data/Thames_d8.nc (digital drainage network used in examples)
- Outputs and materials include a set of figures (Acetamiprid, Cocaine, Tramadol, etc.) illustrating observed vs. predicted concentrations, Regularisation vs. Model Roughness, subcatchment source concentrations, and uncertainties.

## Methods and lineage
- Code developed during a six-month NERC Exploring the Frontiers project.
- Methodology uses river network topology and conservative downstream mixing with measured concentrations to invert for source locations and strengths.
- Builds on convex optimisation approaches developed by Lipp, Barnes, Roberts, and colleagues (referenced works from 2020–2024).

## Quality control and uncertainty
- A synthetic data inversion was performed to validate the approach.
- Analysis of Variance (ANOVA) and uncertainty assessments were conducted; further details are in the supporting documentation and cited papers (including the 2024 paper).

## Repository structure and contents
- Data directory contains publicly available inputs sufficient to reproduce results.
- Examples directory includes a minimal working example (MWE) and a Python script (mwe.py).
- Zip file SourceApp-main.zip contains:
  - Top-level mwe.yaml (installation config)
  - Data/ with datasets and supporting inputs
  - Figures/apportionment/ with multiple figures for each chemical
  - In examples/ the mwe.py script
- The repository also includes references and links to the main paper and related literature.

## Installation and running
- Installation steps are provided to enable reproducibility:
  - Clone the repository (or use the included SourceApp snapshot).
  - Create and activate a conda environment from mwe.yaml (e.g., environment named mwe with Python 3.11).
  - Install dependencies: autocatchments (via git) and faster-unmixer (via git submodules).
  - Run the Minimum Working Example from SourceApp/examples (python mwe.py) and view generated PNGs.
- The workflow is designed to be executed in a Unix-like terminal within the conda environment.

## Reproducibility and citations
- If parts of the repository are used in research, cite:
  - Chrapkiewicz et al. (2024) Science of the Total Environment (preprint available; SSRN/DOI links provided).
- Additional references cited within the repository include Egli et al. (2023), Barnes & Lipp (2024), Lipp et al. (2020, 2021).

## Data governance and stewardship considerations
- Public availability: Data and code are described as publicly available to reproduce the results, supporting transparency and reuse.
- Provenance and lineage: Clear attribution to original data sources (e.g., Egli et al. 2023) and the methodological lineage (convex optimisation approaches) are documented.
- Metadata and formats: Uses standard environmental data formats (CSV, TIFF, NetCDF) with explicit units (ng/L) and documented inputs/outputs, facilitating discoverability and interoperability.
- Licensing and reuse: The summary does not specify licensing within the text; stewardship best practice would require checking licenses for Data/ and code components before reuse.
- Documentation and onboarding: Installation and run instructions, along with a Minimal Working Example, support onboarding for data users and researchers.

## References
- Egli et al. (2023). A One-Health environmental risk assessment of contaminants of emerging concern in London's waterways throughout the SARS-CoV-2 pandemic.
- Barnes & Lipp (2024). Using convex optimisation to efficiently apportion tracer and pollutant sources from point concentration observations.
- Lipp et al. (2020, 2021). Source region geochemistry and related unmixing approaches.
- Chrapkiewicz et al. (2024). Apportioning sources of chemicals of emerging concern along an urban river with inverse modelling. Science of the Total Environment.