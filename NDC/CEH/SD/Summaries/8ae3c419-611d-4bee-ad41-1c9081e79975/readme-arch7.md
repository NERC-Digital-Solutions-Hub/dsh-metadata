# Supplementary Information for EIDCHELP-82246, 'Python code to identify sources of chemical pollutants in waterways'

- Purpose: Documents supplementary material for the manuscript on apportioning sources of chemicals of emerging concern along an urban river using inverse modelling; provides a runnable repository snapshot to reproduce results.

- Project and methods overview:
  - Developed as part of a six-month NERC Exploring the Frontiers project.
  - Uses waterway network topology and a simple downstream conservative mixing model to invert for source locations and concentrations from measured concentrations.
  - Builds on convex optimisation approaches for source apportionment developed by Lipp & Barnes (2024) and earlier work by Lipp, Roberts, and colleagues (2020, 2021).

- Nature and units of data:
  - Chemical concentrations are recorded in nanograms per litre (ng/L).
  - Inverted data were generated from experiments reported by Egli et al. (2023).

- Quality control and validation:
  - Includes a synthetic data inversion for validation.
  - Analyses of Variance and uncertainty assessments conducted.
  - Additional details available in the supporting documentation and cited papers.

- Repository structure and reproducibility:
  - Data directory contains publicly available data required to reproduce results (e.g., raw chemical dataset, digital elevation model, and drainage network).
  - Examples directory includes a minimal working example (MWE) and a Python script (mwe.py).
  - Figures/apportionment contains multiple figures illustrating observed vs. predicted concentrations, 1:1 plots, regularisation experiments, subcatchment source concentrations, and uncertainties.
  - The repository SourceApp-main.zip consolidates configuration (mwe.yaml), data, and example assets; installation instructions are provided to enable replication.

- Installation and running guidance (summarised):
  - Recommend using a conda environment (name: mwe) and Python 3.11.
  - Steps include cloning the repository, creating the conda environment from mwe.yaml, and activating it.
  - External dependencies to install:
    - autocatchments package (via git clone and pip install -e .)
    - faster-unmixer package (submodules and pip install -e .)
  - Run the Minimal Working Example: navigate to SourceApp/examples and execute python mwe.py; view generated PNG outputs.

- Outputs and visuals:
  - Figures depict: observed vs. predicted concentrations at sample sites A-J, 1:1 comparison plots, regularisation vs. data misfit for various lambda values, calculated subcatchment (source) concentrations, and uncertainties.

- Citing and references:
  - If using any part of the repository, cite:
    - Chrapkiewicz, Kajetan; Lipp, Alex; Barron, Leon Patrick; Barnes, Richard; Roberts, Gareth (2024), 'Apportioning sources of chemicals of emerging concern along an urban river with inverse modelling'. Science of the Total Environment. Preprint available at SSRN or DOI.
  - Related foundational references:
    - Egli et al. (2023)
    - Barnes & Lipp (2024)
    - Lipp et al. (2020, 2021)